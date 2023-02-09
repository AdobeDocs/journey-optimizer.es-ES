---
product: journey optimizer
title: toDateOnly
description: Obtenga información sobre la función toDateOnly
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateOnly, función, expresión, recorrido
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 10%

---

# toDateOnly{#toDateOnly}

Convierte un argumento en un valor de tipo dateOnly . Para obtener más información sobre los tipos de datos, consulte esta [sección](../expression/data-types.md).

## Categoría

Conversión

## Sintaxis de función

`toDateOnly(<parameters>)`

## Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| Representación de cadena de una fecha como &quot;AAAA-MM-DD&quot; (formato XDM). También admite el formato ISO-8601: only **fecha completa** parte se considera (consulte [RFC 3339, sección 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | string |
| fecha y hora | dateTime |
| fecha y hora sin zona horaria | dateTimeOnly |
| valor entero de una epoch en milisegundos | entero |

## Firmas y tipos devueltos

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Devuelve un valor de tipo dateOnly.

## Ejemplos

`toDateOnly("2016-08-18")`

`toDateOnly("2016-08-18T00:00:00.000Z")`

`toDateOnly("2016-08-18T00:00:00")`

todos devuelven un objeto dateOnly que representa 2016-08-18.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Devuelve un dateOnly.
