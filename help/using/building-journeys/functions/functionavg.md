---
product: adobe campaign
title: avg
description: Obtenga información sobre la función avg
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 12%

---

# avg {#avg}

Devuelve el valor promedio entre un conjunto de expresiones, dado como una lista o como dos expresiones. Se omiten los valores nulos.


## Categoría

Agregación

## Sintaxis de función

`avg(<parameter>)`

## Parámetros

Tipos compatibles:

* listInteger
* listDecimal
* decimal
* integer

## Firmas y tipo devuelto

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Devuelve un decimal.

## Ejemplos

`avg(@{BarBeacon.inventory},5)`

`avg([10,3,8])`

Devuelve 7.0.

`avg(10.2, 3)`

Devuelve 6.6.
