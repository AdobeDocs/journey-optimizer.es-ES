---
product: journey optimizer
title: min
description: Más información sobre la función min
feature: Journeys
role: Engineer
level: Experienced
keywords: min, function, expression, recorrido
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# min {#min}

Devuelve el valor mínimo entre un conjunto de expresiones, dado como una lista o dos expresiones. Los valores nulos se omiten.

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
* entero
* decimal
* dateTime
* dateTimeOnly

## Firmas y tipos devueltos

`min(<listDuration>)`

Devuelve una duración.

`min(<listInteger>)`

Devuelve una duración.

`min(<listDateTimeOnly>)`

Devuelve una fecha y hora sin considerar la zona horaria.

`min(<listDateTime>)`

Devuelve una fecha y hora.

`min(<listDateOnly>)`

Devuelve una fecha.

`min(<listDecimal>)`

Devuelve un valor decimal.

`min(<decimal>,<decimal>)`

Devuelve un valor decimal.

`min(<duration>,<duration>)`

Devuelve una duración.

`min(<dateTime>,<dateTime>)`

Devuelve una fecha y hora.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Devuelve una fecha y hora sin considerar la zona horaria.

`min(<integer>,<integer>)`

Devuelve un entero.

## Ejemplos

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Devuelve 3.

`min([10,null,8])`

Devuelve 8.
