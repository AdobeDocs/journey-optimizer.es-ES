---
product: adobe campaign
title: getListItem
description: Obtenga información sobre la función gstListItem
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 20%

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
| índice | integer |

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
