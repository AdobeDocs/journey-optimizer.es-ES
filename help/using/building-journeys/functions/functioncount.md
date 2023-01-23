---
product: journey optimizer
title: count
description: Obtenga información sobre el recuento de funciones
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: count, function, expression, recorrido
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: ad113c0414b20ac2f758ad06a44315b24a3d3d0c
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 28%

---

# count {#count}

Cuenta los elementos de la lista que no tienen en cuenta los valores nulos.

## Categoría

Agregación

## Sintaxis de función

`count(<listAny>)`

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

## Firmas y tipo devuelto

`count(<listAny>)`

Devuelve un número entero.

## Ejemplo

`count([10,2,10,null])`

Devuelve 3.
