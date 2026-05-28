---
title: Fórmulas de Personalization
description: Patrones de personalización comunes y ejemplos reales para Adobe Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: ac5d9310-7772-40fb-9d78-864562e1bfd6
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 815
ht-degree: 0%

---

# Fórmulas de Personalization {#personalization-recipes}

Esta página proporciona patrones de personalización listos para usar para los casos de uso más comunes en Adobe Journey Optimizer. Todos los ejemplos utilizan la sintaxis del editor de personalización y se pueden copiar directamente en el contenido de correo electrónico, SMS o push.

Para obtener una referencia completa de las funciones disponibles, vea [Funciones de ayuda](functions/helpers.md), [Funciones de fecha y hora](functions/dates.md), [Funciones de cadena](functions/string.md) y [Funciones de matriz](functions/arrays-list.md).

>[!TIP]
>
>Antes de copiar ejemplos, revise las [prácticas recomendadas de Personalization](personalization-syntax.md#best-practices) para evitar los errores de sintaxis más comunes.

## Fechas y recetas de hora {#date-time-recipes}

### Fórmula 1: mostrar la fecha actual en un formato legible {#recipe-current-date}

Use `formatDate` con `getCurrentZonedDateTime()` para procesar la fecha de hoy en cualquier formato:

```sql
{%= formatDate(getCurrentZonedDateTime(), "MMMM dd, yyyy") %}
```

Salida (ejemplo): `April 11, 2026`

**Patrones de formato comunes:**

| Patrón | Ejemplo de salida |
|---------|---------------|
| `"dd/MM/yyyy"` | `11/04/2026` |
| `"MM/dd/yyyy"` | `04/11/2026` |
| `"EEEE, MMMM dd"` | `Saturday, April 11` |
| `"yyyy-MM-dd"` | `2026-04-11` |

>[!NOTE]
>
>Use minúsculas en `y` (año natural) en lugar de `Y` (año basado en semanas) para evitar resultados inesperados en los límites de los años. Consulte [caracteres de patrón](functions/dates.md#pattern-characters) para obtener la referencia completa.

### Fórmula 2: Cuenta atrás hasta una fecha de vencimiento o evento {#recipe-countdown}

Use `dateDiff` para calcular el número de días restantes hasta un atributo de fecha de perfil y luego renderizarlo dinámicamente:

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your reward points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%}. Use them before they're gone!
{%else%}
Your reward points have expired.
{%/if%}
```

Salida (ejemplo): `Your reward points expire in 7 days. Use them before they're gone!`

### Fórmula 3: X días antes de una fecha de finalización dinámica {#recipe-days-before}

Para calcular una fecha X días antes de un atributo de perfil (por ejemplo, para hacer referencia a en el contenido o en las líneas de asunto), use `addDays` con un desplazamiento negativo:

```sql
{%= formatDate(addDays(stringToDate(profile.subscription.endDate), -7), "MMMM dd, yyyy") %}
```

Salida (ejemplo): `April 04, 2026` *(7 días antes del 11 de abril)*

Para establecer también una hora fija del día (por ejemplo, 9 a. m.), combine con `setHours`:

```sql
{%= formatDate(setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9), "dd/MM/yyyy HH:mm") %}
```

### Fórmula 4: mostrar el tiempo actual solo como HH:MM {#recipe-time-only}

Use `extractHours` y `extractMinutes` para mostrar solamente la porción de tiempo, con un protector de cero a la izquierda para los minutos:

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is at {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

Salida (ejemplo): `Your appointment is at 14:05.`

### Fórmula 5: Detectar fin de semana frente a día laborable {#recipe-weekend}

Use `dayOfWeek` para adaptar el contenido en función del día. La función devuelve 1 (lunes) a 7 (domingo). Utilice el solo operador `=` (sintaxis de PQL, no `==`):

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — our team will follow up on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

>[!NOTE]
>
>`dayOfWeek()` es para adaptar **contenido** según el día. Para perfiles de enrutamiento diferentes en un recorrido según el día de la semana, use la opción integrada **Condición horaria → día de la semana** en la actividad Condición de recorrido. [Más información](../building-journeys/condition-activity.md#date_condition)

## Fórmulas de matriz y bucle {#array-recipes}

### Fórmula 6: enumerar todos los elementos de una matriz de perfiles {#recipe-list-items}

Use `{{#each}}` para recorrer en iteración una matriz de perfiles y procesar cada elemento. Solo está disponible en el editor de personalización (correo electrónico, SMS, push):

```handlebars
{{#each profile.purchases.recentItems}}
  - {{this.name}}: {{this.price}}&euro;
{{/each}}
```

Salida (ejemplo):

```
- Running shoes: 89&euro;
- Water bottle: 15&euro;
- Gym bag: 45&euro;
```

>[!NOTE]
>
>`{{#each}}` no se admite en la actividad de condición de recorrido. Para filtrar matrices en condiciones, use [funciones de administración de colecciones](../building-journeys/expression/collection-management-functions.md).

### Fórmula 7: mostrar los N elementos principales de una matriz por precio {#recipe-first-n}

Use `topN` para ordenar y recuperar los elementos N principales por un campo numérico. Dado que `topN` es una función de PQL, asígnela primero a una variable con `{% let %}` y, a continuación, realice un bucle con `{{#each}}`:

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

>[!NOTE]
>
>`topN(profile.orders, price, 3)` ordena los pedidos por `price` en orden descendente y devuelve los 3 elementos principales, no devuelve simplemente los 3 primeros elementos en el orden de matriz original.

O bien, use `head` para obtener solamente el elemento principal único:

```sql
{%= head(profile.purchases.recentItems).name %}
```

### Fórmula 8: procesar contenido de forma condicional por elemento de matriz {#recipe-conditional-loop}

Use `{%#if%}` dentro de `{{#each}}` para procesar la salida solo para los elementos coincidentes. Defina un alias de bucle con `as |order|` para que el evaluador de PQL pueda resolver la referencia de atributo en la condición:

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending — we'll notify you when it ships.
  {%/if%}
{{/each}}
```

>[!NOTE]
>
>`this.status` funciona en expresiones Handlebars, pero no lo ha resuelto el evaluador de PQL dentro de `{%#if%}`. El uso de un alias de bucle con nombre (p. ej. `order`) hace que el atributo esté disponible para los contextos Handlebars y PQL.

## Cadena y fórmulas de formato {#string-recipes}

### Fórmula 9: Limpiar una cadena con replaceAll y reutilizarla {#recipe-replaceall-reuse}

`replaceAll` devuelve un nuevo valor (no modifica el original). Use `{% let %}` para almacenar el resultado y hacer referencia a él varias veces sin repetir la llamada a la función:

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}},
Your exclusive code is: WELCOME-{%= upperCase(cleanName) %}
```

Salida (ejemplo):

```
Hi John,
Your exclusive code is: WELCOME-JOHN
```

### Fórmula 10: Comilla doble un valor en la salida JSON {#recipe-json-quotes}

Para incluir una comilla doble literal dentro de una cadena (por ejemplo, generar JSON para una carga útil personalizada), escríbala con una barra invertida (`\"`):

```handlebars
{ "greeting": "Hello \"{{profile.person.name.firstName}}\"" }
```

Salida: `{ "greeting": "Hello \"John\"" }`

### Fórmula 11: Dar formato a un componente de fecha en mayúsculas {#recipe-uppercase-date}

Combinar `formatDate` con `upperCase` para representar nombres de mes o día en mayúsculas:

```sql
{%= upperCase(formatDate(getCurrentZonedDateTime(), "MMMM")) %}
```

Salida (ejemplo): `APRIL`

Para una cadena de fecha en mayúsculas completa:

```sql
{%= upperCase(formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy")) %}
```

Salida (ejemplo): `WEDNESDAY JANUARY 01 2020`

## Fórmulas de lógica condicional {#conditional-recipes}

### Fórmula 12 — IF/ELSEIF/ELSE en contenido personalizado {#recipe-if-elseif}

Use `{%#if%}`, `{%else if%}` y `{%else%}` para la lógica condicional de varias ramas. Este patrón funciona en el contenido del correo electrónico y en los fragmentos:

```handlebars
{%#if profile.loyalty.tier = "gold"%}
As a Gold member, enjoy free shipping on all orders.
{%else if profile.loyalty.tier = "silver"%}
As a Silver member, enjoy free shipping on orders over &euro;50.
{%else%}
Join our loyalty program to unlock exclusive benefits.
{%/if%}
```

### Fórmula 13: visualización de atributos con seguridad nula {#recipe-null-safe}

Utilice una reserva condicional para evitar la representación de valores vacíos cuando un atributo de perfil pueda ser nulo o faltar:

```handlebars
{%#if profile.person.name.firstName%}
Hi {{profile.person.name.firstName}},
{%else%}
Hi there,
{%/if%}
```

O en línea con un patrón de estilo ternario usando `isEmpty`:

```handlebars
Hi {%#if isEmpty(profile.person.name.firstName)%}valued customer{%else%}{{profile.person.name.firstName}}{%/if%},
```

## Fórmulas de casos extremos de PQL {#pql-edge-cases}

### Fórmula 14 — Hacer referencia a una clave de atributo con guiones {#recipe-hyphenated-key}

Si el nombre del campo de esquema XDM contiene guiones (p. ej. `order-total`, `event-type`), encapsúlelo en comillas invertidas dentro de una expresión PQL para evitar que el guión se interprete como un operador de resta:

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>Las comillas invertidas solo se admiten dentro de expresiones PQL (`{%= ... %}`). No se aceptan en la interpolación simple de Handlebars (`{{...}}`). Si necesita procesar directamente un valor de campo con guiones, evaluarlo mediante una expresión PQL o almacenarlo primero en una variable usando `{% let %}`.

### Fórmula 15: Hacer referencia a un ID de evento numérico en un atributo de contexto {#recipe-numeric-event-id}

Cuando utilice un evento de contexto de recorrido cuyo ID sea una cadena numérica (p. ej. `1697323153`), ajuste el ID en comillas invertidas y use `{% let %}` con `toDateTime()` y `formatDate()`:

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
Your appointment: {{appointmentDate}}
```

Salida (ejemplo): `Your appointment: 18/03/2026 14:30`

### Fórmula 16 — Coerción de tipo: comparar un campo de cadena con un número {#recipe-type-coercion}

PQL tiene establecimiento inflexible de tipos. Cuando un campo de perfil se almacena como una cadena pero necesita compararlo numéricamente, conviértalo primero con `stringToNumber()`:

```sql
{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}
```

Para campos booleanos almacenados como cadenas:

```sql
{%= toBool(profile.consents.email.val) = true %}
```

