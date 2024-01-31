---
product: journey optimizer
title: filter
description: Obtenga información sobre el filtro de funciones
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: filtro, función, expresión, recorrido
exl-id: 05e3d2ba-1a27-4f27-88cc-3d83eb3b14af
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 9%

---

# filter{#filter}

Devuelve un listObject con objetos cuyo atributo key coincide con uno de los valores de clave determinados.

## Categoría

Lista

## Sintaxis de función

`filter(<parameters>)`

## Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToFilter | listObject | lista de objetos que se van a filtrar. Debe ser una referencia de campo. |
| keyAttributeName | string | nombre del atributo en los objetos de la lista dada, utilizado como clave para el filtrado |
| keyValueList | list | matriz de valores clave para el filtrado |

## Firmas y tipos devueltos

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Devuelve un listObject.

## Ejemplos

Este es un ejemplo de una carga útil pasada en un evento entrante &quot;myevent&quot;:

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

Puede utilizar la siguiente expresión:

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Devuelve un listObject que contiene los dos objetos con &quot;product2&quot; y &quot;product3&quot; como id.
