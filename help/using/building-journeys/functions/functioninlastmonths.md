---
product: journey optimizer
title: inLastMonths
description: Obtenga información sobre la función en LastMonths
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastMonths, función, expresión, recorrido
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastMonths {#inLastMonths}

Devuelve true si una fecha o dateTime determinada está entre ahora y ahora (meses delta).

## Categoría

Fecha

## Sintaxis de función

`inLastMonths(<dateTime>,<delta>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

## Firmas y tipo devuelto

`inLastMonths(<dateTime>,<integer>)`

Devuelve un valor booleano.

## Ejemplos

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.
