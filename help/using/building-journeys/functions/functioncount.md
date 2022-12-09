---
product: journey optimizer
title: count
description: Obtenga información sobre el recuento de funciones
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

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
