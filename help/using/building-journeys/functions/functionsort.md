---
product: journey optimizer
title: sort
description: Obtenga información sobre la ordenación de funciones
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 8%

---

# sort {#sort}

Ordena una lista de valores u objetos en el orden natural.

>[!NOTE]
>
>Si la lista de destino es un listObject, esta función solo se puede utilizar en expresiones de acción personalizadas.

## Categoría

Lista

## Sintaxis de función

`sort(<parameters>)`

## Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para ordenar. Para listObject, debe ser una referencia de campo. |
| keyAttributeName | string | Este parámetro solo es para listObject. El nombre de atributo de los objetos de la lista dada se utiliza como clave para la ordenación. |
| sortingOrder | Booleano | Ascendente (true) o descendente (false) |

## Firma y tipo devuelto

`sort(<listInteger>,<boolean>)`

Devuelve una lista de enteros.

`sort(<listDecimal>,<boolean>)`

Devuelve una lista de decimales.

`sort(<listString>,<boolean>)`

Devuelve una lista de cadenas.

`sort(<listDateTimeOnly>,<boolean>)`

Devuelve una lista de tiempos de datos sin tener en cuenta la zona horaria.

`sort(<listDateTime>,<boolean>)`

Devuelve una lista de tiempos de datos.

`sort(<listDateOnly>,<boolean>)`

Devuelve una lista de fechas.

`sort(<listBoolean>,<boolean>)`

Devuelve una lista de booleanos.

`sort(<listObject>,<string>,<boolean>)`

Devuelve una lista de objetos.

## Ejemplo

`sort(["A", "C", "B"], true)`

Devuelve `["A","B","C"]`.

`sort([1, 3, 2], false)`

Devuelve `[3, 2, 1]`.

