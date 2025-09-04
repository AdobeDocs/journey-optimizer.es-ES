---
product: journey optimizer
title: matchRegExp
description: Obtenga información sobre la función matchRegExp
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: matchRegExp, función, expresión, recorrido
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 19%

---

# matchRegExp {#matchRegExp}

Devuelve true si la cadena del primer parámetro coincide con la expresión regular del segundo parámetro. Para obtener más información, vea [esta página](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Categoría

Cadena

## Sintaxis de función

`matchRegExp(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|--- |--- |
| cadena | cadena |
| regexp | cadena |

## Firma y tipo devuelto

`matchRegExp(<string>,<string>)`

Devuelve un valor booleano.

## Ejemplo

`matchRegExp("12345", "\\d+")`

Devuelve verdadero.
