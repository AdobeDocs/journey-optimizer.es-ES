---
product: journey optimizer
title: concatena
description: Obtenga información acerca de la función concat.
feature: Journeys
role: Engineer
level: Experienced
keywords: concat, función, expresión, recorrido
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 25%

---

# concatena {#concat}

Concatena dos parámetros de cadena o una lista de cadenas.

## Categoría

Cadena

## Sintaxis de función

`concat(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| Lista | listString |
| cadena | cadena |

## Firma y tipo devuelto

`concat(<string>,<string>)`

`concat(<listString>)`

Devuelve una cadena.

## Ejemplo

`concat("Hello","World")`

Devuelve &quot;HelloWorld&quot;.

`concat(["Hello"," ","World"])`

Devuelve &quot;Hello World&quot;.
