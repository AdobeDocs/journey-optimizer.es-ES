---
product: journey optimizer
title: listSize
description: Obtenga información sobre la función listSize
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: listSize, función, expresión, recorrido
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 11%

---

# listSize {#listSize}

Cuenta el número de elementos de la lista.

## Categoría

Lista

## Sintaxis de función

`listSize(<parameters>)`

## Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para procesar. Para listObject, debe ser una referencia de campo. Un listObject no puede contener un objeto nulo. |

## Firmas y tipo devuelto

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Devuelve un entero.

`listSize(<listObject>)`

## Ejemplo

`listSize([10,2,3])`

Devuelve 3.

`listSize(@event{my_event.productListItems})`

Devuelve el número de objetos de una matriz determinada de objetos (tipo listObject).
