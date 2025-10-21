---
product: journey optimizer
title: inNextYears
description: Obtenga información sobre la función en NextYears
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextYears, función, expresión, recorrido
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextYears {#inNextYears}

Devuelve true si una fecha o dateTime determinada está entre ahora y ahora + años delta.

## Categoría

Fecha

## Sintaxis de función

`inNextYears(<dateTime>,<delta>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

## Firmas y tipo devuelto

`inNextYears(<dateTime>,<integer>)`

Devuelve un valor booleano.

## Ejemplos

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Devuelve verdadero.
