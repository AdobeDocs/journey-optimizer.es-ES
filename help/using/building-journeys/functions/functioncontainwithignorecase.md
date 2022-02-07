---
product: adobe campaign
title: containIgnoreCase
description: Obtenga información sobre la función containIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 22%

---

# containIgnoreCase {#containIgnoreCase}

Comprueba si la segunda cadena de argumento está contenida en la primera cadena de argumento, sin tener en cuenta las mayúsculas y minúsculas.

## Categoría

Cadena

## Sintaxis de función

`containIgnoreCase(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| string | string |
| cadena buscada | string |

## Firma y tipo devuelto

`containIgnoreCase(<string>,<string>)`

Devuelve un valor booleano.

## Ejemplo

`containIgnoreCase("rowing is great", "GREAT")`

Devuelve verdadero.
