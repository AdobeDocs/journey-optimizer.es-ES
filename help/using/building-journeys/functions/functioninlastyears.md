---
product: journey optimizer
title: inLastYears
description: Obtenga información sobre la función en LastYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastYears, función, expresión, recorrido
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastYears {#inLastYears}

Devuelve el valor verdadero si una fecha determinada o dateTime está entre ahora y ahora: años delta.

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

`inLastYears(toDateTime('2010-12-12T01:11:00Z'), 4)`

Devuelve verdadero.
