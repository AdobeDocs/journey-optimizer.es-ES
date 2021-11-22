---
product: adobe campaign
title: min
description: Obtenga información sobre el administrador de funciones
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 6%

---

# min {#min}

Devuelve el valor mínimo entre un conjunto de expresiones, dadas como una lista o dos expresiones. Se omiten los valores nulos.

## Categoría

Agregación

## Sintaxis de función

`min(<parameters>)`

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

`min(<listDuration>)`

Devuelve una duración.

`min(<listInteger>)`

Devuelve una duración.

`min(<listDateTimeOnly>)`

Devuelve una fecha y hora sin tener en cuenta la zona horaria.

`min(<listDateTime>)`

Devuelve una fecha y hora.

`min(<listDateOnly>)`

Devuelve una fecha.

`min(<listDecimal>)`

Devuelve un decimal.

`min(<decimal>,<decimal>)`

Devuelve un decimal.

`min(<duration>,<duration>)`

Devuelve una duración.

`min(<dateTime>,<dateTime>)`

Devuelve una fecha y hora.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Devuelve una fecha y hora sin tener en cuenta la zona horaria.

`min(<integer>,<integer>)`

Devuelve un número entero.

## Ejemplos

`min(@{BarBeacon.inventory},5)`

`min([10,3,8])`

Devuelve 3.

`min([10,null,8])`

Devuelve 8.
