---
product: journey optimizer
title: límite
description: Obtenga información sobre el límite de funciones
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 8%

---

# límite {#limit}

Devuelve el primer o el último N elementos de una lista.

>[!NOTE]
>
>Si la lista de destino es un listObject, esta función solo se puede utilizar en expresiones de acción personalizadas.

## Categoría

Lista

## Sintaxis de función

`limit(<parameters>)`

## Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para ordenar. Para listObject, debe ser una referencia de campo. |
| numberOfItems | integer | Número de elementos que se van a devolver de la lista dada. |
| firstOrLastItems | Booleano | Este parámetro es opcional (true de forma predeterminada). true devuelve los primeros elementos. false devuelve los últimos elementos. |

## Firma y tipo devuelto

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

Devuelve una lista de cadenas.

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

Devuelve una lista de enteros.

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

Devuelve una lista de decimales.

`limit(<listBoolean>,<integer>)`
`limit(<listBoolean>,<integer>,<boolean>)`

Devuelve una lista de booleanos.

`limit(<listDateOnly>,<integer>)`
`limit(<listDateOnly>,<integer>,<boolean>)`

Devuelve una lista de fechas.

`limit(<listDateTimeOnly>,<integer>)`
`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Devuelve una lista de tiempos de datos sin tener en cuenta la zona horaria.

`limit(<listDateTime>,integer>)`
`limit(<listDateTime>,<integer>,<boolean>)`

Devuelve una lista de tiempos de datos.

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

Devuelve una lista de duraciones.

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

Devuelve una lista de objetos.

## Ejemplo

`limit(["A", "B", "C", "D", "E"], 3)`

Devuelve `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Devuelve `["C","D","E"]`.
