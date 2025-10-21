---
product: journey optimizer
title: setDays
description: Obtenga información sobre la función setDays
feature: Journeys
role: Engineer
level: Experienced
keywords: setDays, función, expresión, recorrido
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 12%

---

# setDays {#setDays}

Establece solo el día de una fecha y hora o la fecha y hora. Por ejemplo, si desea esperar hasta un día determinado del mes, puede forzar el día.

## Categoría

Fecha

## Sintaxis de función

`setDays(<parameter>)`

## Parámetros

| Parámetro | Tipo |
|--- |--- |
| fecha y hora | dateTime |
| fecha y hora sin considerar la zona horaria | dateTimeOnly |
| días | entero |

## Firmas y tipo devuelto

`setDays(<dateTime>,<days>)`

Devuelve una fecha y hora.

`setDays(<dateTimeOnly>,<days>)`

Devuelve una fecha y hora sin considerar la zona horaria.

## Ejemplos

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Devuelve 2023-12-25T01:11:00Z.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`
