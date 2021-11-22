---
product: adobe campaign
title: distinctWithNull
description: Obtenga información sobre la función distinctWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 15%

---

# distinctWithNull {#distinctWithNull}

Devuelve los distintos valores de la lista. Si la lista tiene al menos un valor nulo, se mostrará un valor nulo en la lista devuelta.

## Categoría

Lista

## Sintaxis de función

`distinctWithNull(<parameter>)`

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

`distinctWithNull(<listInteger>)`

Devuelve una lista de enteros.

`distinctWithNull(<listDecimal>)`

Devuelve una lista de decimales.

`distinctWithNull(<listString>)`

Devuelve una lista de cadenas.

`distinctWithNull(<listDateTimeOnly>)`

Devuelve una lista de tiempos de datos sin tener en cuenta la zona horaria.

`distinctWithNull(<listDateTime>)`

Devuelve una lista de tiempos de datos.

`distinctWithNull(<listDateOnly>)`

Devuelve una lista de fechas.

`distinctWithNull(<listBoolean>)`

Devuelve una lista de booleanos.

`distinctWithNull(<listDuration>)`

Devuelve una lista de duraciones.

## Ejemplos

`distinctWithNull([10,2,10,null])`

Devuelve [10, 2, nulo]
