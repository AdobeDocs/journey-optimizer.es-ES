---
product: journey optimizer
title: toBool
description: Obtenga información acerca de la función toBool
feature: Journeys
role: Developer
level: Experienced
keywords: tobool, función, expresión, recorrido
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 11%

---

# toBool {#toBool}

Convierte un valor de argumento en un valor booleano, según su tipo.

* Desde cadena: intente convertir el valor de cadena como booleano, de &quot;true&quot; si el valor de cadena es &quot;true&quot; y de &quot;false&quot; en caso contrario
* Desde numérico: true si el valor numérico no es igual a 0, false en caso contrario

## Categoría

Conversión

## Sintaxis de función

`toBool(<parameter>)`

## Parámetros

* decimal
* Booleano
* cadena
* entero

## Firmas y tipos devueltos

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Devuelve un valor booleano.

## Ejemplos

`toBool("true")`

`toBool(1)`

Devuelve verdadero.

`toBool("this is not a boolean")`

Devuelve falso.
