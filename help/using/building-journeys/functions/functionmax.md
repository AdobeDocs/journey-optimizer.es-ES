---
product: journey optimizer
title: max
description: Más información sobre la función máxima
feature: Journeys
role: Developer
level: Experienced
keywords: max, function, expression, recorrido
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# max{#max}

Devuelve el valor máximo entre un conjunto de expresiones, dado como una lista o dos expresiones. Los valores nulos se omiten.

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
* entero
* decimal
* dateTime
* dateTimeOnly

## Firmas y tipos devueltos

`max(<listDuration>)`

Devuelve una duración.

`max(<listInteger>)`

Devuelve una duración.

`max(<listDateTimeOnly>)`

Devuelve una fecha y hora sin considerar la zona horaria.

`max(<listDateTime>)`

Devuelve una fecha y hora.

`max(<listDateOnly>)`

Devuelve una fecha.

`max(<listDecimal>)`

Devuelve un valor decimal.

`max(<decimal>,<decimal>)`

Devuelve un valor decimal.

`max(<duration>,<duration>)`

Devuelve una duración.

`max(<dateTime>,<dateTime>)`

Devuelve una fecha y hora.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Devuelve una fecha y hora sin considerar la zona horaria.

`max(<integer>,<integer>)`

Devuelve un entero.

## Ejemplos

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

Devuelve 10.

`max([10,null,8])`

Devuelve 10.
