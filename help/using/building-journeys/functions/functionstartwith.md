---
product: journey optimizer
title: startWith
description: Obtenga información sobre la función startWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 0%

---

# startWith {#startWith}

Devuelve true si el segundo parámetro es un prefijo del primero.

## Categoría

Cadena

## Sintaxis de función

`startWith(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-------------|--------|
| string | string |
| prefix | string |

## Firma y tipo devuelto

`startWith(<string>,<string>)`

Devuelve un booleano.

## Ejemplo

`startWith("Hello World", "Hello")`

Devuelve verdadero.

`startWith("Hello World", "World")`

Devuelve falso.
