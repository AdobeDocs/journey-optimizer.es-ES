---
product: journey optimizer
title: toDateTimeOnly
description: Obtenga información sobre la función toDateTime
feature: Journeys
role: Developer
level: Experienced
keywords: toDateTimeOnly, función, expresión, recorrido
exl-id: db54c119-5080-403a-b254-43645be6b4a8
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 14%

---

# toDateTimeOnly{#toDateTimeOnly}

Convierte un valor de argumento en un valor de solo fecha y hora.

## Categoría

Conversión

## Sintaxis de función

`toDateTimeOnly(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora en formato ISO-8601 o &quot;AAAA-MM-DD&quot; (formato de fecha XDM) | cadena |
| fecha y hora | dateTime |

## Firmas y tipos devueltos

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`
<!--`toDateTimeOnly(<integer>,<integer>,<integer>)`
`toDateTimeOnly(<integer>,<integer>,<integer>,<integer>,<integer>,<integer>)`-->

Devuelve una fecha y hora sin tener en cuenta la zona horaria.

## Ejemplos

`toDateTimeOnly ("2023-08-18")`

devuelve un valor dateTime que representa el valor 2023-08-18T00:00:00.000

`toDateTimeOnly(now())`

<!--`toDateTimeOnly(2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000.

`toDateTimeOnly(2016,8,18)`

Returns 2016-08-18T00:00:00.000.-->
