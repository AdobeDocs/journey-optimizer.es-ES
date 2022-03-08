---
product: adobe campaign
title: distinct
description: Obtenga información sobre la función distinta
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 18%

---

# distinct {#distinct}

Devuelve los valores distintos de la lista sin valores nulos.

## Categoría

Lista

## Sintaxis de función

`distinct(<parameter>)`

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

## Firmas y tipos devueltos

`distinct(<listInteger>)`

Devuelve una lista de enteros.

`distinct(<listDecimal>)`

Devuelve una lista de decimales.

`distinct(<listString>)`

Devuelve una lista de cadenas.

`distinct(<listDateTimeOnly>)`

Devuelve una lista de tiempos de datos sin tener en cuenta la zona horaria.

`distinct(<listDateTime>)`

Devuelve una lista de tiempos de datos.

`distinct(<listDateOnly>)`

Devuelve una lista de fechas.

`distinct(<listBoolean>)`

Devuelve una lista de booleanos.

`distinct(<listDuration>)`

Devuelve una lista de duraciones.

## Ejemplos

`distinct([10,2,10,null])`

Devuelve `[10, 2]`.
