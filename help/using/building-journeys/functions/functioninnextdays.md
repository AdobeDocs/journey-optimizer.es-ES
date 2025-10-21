---
product: journey optimizer
title: inNextDays
description: Obtenga información sobre la función en NextDays
feature: Journeys
role: Engineer
level: Experienced
keywords: inNextDays, función, expresión, recorrido
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextDays {#inNextDays}

Devuelve true si una fecha o dateTime determinados están entre ahora y ahora + días delta.

## Categoría

Fecha

## Sintaxis de función

`inNextDays(<dateTime>,<delta>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

## Firmas y tipo devuelto

`inNextDays(<dateTime>,<integer>)`

Devuelve un valor booleano.

## Ejemplos

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.
