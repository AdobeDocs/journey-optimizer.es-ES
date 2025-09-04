---
product: journey optimizer
title: endWith
description: Obtenga información sobre la función endWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWith, función, expresión, recorrido
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# endWith {#endWith}

Devuelve true si el segundo parámetro es un sufijo del primero.

## Categoría

Cadena

## Sintaxis de función

`endWith(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| cadena | cadena |
| sufijo | cadena |

## Firma y tipo devuelto

`endWith(<string>,<string>)`

Devuelve un valor booleano.

## Ejemplo

`endWith("Hello World", "World")`

Devuelve verdadero.

`endWith("Hello World", "Hello")`

Devuelve falso.
