---
product: journey optimizer
title: distinctCountWithNull
description: Obtenga información sobre la función distinctCountWithNull
feature: Journeys
role: Engineer
level: Experienced
keywords: distinctCountWithNull, función, expresión, recorrido
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# distinctCountWithNull {#distinctCountWithNull}

Cuenta el número de valores diferentes, incluidos los valores nulos.

Tenga en cuenta que el parámetro `<listObject>` no se admite en esta función.

## Categoría

Agregación

## Sintaxis de función

`distinctCountWithNull(<listAny>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Firma y tipo devuelto

`distinctCountWithNull(<listAny>)`

Devuelve un entero.

## Ejemplo

`distinctCountWithNull([10,2,10,null])`

Devuelve 3.
