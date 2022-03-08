---
product: adobe campaign
title: toDateOnly
description: Obtenga información sobre la función toDateOnly
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# toDateOnly{#toDateOnly}

Convierte un valor de argumento en un valor de solo fecha.

## Categoría

Conversión

## Sintaxis de función

`toDateOnly(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha en formato ISO-8601 o &quot;AAAA-MM-DD&quot; (formato de fecha XDM) | string |
| date | date |

## Firmas y tipos devueltos

`toDateOnly(<date>)`

`toDateOnly(<string>)`

Devolver una fecha y hora sin considerar la zona horaria.

## Ejemplos

`toDateOnly("2016-08-18")`

devuelve un objeto dateOnly que representa 2016-08-18.
