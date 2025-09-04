---
product: journey optimizer
title: serializeList
description: Obtenga información sobre la función serializeList
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: serializeList, función, expresión, recorrido
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

---

# serializeList {#serializeList}

Convierte una lista determinada (cualquier tipo excepto listObject) en una cadena.

## Categoría

Lista

## Sintaxis de función

`serializeList(<parameters>)`

## Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Lista para convertir en cadena. |
| separador | cadena | Separador entre cada elemento de lista en la cadena de salida. |
| addQuotes | Booleano | Este parámetro indica si cada elemento de la cadena de salida debe incluir comillas (true) o no (false). |

## Firma y tipo devuelto

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Devolver una cadena.

## Ejemplo

`serializeList(["Hello","World"], " ", false)`

Devuelve &quot;Hello World&quot;.

`serializeList(["Hello", "World"], ",", true)`

Devuelve &quot;Hello&quot;,&quot;World&quot;.
