---
product: journey optimizer
title: nowWithDelta
description: Obtenga información sobre la función nowWithDelta
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cb1eb221-8532-4637-ac6c-8e058463ac94
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# nowWithDelta {#nowWithDelta}

Devuelve la fecha y hora actuales, incluyendo un desplazamiento. Si se especifica un id de zona horaria, se aplicará el desplazamiento de zona horaria. Para obtener más información sobre los tipos de datos, consulte [esta página](../expression/data-types.md).

## Categoría

Fecha

## Sintaxis de función

`nowWithDelta(<parameters>)`

## Parámetros

| Parámetro | Descripción |
|--- |--- |
| delta | valor entero positivo o negativo |
| partición de fecha | años, meses, días, horas, minutos o segundos como una cadena |
| id de zona horaria | representación de cadena del valor de zona horaria. Para obtener más información, consulte [Tipos de datos](../expression/data-types.md). El ID de zona horaria debe ser una constante de cadena. No puede ser una referencia de campo ni una expresión. |

## Firmas y tipo devuelto

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Devuelve un dateTime.

## Ejemplos

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Devuelve un dateTime exactamente hace 2 horas.
