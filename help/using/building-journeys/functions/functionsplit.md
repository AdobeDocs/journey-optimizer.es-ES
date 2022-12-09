---
product: journey optimizer
title: split
description: Obtenga información sobre la división de funciones
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# split {#split}

Divide la primera cadena de argumento con una cadena separador (la segunda cadena de argumento, que puede ser una expresión regular) para generar una lista de cadenas (tokens).

## Categoría

Cadena

## Sintaxis de función

`split(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| cadena de entrada | string |
| cadena de separador | string |

## Firmas y tipo devuelto

`split(<input string>, <separator string>)`

Devuelve un listString.

## Ejemplo

`split(["A_B_C"], "_")`

Devuelve `["A","B","C"]`

Ejemplo con un campo de evento &quot;event.appVersion&quot; con valor: &quot;20.45.2.3434&quot;

`split(@{event.appVersion}, "\\.")`

Devuelve `["20", "45", "2", "3434"]`
