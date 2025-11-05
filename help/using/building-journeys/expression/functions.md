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
source-git-commit: 42abfcc9711d87b2dc00df47e964dad07443f0ed
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
| Conversión | [toBool](../functions/conversion-functions.md#toBool) |
| Conversión | [toDateOnly](../functions/conversion-functions.md#toDateOnly) |
| Conversión | [toDateTime](../functions/conversion-functions.md#toDateTime) |
| Conversión | [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) |
| Conversión | [toDecimal](../functions/conversion-functions.md#toDecimal) |
| Conversión | [toDuration](../functions/conversion-functions.md#toDuration) |
| Conversión | [toInteger](../functions/conversion-functions.md#toInteger) |
| Conversión | [toString](../functions/conversion-functions.md#toString) |
| Fecha | [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) |
| Fecha | [inLastDays](../functions/date-functions.md#inLastDays) |
| Fecha | [inLastHours](../functions/date-functions.md#inLastHours) |
| Fecha | [inLastMonths](../functions/date-functions.md#inLastMonths) |
| Fecha | [inLastYears](../functions/date-functions.md#inLastYears) |
| Fecha | [inNextDays](../functions/date-functions.md#inNextDays) |
| Fecha | [inNextHours](../functions/date-functions.md#inNextHours) |
| Fecha | [inNextMonths](../functions/date-functions.md#inNextMonths) |
| Fecha | [inNextYears](../functions/date-functions.md#inNextYears) |
| Fecha | [now](../functions/date-functions.md#now) |
| Fecha | [nowWithDelta](../functions/date-functions.md#nowWithDelta) |
| Fecha | [setHours](../functions/date-functions.md#setHours) |
| Fecha | [setDays](../functions/date-functions.md#setDays) |
| Fecha | [updateTimeZone](../functions/date-functions.md#updateTimeZone) |
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
