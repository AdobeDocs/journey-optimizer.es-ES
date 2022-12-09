---
product: journey optimizer
title: toBool
description: Obtenga información sobre la función aBool
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# toBool {#toBool}

Convierte un valor de argumento en un valor booleano, según su tipo.

* De cadena: intente convertir el valor de cadena como booleano, de &quot;true&quot; si el valor de cadena es &quot;true&quot;, en &quot;false&quot; en caso contrario
* De cifras: true si el valor numérico no es igual a 0, false en caso contrario

## Categoría

Conversión

## Sintaxis de función

`toBool(<parameter>)`

## Parámetros

* decimal
* booleano
* string
* integer

## Firmas y tipos devueltos

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Devuelve un booleano.

## Ejemplos

`toBool("true")`

`toBool(1)`

Devuelve verdadero.

`toBool("this is not a boolean")`

Devuelve falso.
