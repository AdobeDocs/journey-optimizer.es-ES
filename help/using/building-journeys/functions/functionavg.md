---
product: journey optimizer
title: avg
description: Obtenga información acerca de la función avg
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: avg, función, expresión, recorrido
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 12%

---

# avg {#avg}

Devuelve el valor promedio entre un conjunto de expresiones, dado como una lista o dos expresiones. Los valores nulos se omiten.


## Categoría

Agregación

## Sintaxis de función

`avg(<parameter>)`

## Parámetros

Tipos admitidos:

* listInteger
* listDecimal
* decimal
* entero

## Firmas y tipo devuelto

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Devuelve un valor decimal.

## Ejemplos

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Devuelve 7.0.

`avg(10.2, 3)`

Devuelve 6.6.
