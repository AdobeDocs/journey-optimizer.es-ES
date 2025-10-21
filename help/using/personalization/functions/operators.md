---
title: Biblioteca de funciones de operadores
description: Biblioteca de funciones de operadores
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 11%

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
