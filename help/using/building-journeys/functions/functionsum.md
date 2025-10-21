---
product: journey optimizer
title: sum
description: Obtenga información sobre la suma de funciones
feature: Journeys
role: Developer
level: Experienced
keywords: suma, función, expresión, recorrido
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 12%

---

# sum {#sum}

Devuelve la suma de los valores de un conjunto de expresiones. Los valores nulos se omiten.

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

Devuelve un valor decimal.

`sum(<listInteger>)`

Devuelve un entero.

`sum(<integer>,<integer>)`

Devuelve un entero.

`sum(<decimal>,<decimal>)`

Devuelve un valor decimal.

## Ejemplos

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Devuelve 21.

`sum([10.5,null,8.1])`

Devuelve 18.6.
