---
product: journey optimizer
title: ordenar
description: Obtenga información acerca de la ordenación de funciones
feature: Journeys
role: Developer
level: Experienced
keywords: ordenar, función, expresión, recorrido
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 7%

---

# ordenar {#sort}

Ordena una lista de valores u objetos en orden natural.

## Categoría

Lista

## Sintaxis de función

`sort(<parameters>)`

## Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para ordenar. Para listObject, debe ser una referencia de campo. |
| keyAttributeName | cadena | Este parámetro solo es para listObject. El nombre del atributo en los objetos de la lista dada se utiliza como clave para ordenar. |
| sortingOrder | Booleano | Ascendente (true) o descendente (false) |

## Firma y tipo devuelto

`sort(<listInteger>,<boolean>)`

Devuelve una lista de enteros.

`sort(<listDecimal>,<boolean>)`

Devuelve una lista de decimales.

`sort(<listString>,<boolean>)`

Devuelve una lista de cadenas.

`sort(<listDateTimeOnly>,<boolean>)`

Devuelve una lista de horas de fecha sin tener en cuenta la zona horaria.

`sort(<listDateTime>,<boolean>)`

Devuelve una lista de fechas y horas.

`sort(<listDateOnly>,<boolean>)`

Devuelve una lista de fechas.

`sort(<listBoolean>,<boolean>)`

Devuelve una lista de valores booleanos.

`sort(<listObject>,<string>,<boolean>)`

Devuelve una lista de objetos.

## Ejemplo

`sort(["A", "C", "B"], true)`

Devuelve `["A","B","C"]`.

`sort([1, 3, 2], false)`

Devuelve `[3, 2, 1]`.

`sort(@event{my_event.productListItems}, "SKU", true)`

Devuelve el listObject ordenado por atributo SKU (orden ascendente)

