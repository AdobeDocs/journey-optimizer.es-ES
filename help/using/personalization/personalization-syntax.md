---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxis de personalización
description: Aprenda a utilizar la sintaxis de personalización.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: expresión, editor, sintaxis, personalización
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
TQID: https://experienceleague.adobe.com/kZEw2lITdt8SMWMe-UT2vPzdoiAjB2vbItmK9zt-WJo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: c5ecc28ec44a9c608f4fe5011e061cad62d92e2b
workflow-type: tm+mt
source-wordcount: 1299
ht-degree: 3%

---

# Sintaxis de personalización {#personalization-syntax}

Personalization en [!DNL Journey Optimizer] usa dos sintaxis complementarias que funcionan juntas en la misma expresión:

* **Handlebars** (`{{...}}`): se usa para procesar atributos de perfil, recorrer en bucle matrices y llamar a ayudantes de bloque. Consulte la [documentación de HandlebarsJS](https://handlebarsjs.com/) para obtener una referencia completa.
* **Profile Query Language (PQL)** (`{%= ... %}`): se usa para llamar a funciones integradas (por ejemplo, `upperCase()`, `formatDate()`, `dateDiff()`) y evaluar expresiones condicionales.

Es fundamental comprender en qué contexto se encuentra para evitar errores de tiempo de ejecución. Por ejemplo, una llamada a una función de PQL colocada dentro de `{{...}}` fallará porque Handlebars intenta resolverla como un ayudante en lugar de evaluarla como una expresión de PQL.

**Ejemplos:**

| Ejemplo de uso | Sintaxis |
|----------|--------|
| Procesamiento de un atributo de perfil | `{{profile.person.name.firstName}}` |
| Llamar a una función de PQL | `{%= upperCase(profile.person.name.firstName) %}` |
| Bloque condicional | `{%#if profile.loyalty.tier = "gold"%}...{%/if%}` |
| Repetir sobre una matriz | `{{#each profile.orders}}...{{/each}}` |

La estructura de atributos se define en un esquema XDM de Adobe Experience Platform. [Más información](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

>[!TIP]
>
>Para obtener expresiones listas para usar que apliquen estas sintaxis a escenarios reales (formato de fecha, cuenta atrás, reserva condicional, etc.), consulte la página **[Fórmulas de Personalization](personalization-recipes.md)**.

## Sintaxis: reglas generales {#general-rules}

* Los identificadores pueden ser cualquier carácter Unicode excepto los siguientes caracteres especiales, que están reservados para la sintaxis Handlebars:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* La sintaxis distingue entre mayúsculas y minúsculas.

* Las palabras **true**, **false**, **null** y **undefined** solo se permiten en la primera parte de una expresión de ruta.

* En Handlebars, los valores devueltos por {{expression}} son **HTML-escaped**. Si la expresión contiene `&`, el resultado devuelto con escape de HTML se generará como `&amp;`. Si no desea que Handlebars escape un valor, utilice la &quot;pila triple&quot;.

  Supongamos que el valor del campo `profile.person.name` es &quot;Mark &amp; Mary&quot;. La sintaxis `{{profile.person.name}}` mostrará `Mark &amp; Mary`, mientras que `{{{profile.person.name}}}` mostrará `Mark & Mary`.

* En cuanto a los argumentos de funciones literales, el analizador de idioma de creación de plantillas no admite un único símbolo de barra invertida sin escape (`\`). Este carácter debe especificarse con una barra invertida (`\`) adicional. Por ejemplo:

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

* Para incluir **comillas dobles literales** dentro de un valor de cadena (por ejemplo, al generar la salida JSON), escríbalo con una barra invertida (`\"`):

  ```handlebars
  { "message": "Hello \"{{profile.person.name.firstName}}\"" }
  ```

  Salida: `{ "message": "Hello \"John\"" }`

  Como alternativa, utilice la triple pila `{{{ }}}` para generar HTML sin escape cuando el valor en sí contenga caracteres especiales que no desee codificar en HTML.

## Palabras clave reservadas {#reserved-keywords}

Algunas palabras clave están reservadas en Profile Query Language (PQL) y no se pueden usar directamente como nombres de campo o variable en expresiones de personalización. Si el esquema XDM contiene campos con nombres que coinciden con palabras clave reservadas, debe escaparlos utilizando comillas invertidas (`` ` ``) para hacer referencia a ellos en las expresiones.

**Las palabras clave reservadas incluyen:**

* `next`
* `last`
* `this`

**Ejemplo:**

Si el esquema de perfil tiene un campo denominado `next`, debe envolverlo en acentos graves:

```
{{profile.person.`next`.name}}
```

Sin las comillas invertidas, el editor de personalización falla en la validación con un error.

>[!NOTE]
>
>El escape de acento grave para palabras clave reservadas se aplica tanto a las rutas de acceso de Handlebars `{{...}}` como a las expresiones PQL `{%= ... %}`, ya que estas palabras clave están reservadas en el nivel de resolución de ruta de acceso. Esto es diferente a los nombres de campo con guiones, donde el escape de acento grave solo se admite dentro de expresiones PQL. Consulte [Claves de atributo con división de palabras](#hyphenated-keys).

## Reglas de sintaxis de PQL para claves de atributo especiales {#pql-special-keys}

Más allá de las palabras clave reservadas, dos casos adicionales requieren el escape de acento grave en las expresiones PQL.

### Claves de atributo con guiones {#hyphenated-keys}

Si el esquema XDM contiene nombres de campo con guiones (p. ej. `my-field`, `event-type`) o nombres que comiencen o contengan números, ajuste la clave en comillas invertidas dentro de expresiones PQL:

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>El escape de acento grave solo se admite dentro de expresiones PQL (`{%= ... %}`). No se admite en la interpolación Handlebars (`{{...}}`). Sin embargo, se puede hacer referencia directamente a los nombres de campo con guiones en `{{...}}` bloques (p. ej. `{{profile.my-custom-field}}`); solo falla la sintaxis de acento grave en ellos.

Sin comilla invertida en una expresión PQL, el guión se interpreta como un operador de resta y provoca un error de sintaxis de PQL.

### ID de eventos numéricos en atributos de contexto {#numeric-event-ids}

Cuando se haga referencia a atributos de evento de contexto en los que el ID de evento sea un número (por ejemplo, `1697323153`), encapsúlelo con acentos graves. Esto también se aplica dentro de funciones como `formatDate()`:

```handlebars
{% let ts = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy") %}
{{ts}}
```

## Coerción de tipo {#type-coercion}

PQL tiene establecimiento inflexible de tipos. Al comparar o pasar valores, ambos lados deben ser del mismo tipo. Casos frecuentes:

| Situación | Solución |
|----------|----------|
| Valor numérico almacenado como cadena | Usar `stringToNumber()` antes de la comparación o aritmética: `{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}` |
| Entero almacenado como cadena | Usar `string_to_integer()` o `stringToNumber()` antes de la aritmética |
| Booleano almacenado como cadena | Usar `toBool()` para convertir: `{%= toBool(profile.consents.email.val) = true %}` |

## Áreas de nombres disponibles {#namespaces}

* **Perfil**

  Este espacio de nombres le permite hacer referencia a todos los atributos definidos en el esquema de perfil descrito en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

  Es necesario definir los atributos en el esquema antes de hacer referencia a ellos en un bloque personalizado [!DNL Journey Optimizer].

  Para obtener más información sobre cómo aprovechar los atributos de perfil en condiciones, consulte [esta sección](functions/helpers.md#if-function).

  +++Referencias de muestra

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * `{{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

  +++

* **Audiencia**

  Para obtener más información sobre el servicio de segmentación, consulte [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=es){target="_blank"}.

* **Ofertas**

  Este área de nombres le permite hacer referencia a decisiones de ofertas existentes.

  Para hacer referencia a una oferta, debe declarar una ruta con la diferente información que define una oferta. Esta ruta tiene la siguiente estructura:

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  donde:

   * `offers` identifica la expresión de ruta que pertenece al área de nombres de la oferta
   * `Type` determina el tipo de representación de la oferta. Los valores posibles son: `image`, `html` y `text`
   * `Placement Id` y `Activity Id` son identificadores de ubicación y actividad
   * `Attributes` son atributos específicos de la oferta que dependen del tipo de oferta. Ejemplo: `deliveryUrl` para imágenes

  Para obtener más información sobre la API Decisions y las representaciones Offer, consulte [esta página](../offers/api-reference/offer-delivery-api/decisioning-api.md)

  Todas las referencias se validan con el esquema de ofertas con un mecanismo de validación descrito en [esta página](../personalization/personalization-build-expressions.md)

  +++Referencias de muestra

   * Ubicación donde se aloja la imagen:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * URL de destino al hacer clic en la imagen:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * Contenido de texto de la oferta procedente del motor de decisión:

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * Contenido de HTML de la oferta proveniente del motor de decisión:

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

  +++

## Ayudantes {#helpers-all}

Un asistente de Handlebars es un identificador simple que puede ir seguido de parámetros. Cada parámetro es una expresión Handlebars. Se puede acceder a estos ayudantes desde cualquier contexto de una plantilla.

Estos ayudantes de bloque se identifican con un `#` antes del nombre del ayudante y requieren un `/` de cierre coincidente, del mismo nombre.

Los bloques son expresiones que tienen un bloque de apertura (`{{# }}`) y cierre (`{{/}}`).

Para obtener más información sobre las funciones de ayuda, consulte [esta sección](functions/helpers.md).

## Tipos literales {#literal-types}

[!DNL Adobe Journey Optimizer] admite los siguientes tipos literales:

| Literal | Definición |
| ------- | ---------- |
| Cadena | Un tipo de datos compuesto por caracteres entre comillas dobles. <br>Ejemplos: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Un tipo de datos que puede ser verdadero o falso. |
| Número entero | Un tipo de datos que representa un número entero. Puede ser positivo, negativo o cero. <br>Ejemplos: `-201`, `0`, `412` |
| Matriz | Un tipo de datos que se comprende como un grupo de otros valores literales. Utiliza corchetes para agrupar y comas para delimitar entre distintos valores. <br> **Nota:** No puede tener acceso directo a las propiedades de los elementos de una matriz. <br> Ejemplos: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>El uso de la variable **xEvent** no está disponible en expresiones de personalización. Cualquier referencia a xEvent producirá errores de validación.

## Prácticas recomendadas {#best-practices}

Revise estas reglas de sintaxis antes de crear expresiones de personalización. La mayoría de los errores de tiempo de ejecución provienen de la mezcla de Handlebars y contextos PQL.

**Use la sintaxis de bloque condicional correcta**

Use siempre `{%#if%}` / `{%else if%}` / `{%else%}` / `{%/if%}`. No se admite la sintaxis `{% if %}` / `{% elseif %}` / `{% endif %}`.

```handlebars
{%#if profile.loyalty.tier = "gold"%}
Gold member content
{%else if profile.loyalty.tier = "silver"%}
Silver member content
{%else%}
Default content
{%/if%}
```

**No llame a funciones de PQL dentro de `{{...}}` bloques de Handlebars**

`{{...}}` solo resuelve las variables Handlebars y los ayudantes, no evalúa PQL. Al ajustar una función de PQL como `upperCase()` dentro de `{{...}}`, se produce el error &quot;no se pudo encontrar el asistente&quot;. Usar `{%= ... %}` en su lugar:

| Incorrecto | Correcto |
|-----------|---------|
| `{{upperCase(cleanName)}}` | `{%= upperCase(cleanName) %}` |

**Use un alias de bucle con nombre al combinar `{{#each}}` con`{%#if%}`**

`this.field` lo ha resuelto el procesador Handlebars, pero no el evaluador PQL dentro de una condición `{%#if%}`. Defina un alias con nombre con `as |item|` para que ambos contextos puedan resolver el campo:

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending.
  {%/if%}
{{/each}}
```

**Asignar resultados de funciones de PQL a una variable antes del bucle**

No se puede llamar a las UDF de PQL como `topN` directamente dentro de `{{#each}}`. Evalúelos primero con `{% let %}` y después itere en el resultado:

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

**Use `{% let %}` para evitar repetir llamadas a funciones**

Cuando un valor calculado se necesite más de una vez, almacénelo en una variable. Esto mejora la legibilidad y evita evaluaciones redundantes:

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}}, your code is: WELCOME-{%= upperCase(cleanName) %}
```

**Use el orden de argumentos correcto para`dateDiff`**

`dateDiff(start, end)` toma primero la fecha anterior. Para calcular los días restantes hasta una fecha futura, pase la fecha actual como primer argumento:

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
```

**Use `=` para comparaciones de igualdad en PQL, no`==`**

PQL usa un solo operador `=` para la igualdad. Usar `==` resulta en un error de sintaxis.

**Use comillas invertidas para nombres de campos con guiones, solo en expresiones PQL**

Si el nombre de un campo de esquema XDM contiene un guion (por ejemplo, `order-total`), encapsúlelo en comillas invertidas para evitar que el guion se analice como operador de resta. Esto solo se admite dentro de `{%= ... %}` expresiones PQL, no en `{{...}}` bloques Handlebars:

```sql
{%= profile.events.`order-total` > 100 %}
```

Para ver las expresiones listas para usar que puede copiar directamente en el contenido, consulte [Fórmulas de Personalization](personalization-recipes.md).
