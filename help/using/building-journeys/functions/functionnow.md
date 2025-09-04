---
product: journey optimizer
title: now
description: Obtenga información acerca de la función ahora
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: ahora, función, expresión, recorrido
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 15%

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
| cadena |  |

## Firmas y tipo devuelto

`now()`

`now("<timeZone id>")`

Devuelve un valor dateTime.

## Ejemplos

`now()`

Devuelve 2023-06-03T06:30Z.

`toString(now())`

Devuelve &quot;2023-06-03T06:30Z&quot;

`now("Europe/Paris")`

Devuelve 2023-06-03T08:30+02:00.
