---
product: journey optimizer
title: substr
description: Obtenga información sobre la subcategoría de funciones
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: substr, function, expression, recorrido
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
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
| string | string |
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
