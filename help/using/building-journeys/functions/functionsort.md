---
product: adobe campaign
title: sort
description: Obtenga información sobre la ordenación de funciones
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 18%

---

# sort {#sort}

Ordena una lista de valores en el orden natural. El primer argumento es la lista de valores y el segundo es un valor booleano que indica si la ordenación es ascendente (true) o descendente (false).

## Categoría

Lista

## Sintaxis de función

`sort(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| Lista | listString |
| Lista | listBoolean |
| Lista | listInteger |
| Lista | listDecimal |
| Lista | listDuration |
| Lista | listDateTime |
| Lista | listDateTimeOnly |
| Lista | listDateOnly |
| Booleano | Booleano |

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

## Ejemplo

`sort(["A", "C", "B"], true)`

Devuelve `["A","B","C"]`.

`sort([1, 3, 2], false)`

Devuelve `[3, 2, 1]`.
