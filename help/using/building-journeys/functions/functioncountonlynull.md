---
product: journey optimizer
title: countOnlyNull
description: Obtenga información sobre la función countOnlyNull
feature: Journeys
role: Developer
level: Experienced
keywords: countOnlyNull, función, expresión, recorrido
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

---

# countOnlyNull {#countOnlyNull}

Cuenta el número de valores nulos de la lista.

Tenga en cuenta que el parámetro `<listObject>` no se admite en esta función.

## Categoría

Agregación

## Sintaxis de función

`countOnlyNull(<listAny>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Firma y tipo devuelto

`countOnlyNull(<listAny>)`

Devuelve un entero.

## Ejemplo

`countOnlyNull([10,2,10,null])`

Devuelve 1.
