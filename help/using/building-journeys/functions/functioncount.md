---
product: journey optimizer
title: recuento
description: Más información sobre el recuento de funciones
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: recuento, función, expresión, recorrido
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 10%

---

# recuento {#count}

Cuenta los elementos de la lista que no tienen en cuenta los valores nulos.

## Categoría

Agregación

## Sintaxis de función

`count(<listAny>)`

`count(<listObject>)`

## Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para procesar. Para listObject, debe ser una referencia de campo. Un listObject no puede contener un objeto nulo. |

## Firmas y tipo devuelto

`count(<listAny>)`

Devuelve un entero.

## Ejemplo

`count([10,2,10,null])`

Devuelve 3.

`count(@event{my_event.productListItems})`

Devuelve el número de objetos de una matriz determinada de objetos (tipo listObject). Nota: un listObject no puede contener un objeto nulo
