---
product: journey optimizer
title: countOnlyNull
description: Obtenga información sobre la función countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull, función, expresión, recorrido
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

---

# countOnlyNull {#countOnlyNull}

Cuenta el número de valores nulos de la lista.

Observe que el parámetro `<listObject>` no es compatible con esta función.

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
