---
product: journey optimizer
title: inNextDays
description: Obtenga información sobre la función en NextDays
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inNextDays {#inNextDays}

Devuelve el valor verdadero si una fecha determinada o dateTime está entre ahora y ahora + días delta.

## Categoría

Fecha

## Sintaxis de función

`inNextDays(<dateTime>,<delta>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | integer |

## Firmas y tipo devuelto

`inNextDays(<dateTime>,<integer>)`

Devuelve un valor booleano.

## Ejemplos

`inNextDays(toDateTime('2010-12-12T01:11:00Z'), 4)`

Devuelve verdadero.
