---
product: journey optimizer
title: split
description: Obtenga información acerca de la división de funciones
feature: Journeys
role: Developer
level: Experienced
keywords: split, function, expression, recorrido
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 14%

---

# split {#split}

Divide la cadena del primer argumento con una cadena de separador (cadena del segundo argumento, que puede ser una expresión regular) para producir una lista de cadenas (tokens).

## Categoría

Cadena

## Sintaxis de función

`split(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| cadena de entrada | cadena |
| cadena de separación | cadena |

## Firmas y tipo devuelto

`split(<input string>, <separator string>)`

Devuelve un valor listString.

## Ejemplo

`split("A_B_C", "_")`

Devuelve `["A","B","C"]`

Ejemplo con un campo de evento &quot;event.appVersion&quot; con el valor: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Devuelve `["20", "45", "2", "3434"]`
