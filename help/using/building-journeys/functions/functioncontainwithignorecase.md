---
product: journey optimizer
title: containIgnoreCase
description: Obtenga información sobre la función containIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: containIgnoreCase, función, expresión, recorrido
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# containIgnoreCase {#containIgnoreCase}

Comprueba si la cadena del segundo argumento está contenida en la cadena del primer argumento, sin tener en cuenta el caso.

## Categoría

Cadena

## Sintaxis de función

`containIgnoreCase(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| cadena | cadena |
| cadena buscada | cadena |

## Firma y tipo devuelto

`containIgnoreCase(<string>,<string>)`

Devuelve un valor booleano.

## Ejemplo

`containIgnoreCase("rowing is great", "GREAT")`

Devuelve verdadero.
