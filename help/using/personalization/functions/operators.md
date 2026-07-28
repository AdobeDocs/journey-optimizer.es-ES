---
title: Biblioteca de funciones de operadores
description: Biblioteca de funciones de operadores
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
TQID: https://experienceleague.adobe.com/b4Tz4auDyWb-iaUYAie31DL5hlHh97n3rYm7EP-JjIw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: b08de542c4f952f82a503103c783e54196c6d5b6
workflow-type: tm+mt
source-wordcount: 461
ht-degree: 9%

---

# Operadores {#operators}

## Funciones booleanas {#boolean-functions}

Las funciones booleanas se utilizan para realizar lógica booleana en diferentes elementos.

### Y{#and}

La función `and` se usa para crear una conjunción lógica.

**Sintaxis**

```sql
{%= query1 and query2 %}
```

**Ejemplo**

La siguiente operación devolverá a todas las personas con país de origen como Francia y año de nacimiento de 1985.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### O{#or}

La función `or` se usa para crear una disyunción lógica.

**Sintaxis**

```sql
{%= query1 or query2 %}
```

**Ejemplo**

La siguiente operación devolverá a todas las personas con país de origen como Francia o año de nacimiento de 1985.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->

## Funciones de comparación {#comparison-functions}

Las funciones de comparación se utilizan para comparar entre diferentes expresiones y valores, lo que devuelve true o false en consecuencia.

### Es igual a{#equals}

La función `=` (igual) comprueba si un valor o expresión es igual a otro valor o expresión.

**Sintaxis**

```sql
{%= expression = value %}
```

**Ejemplo**

La siguiente operación comprueba si el país de la dirección postal es Francia.

```sql
{%= profile.homeAddress.country = "France" %}
```

### Distinto a{#notequal}

La función `!=` (no es igual) comprueba si un valor o expresión es **no** igual a otro valor o expresión.

**Sintaxis**

```sql
{%= expression != value %}
```

**Ejemplo**

La siguiente operación comprueba si el país de la dirección postal no es Francia.

```sql
{%= profile.homeAddress.country != "France" %}
```

### Mayor que{#greaterthan}

La función `>` (mayor que) se usa para comprobar si el primer valor es mayor que el segundo valor.

**Sintaxis**

```sql
{%= expression1 > expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas estrictamente después de 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Mayor o igual que{#greaterthanorequal}

La función `>=` (mayor o igual que) se usa para comprobar si el primer valor es mayor o igual que el segundo valor.

**Sintaxis**

```sql
{%= expression1 >= expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas en o después de 1970.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Menor que{#lessthan}

La función de comparación `<` (menor que) se usa para comprobar si el primer valor es menor que el segundo valor.

**Sintaxis**

```sql
{%= expression1 < expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas antes del año 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

### Menor o igual que{#lessthanorequal}

La función de comparación `<=` (menor o igual que) se usa para comprobar si el primer valor es menor o igual que el segundo valor.

**Sintaxis**

```sql
{%= expression1 <= expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas en 2000 o antes.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Operaciones con números**

## Funciones de migración de plantillas {#template-migration-functions}

Las funciones de migración de plantillas están disponibles en el editor de personalización para ayudarle a migrar las plantillas existentes a Journey Optimizer.

### Comparar mediante el operador{#amp-compare}

La función `ampCompare` compara dos valores utilizando el operador de comparación especificado.

**Sintaxis**

```sql
{%= ampCompare(value1, value2, operator) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `value1` | Primer valor para comparar. |
| `value2` | Segundo valor para comparar. |
| `operator` | Entero que representa el operador de comparación que se va a utilizar. |

**Ejemplo**

```sql
{%= ampCompare(profile.person.age, 18, 4) %}
```

### Rango de subcadenas{#amp-substr}

La función `ampSubstr` devuelve una parte de una cadena entre los índices de inicio y fin especificados.

**Sintaxis**

```sql
{%= ampSubstr(string, startIndex, endIndex) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `string` | La cadena de origen. |
| `startIndex` | Índice de inicio de la subcadena (entero). |
| `endIndex` | Índice final de la subcadena (entero). |

**Ejemplo**

La siguiente expresión devuelve los cinco primeros caracteres de la cadena &quot;Hello World&quot;.

```sql
{%= ampSubstr("Hello World", 0, 5) %}
```

Devuelve `Hello`.

### Comparar con{#compare-to}

La función `compareTo` compara dos cadenas lexicográficamente. Devuelve un entero negativo si la primera cadena va antes que la segunda, cero si son iguales o un entero positivo si la primera cadena va después de la segunda.

**Sintaxis**

```sql
{%= compareTo(string1, string2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `string1` | Primera cadena que comparar. |
| `string2` | Segunda cadena para comparar. |

**Ejemplo**

```sql
{%= compareTo("apple", "banana") %}
```
