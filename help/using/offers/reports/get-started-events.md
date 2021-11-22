---
title: Introducción a los eventos de Administración de decisiones
description: Obtenga información sobre cómo crear informes de Administración de decisiones en Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 57%

---

# Introducción a los eventos de Administración de decisiones {#monitor-offer-events}

Cada vez que la Administración de decisiones toma una decisión sobre un perfil determinado, la información relacionada con estos eventos se envía automáticamente a Adobe Experience Platform.

Esto le permite exportar estos datos para analizarlos en su propio sistema de informes. También puede aprovechar Adobe Experience Platform [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=es) con otras herramientas para mejorar los análisis y la creación de informes.

Los conjuntos de datos que contienen eventos de Administración de decisiones son accesibles desde Adobe Experience Platform **[!UICONTROL Datasets]** para abrir el Navegador. Se crea automáticamente un conjunto de datos en el aprovisionamiento para cada una de las instancias.

![](../../assets/events-datasets-list.png)

Estos conjuntos de datos se basan en la variable **[!UICONTROL ODE DecisionEvents]** esquema, que contiene todos los campos XDM necesarios para enviar información de Administración de decisiones a Adobe Experience Platform.

>[!NOTE]
>
>Tenga en cuenta que los conjuntos de datos de ODE DecisionEvents son **conjuntos de datos que no son de perfil**, lo que significa que no se pueden ingerir en Experience Platform para que los use el perfil de cliente en tiempo real.

**Temas relacionados:**

* [Información clave sobre eventos de Administración de decisiones](../reports/key-information.md)
* [Campos XDM de eventos de acceso](../reports/xdm-fields.md)
