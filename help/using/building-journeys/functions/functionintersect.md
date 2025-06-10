---
product: journey optimizer
title: intersect
description: Obtenga información sobre la intersección de funciones
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: intersect, función, expresión, recorrido
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: 49c3fd09d23e6394b6eff8ba4da71ed7bab8c82c
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 11%

---

# intersect{#intersect}

Devuelve los valores comunes de las dos listas de entrada. Si una de las dos listas es nula, devuelve una lista vacía.

## Categoría

Lista

## Sintaxis de función

`intersect(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| lista 1 | list |
| lista 2 | list |

## Firmas y tipos devueltos

`intersect(listString,listString)`: listString
`intersect(listDecimal,listDecimal)`: listDecimal
`intersect(listInteger,listInteger)`: listInteger
`intersect(listDateTime,listDateTime)`: listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly
`intersect(listDateOnly,listDateOnly)`: listDateOnly
`intersect(listDuration,listDuration)`: listDuration
`intersect(listBoolean,listBoolean)`: listBoolean

Devuelve una lista.

## Ejemplos

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Devuelve [&quot;deportes&quot;, &quot;noticias&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

Devuelve elementos comunes entre atributos de perfil y una lista de categorías determinada.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

Devuelve elementos comunes entre atributos de perfil y un campo de evento determinado.
