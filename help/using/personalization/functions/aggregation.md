---
title: Biblioteca de funciones de agregación
description: Biblioteca de funciones de agregación
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---

# Funciones de agregación {#aggregation}

Las funciones de agregación se utilizan para agrupar varios valores para formar un único valor de resumen.

## Promedio{#average}

La función `average` devuelve la media aritmética de todos los valores seleccionados dentro de la matriz.

**Sintaxis**

```sql
{%= average(array) %}
```

**Ejemplo**

La siguiente operación devuelve el precio medio de todos los pedidos.

```sql
{%=average(orders.order.price)%}
```

## Count{#count}

La función `count` devuelve el número de elementos dentro de la matriz determinada.

**Sintaxis**

```sql
{%= count(array) %}
```

**Ejemplo**

La siguiente operación devuelve el número de pedidos de la matriz.

```sql
{%= count(orders) %}
```

## Máximo{#max}

La función `max` devuelve el mayor de todos los valores seleccionados dentro de la matriz.

**Sintaxis**

```sql
{%= max(array) %}
```

**Ejemplo**

La siguiente operación devuelve el precio más alto de todos los pedidos.

```sql
{%=max(orders.order.price)%}
```

## Mínimo{#min}

La función `min` devuelve el menor de todos los valores seleccionados dentro de la matriz.

**Sintaxis**

```sql
{%= min(array) %}
```

**Ejemplo**

La siguiente operación devuelve el precio más bajo de todos los pedidos.

```sql
{%=min(orders.order.price) %}
```

## Sum{#sum}

La función `sum` devuelve la suma de todos los valores seleccionados dentro de la matriz.

**Sintaxis**

```sql
{%= sum(array) %}
```

**Ejemplo**

La siguiente operación devuelve la suma de todos los precios de los pedidos.

```sql
{%=sum(orders.order.price)%}
```
