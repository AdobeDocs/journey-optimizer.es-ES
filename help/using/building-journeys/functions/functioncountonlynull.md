---
product: adobe campaign
title: countOnlyNull
description: Obtenga información sobre la función countOnlyNull
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 33%

---

# countOnlyNull {#countOnlyNull}

Cuenta el número de valores nulos en la lista.

## Categoría

Agregación

## Sintaxis de función

`countOnlyNull(<listAny>)`

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

`countOnlyNull(<listAny>)`

Devuelve un número entero.

## Ejemplo

`countOnlyNull([10,2,10,null])`

Devuelve 1.
