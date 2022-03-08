---
product: adobe campaign
title: replaceAll
description: Obtenga información sobre la función replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 16%

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
| Target | string |
| reemplazo | string |

## Firma y tipo devuelto

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Devuelve una cadena.

## Ejemplo

`replaceAll("Hello World", "l", "x")`

Devuelve &quot;Hexxo Worxd&quot;.
