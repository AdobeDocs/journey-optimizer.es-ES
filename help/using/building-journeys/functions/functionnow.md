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
source-git-commit: 7ac246c0aa6776d3ec67223c4b07536b8ed0c881
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 14%

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
| cadena | Identificador de zona horaria (opcional) |

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
