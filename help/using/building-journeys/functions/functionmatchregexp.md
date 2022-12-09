---
product: journey optimizer
title: matchRegExp
description: Obtenga información sobre la función matchRegExp
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 0%

---

# matchRegExp {#matchRegExp}

Devuelve true si la cadena del primer parámetro coincide con la expresión regular del segundo parámetro. Para obtener más información, consulte [esta página](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## Categoría

Cadena

## Sintaxis de función

`matchRegExp(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|--- |--- |
| string | string |
| regexp | string |

## Firma y tipo devuelto

`matchRegExp(<string>,<string>)`

Devuelve un valor booleano.

## Ejemplo

`matchRegExp("username@adobe.com", "*adobe")`

Devuelve verdadero.
