---
product: journey optimizer
title: getListItem
description: Obtenga información sobre la función gstListItem
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: getListItem, función, expresión, recorrido
exl-id: e995f479-bbaa-45f3-9531-e05680c5a723
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 18%

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
| índice | entero |

## Firmas y tipo devuelto

`getListItem(<listInteger>,<index>)`

Devuelve un entero.

`getListItem(<listDecimal>,<index>)`

Devuelve un valor decimal.

`getListItem(<listString>,<index>)`

Devuelve una cadena.

`getListItem(<listDateTimeOnly>,<index>)`

Devuelve una fecha y hora sin considerar la zona horaria.

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

`split(@event{event.appVersion}, "\\.")`

Devuelve `["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

Devuelve &quot;20&quot;
