---
product: adobe campaign
title: serializeList
description: Learn about the function serializeList
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 22%

---

# serializeList {#serializeList}

Converts the list (any type) given in the first parameter to a string. The second parameter represents the separator to use. The third parameter is a boolean value indicating if each element of the expression should include quotes.

## Categoría

Lista

## Function syntax

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

## Signature and returned type

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

`serializeList(<listPoint>,<string>,<boolean>)`

Return a string.

## Ejemplo

`serializeList(["Hello","World"], " ", false)`

Returns &quot;Hello World&quot;.

`serializeList(["Hello", "World"], ",", true)`

Returns &quot;&quot;Hello&quot;,&quot;World&quot;&quot;.
