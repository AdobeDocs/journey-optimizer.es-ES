---
product: adobe campaign
title: toInteger
description: Obtenga información sobre la función toInteger
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 14%

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
| string | convierte el valor de cadena en un entero |
| dateTime | convierte la fecha en el número de milisegundos (epoch miliseconds) |
| decimal | se convierte en entero eliminando la parte decimal (ejemplo: 1,5 se convierte en 1) |
| Booleano | convierte el valor booleano en 1 si es verdadero, 0 si es falso |

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
