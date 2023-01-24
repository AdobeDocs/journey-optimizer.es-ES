---
product: journey optimizer
title: toDecimal
description: Obtenga información sobre la función aDecimal
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: decimal, función, expresión, recorrido
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '75'
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
