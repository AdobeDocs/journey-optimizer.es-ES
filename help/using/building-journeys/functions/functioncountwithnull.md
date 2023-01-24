---
product: journey optimizer
title: countWithNull
description: Obtenga información sobre la función countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull, función, expresión, recorrido
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 30%

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
