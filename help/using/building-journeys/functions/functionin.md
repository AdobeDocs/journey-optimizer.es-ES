---
product: journey optimizer
title: en
description: Obtenga información acerca de la función en
feature: Journeys
role: Developer
level: Experienced
keywords: en, función, expresión, recorrido
exl-id: 629b7aa3-8904-453b-ba3c-c6a333b13c81
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 23%

---

# en {#in}

Comprueba si el primer valor del argumento está en la lista. La comprobación se realiza mediante un valor Equal en cada argumento value. Devuelve true si se encuentra el valor del argumento; en caso contrario, devuelve false.

El tipo de `<expression>` debe coincidir con los elementos de la lista. Los tipos de elementos de la lista, como recordatorio, deben coincidir entre sí.

## Categoría

Lista

## Sintaxis de función

`in(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| Cadena | Cadena |
| Booleano | Booleano |
| Entero | Entero |
| Decimal | Decimal |
| Duración | Duración |
| Fecha/Hora | Fecha/Hora |
| DateTimeOnly | DateTimeOnly |
| Lista | listString |
| Lista | listBoolean |
| Lista | listInteger |
| Lista | listDecimal |
| Lista | listDuration |
| Lista | listDateTime |
| Lista | listDateTimeOnly |
| Lista | listDateOnly |

## Firma y tipo devuelto

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Devuelve un valor booleano.

## Ejemplo

`in(4,[4,5,3,4])`

Devuelve verdadero.

`in(8,[4,5,3,4])`

Devuelve falso.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
