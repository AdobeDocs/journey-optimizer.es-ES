---
product: journey optimizer
title: serializeList
description: Obtenga información sobre la función serializeList
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# serializeList {#serializeList}

Convierte la lista (cualquier tipo) proporcionada en el primer parámetro en una cadena. El segundo parámetro representa el separador que se va a utilizar. El tercer parámetro es un valor booleano que indica si cada elemento de la expresión debe incluir comillas.

## Categoría

Lista

## Sintaxis de función

`serializeList(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| Cadena | Cadena |
| Booleano | Booleano |
| DateTimeOnly | DateTimeOnly |
| Lista | listString |
| Lista | listBoolean |
| Lista | listPoint |
| Lista | listDecimal |
| Lista | listDuration |
| Lista | listDateTime |
| Lista | listDateTimeOnly |
| Lista | listDateOnly |

## Firma y tipo devuelto

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

`serializeList(<listPoint>,<string>,<boolean>)`

Devuelve una cadena.

## Ejemplo

`serializeList(["Hello","World"], " ", false)`

Devuelve &quot;Hello World&quot;.

`serializeList(["Hello", "World"], ",", true)`

Devuelve &quot;Hello&quot;, &quot;World&quot;.
