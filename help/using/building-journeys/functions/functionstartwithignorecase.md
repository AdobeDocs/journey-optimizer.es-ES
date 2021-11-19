---
product: adobe campaign
title: startWithIgnoreCase
description: Obtenga información sobre la función startWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 25%

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
| string | string |
| prefix | string |

## Firma y tipo devuelto

`startWithIgnoreCase(<string>,<string>)`

Devuelve un booleano.

## Ejemplo

`startWithIgnoreCase("rowing is great", "RO")`

Devuelve verdadero.
