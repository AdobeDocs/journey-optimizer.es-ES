---
product: journey optimizer
title: inNextHours
description: Obtenga información sobre la función en NextHours
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextHours, función, expresión, recorrido
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextHours {#inNextHours}

Devuelve true si una fecha o dateTime determinada está entre ahora y ahora + horas delta.

## Categoría

Fecha

## Sintaxis de función

`inNextHours(<dateTime>,<delta>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

## Firmas y tipo devuelto

`inNextHours(<dateTime>,<integer>)`

Devuelve un valor booleano.

## Ejemplos

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.
