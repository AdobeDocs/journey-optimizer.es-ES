---
product: adobe campaign
title: setHours
description: Obtenga información sobre la función setHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 8%

---

# setHours {#setHours}

Establece las horas de una fecha, hora u hora únicamente. Por ejemplo, si desea esperar hasta una hora determinada mañana, puede forzar la hora.

## Categoría

Fecha 

## Sintaxis de función

`setHours(<parameter>)`

## Parámetros

| Parámetro | Tipo |
|--- |--- |
| fecha y hora | dateTime |
| fecha y hora sin considerar zona horaria | dateTimeOnly |
| horas | integer |

## Firmas y tipo devuelto

`setHours(<dateTime>,<hours>)`

Devuelve una fecha y hora.

`setHours(<dateTimeOnly>,<hours>)`

Devuelve una fecha y hora sin tener en cuenta la zona horaria.

## Ejemplos

`setHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

Devuelve 2010-12-12T04:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Devuelve mañana a las 8:XY PM, siendo XY los minutos en el momento de la evaluación horaria actual. Si la evaluación se realiza a las 2:45 AM, la hora devuelta será a las 20:45.
