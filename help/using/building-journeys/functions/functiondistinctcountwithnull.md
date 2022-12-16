---
product: journey optimizer
title: distinctCountWithNull
description: Obtenga información sobre la función distinctCountWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 24%

---

# distinctCountWithNull {#distinctCountWithNull}

Cuenta el número de valores diferentes, incluidos los valores nulos.

>[!NOTE]
>
>Si la lista de destino es un listObject, esta función solo se puede utilizar en expresiones de acción personalizadas.

## Categoría

Agregación

## Sintaxis de función

`distinctCountWithNull(<listAny>)`

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

## Firma y tipo devuelto

`distinctCountWithNull(<listAny>)`

Devuelve un número entero.

## Ejemplo

`distinctCountWithNull([10,2,10,null])`

Devuelve 3.
