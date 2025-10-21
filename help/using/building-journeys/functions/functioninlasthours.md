---
product: journey optimizer
title: inLastHours
description: Obtenga información sobre la función en LastHours
feature: Journeys
role: Developer
level: Experienced
keywords: inLastHours, función, expresión, recorrido
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# inLastHours {#inLastHours}

Devuelve verdadero si la fecha y hora dadas son entre ahora y ahora (horas delta).

## Categoría

Fecha

## Sintaxis de función

`inLastHours(<dateTime>,<delta>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

## Firmas y tipo devuelto

`inLastHours(<dateTime>,<integer>)`

Devuelve un valor booleano.

## Ejemplos

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.

`inLastHours(@event{MyEvent.timestamp}, 4)`

Devuelve verdadero.
