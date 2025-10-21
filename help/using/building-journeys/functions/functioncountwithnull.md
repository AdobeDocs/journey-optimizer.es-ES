---
product: journey optimizer
title: countWithNull
description: Obtenga información acerca de la función countWithNull
feature: Journeys
role: Engineer
level: Experienced
keywords: countWithNull, función, expresión, recorrido
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# countWithNull {#countWithNull}

Cuenta todos los elementos de la lista, incluidos los valores nulos.

Tenga en cuenta que el parámetro `<listObject>` no se admite en esta función.

## Categoría

Agregación

## Sintaxis de función

`countWithNull(<listAny>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Firma y tipo devuelto

`countWithNull(<listAny>)`

Devuelve un entero.

## Ejemplo

`countWithNull([10,2,10,null])`

Devuelve 4.
