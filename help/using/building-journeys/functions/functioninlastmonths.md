---
product: journey optimizer
title: inLastMonths
description: Obtenga información sobre la función en LastMonths
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inLastMonths {#inLastMonths}

Devuelve el valor verdadero si una fecha determinada o dateTime está entre ahora y ahora: meses delta.

## Categoría

Fecha

## Sintaxis de función

`inLastMonths(<dateTime>,<delta>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | integer |

## Firmas y tipo devuelto

`inLastMonths(<dateTime>,<integer>)`

Devuelve un valor booleano.

## Ejemplos

`inLastMonths(toDateTime('2010-12-12T01:11:00Z'), 4)`

Devuelve verdadero.
