---
product: journey optimizer
title: toInteger
description: Obtenga información acerca de la función toInteger
feature: Journeys
role: Developer
level: Experienced
keywords: toInteger, función, expresión, recorrido
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 12%

---

# toInteger {#toInteger}

Convierte un valor de argumento en un entero.

## Categoría

Conversión

## Sintaxis de función

`toInteger(<parameter>)`

## Parámetros

| Parámetro | Descripción |
|--- |--- |
| cadena | convierte el valor de cadena como un entero |
| dateTime | convierte la fecha como el número de milisegundos (epoch milisegundos) |
| decimal | convierte en entero eliminando la parte decimal (ejemplo: 1,5 se convierte en 1) |
| Booleano | convierte el valor booleano como 1 si es verdadero, 0 si es falso |

## Firmas y tipo devuelto

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Devuelve un entero.

## Ejemplos

`toInteger("4")`

Devuelve 4.
