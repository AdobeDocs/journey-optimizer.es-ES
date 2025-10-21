---
product: journey optimizer
title: inLastDays
description: Obtenga información sobre la función en LastDays
feature: Journeys
role: Developer
level: Experienced
keywords: inLastDays, función, expresión, recorrido
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 19%

---

# inLastDays {#inLastDays}

Devuelve verdadero si un dateTime determinado está entre ahora y ahora (días delta).

## Categoría

Fecha

## Sintaxis de función

`inLastDays(<dateTime>,<delta>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

## Firmas y tipo devuelto

`inLastDays(<dateTime>,<integer>)`

Devuelve un valor booleano.

## Ejemplos

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.
