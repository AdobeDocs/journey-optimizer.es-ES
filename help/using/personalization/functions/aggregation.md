---
title: Biblioteca de funciones
description: Biblioteca de funciones
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---

# Funciones de agregación {#aggregation}

![](../../assets/do-not-localize/badge.png)

Las funciones de agregación se utilizan para agrupar varios valores y formar un único valor de resumen.

## Recuento{#count}

La función `count` devuelve el número de elementos dentro de la matriz dada.

**Formato**

```sql
{%= count(array) %}
```

**Ejemplo**

La siguiente operación devuelve el número de pedidos de la matriz.

```sql
{%= count(orders) %}
```

## Sum{#sum}

La función `sum` devuelve la suma de todos los valores seleccionados dentro de la matriz.

**Formato**

```sql
{%= sum(array) %}
```

**Ejemplo**

La siguiente operación devuelve la suma de todos los precios de los pedidos.

```sql
{%=sum(orders.order.price)%}
```

## Promedio{#average}

La función `average` devuelve la media aritmética de todos los valores seleccionados dentro de la matriz.

**Formato**

```sql
{%= average(array) %}
```

**Ejemplo**

La siguiente operación devuelve el precio promedio de todos los pedidos.

```sql
{%=average(orders.order.price)%}
```

## Mínimo{#min}

La función `min` devuelve el menor de todos los valores seleccionados dentro de la matriz.

**Formato**

```sql
{%= min(array) %}
```

**Ejemplo**

La siguiente operación devuelve el precio más bajo de todos los pedidos.

```sql
{%=min(orders.order.price)%}
```

## Máximo{#max}

La función `max` devuelve el mayor de todos los valores seleccionados dentro de la matriz.

**Formato**

```sql
{%= max(array) %}
```

**Ejemplo**

La siguiente operación devuelve el precio más alto de todos los pedidos.

```sql
{%=max(orders.order.price)%}
```
