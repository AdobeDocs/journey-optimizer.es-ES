---
product: adobe campaign
title: inLastDays
description: Obtenga información sobre la función en LastDays
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inLastDays {#inLastDays}

Devuelve el valor verdadero si una fecha determinada o dateTime está entre ahora y ahora: días delta.

## Categoría

Fecha 

## Sintaxis de función

`inLastDays(<dateTime>,<delta>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | integer |

## Firmas y tipo devuelto

`inLastDays(<dateTime>,<integer>)`

Devuelve un valor booleano.

## Ejemplos

`inLastDays(toDateTime('2019-12-12T01:11:00Z'), 4)`

Devuelve verdadero.
