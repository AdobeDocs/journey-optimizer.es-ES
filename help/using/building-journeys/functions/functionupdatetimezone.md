---
product: journey optimizer
title: updateTimeZone
description: Obtenga información acerca de la función updateTimeZone
feature: Journeys
role: Engineer
level: Experienced
keywords: updateTimeZone, función, expresión, recorrido
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 9%

---

# updateTimeZone {#updateTimeZone}

Devuelve una nueva fecha y hora, con una nueva zona horaria en el mismo instante.

## Categoría

Fecha

## Sintaxis de función

`updateTimeZone(<parameters>)`

## Parámetros

* id de zona horaria: cadena
* dateTime

## Firma y tipo devuelto

`updateTimeZone(<dateTime>,<timeZone id>)`

Devuelve una fecha y hora.

## Ejemplos

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Devuelve 2023-08-28T17:15:30.123+02:00.

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

Si el valor del campo de marca de tiempo es `2021-11-16T16:55:12.939318+01:00`, la función devuelve `2021-11-17T02:55:12.942115+11:00`.
