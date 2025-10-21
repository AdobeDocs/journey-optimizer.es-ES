---
product: journey optimizer
title: startWith
description: Obtenga información acerca de la función startWith
feature: Journeys
role: Developer
level: Experienced
keywords: startWith, function, expression, recorrido
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

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
| cadena | cadena |
| prefijo | cadena |

## Firma y tipo devuelto

`startWith(<string>,<string>)`

Devuelve un valor booleano.

## Ejemplo

`startWith("Hello World", "Hello")`

Devuelve verdadero.

`startWith("Hello World", "World")`

Devuelve falso.
