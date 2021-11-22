---
product: adobe campaign
title: countOnlyNull
description: Obtenga información sobre la función countOnlyNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
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
