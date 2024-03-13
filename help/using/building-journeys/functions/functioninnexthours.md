---
product: journey optimizer
title: inNextHours
description: Obtenga información sobre la función en NextHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextHours, función, expresión, recorrido
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
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
