---
product: journey optimizer
title: startWithIgnoreCase
description: Obtenga información sobre la función startWithIgnoreCase
feature: Journeys
role: Engineer
level: Experienced
keywords: startWithIgnoreCase, función, expresión, recorrido
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 22%

---

# startWithIgnoreCase {#startWithIgnoreCase}

Devuelve true si el segundo parámetro es un prefijo del primero sin tener en cuenta las mayúsculas y minúsculas.

## Categoría

Cadena

## Sintaxis de función

`startWithIgnoreCase(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-------------|--------|
| cadena | cadena |
| prefijo | cadena |

## Firma y tipo devuelto

`startWithIgnoreCase(<string>,<string>)`

Devuelve un valor booleano.

## Ejemplo

`startWithIgnoreCase("rowing is great", "RO")`

Devuelve verdadero.
