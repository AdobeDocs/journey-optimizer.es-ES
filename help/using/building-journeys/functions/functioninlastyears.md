---
product: journey optimizer
title: inLastYears
description: Obtenga información sobre la función en LastYears
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastYears, función, expresión, recorrido
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastYears {#inLastYears}

Devuelve true si una fecha o dateTime determinada está entre ahora y ahora (años delta).

## Categoría

Fecha

## Sintaxis de función

`inLastYears(<dateTime>,<delta>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

## Firmas y tipo devuelto

`inLastYears(<dateTime>,<integer>)`

Devuelve un valor booleano.

## Ejemplos

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.
