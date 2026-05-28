---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Trabajar con eventos de gestión de decisiones
description: Obtenga información sobre cómo crear informes de Gestión de decisiones en Adobe Experience Platform.
badge: label="Heredado" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/r3bOKyWcAT-sqI7KXA3J-Yi5TUax9KGi-8JY62QD6tA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 321
ht-degree: 100%

---

# Introducción a los eventos de Gestión de decisiones {#monitor-offer-events}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../experience-decisioning/gs-experience-decisioning.md)

Cada vez que Gestión de decisiones toma una decisión sobre un perfil determinado, la información relacionada con estos eventos se envía automáticamente a Adobe Experience Platform.

Esto le permite obtener información sobre sus decisiones, por ejemplo, para saber qué oferta se presentó a un perfil determinado. Puede exportar estos datos para analizarlos en su propio sistema de informes o aprovechar el [Servicio de consultas](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=es) de Adobe Experience Platform en combinación con otras herramientas para mejorar el análisis y la creación de informes.

## Información clave disponible en conjuntos de datos {#key-information}

Cada evento que se envía cuando se toma una decisión contiene cuatro puntos de datos clave que puede aprovechar para realizar análisis e informes:

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Reserva]**: Nombre e ID de la oferta de reserva, si no se ha seleccionado ninguna oferta personalizada,
* **[!UICONTROL Ubicación]**: Nombre, ID y canal de la ubicación utilizada para entregar la oferta,
* **[!UICONTROL Selecciones]**: Nombre e ID de la oferta seleccionada para el perfil,
* **[!UICONTROL Actividad]**: Nombre e ID de la decisión.

Además, también puede aprovechar los campos  **[!UICONTROL identityMap]** y **[!UICONTROL Marca de tiempo]** para recuperar información sobre el perfil y la hora a la que se entregó la oferta.

Para obtener más información sobre todos los campos XDM que se envían con cada decisión, consulte [esta sección](xdm-fields.md).

## Acceso a conjuntos de datos {#access-datasets}

Se puede acceder a los conjuntos de datos que contienen eventos de Gestión de decisiones desde el menú **[!UICONTROL Conjuntos de datos]** de Adobe Experience Platform. Se crea automáticamente un conjunto de datos en el aprovisionamiento para cada una de las instancias.

![](../assets/events-datasets-list.png)

Estos conjuntos de datos se basan en el esquema **[!UICONTROL ODE DecisionEvents]**, que contiene todos los campos XDM necesarios para enviar información desde Gestión de decisiones a Adobe Experience Platform.

>[!NOTE]
>
>Tenga en cuenta que los conjuntos de datos de ODE DecisionEvents son **conjuntos de datos que no son de perfil**, lo que significa que no se pueden ingerir en Experience Platform para que los use el perfil del cliente en tiempo real.
