---
title: Biblioteca de funciones
description: Biblioteca de funciones
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 9%

---

# Operadores {#operators}

![](../../assets/do-not-localize/badge.png)

## Y

La función `and` se utiliza para crear una conjunción lógica.

**Formato**

```sql
{QUERY} and {QUERY}
```

**Ejemplo**

La siguiente consulta PQL devolverá todas las personas con el país de origen como Canadá y el año de nacimiento de 1985.

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## O

La función `or` se utiliza para crear una disyunción lógica.

**Formato**

```sql
{QUERY} or {QUERY}
```

**Ejemplo**

La siguiente consulta PQL devolverá a todas las personas con el país de origen como Canadá o año de nacimiento de 1985.

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## No

La función `not` (o `!`) se utiliza para crear una negación lógica.

**Formato**

```sql
not ({QUERY})
!({QUERY})
```

**Ejemplo**

La siguiente consulta PQL devolverá a todas las personas que no tengan su país de origen como Canadá.

```sql
not (homeAddress.countryISO = "CA")
```

## Si

La función `if` se utiliza para resolver una expresión en función de si una condición especificada es verdadera.

**Formato**

```sql
if ({TEST_EXPRESSION}, {TRUE_EXPRESSION}, {FALSE_EXPRESSION})
```

| Argumento | Descripción |
| --------- | ----------- |
| `{TEST_EXPRESSION}` | La expresión booleana que se está probando. |
| `{TRUE_EXPRESSION}` | La expresión cuyo valor se utilizará si `{TEST_EXPRESSION}` es verdadera. |
| `{FALSE_EXPRESSION}` | La expresión cuyo valor se utilizará si `{TEST_EXPRESSION}` es false. |

**Ejemplo**

La siguiente consulta PQL establecerá el valor como `1` si el país de origen es Canadá y `2` si el país de origen no es Canadá.

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## Es igual a

La función `=` (es igual que) comprueba si un valor o expresión es igual a otro valor o expresión.

**Formato**

```sql
{EXPRESSION} = {VALUE}
```

**Ejemplo**

La siguiente consulta PQL comprueba si el país de la dirección principal está en Canadá.

```sql
homeAddress.countryISO = "CA"
```

## Distinto a

La función `!=` (no igual) comprueba si un valor o expresión es **no** igual a otro valor o expresión.

**Formato**

```sql
{EXPRESSION} != {VALUE}
```

**Ejemplo**

La siguiente consulta PQL comprueba si el país de la dirección principal no está en Canadá.

```sql
homeAddress.countryISO != "CA"
```

## Greater than

La función `>` (buena que) se utiliza para comprobar si el primer valor es bueno que el segundo valor.

**Formato**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**Ejemplo**

La siguiente consulta PQL define las personas cuyo cumpleaños no cae en enero o febrero.

```sql
person.birthMonth > 2
```

## Greater than or equal to

La función `>=` (buena o igual que) se utiliza para comprobar si el primer valor es bueno o igual al segundo valor.

**Formato**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**Ejemplo**

La siguiente consulta PQL define las personas cuyo cumpleaños no cae en enero o febrero.

```sql
person.birthMonth >= 3
```

## Less than

La función de comparación `<` (menor que) se utiliza para comprobar si el primer valor es menor que el segundo valor.

**Formato**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**Ejemplo**

La siguiente consulta PQL define las personas cuyo cumpleaños es en enero.

```sql
person.birthMonth < 2
```

## Less than or equal to

La función de comparación `<=` (menor o igual que) se utiliza para comprobar si el primer valor es menor o igual que el segundo valor.

**Formato**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**Ejemplo**

La siguiente consulta PQL define las personas cuyo cumpleaños es enero o febrero.

```sql
person.birthMonth <= 2
```

## Add

La función `+` (suma) se utiliza para encontrar la suma de dos expresiones de argumento.

**Formato**

```sql
{NUMBER} + {NUMBER}
```

**Ejemplo**

La siguiente consulta PQL resume el precio de dos productos diferentes.

```sql
product1.price + product2.price
```

## Multiplicar

La función `*` (multiplicación) se utiliza para encontrar el producto de dos expresiones de argumento.

**Formato**

```sql
{NUMBER} * {NUMBER}
```

**Ejemplo**

La siguiente consulta PQL encuentra el producto del inventario y el precio de un producto para encontrar el valor bruto del producto.

```sql
product.inventory * product.price
```

## Sustraer

La función `-` (resta) se utiliza para encontrar la diferencia de dos expresiones de argumento.

**Formato**

```sql
{NUMBER} - {NUMBER}
```

**Ejemplo**

La siguiente consulta PQL encuentra la diferencia de precio entre dos productos diferentes.

```sql
product1.price - product2.price
```

## Dividir

La función `/` (división) se utiliza para encontrar el cociente de dos expresiones de argumento.

**Formato**

```sql
{NUMBER} / {NUMBER}
```

**Ejemplo**

La siguiente consulta PQL encuentra el cociente entre el total de productos vendidos y el total de dinero ganado para ver el coste promedio por artículo.

```sql
totalProduct.price / totalProduct.sold
```

## Remainte

La función `%` (módulo/resto) se utiliza para encontrar el resto después de dividir las dos expresiones de argumento.

**Formato**

```sql
{NUMBER} % {NUMBER}
```

**Ejemplo**

La siguiente consulta PQL comprueba si la edad de la persona es divisible entre cinco.

```sql
person.age % 5 = 0
```
