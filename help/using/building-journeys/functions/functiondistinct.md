---
product: journey optimizer
title: distinct
description: Obtenga información acerca de la función distinct
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinct, función, expresión, recorrido
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 6%

---

# distinct {#distinct}

Devuelve los distintos valores u objetos de una lista determinada. Las entradas nulas se omiten.

## Categoría

Lista

## Sintaxis de función

`distinct(<parameters>)`

## Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para procesar. Para listObject, debe ser una referencia de campo. |
| keyAttributeName | cadena | Este parámetro es opcional y solo para listObject. Si no se proporciona el parámetro, un objeto se considera duplicado si todos los atributos tienen los mismos valores. De lo contrario, un objeto se considera duplicado si el atributo dado tiene el mismo valor. |

## Firmas y tipos devueltos

`distinct(<listInteger>)`

Devuelve una lista de enteros.

`distinct(<listDecimal>)`

Devuelve una lista de decimales.

`distinct(<listString>)`

Devuelve una lista de cadenas.

`distinct(<listDateTimeOnly>)`

Devuelve una lista de horas de fecha sin tener en cuenta la zona horaria.

`distinct(<listDateTime>)`

Devuelve una lista de fechas y horas.

`distinct(<listDateOnly>)`

Devuelve una lista de fechas.

`distinct(<listBoolean>)`

Devuelve una lista de valores booleanos.

`distinct(<listDuration>)`

Devuelve una lista de duraciones.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Devuelve una lista de objetos.


## Ejemplos

`distinct([10,2,10,null])`

Devuelve `[10, 2]`.
