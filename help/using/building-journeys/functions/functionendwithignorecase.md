---
product: journey optimizer
title: endWithIgnoreCase
description: Obtenga información sobre la función endWithIgnoreCase
feature: Journeys
role: Developer
level: Experienced
keywords: endWithIgnoreCase, función, expresión, recorrido
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 17%

---

# endWithIgnoreCase {#endWithIgnoreCase}

Comprueba si la cadena del primer argumento termina con una cadena específica (cadena del segundo argumento), sin tener en cuenta el caso.

## Categoría

Cadena

## Sintaxis de función

`endWithIgnoreCase(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| cadena | cadena |
| sufijo | cadena |

## Firma y tipo devuelto

`endWithIgnoreCase(<string>,<string>)`

Devuelve un valor booleano.

## Ejemplo

`endWithIgnoreCase("rowing is great", "AT")`

Devuelve verdadero.
