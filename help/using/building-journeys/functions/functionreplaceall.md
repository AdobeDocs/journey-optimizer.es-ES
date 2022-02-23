---
product: adobe campaign
title: replaceAll
description: Obtenga información sobre la función replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 87b8056d26fe91a71e92ca346a9811c609d41128
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---

# replaceAll {#replaceAll}

Reemplaza todas las ocurrencias que coinciden con la cadena de destino por la cadena de reemplazo en la cadena base.

La sustitución procede desde el principio de la cadena hasta el final, por ejemplo, reemplazar &quot;aa&quot; por &quot;b&quot; en la cadena &quot;aaa&quot; resultará en &quot;ba&quot; en lugar de &quot;ab&quot;.

## Categoría

Cadena

## Sintaxis de función

`replaceAll(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|--------------|
| base | string |
| Target | string (RegExp) |
| reemplazo | string |

## Firma y tipo devuelto

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Devuelve una cadena.

## Ejemplo{#example}

`replaceAll("Hello World", "l", "x")`

Devuelve &quot;Hexxo Worxd&quot;.

Como el parámetro de destino es un RegExp, según la cadena que desee reemplazar, es posible que tenga que escapar algunos caracteres. Consulte el ejemplo en [esta página](../functions/functionreplace.md#example_2).
