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
source-git-commit: d58319d687d113ce680c415524fdea0400cb38f0
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
| Lista | [distinct](../functions/list-functions.md#distinct) |
| Lista | [distinctWithNull](../functions/list-functions.md#distinctWithNull) |
| Lista | [filtro](../functions/list-functions.md#filter) |
| Lista | [getListItem](../functions/list-functions.md#getListItem) |
| Lista | [in](../functions/list-functions.md#in) |
| Lista | [intersección](../functions/list-functions.md#intersect) |
| Lista | [límite](../functions/list-functions.md#limit) |
| Lista | [listSize](../functions/list-functions.md#listSize) |
| Lista | [serializeList](../functions/list-functions.md#serializeList) |
| Lista | [sort](../functions/list-functions.md#sort) |
| Matemáticas | [random](../functions/functionrandom.md) |
| Matemáticas | [round](../functions/functionround.md) |
| Cadena | [concat](../functions/string-functions.md#concat) |
| Cadena | [contain](../functions/string-functions.md#contain) |
| Cadena | [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) |
| Cadena | [endWith](../functions/string-functions.md#endWith) |
| Cadena | [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) |
| Cadena | [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) |
| Cadena | [indexOf](../functions/string-functions.md#indexOf) |
| Cadena | [isEmpty](../functions/string-functions.md#isEmpty) |
| Cadena | [isNotEmpty](../functions/string-functions.md#isNotEmpty) |
| Cadena | [lastIndexOf](../functions/string-functions.md#lastIndexOf) |
| Cadena | [length](../functions/string-functions.md#length) |
| Cadena | [lower](../functions/string-functions.md#lower) |
| Cadena | [matchRegExp](../functions/string-functions.md#matchRegExp) |
| Cadena | [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) |
| Cadena | [replace](../functions/string-functions.md#replace) |
| Cadena | [replaceAll](../functions/string-functions.md#replaceAll) |
| Cadena | [split](../functions/string-functions.md#split) |
| Cadena | [startWith](../functions/string-functions.md#startWith) |
| Cadena | [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) |
| Cadena | [substr](../functions/string-functions.md#substr) |
| Cadena | [trim](../functions/string-functions.md#trim) |
| Cadena | [upper](../functions/string-functions.md#upper) |
| Cadena | [uuid](../functions/string-functions.md#uuid) |
