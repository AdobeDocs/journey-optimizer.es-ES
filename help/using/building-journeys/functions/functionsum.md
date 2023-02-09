---
product: journey optimizer
title: sum
description: Obtenga información sobre la suma de funciones
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sum, función, expresión, recorrido
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 16%

---

# sum {#sum}

Devuelve la suma de los valores de un conjunto de expresiones. Se omiten los valores nulos.

## Categoría

Agregación

## Sintaxis de función

`sum(<parameters>)`

## Parámetros

* listInteger
* listDecimal
* duration
* entero
* decimal

## Firmas y tipos devueltos

`sum(<listDecimal>)`

Devuelve un decimal.

`sum(<listInteger>)`

Devuelve un número entero.

`sum(<integer>,<integer>)`

Devuelve un número entero.

`sum(<decimal>,<decimal>)`

Devuelve un decimal.

## Ejemplos

`sum(@{BarBeacon.inventory},5)`

`sum([10,3,8])`

Devuelve 21.

`sum([10.5,null,8.1])`

Devuelve 18.6.
