---
product: journey optimizer
title: notEqualIgnoreCase
description: Obtenga información sobre la función notEqualIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 13%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

Compruebe si la primera cadena de argumento con la segunda cadena de argumento es diferente, ignorando las consideraciones de mayúsculas y minúsculas.

## Categoría

Cadena

## Sintaxis de función

`notEqualIgnoreCase(<parameters>)`

## Parámetros

* string

## Firma y tipo devuelto

`notEqualIgnoreCase(<string>,<string>)`

Devuelve un valor booleano.

## Ejemplo

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
