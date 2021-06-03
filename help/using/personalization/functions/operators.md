---
title: Biblioteca de funciones
description: Biblioteca de funciones
source-git-commit: ca739254e8b113d6f511573c0aa427427b263b3b
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 11%

---

# Operadores {#operators}

![](../../assets/do-not-localize/badge.png)

## Funciones booleanas

Las funciones booleanas se utilizan para realizar lógicas booleanas en distintos elementos.

### Y{#and}

La función `and` se utiliza para crear una conjunción lógica.

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

La función `or` se utiliza para crear una disyunción lógica.

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





## Funciones de comparación

Las funciones de comparación se utilizan para comparar diferentes expresiones y valores, devolviendo true o false en consecuencia.

### Es igual a{#equals}

La función `=` (es igual que) comprueba si un valor o expresión es igual a otro valor o expresión.

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

La función `!=` (no igual) comprueba si un valor o expresión es **no** igual a otro valor o expresión.

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

La función `>` (buena que) se utiliza para comprobar si el primer valor es bueno que el segundo valor.

**Formato**

```sql
{%= expression1 > expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas estrictamente después de 1970.

```sql
{%= profile.person.birthYear > 1970 %}
```

### Greater than or equal to{#greaterthanorequal}

La función `>=` (buena o igual que) se utiliza para comprobar si el primer valor es bueno o igual al segundo valor.

**Formato**

```sql
{%= expression1 >= expression2 %}
```

**Ejemplo**

La siguiente operación define a las personas nacidas en 1970 o después de 1970.

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Less than{#lessthan}

La función de comparación `<` (menor que) se utiliza para comprobar si el primer valor es menor que el segundo valor.

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

La función de comparación `<=` (menor o igual que) se utiliza para comprobar si el primer valor es menor o igual que el segundo valor.

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

