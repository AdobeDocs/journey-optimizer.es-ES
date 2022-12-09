---
product: journey optimizer
title: getListItem
description: Obtenga información sobre la función gstListItem
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e995f479-bbaa-45f3-9531-e05680c5a723
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# getListItem {#gestListItem}

Devuelve el elemento de la lista en el índice dado.

## Categoría

Lista

## Sintaxis de función

`getListItem(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| index | integer |

## Firmas y tipo devuelto

`getListItem(<listInteger>,<index>)`

Devuelve un número entero.

`getListItem(<listDecimal>,<index>)`

Devuelve un decimal.

`getListItem(<listString>,<index>)`

Devuelve una cadena.

`getListItem(<listDateTimeOnly>,<index>)`

Devuelve una fecha y hora sin tener en cuenta la zona horaria.

`getListItem(<listDateTime>,<index>)`

Devuelve una fecha y hora.

`getListItem(<listDateOnly>,<index>)`

Devuelve una lista de fechas.

`getListItem(<listBoolean>,<index>)`

Devuelve un valor booleano.

`getListItem(<listDuration>,<index>)`

Devuelve una duración.

## Ejemplo

`getListItem([10, 2, 3], 1)`

Devuelve &quot;2&quot;

`getListItem(["A", "B", "C"], 2)`
Devuelve &quot;C&quot;

Ejemplos con un campo de evento &quot;event.appVersion&quot; con valor: &quot;20.45.2.3434&quot;

`split(@{event.appVersion}, "\\.")`

Devuelve `["20", "45", "2", "3434"]`

`getListItem(split(@{event.appVersion}, "\\."), 0)`

Devuelve &quot;20&quot;
