---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Creación de modelos de IA
description: Aprenda a crear modelos de IA para clasificar ofertas
badge: label="Heredado" type="Informative"
feature: Ranking, Decision Management
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/B33mvmBY4p0K43oK-NeaWGfbwhvHMyiLkM7dhxT8-WI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 523
ht-degree: 29%

---

# Creación de modelos de IA {#ai-rankings}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../experience-decisioning/gs-experience-decisioning.md)

[!DNL Journey Optimizer] le permite crear **modelos de IA** para clasificar ofertas según sus objetivos comerciales.

>[!CAUTION]
>
>Para crear, editar o eliminar modelos de IA, debe tener el permiso **Administrar estrategias de clasificación**. [Más información](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Creación de un modelo de IA {#create-ranking-strategy}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_metric"
>title="Métrica de optimización"
>abstract="[!DNL Journey Optimizer] clasifica ofertas según la **tasa de conversión** (la tasa de conversión es igual al número total de eventos de conversión/número total de eventos de impresión). La tasa de conversión se calcula usando dos tipos de métricas: **Eventos de impresión** (ofertas que se muestran) y **Eventos de conversión** (ofertas que se generan por clics de correos electrónicos o por la web). Estos eventos se capturan automáticamente mediante el SDK web o el SDK móvil proporcionado."

Para crear un modelo de IA, siga los pasos a continuación:

1. Cree un conjunto de datos donde se recopilen los eventos de conversión. [Descubra cómo](../data-collection/create-dataset.md)

1. En el menú **[!UICONTROL Componentes]**, acceda a la pestaña **[!UICONTROL Clasificación]** y, a continuación, seleccione **[!UICONTROL modelos de IA]**.

   ![](../assets/ai-ranking-list.png)

   Se muestran todos los modelos de IA creados hasta el momento.

1. Haga clic en el botón **[!UICONTROL Crear modelo de IA]**.

1. Especifique un nombre único y una descripción para el modelo de IA y, a continuación, seleccione el tipo de modelo de IA que desea crear:

   * **[!UICONTROL Optimización automática]** optimiza las ofertas basándose en el rendimiento de las ofertas anteriores. [Más información](auto-optimization-model.md)
   * **[!UICONTROL Optimización personalizada]** optimiza y personaliza ofertas basadas en audiencias y rendimiento de ofertas. [Más información](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >La sección **[!UICONTROL Métrica de optimización]** proporciona información sobre el evento de conversión utilizado por el modelo de IA para calcular la clasificación de las ofertas.
   >
   >[!DNL Journey Optimizer] clasifica ofertas según la **tasa de conversión** (la tasa de conversión es igual al número total de eventos de conversión/número total de eventos de impresión). La tasa de conversión se calcula mediante dos tipos de métricas:
   >* **Eventos de impresión** (ofertas que se muestran)
   >* **Eventos de conversión** (ofertas que generan clics por correo electrónico o web).
   >
   >Estos eventos se capturan automáticamente mediante el SDK web o el SDK móvil proporcionado. Obtenga más información sobre esto en [Información general de Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es).

1. Seleccione los conjuntos de datos donde se recopilan los eventos de conversión e impresión. Aprenda a crear este conjunto de datos en [esta sección](../data-collection/create-dataset.md). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >En la lista desplegable solo se muestran los conjuntos de datos creados a partir de esquemas asociados con el grupo de campos **[!UICONTROL Evento de experiencia: interacciones de propuesta]** (anteriormente conocido como mixin).

1. Si está creando un modelo de IA de **[!UICONTROL optimización personalizada]**, seleccione los segmentos que se usarán para entrenar el modelo de IA.

   ➡️ [Descubra esta funcionalidad en vídeo](#video)

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >Puede seleccionar hasta cinco audiencias.

1. Guarde y active el modelo de IA.

   ![](../assets/ai-ranking-save-activate.png)

<!--
At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.
-->

Ahora, cada vez que se muestra una oferta o se hace clic en ella, desea que el grupo de campos **[!UICONTROL Evento de experiencia - Interacciones de propuesta]** capture automáticamente el evento correspondiente mediante [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=es#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} o Mobile SDK.

Para poder enviar tipos de eventos (oferta mostrada u oferta seleccionada), debe establecer el valor correcto para cada tipo de evento en un evento de experiencia que se envíe a Adobe Experience Platform. [Descubra cómo](../data-collection/schema-requirement.md)

## Vídeo práctico {#video}

Obtenga información sobre cómo crear un modelo de optimización personalizado y cómo aplicarlo a una decisión.

>[!VIDEO](https://video.tv.adobe.com/v/3445954?captions=spa&quality=12)
