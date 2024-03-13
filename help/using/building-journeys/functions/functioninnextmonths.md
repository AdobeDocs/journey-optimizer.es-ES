---
product: journey optimizer
title: inNextMonths
description: Obtenga información sobre la función en NextMonths
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextMonths, función, expresión, recorrido
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextMonths {#inNextMonths}

Devuelve verdadero si una fecha o fechaHora determinada está entre ahora y ahora + meses delta.

## Categoría

Fecha

## Sintaxis de función

`inNextMonths(<dateTime>,<delta>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

## Firmas y tipo devuelto

`inNextMonths(<dateTime>,<integer>)`

Devuelve un valor booleano.

## Ejemplos

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Devuelve verdadero.
