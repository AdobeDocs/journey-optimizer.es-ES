---
product: journey optimizer
title: setHours
description: Obtenga información sobre la función setHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setHours, función, expresión, recorrido
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 9%

---

# setHours {#setHours}

Establece solo las horas de una fecha, hora u hora. Por ejemplo, si desea esperar hasta una hora determinada mañana, puede forzar la hora.

## Categoría

Fecha

## Sintaxis de función

`setHours(<parameter>)`

## Parámetros

| Parámetro | Tipo |
|--- |--- |
| fecha y hora | dateTime |
| fecha y hora sin considerar la zona horaria | dateTimeOnly |
| horas | entero |

## Firmas y tipo devuelto

`setHours(<dateTime>,<hours>)`

Devuelve una fecha y hora.

`setHours(<dateTimeOnly>,<hours>)`

Devuelve una fecha y hora sin considerar la zona horaria.

## Ejemplos

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve 2023-12-12T04:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Vuelve mañana a las 8:XY PM, siendo XY los minutos en el momento de la evaluación de la hora actual. Si la evaluación se realiza a las 2:45, la hora de retorno será las 8:45 p.m.
