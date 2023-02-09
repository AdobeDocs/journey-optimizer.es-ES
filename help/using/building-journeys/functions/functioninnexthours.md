---
product: journey optimizer
title: inNextHours
description: Obtenga información sobre la función en NextHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextHours, función, expresión, recorrido
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextHours {#inNextHours}

Devuelve el valor verdadero si una fecha determinada o dateTime está entre ahora y ahora + horas delta.

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

`inNextHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

Devuelve verdadero.
