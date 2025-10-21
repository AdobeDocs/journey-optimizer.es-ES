---
product: journey optimizer
title: nowWithDelta
description: Obtenga información acerca de la función nowWithDelta
feature: Journeys
role: Developer
level: Experienced
keywords: nowWithDelta, function, expression, recorrido
exl-id: cb1eb221-8532-4637-ac6c-8e058463ac94
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 7%

---

# nowWithDelta {#nowWithDelta}

Devuelve la fecha y hora actuales, incluido un desplazamiento. Si se especifica un ID de zona horaria, se aplica el desplazamiento de zona horaria. Para obtener más información sobre los tipos de datos, consulte [esta página](../expression/data-types.md).

## Categoría

Fecha

## Sintaxis de función

`nowWithDelta(<parameters>)`

## Parámetros

| Parámetro | Descripción |
|--- |--- |
| delta | valor entero positivo o negativo |
| parte de fecha | años, meses, días, horas, minutos o segundos como una cadena |
| id de zona horaria | representación de cadena del valor de zona horaria. Para obtener más información, consulte [Tipos de datos](../expression/data-types.md). El ID de zona horaria debe ser una constante de cadena. No puede ser una referencia de campo ni una expresión. |

## Firmas y tipo devuelto

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Devuelve un valor dateTime.

## Ejemplos

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Devuelve un valor dateTime de hace exactamente 2 horas.
