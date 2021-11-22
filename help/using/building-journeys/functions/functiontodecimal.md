---
product: adobe campaign
title: toDecimal
description: Obtenga información sobre la función aDecimal
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 14%

---

# toDecimal {#toDecimal}

Convierte un valor de argumento en un valor decimal, según su tipo.

## Categoría

Conversión

## Sintaxis de función

`toDecimal(<parameter>)`

## Parámetros

| Parámetro | Descripción |
|--- |--- |
| string | convierte el valor de cadena en decimal |
| dateTime | convierte la fecha en el número de milisegundos (epoch miliseconds) |
| Booleano | convierte el valor booleano en 1 si es verdadero, 0 si es falso |
| integer | se convierte en decimal (ejemplo.: 1 se convierte en 1.0) |

## Firmas y tipos devueltos

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Devuelve un decimal.

## Ejemplos

`toDecimal("4.0")`

Devuelve 4.0.
