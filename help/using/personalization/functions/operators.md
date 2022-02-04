---
title: Biblioteca de funciones de operadores
description: Biblioteca de funciones de operadores
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: baa98afcc8e5e9be3062c8c16adc7f4ae17b15b7
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 11%

---

# Operadores {#operators}

## Funciones booleanas {#boolean-functions}

Las funciones booleanas se utilizan para realizar lógicas booleanas en distintos elementos.

### Y{#and}

La variable `and` para crear una conjunción lógica.

**Formato**

```sql
{%= query1 and query2 %}
```

**Ejemplo**

La siguiente operación devolverá a todas las personas con el país de origen como Francia y el año de nacimiento de 1985.

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### O{#or}

La variable `or` para crear una disyunción lógica.

**Formato**

```sql
{%= query1 or query2 %}
```

**Ejemplo**

La siguiente operación devolverá a todas las personas que tengan un país de origen como Francia o el año de nacimiento de 1985.

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Format**

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

Las funciones de comparación se utilizan para comparar diferentes expresiones y valores, devolviendo true o false en consecuencia.

### Es igual a{#equals}

La variable `=` (es igual que) comprueba si un valor o expresión es igual a otro valor o expresión.

**Formato**

```sql
{%= expression = value %}
```

**Ejemplo**

La siguiente operación comprueba si el país de dirección es Francia.

```sql
{%= profile.homeAddress.country = "France" %}
```

### Distinto a{#notequal}

La variable `!=` función (no igual) comprueba si hay un valor o expresión **not** igual a otro valor o expresión.

**Formato**

```sql
{%= expression != value %}
```

**Ejemplo**

La siguiente operación comprueba si el país de la dirección principal no es Francia.

```sql
{%= profile.homeAddress.country != "France" %}
```

### Greater than{#greaterthan}

La variable `>` (bueno que) se utiliza para comprobar si el primer valor es bueno que el segundo valor.

**Formato**

```sql
{%= expression1 > expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas estrictamente después de 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Mayor o igual que{#greaterthanorequal}

La variable `>=` (buena o igual que) se utiliza para comprobar si el primer valor es bueno o igual al segundo valor.

**Formato**

```sql
{%= expression1 >= expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas en 1970 o después de 1970.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Menos de{#lessthan}

La variable `<` (menor que) para comprobar si el primer valor es menor que el segundo valor.

**Formato**

```sql
{%= expression1 < expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas antes de 2000.

```sql
{%= profile.person.birthYear < 2000 %}
```

### Less than or equal to{#lessthanorequal}

La variable `<=` (menor o igual que) se utiliza la función de comparación para comprobar si el primer valor es menor o igual que el segundo valor.

**Formato**

```sql
{%= expression1 <= expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas en 2000 o antes.

```sql
{%= profile.person.birthYear <= 2000 %}
```

**Operaciones con números**
