---
product: adobe campaign
title: setDays
description: Obtenga información sobre la función setDays
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 12%

---

# setDays {#setDays}

Establece el día de una fecha, hora o hora. Por ejemplo, si desea esperar hasta un día determinado del mes, puede forzar el día.

## Categoría

Fecha 

## Sintaxis de función

`setDays(<parameter>)`

## Parámetros

| Parámetro | Tipo |
|--- |--- |
| fecha y hora | dateTime |
| fecha y hora sin considerar zona horaria | dateTimeOnly |
| días | integer |

## Firmas y tipo devuelto

`setDays(<dateTime>,<days>)`

Devuelve una fecha y hora.

`setDays(<dateTimeOnly>,<days>)`

Devuelve una fecha y hora sin tener en cuenta la zona horaria.

## Ejemplos

`setDays(toDateTime('2010-12-12T01:11:00Z'), 25)`

Devuelve 2010-12-25T01:11:00Z.

`setDays(toDateTimeOnly(@{MyEvent.registrationDate}), 1)`
