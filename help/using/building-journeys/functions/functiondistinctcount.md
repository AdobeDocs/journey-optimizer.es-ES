---
product: journey optimizer
title: distinctCount
description: Obtenga información sobre la función distinctCount
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount, función, expresión, recorrido
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---

# distinctCount{#distinctCount}

Cuenta el número de valores diferentes e ignora los valores nulos.

## Categoría

Agregación

## Sintaxis de función

`distinctCount(<listAny>)`

## Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para procesar. Para listObject, debe ser una referencia de campo. |
| keyAttributeName | cadena | Este parámetro es opcional y solo para listObject. Si no se proporciona el parámetro, un objeto se considera duplicado si todos los atributos tienen los mismos valores. De lo contrario, un objeto se considera duplicado si el atributo dado tiene el mismo valor. |

## Firma y tipo devuelto

`distinctCount(<listAny>)`

Devuelve un entero.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Devuelve una lista de objetos.


## Ejemplo

`distinctCount([10,2,10,null])`

Devuelve 2.

`distinctCount(@event{my_event.productListItems})`

Devuelve el número de objetos estrictamente distintos en la matriz de objetos determinada (tipo listObject).

`distinctCount(@event{my_event.productListItems}, "SKU")`

Devuelve el número de objetos que tienen un valor de atributo SKU distinto {}.
