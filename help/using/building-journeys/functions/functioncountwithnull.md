---
product: journey optimizer
title: countWithNull
description: Obtenga información acerca de la función countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull, función, expresión, recorrido
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# countWithNull {#countWithNull}

Cuenta todos los elementos de la lista, incluidos los valores nulos.

Observe que el parámetro `<listObject>` no es compatible con esta función.

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
