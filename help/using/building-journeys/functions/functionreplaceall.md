---
product: journey optimizer
title: replaceAll
description: Obtenga información acerca de la función replaceAll
feature: Journeys
role: Developer
level: Experienced
keywords: replaceAll, función, expresión, recorrido
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

---

# replaceAll {#replaceAll}

Reemplaza todas las ocurrencias que coincidan con la cadena de destino por la cadena de reemplazo de la cadena base.

La sustitución se realiza desde el principio de la cadena hasta el final, por ejemplo, si se sustituye &quot;a&quot; por &quot;b&quot; en la cadena &quot;aaa&quot;, el resultado será &quot;ba&quot; en lugar de &quot;ab&quot;.

## Categoría

Cadena

## Sintaxis de función

`replaceAll(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|--------------|
| basar | cadena |
| destino | cadena (RegExp) |
| reemplazo | cadena |

## Firma y tipo devuelto

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Devuelve una cadena.

## Ejemplo{#example}

`replaceAll("Hello World", "l", "x")`

Devuelve &quot;Hexxo Worxd&quot;.

Dado que el parámetro de destino es RegExp, en función de la cadena que desee reemplazar, es posible que tenga que omitir algunos caracteres. Consulte el ejemplo en [esta página](../functions/functionreplace.md#example_2).
