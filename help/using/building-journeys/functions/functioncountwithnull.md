---
product: adobe campaign
title: countWithNull
description: Obtenga información sobre la función countWithNull
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 32%

---

# countWithNull {#countWithNull}

Cuenta todos los elementos de la lista, incluidos los valores nulos.

## Categoría

Agregación

## Sintaxis de función

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

## Firma y tipo devuelto

`countWithNull(<listAny>)`

Devuelve un número entero.

## Ejemplo

`countWithNull([10,2,10,null])`

Devuelve 4.
