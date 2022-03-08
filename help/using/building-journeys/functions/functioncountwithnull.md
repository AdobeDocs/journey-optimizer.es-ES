---
product: adobe campaign
title: countWithNull
description: Learn about the function countWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 32%

---

# countWithNull {#countWithNull}

Counts all the elements of the list including null values.

## Categoría

Agregación

## Function syntax

`countWithNull(<listAny>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| Lista | listString |
| Lista | listBoolean |
| Lista | listInteger |
| Lista | listDecimal |
| Lista | listDuration |
| Lista | listDateTime |
| Lista | listDateTimeOnly |
| Lista | listDateOnly |

## Signature and returned type

`countWithNull(<listAny>)`

Returns an integer.

## Ejemplo

`countWithNull([10,2,10,null])`

Returns 4.
