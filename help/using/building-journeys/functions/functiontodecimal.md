---
product: journey optimizer
title: toDecimal
description: Obtenga información acerca de la función toDecimal
feature: Journeys
role: Developer
level: Experienced
keywords: decimal, función, expresión, recorrido
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 13%

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
| cadena | convierte el valor de cadena como decimal |
| dateTime | convierte la fecha como el número de milisegundos (epoch milisegundos) |
| Booleano | convierte el valor booleano como 1 si es verdadero, 0 si es falso |
| entero | convierte a decimal (ejemplo).: 1 se convierte en 1,0) |

## Firmas y tipos devueltos

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Devuelve un decimal.

## Ejemplos

`toDecimal("4.0")`

Devuelve 4.0.
