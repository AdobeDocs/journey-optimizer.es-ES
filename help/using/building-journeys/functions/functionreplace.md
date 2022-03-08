---
product: adobe campaign
title: replace
description: Obtenga información sobre la sustitución de funciones
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 15%

---

# replace {#replace}

Reemplaza la primera incidencia que coincide con la cadena de destino por la cadena de reemplazo de la cadena base.

La sustitución procede desde el principio de la cadena hasta el final, por ejemplo, reemplazar &quot;aa&quot; por &quot;b&quot; en la cadena &quot;aaa&quot; resultará en &quot;ba&quot; en lugar de &quot;ab&quot;.

## Categoría

Cadena

## Sintaxis de función

`replace(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|--------------|
| base | string |
| Target | string |
| reemplazo | string |

## Firma y tipo devuelto

`replace(<base>,<target>,<replacement>)`

Devuelve una cadena.

## Ejemplo

`replace("Hello World", "l", "x")`

Devuelve &quot;Hexlo World&quot;.
