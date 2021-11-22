---
product: adobe campaign
title: max
description: Obtenga información sobre la función max
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 6%

---

# max{#max}

Devuelve el valor máximo entre un conjunto de expresiones, dadas como una lista o dos expresiones. Se omiten los valores nulos.

## Categoría

Agregación

## Sintaxis de función

`max(<parameter>)`

## Parámetros

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duration
* integer
* decimal
* dateTime
* dateTimeOnly

## Firmas y tipos devueltos

`max(<listDuration>)`

Devuelve una duración.

`max(<listInteger>)`

Devuelve una duración.

`max(<listDateTimeOnly>)`

Devuelve una fecha y hora sin tener en cuenta la zona horaria.

`max(<listDateTime>)`

Devuelve una fecha y hora.

`max(<listDateOnly>)`

Devuelve una fecha.

`max(<listDecimal>)`

Devuelve un decimal.

`max(<decimal>,<decimal>)`

Devuelve un decimal.

`max(<duration>,<duration>)`

Devuelve una duración.

`max(<dateTime>,<dateTime>)`

Devuelve una fecha y hora.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Devuelve una fecha y hora sin tener en cuenta la zona horaria.

`max(<integer>,<integer>)`

Devuelve un número entero.

## Ejemplos

`max(@{BarBeacon.inventory},5)`

`max([10,3,8])`

Devuelve 10.

`max([10,null,8])`

Devuelve 10.
