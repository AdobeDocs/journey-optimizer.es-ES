---
product: adobe campaign
title: endWith
description: Obtenga información sobre la función endWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 25%

---

# endWith {#endWith}

Devuelve el valor verdadero si el segundo parámetro es un sufijo del primero.

## Categoría

Cadena

## Sintaxis de función

`endWith(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| string | string |
| sufijo | string |

## Firma y tipo devuelto

`endWith(<string>,<string>)`

Devuelve un valor booleano.

## Ejemplo

`endWith("Hello World", "World")`

Devuelve verdadero.

`endWith("Hello World", "Hello")`

Devuelve falso.
