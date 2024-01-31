---
product: journey optimizer
title: distinctWithNull
description: Obtenga información sobre la función distinctWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctWithNull, función, expresión, recorrido
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---

# distinctWithNull {#distinctWithNull}

Devuelve los distintos valores u objetos de una lista determinada. Si la lista tiene al menos una entrada nula, aparecerá una entrada nula en la lista devuelta.

Observe que el parámetro `<listObject>` no es compatible con esta función.

## Categoría

Lista

## Sintaxis de función

`distinctWithNull(<parameters>)`

## Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Lista para procesar. |

## Firmas y tipos devueltos

`distinctWithNull(<listInteger>)`

Devuelve una lista de enteros.

`distinctWithNull(<listDecimal>)`

Devuelve una lista de decimales.

`distinctWithNull(<listString>)`

Devuelve una lista de cadenas.

`distinctWithNull(<listDateTimeOnly>)`

Devuelve una lista de horas de fecha sin tener en cuenta la zona horaria.

`distinctWithNull(<listDateTime>)`

Devuelve una lista de fechas y horas.

`distinctWithNull(<listDateOnly>)`

Devuelve una lista de fechas.

`distinctWithNull(<listBoolean>)`

Devuelve una lista de valores booleanos.

`distinctWithNull(<listDuration>)`

Devuelve una lista de duraciones.

## Ejemplos

`distinctWithNull([10,2,10,null])`

Devuelve [10, 2, nulo]
