---
solution: Journey Optimizer
product: journey optimizer
title: Operadores
description: Obtenga información sobre los operadores en expresiones avanzadas
feature: Journeys
role: Developer
level: Experienced
keywords: expresión, sintaxis, operadores, editor, recorrido
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sK2GNHkkiJ4M5V99Uucc-b68iESNW7kCNBjHVNT-dMs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1001
ht-degree: 3%

---

# Operadores {#operators}

Existen dos tipos de operadores: operadores unarios y operadores binarios. Hay operadores unarios de la izquierda y operadores unarios de la derecha.

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@event{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## Notas importantes{#important-notes}

* Al utilizar una multiplicación (`*`), ambos campos de operación deben tener el mismo tipo, ya sea entero o decimal. Ejemplo :
   * el siguiente ejemplo es correcto: `3.0 * 4.0`
   * `3 * 4.0` generará un error

* Al utilizar el operador `+`, la expresión debe encapsularse entre paréntesis. Por ejemplo:
   * `toDateTimeOnly(toDateTime((currentTimeInMillis()) + 1))` es correcto
   * `toDateTimeOnly(toDateTime(currentTimeInMillis() + 1))` generará un error

## Lógico  {#logical}

### y

```json
<expression1> and <expression2>
```

Tanto &lt;expression1> como &lt;expression2> deben ser booleanas. El resultado es booleano.

Por ejemplo:

```json
3.14 > 2 and 3.15 < 1
```

### o

```json
<expression1> or <expression2>
```

Tanto &lt;expression1> como &lt;expression2> deben ser booleanas. El resultado es booleano.

Por ejemplo:

```json
3.14 > 2 or 3.15 < 1
```

### no

```json
not <expression>
```

&lt;expression> debe ser booleano. El resultado es booleano.

Por ejemplo:

```json
not 3.15 < 1
```

## Comparación {#comparison}

### es nulo

```json
<expression> is null
```

El resultado es booleano.

Tenga en cuenta que nulo significa que la expresión no tiene ningún valor evaluado.

Por ejemplo:

```json
@event{BarBeacon.location} is null
```

### no es nulo

```json
<expression> is not null
```

El resultado es booleano.

Tenga en cuenta que nulo significa que la expresión no tiene ningún valor evaluado.

Por ejemplo:

```json
@event{BarBeacon.location} is not null
```

### tiene null

```json
<expression> has null
```

&lt;expression> debe ser una lista. El resultado es booleano.

Resulta útil para identificar que una lista contiene al menos un valor nulo.

Por ejemplo:

```json
["foo", "bar", null] has null
```

Devuelve verdadero

```json
["foo", "bar", ""] has null
```

Devuelve falso porque &quot;&quot; no se considera nulo.

### ==

```json
<expression1> == <expression2>
```

>[!NOTE]
>
>Para &lt;expression1> y &lt;expression2> no hay ningún control de tipo de datos.

Por ejemplo:

```json
3.14 == 42
```

```json
"foo" == "bar"
```

### !=

```json
<expression1> != <expression2>
```

>[!NOTE]
>
>Para &lt;expression1> y &lt;expression2> no hay ningún control de tipo de datos.

El resultado es booleano.

Por ejemplo:

```json
3.14 != 42
```

```json
"foo" != "bar"
```

### >

```json
<expression1> > <expression2>
```

Datetime se puede comparar con Datetime.

Datetimeonly se puede comparar con Datetimeonly.

Tanto el entero como el decimal pueden compararse con ambos valores, entero o decimal.

Cualquier otra combinación está prohibida.

El resultado es booleano.

Por ejemplo:

```json
3.14 > 42
```

### >=

```json
<expression1> >= <expression2>
```

Datetime se puede comparar con Datetime.

Datetimeonly se puede comparar con Datetimeonly.

Tanto el entero como el decimal pueden compararse con ambos valores, entero o decimal.

Cualquier otra combinación está prohibida.

El resultado es booleano.

Por ejemplo:

```json
42 >= 3.14
```

### &lt;

```json
<expression1> < <expression2>
```

Datetime se puede comparar con Datetime.

Datetimeonly se puede comparar con Datetimeonly.

Tanto el entero como el decimal pueden compararse con ambos valores, entero o decimal.

Cualquier otra combinación está prohibida.

El resultado es booleano.

Por ejemplo:

```json
42 < 3.14
```

### &lt;=

```json
<expression1> <= <expression2>
```

Datetime se puede comparar con Datetime.

Datetimeonly se puede comparar con Datetimeonly.

Tanto el entero como el decimal pueden compararse con ambos valores, entero o decimal.

Cualquier otra combinación está prohibida.

El resultado es booleano.

Por ejemplo:

```json
42 <= 3.14
```

## Aritmética {#arithmetic}

### +

```json
<expression1> + <expression2>
```

Ambas expresiones deben ser numéricas (enteras o decimales).

El resultado también es numérico.

Por ejemplo:

```json
1 + 2
```

Devuelve 3

### -

```json
<expression1> - <expression2>
```

Ambas expresiones deben ser numéricas (enteras o decimales).

El resultado también es numérico.

Por ejemplo:

```json
2 - 1 
```

Devuelve 1

### /

```json
<expression1> / <expression2>
```

Ambas expresiones deben ser numéricas (enteras o decimales).

El resultado también es numérico.

&lt;expression2> no debe ser igual a 0 (devuelve 0).

Por ejemplo:

```json
4 / 2
```

Devuelve 2

### *

```json
<expression1> * <expression2>
```

Ambas expresiones deben ser numéricas (enteras o decimales).

El resultado también es numérico.

Por ejemplo:

```json
3 * 4
```

Devuelve 12

### %

```json
<expression1> % <expression2>
```

Ambas expresiones deben ser numéricas (enteras o decimales).

El resultado también es numérico.

Por ejemplo:

```json
3 % 2
```

Devuelve 1.

## Matemáticas {#math}

### es numérico

```json
<expression> is numeric
```

El tipo de expresión es entero o decimal.

Por ejemplo:

```json
@ is numeric
```

### es entero

```json
<expression> is integer
```

El tipo de expresión es entero.

Por ejemplo:

```json
@ is integer
```

### es decimal

```json
<expression> is decimal
```

El tipo de expresión es decimal.

Por ejemplo:

```json
@ is decimal
```

## Cadena {#string}

### +

```json
<string> + <expression>
```

```json
<expression> + <string>
```

Concatena dos expresiones.

Una expresión debe ser una cadena encadenada.

Por ejemplo:

```json
"the current time is " + (now())
```

Devuelve &quot;la hora actual es 2023-09-23T09:30:06.693Z&quot;

```json
(now()) + " is the current time"
```

Devuelve &quot;2023-09-23T09:30:06.693Z es la hora actual&quot;

```json
"a" + "b" + "c" + 1234
```

Devuelve &quot;abc1234&quot;.

## Fecha {#date}

### +

```json
<expression> + <duration>
```

Anexe una duración a dateTime, dateTimeOnly o duration.

Por ejemplo:

```json
(toDateTime("2023-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

Devuelve _dateTime_ 2023-12-03T15:30:30Z

```json
(toDateTimeOnly("2023-12-03T15:15:30")) + (toDuration("PT15M"))
```

Devuelve _dateTimeOnly_ 2023-12-03T15:30:30

```json
(now()) + (toDuration("PT1H"))
```

Devuelve _dateTime_ (con zona horaria UTC) una hora más tarde de la hora actual

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

Devuelve _duration_ PT2H

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página es una referencia completa de los operadores disponibles en el editor de expresiones avanzadas de Recorrido, que abarcan los operadores lógicos (`and`, `or`, `not`), comparativos (`==`, `!=`, `>`, `>=`, `<`, `<=`, `is null`, `is not null`, `has null`), aritméticos (`+`, `-`, `/`, `*`, `%`), comprobación de tipos matemáticos (`is numeric`, `is integer`, `is decimal`), concatenación de cadenas y operadores aritméticos de fecha.

**Intenciones:**

* Combinar condiciones booleanas utilizando los operadores lógicos `and`, `or` y `not`
* Compruebe si un campo o valor de expresión es nulo o no mediante `is null` / `is not null`
* Detectar valores nulos en una lista utilizando el operador `has null`
* Comparar valores numéricos, datetime y datetimeonly usando `>`, `>=`, `<`, `<=`, `==` y `!=`
* Realizar operaciones aritméticas en valores numéricos usando `+`, `-`, `/`, `*` y `%`
* Agregue una duración a un valor dateTime, dateTimeOnly o duration utilizando el operador `+`

**Glosario:**

* **Operador unario**: Operador aplicado a un solo operando; puede ser de izquierda (p. ej. `not`) o de derecha (p. ej. `is null`) *(específico del producto)*
* **Operador binario**: Operador aplicado entre dos operandos (por ejemplo, `and`, `==`, `+`) *(específico del producto)*
* **tiene null**: un operador unario derecho que devuelve true si una lista contiene al menos un elemento null *(específico del producto)*
* **es numérico / es entero / es decimal**: Operadores de comprobación de tipo que devuelven un booleano basado en el subtipo numérico de la expresión *(específico del producto)*

**Protecciones:**

* Al utilizar la multiplicación (`*`), ambos operandos deben ser del mismo tipo numérico (ambos enteros o ambos decimales); los tipos de mezcla producen un error
* Al utilizar el operador `+` para la aritmética de fechas, la expresión debe incluirse entre paréntesis para evitar errores de análisis
* Los operadores de comparación (`>`, `>=`, `<`, `<=`) solo son válidos entre tipos compatibles: Datetime con Datetime, DatetimeOnly con DatetimeOnly o numeric con numeric; cualquier otra combinación está prohibida
* Una cadena vacía `""` no se considera nula — `has null` devuelve el valor &quot;False&quot; para una lista que contiene `""`
* Los operadores `==` y `!=` no realizan ningún control de tipo de datos entre operandos

**Terminología:**

* Nombre canónico: Operators — Acrónimo: none — variantes: operadores de expresión, operadores de recorrido
* Sinónimos: `and` = &quot;AND lógico&quot;; `or` = &quot;OR lógico&quot;; `not` = &quot;NOT lógico&quot;; `%` = &quot;módulo&quot;
* No confunda: `is null` (la expresión no tiene ningún valor evaluado) ≠ `== null` (sintaxis no válida); `has null` (la lista contiene null) ≠ `is null` (la expresión en sí es null)

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Puedo multiplicar un entero por un decimal directamente?** — No; ambos operandos de `*` deben ser del mismo tipo. Use `3.0 * 4.0` (ambos decimales) o `3 * 4` (ambos enteros).
* **Q: ¿Cómo se agregan 15 minutos a dateTime?** — Usar `(toDateTime("...")) + (toDuration("PT15M"))`.
* **Q: ¿Cuál es la diferencia entre `is null` y `has null`?** — `is null` comprueba si una sola expresión no tiene ningún valor evaluado; `has null` comprueba si una lista contiene al menos un elemento nulo.
* **Q: ¿Devuelve `"" has null` true?** — No; una cadena vacía no se considera nula, por lo que el resultado es falso.
* **Q: ¿Por qué `3 * 4.0` causa un error?** — El operador `*` requiere que ambos operandos sean del mismo tipo numérico; no se permite mezclar entero y decimal.

+++
