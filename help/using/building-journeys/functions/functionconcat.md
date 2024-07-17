---
product: journey optimizer
title: concatena
description: Obtenga información acerca de la función concat.
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: concat, función, expresión, recorrido
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
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
