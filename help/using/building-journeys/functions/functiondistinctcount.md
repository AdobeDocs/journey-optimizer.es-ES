---
product: journey optimizer
title: distinctCount
description: Obtenga información sobre la función distinctCount
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount, función, expresión, recorrido
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 29%

---

# distinctCount{#distinctCount}

Cuenta el número de valores diferentes e ignora los valores nulos.

## Categoría

Agregación

## Sintaxis de función

`distinctCount(<listAny>)`

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

`distinctCount(<listAny>)`

Devuelve un entero.

## Ejemplo

`distinctCount([10,2,10,null])`

Devuelve 2.
