---
product: experience platform
solution: Experience Platform
title: Introducción a los datos de contexto
description: Aprenda a aprovechar los datos de contexto en la administración de decisiones.
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Introducción a los datos de contexto {#context-data}

Los datos enviados como parte de la solicitud de toma de decisiones se consideran datos de contexto. Puede aprovechar los datos de contexto en el motor de toma de decisiones, por ejemplo, para diseñar una regla de decisión que requiera que el clima actual sea de ≥80 grados en el momento en que se realice la solicitud de decisión.

Los datos de contexto se definen de manera diferente entre las solicitudes de API **Decisioning** y **Edge Decisioning**. Para ambos tipos de solicitudes, los datos de contexto se pueden utilizar en reglas de idoneidad o en fórmulas de clasificación, pero solo las solicitudes de API de Edge Decisioning pueden utilizar datos de contexto para personalizar el contenido.

Antes de empezar, compruebe las siguientes protecciones y limitaciones:

* Debido a la diferente forma de pasar el contexto entre las llamadas de Decisioning y Edge Decisioning, las reglas de elegibilidad basadas en el contexto y las fórmulas de clasificación no son intercambiables entre las llamadas de Decisioning y Edge Decisioning.
* Solo es posible realizar pruebas con el parámetro `dryrun` con la API Decisioning. No está disponible con la API de Edge Decisioning. Tenga en cuenta que configurar este parámetro en `true` con la API de decisiones no afecta a los límites ni al número de propuestas.

Para obtener información detallada sobre cómo utilizar los datos de contexto en cada API, consulte estas secciones:

* [Uso de datos de contexto en solicitudes de Edge Decisioning](context-data-edge.md)
* [Uso de datos de contexto en solicitudes de Decisioning](context-data-decisioning.md)

