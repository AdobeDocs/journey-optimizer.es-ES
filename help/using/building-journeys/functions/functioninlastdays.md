---
product: journey optimizer
title: inLastDays
description: Obtenga información sobre la función en LastDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays, función, expresión, recorrido
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastDays {#inLastDays}

Devuelve true si una fecha o dateTime determinada está entre ahora y ahora (días delta).

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
