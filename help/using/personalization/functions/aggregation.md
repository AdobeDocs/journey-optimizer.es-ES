---
title: Biblioteca de funciones de agregación
description: Biblioteca de funciones de agregación
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
TQID: https://experienceleague.adobe.com/y1ivXVJe-Y5aIkMu--Tz22U0j-cuGcTUYrdkCkl1xyE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 157
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
