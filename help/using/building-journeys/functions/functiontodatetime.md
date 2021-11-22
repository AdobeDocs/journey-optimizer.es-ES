---
product: adobe campaign
title: toDateTime
description: Obtenga información sobre la función toDateTime
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 2b487e60-593e-4bf7-9639-f469ba0f5cdc
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 10%

---

# toDateTime {#toDateTime}

Convierte los parámetros en un valor de fecha y hora, según sus tipos.

## Categoría

Conversión

## Sintaxis de función

`toDateTime(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora en formato ISO-8601 | string |
| id de zona horaria | string |
| fecha y hora sin zona horaria | dateTimeOnly |
| valor entero de una epoch en milisegundos | integer |

>[!NOTE]
>
>El ID de zona horaria debe ser una constante de cadena. No puede ser una referencia de campo ni una expresión. Para obtener más información sobre los tipos de datos, consulte [esta página](../expression/data-types.md).

## Firmas y tipos devueltos

`toDateTime(<string>)`

`toDateTime(<stringified time zone id>, <dateTimeOnly>)`

`toDateTime(<integer>)`

Devolver un **dateTime**.

<!--`toDateTime(<year>,<month>,<dayOfMonth>,<hour>,<minute>,<second>)`

Returns a date time with default time zone UTC.

`toDateTime(<year>,<month>,<dayOfMonth>)`
`toDateTime(<stringified timeZone>,<year>,<month>,<dayOfMonth>)`
`toDateTime(<timeZone>,<year>,<month>,<dayOfMonth>)`

Return a datetime where hour, minute and second set to 0.

`toDateTime(<stringified timeZone>,<year>,<month>,<dayOfMonth>,<hour>,<minute>,<second>)`
`toDateTime(<string>)`
`toDateTime(<string>,<integer>)`
`toDateTime(<stringified timeZone>,<dateTimeOnly)`

`toDateTime(<timeZone>,<integer>)`

Return a datetime.

-->

## Ejemplos

`toDateTime ("2016-08-18T23:17:59.123Z")`

Devuelve 2016-08-18T23:17:59,123Z

`toDateTime(toDateTimeOnly("UTC", "2016-08-18T23:17:59.123"))`

Devuelve 2016-08-18T23:17:59,123Z

`toDateTime(1560762190189)`

Devuelve 2019-06-17T09:03:10,189Z

<!--`toDateTime ("2016-08-18T23:17:59.123", "UTC")`

Returns 2016-08-18T23:17:59.123Z.

`toDateTime("Z",2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000Z.

`toDateTime("Z",2016,8,18)`

Returns 2016-08-18T00:00:00.000Z.-->
