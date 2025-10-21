---
product: journey optimizer
title: notEqualIgnoreCase
description: Obtenga información sobre la función notEqualIgnoreCase
feature: Journeys
role: Developer
level: Experienced
keywords: notEqualIgnoreCase, función, expresión, recorrido
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 12%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

Compruebe si la cadena del primer argumento con la cadena del segundo argumento es diferente, ignorando las consideraciones de mayúsculas y minúsculas.

## Categoría

Cadena

## Sintaxis de función

`notEqualIgnoreCase(<parameters>)`

## Parámetros

* cadena

## Firma y tipo devuelto

`notEqualIgnoreCase(<string>,<string>)`

Devuelve un valor booleano.

## Ejemplo

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`
