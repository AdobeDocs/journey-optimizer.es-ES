---
product: journey optimizer
title: distinctWithNull
description: Obtenga información sobre la función distinctWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# distinctWithNull {#distinctWithNull}

Devuelve los valores u objetos distintos de una lista determinada. Si la lista tiene al menos una entrada nula, estará presente una entrada nula en la lista devuelta.

## Categoría

Lista

## Sintaxis de función

`distinctWithNull(<parameters>)`

## Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para procesar. Para listObject, debe ser una referencia de campo. |
| keyAttributeName | string | Este parámetro es opcional y solo para listObject. Si no se proporciona el parámetro, un objeto se considera duplicado si todos los atributos tienen los mismos valores. De lo contrario, un objeto se considera duplicado si el atributo dado tiene el mismo valor. |

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

`distinctWithNull(<listObject>)`

`distinctWithNull(<listObject>,<string>)`

Devuelve una lista de objetos.

## Ejemplos

`distinctWithNull([10,2,10,null])`

Devuelve [10, 2, nulo]
