---
product: adobe campaign
title: replaceAll
description: Learn about the function replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---

# replaceAll {#replaceAll}

Replaces all occurrences matching the target string by the replacement string in the base string.

The replacement proceeds from the beginning of the string to the end, for example, replacing &quot;aa&quot; with &quot;b&quot; in the string &quot;aaa&quot; will result in &quot;ba&quot; rather than &quot;ab&quot;.

## Categoría

Cadena

## Function syntax

`replaceAll(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|--------------|
| base | string |
| Target | string (RegExp) |
| replacement | string |

## Signature and returned type

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Returns a string.

## Ejemplo{#example}

`replaceAll("Hello World", "l", "x")`

Returns &quot;Hexxo Worxd&quot;.

Because the target parameter is a RegExp, depending on the string you want to replace, you may need to escape some characters. [](../functions/functionreplace.md#example_2)
