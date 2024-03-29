---
product: journey optimizer
title: inNextDays
description: Obtenga información sobre la función en NextDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextDays, función, expresión, recorrido
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
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
