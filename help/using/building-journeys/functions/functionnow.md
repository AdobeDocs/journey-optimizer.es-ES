---
product: adobe campaign
title: now
description: Obtenga información sobre la función ahora
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# now {#now}

Devuelve la fecha actual en formato de fecha y hora. Para obtener más información sobre los tipos de datos, consulte [esta página](../expression/data-types.md).

## Categoría

Fecha

## Sintaxis de función

`now(<parameter>)`

## Parámetros

| Parámetro | Descripción |
|--- |--- |
| string |  |

## Firmas y tipo devuelto

`now()`

`now("<timeZone id>")`

Devuelve un dateTime.

## Ejemplos

`now()`

Devuelve 2019-06-03T06:30Z.

`toString(now())`

Devuelve &quot;2019-06-03T06:30Z&quot;

`now("Europe/Paris")`

Devuelve 2019-06-03T08:30+02:00.
