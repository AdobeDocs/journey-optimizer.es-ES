---
title: Biblioteca de funciones de agregación
description: Biblioteca de funciones de agregación
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---

# Funciones de agregación {#aggregation}

Las funciones de agregación se utilizan para agrupar varios valores y formar un único valor de resumen.

## Recuento{#count}

La variable `count` devuelve el número de elementos dentro de la matriz dada.

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

La variable `sum` devuelve la suma de todos los valores seleccionados dentro de la matriz.

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

La variable `average` devuelve la media aritmética de todos los valores seleccionados dentro de la matriz.

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

La variable `min` devuelve el menor de todos los valores seleccionados dentro de la matriz.

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

La variable `max` devuelve el mayor de todos los valores seleccionados dentro de la matriz.

**Formato**

```sql
{%= max(array) %}
```

**Ejemplo**

La siguiente operación devuelve el precio más alto de todos los pedidos.

```sql
{%=max(orders.order.price)%}
```
