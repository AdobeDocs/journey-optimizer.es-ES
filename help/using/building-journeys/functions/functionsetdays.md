---
product: journey optimizer
title: setDays
description: Obtenga información sobre la función setDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setDays, función, expresión, recorrido
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
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
