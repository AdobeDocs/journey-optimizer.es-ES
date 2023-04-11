---
product: experience platform
solution: Experience Platform
title: Creación de modelos de IA
description: Aprenda a crear modelos de IA para clasificar ofertas
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 6%

---

# Creación de modelos de IA {#ai-rankings}

[!DNL Journey Optimizer] permite crear **Modelos de IA** para clasificar las ofertas según los objetivos comerciales.

>[!CAUTION]
>
>Para crear, editar o eliminar modelos de IA, debe tener la variable **Administrar estrategias de clasificación** permiso. [Más información](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Creación de un modelo de IA {#create-ranking-strategy}

Para crear un modelo de IA, siga los pasos a continuación:

1. Cree un conjunto de datos donde se recopilen los eventos de conversión. [Descubra cómo](../data-collection/create-dataset.md)

1. En el **[!UICONTROL Componentes]** , acceda al menú **[!UICONTROL Clasificación]** y, a continuación, seleccione **[!UICONTROL Modelos de IA]**.

   ![](../assets/ai-ranking-list.png)

   Se muestran todos los modelos de IA creados hasta ahora.

1. Haga clic en el **[!UICONTROL Crear modelo AI]** botón.

1. Especifique un nombre único y una descripción para el modelo de IA y, a continuación, seleccione el tipo de modelo de IA que desea crear:

   * **[!UICONTROL Optimización automática]** optimiza las ofertas en función del rendimiento de ofertas anteriores. [Más información](auto-optimization-model.md)
   * **[!UICONTROL Personalizado]** optimiza y personaliza las ofertas en función de segmentos y del rendimiento de las ofertas. [Más información](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >La variable **[!UICONTROL Métrica de optimización]** proporciona información sobre el evento de conversión utilizado por el modelo de IA para calcular la clasificación de las ofertas.
   >
   >[!DNL Journey Optimizer] clasificar ofertas en función de **tasa de conversión** (Tasa de conversión = Número total de eventos de conversión/Número total de eventos de impresión). La tasa de conversión se calcula mediante dos tipos de métricas:
   >* **Eventos de impresión** (ofertas que se muestran)
   >* **Eventos de conversión** (ofertas que resultan en clics por correo electrónico o web).

   >
   >Estos eventos se capturan automáticamente mediante el SDK web o el SDK móvil que se ha proporcionado. Obtenga más información sobre esto en [Información general del SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es).

1. Seleccione los conjuntos de datos donde se recopilan los eventos de impresión y conversión. Obtenga información sobre cómo crear este conjunto de datos en [esta sección](../data-collection/create-dataset.md). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Solo los conjuntos de datos creados a partir de esquemas asociados con la variable **[!UICONTROL Evento de experiencia: interacciones de propuesta]** el grupo de campos (anteriormente conocido como mezcla) se muestra en la lista desplegable.

1. Si está creando un **[!UICONTROL Personalización]** Modelo AI, seleccione los segmentos que se utilizarán para entrenar el modelo AI.

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >Puede seleccionar hasta 5 segmentos.

1. Guarde y active el modelo de IA.

   ![](../assets/ai-ranking-save-activate.png)

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

Ahora, cada vez que se muestra una oferta o se hace clic en ella, desea que el evento correspondiente sea capturado automáticamente por la variable **[!UICONTROL Evento de experiencia: interacciones de propuesta]** grupo de campos con la variable [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} o SDK móvil.

Para poder enviar tipos de eventos (oferta mostrada u oferta pulsada), debe establecer el valor correcto para cada tipo de evento en un evento de experiencia que se envíe a Adobe Experience Platform. [Descubra cómo](../data-collection/schema-requirement.md)