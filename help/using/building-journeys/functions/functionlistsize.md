---
product: adobe campaign
title: listSize
description: Obtenga información sobre la función listSize
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 34%

---

# listSize {#listSize}

Cuenta el número de elementos de la lista.

## Categoría

Lista

## Sintaxis de función

`listSize(<parameters>)`

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

## Firmas y tipo devuelto

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

`listSize(<listPoint>)`

Devuelve un entero.

## Ejemplo

`listSize([10,2,3])`

Devuelve 3.
