---
title: Biblioteca de funciones
description: Biblioteca de funciones
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---

# Funciones matemáticas {#math}

![](../../assets/do-not-localize/badge.png)

Las funciones aritméticas se utilizan para realizar cálculos básicos de los valores de [!DNL Profile Query Language] (PQL).

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
