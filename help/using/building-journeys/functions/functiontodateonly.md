---
product: journey optimizer
title: toDateOnly
description: Obtenga información sobre la función toDateOnly
feature: Journeys
role: Engineer
level: Experienced
keywords: toDateOnly, función, expresión, recorrido
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 10%

---

# toDateOnly{#toDateOnly}

Convierte un argumento en un valor de tipo dateOnly. Para obtener más información sobre los tipos de datos, consulte esta [sección](../expression/data-types.md).

## Categoría

Conversión

## Sintaxis de función

`toDateOnly(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| Representación de cadena de una fecha como &quot;AAAA-MM-DD&quot; (formato XDM). También admite el formato ISO-8601: solo se tiene en cuenta la parte **full-date** (consulte [RFC 3339, sección 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | cadena |
| fecha y hora | dateTime |
| fecha y hora sin zona horaria | dateTimeOnly |
| valor entero de una época en milisegundos | entero |

## Firmas y tipos devueltos

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Devuelve un valor de tipo dateOnly.

## Ejemplos

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

todos devuelven un objeto dateOnly que representa el 18-08-2023.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Devuelve dateOnly.
