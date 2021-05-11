---
title: Biblioteca de funciones
description: Biblioteca de funciones
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 9%

---

# Funciones de agregación {#aggregation}

![](../../assets/do-not-localize/badge.png)

Las funciones de agregación se utilizan para agrupar varios valores dentro de matrices [!DNL Profile Query Language] (PQL) para formar un único valor de resumen.

## Recuento

La función `count` devuelve el número de elementos dentro de la matriz dada.

**Formato**

```sql
count({ARRAY})
```

**Ejemplo**

La siguiente consulta PQL devuelve el número de pedidos de la matriz.

```sql
count(orders)
```

## Sum

La función `sum` devuelve la suma de todos los valores seleccionados dentro de la matriz.

**Formato**

```sql
sum({ARRAY})
```

**Ejemplo**

La siguiente consulta PQL devuelve la suma de todos los precios de los pedidos.

```sql
sum(orders.order.price)
```

## Promedio

La función `average` devuelve la media aritmética de todos los valores seleccionados dentro de la matriz.

**Formato**

```sql
average({ARRAY})
```

**Ejemplo**

La siguiente consulta PQL devuelve el precio promedio de todos los pedidos.

```sql
average(orders.order.price)
```

## Mínimo

La función `min` devuelve el menor de todos los valores seleccionados dentro de la matriz.

**Formato**

```sql
min({ARRAY})
```

**Ejemplo**

La siguiente consulta PQL devuelve el precio más bajo de todos los pedidos.

```sql
min(orders.order.price)
```

## Máximo

La función `max` devuelve el mayor de todos los valores seleccionados dentro de la matriz.

**Formato**

```sql
max({ARRAY})
```

**Ejemplo**

La siguiente consulta PQL devuelve el precio más alto de todos los pedidos.

```sql
max(orders.order.price)
```
