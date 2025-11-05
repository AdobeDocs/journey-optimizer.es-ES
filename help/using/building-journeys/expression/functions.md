---
solution: Journey Optimizer
product: journey optimizer
title: Funciones
description: Más información sobre las funciones
feature: Journeys
role: Developer
level: Experienced
keywords: función, expresiones, editor, recorrido
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: af1babe501a5b2c6a67730396a8f5e2c5d85e60a
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 69%

---

# Funciones {#functions}

Una función puede tener diferentes firmas (un conjunto diferente de parámetros ordenados). Una firma de función puede tener expresiones 0-N como parámetros ordenados.

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

Cada función tiene un tipo devuelto específico.

Esta es la lista de funciones compatibles.

## Funciones principales

| Categoría | Función |
|-------------|-----------------------|
| Adobe Experience Platform | [inAudience](../functions/functioninaudience.md) |
| Agregación | [avg](../functions/aggregation-functions.md#avg) |
| Agregación | [count](../functions/aggregation-functions.md#count) |
| Agregación | [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) |
| Agregación | [countWithNull](../functions/aggregation-functions.md#countWithNull) |
| Agregación | [distinctCount](../functions/aggregation-functions.md#distinctCount) |
| Agregación | [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) |
| Agregación | [max](../functions/aggregation-functions.md#max) |
| Agregación | [min](../functions/aggregation-functions.md#min) |
| Agregación | [sum](../functions/aggregation-functions.md#sum) |
| Conversión | [toBool](../functions/functiontobool.md) |
| Conversión | [toDateOnly](../functions/functiontodateonly.md) |
| Conversión | [toDateTime](../functions/functiontodatetime.md) |
| Conversión | [toDateTimeOnly](../functions/functiontodatetimeonly.md) |
| Conversión | [toDecimal](../functions/functiontodecimal.md) |
| Conversión | [toDuration](../functions/functiontoduration.md) |
| Conversión | [toInteger](../functions/functiontointeger.md) |
| Conversión | [toString](../functions/functiontostring.md) |
| Fecha | [currentTimeInMillis](../functions/functioncurrenttimeinmillis.md) |
| Fecha | [inLastDays](../functions/functioninlastdays.md) |
| Fecha | [inLastHours](../functions/functioninlasthours.md) |
| Fecha | [inLastMonths](../functions/functioninlastmonths.md) |
| Fecha | [inLastYears](../functions/functioninlastyears.md) |
| Fecha | [inNextDays](../functions/functioninnextdays.md) |
| Fecha | [inNextHours](../functions/functioninnexthours.md) |
| Fecha | [inNextMonths](../functions/functioninnextmonths.md) |
| Fecha | [inNextYears](../functions/functioninnextyears.md) |
| Fecha | [now](../functions/functionnow.md) |
| Fecha | [nowWithDelta](../functions/functionnowwithdelta.md) |
| Fecha | [setHours](../functions/functionsethours.md) |
| Fecha | [setDays](../functions/functionsetdays.md) |
| Fecha | [updateTimeZone](../functions/functionupdatetimezone.md) |
| Lista | [distinct](../functions/functiondistinct.md) |
| Lista | [distinctWithNull](../functions/functiondistinctwithnull.md) |
| Lista | [filtro](../functions/functionfilter.md) |
| Lista | [getListItem](../functions/functiongetlistitem.md) |
| Lista | [in](../functions/functionin.md) |
| Lista | [intersección](../functions/functionintersect.md) |
| Lista | [límite](../functions/functionlimit.md) |
| Lista | [listSize](../functions/functionlistsize.md) |
| Lista | [serializeList](../functions/functionserializelist.md) |
| Lista | [sort](../functions/functionsort.md) |
| Matemáticas | [random](../functions/functionrandom.md) |
| Matemáticas | [round](../functions/functionround.md) |
| Cadena | [concat](../functions/functionconcat.md) |
| Cadena | [contain](../functions/functioncontain.md) |
| Cadena | [containIgnoreCase](../functions/functioncontainwithignorecase.md) |
| Cadena | [endWith](../functions/functionendwith.md) |
| Cadena | [endWithIgnoreCase](../functions/functionendwithignorecase.md) |
| Cadena | [equalIgnoreCase](../functions/functionequalignorecase.md) |
| Cadena | [indexOf](../functions/functionindexof.md) |
| Cadena | [isEmpty](../functions/functionisempty.md) |
| Cadena | [isNotEmpty](../functions/functionisnotempty.md) |
| Cadena | [lastIndexOf](../functions/functionlastindexof.md) |
| Cadena | [length](../functions/functionlength.md) |
| Cadena | [lower](../functions/functionlower.md) |
| Cadena | [matchRegExp](../functions/functionmatchregexp.md) |
| Cadena | [notEqualIgnoreCase](../functions/functionnotequalignorecase.md) |
| Cadena | [replace](../functions/functionreplace.md) |
| Cadena | [replaceAll](../functions/functionreplaceall.md) |
| Cadena | [split](../functions/functionsplit.md) |
| Cadena | [startWith](../functions/functionstartwith.md) |
| Cadena | [startWithIgnoreCase](../functions/functionstartwithignorecase.md) |
| Cadena | [substr](../functions/functionsubstr.md) |
| Cadena | [trim](../functions/functiontrim.md) |
| Cadena | [upper](../functions/functionupper.md) |
| Cadena | [uuid](../functions/functionuuid.md) |
