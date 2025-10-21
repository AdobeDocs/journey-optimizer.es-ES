---
product: journey optimizer
title: substr
description: Obtenga información sobre la subcategoría de funciones
feature: Journeys
role: Engineer
level: Experienced
keywords: substr, function, expression, recorrido
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---

# substr {#substr}

Devuelve la subcadena de la expresión de cadena entre el índice inicial y el índice final. Si no se define el índice final, se encuentra entre el índice inicial y el final.

## Categoría

Cadena

## Sintaxis de función

`substr(<parameters>)`

## Parámetros

| Parámetro | tipo |
|-------------|----------|
| cadena | cadena |
| beginIndex | entero |
| endIndex | entero |

## Firma y tipo devuelto

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Devolver una cadena.

## Ejemplo

`substr("Hello World",6)`

Devuelve &quot;World&quot;.

`substr("Hello World", 0, 5)`

Devuelve &quot;Hello&quot;.
