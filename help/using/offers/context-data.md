---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Introducción a los datos de contexto
description: Aprenda a aprovechar los datos de contexto en la administración de decisiones.
badge: label="Heredado" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/aVm2FFqkJWN-k1qngYsp94FgKIZWaLCMUneFd0rVNpA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 12%

---

# Introducción a los datos de contexto {#context-data}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../experience-decisioning/gs-experience-decisioning.md)

Los datos enviados como parte de la solicitud de toma de decisiones se consideran datos de contexto. Puede aprovechar los datos de contexto en el motor de toma de decisiones, por ejemplo, para diseñar una regla de decisión que requiera que el clima actual sea de ≥80 grados en el momento en que se realice la solicitud de decisión.

Los datos de contexto se definen de manera diferente entre las solicitudes de API **Decisioning** y **Edge Decisioning**. Para ambos tipos de solicitudes, los datos de contexto se pueden utilizar en reglas de idoneidad o en fórmulas de clasificación, pero solo las solicitudes de API de Edge Decisioning pueden utilizar datos de contexto para personalizar el contenido.

Antes de empezar, compruebe las siguientes protecciones y limitaciones:

* Debido a la diferente forma de pasar el contexto entre las llamadas de Decisioning y Edge Decisioning, las reglas de elegibilidad basadas en el contexto y las fórmulas de clasificación no son intercambiables entre las llamadas de Decisioning y Edge Decisioning.
* Solo es posible realizar pruebas con el parámetro `dryrun` con la API Decisioning. No está disponible con la API de Edge Decisioning. Tenga en cuenta que configurar este parámetro en `true` con la API de decisiones no afecta a los límites ni al número de propuestas.

Para obtener información detallada sobre cómo utilizar los datos de contexto en cada API, consulte estas secciones:

* [Uso de datos de contexto en solicitudes de Edge Decisioning](context-data-edge.md)
* [Uso de datos de contexto en solicitudes de Decisioning](context-data-decisioning.md)
