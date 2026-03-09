---
title: Modelos de IA de mediación de recorrido
description: Aprenda a crear y utilizar modelos de IA para clasificar recorridos para mediación, de modo que se seleccione el mejor recorrido por perfil en función de las puntuaciones impulsadas por IA.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Disponibilidad limitada" type="Informative"
hide: true
hidefromtoc: true
exl-id: 3e7c3069-b022-4709-936d-acaad56b5882
source-git-commit: afc09bbcb76d53404574bb53c0a896109cd7f1da
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 3%

---

# Uso de modelos de IA para clasificar recorridos {#journey-ai-models}

>[!AVAILABILITY]
>
>Actualmente, esta función se encuentra en disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

[!DNL Adobe Journey Optimizer] le ayuda a controlar qué recorridos puede introducir un perfil cuando cumplen los requisitos para obtener más de lo que permite el sistema. Para ello, puede usar [conjuntos de reglas](rule-sets.md) para definir límites en la entrada de recorrido o la concurrencia. Cuando un perfil es elegible para recibir más recorridos de los que permite el límite, la prioridad asignada a cada recorrido determina qué recorridos se seleccionan.

En lugar de usar priority, también puede usar **modelos de IA** en sus fórmulas de clasificación para clasificar recorridos dinámicamente según puntuaciones de modelos entrenados.

## Creación de un modelo de IA {#create-ai-model}

<!--Do you need specific permissions to create AI models?
>[!CAUTION]
>
>To create, edit, or delete AI models, you must have the **Manage Ranking Strategies** permission. [Learn more](../administration/high-low-permissions.md#manage-ranking-strategies)-->

Para crear un modelo de IA para la clasificación de recorridos, siga los pasos a continuación.

1. Cree un conjunto de datos donde se recopilen los eventos de conversión. [Descubra cómo](../experience-decisioning/data-collection/create-dataset.md)

1. Acceda a la sección **[!UICONTROL Clasificación de orquestaciones]** y, a continuación, seleccione la pestaña **[!UICONTROL Modelos de IA]**. Se muestra la lista de modelos de IA creados anteriormente.

1. Haga clic en **[!UICONTROL Crear modelo de IA]**.

1. Especifique un nombre único y, si es necesario, una descripción para el modelo de IA.

   ![Panel de detalles del modelo de IA con campos de nombre y descripción](assets/journey-model-details.png){width="80%"}

   >[!NOTE]
   >
   >El objeto de clasificación es la entidad a la que se aplica la fórmula de clasificación. De manera predeterminada, el objeto de clasificación está establecido en **[!UICONTROL Recorrido]**.

<!--
1. Select the type of AI model you want to create:

    * **[!UICONTROL Auto-optimization]** optimizes based on past performance. [Learn more](../experience-decisioning/ranking/auto-optimization-model.md)
    * **[!UICONTROL Personalized optimization]** optimizes and personalizes based on audiences and performance. [Learn more](../experience-decisioning/ranking/personalized-optimization-model.md)-->

1. En la **[!UICONTROL métrica de optimización]**, todas las métricas de su [!DNL Customer Journey Analytics] [vista de datos](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"} predeterminada se muestran en la lista. Seleccione la métrica en la que desea optimizar el modelo.

   ![Panel de detalles del modelo de IA con campos de nombre y descripción](assets/journey-model-metrics.png){width="80%"}

   [!DNL Journey Optimizer] se clasifica según la **tasa de conversión** (tasa de conversión = número total de eventos de conversión / número total de eventos de impresión). La tasa de conversión se calcula mediante:

   * **Eventos de impresión** (elementos que se muestran)
   * **Eventos de conversión** (elementos que resultan en clics o conversiones)

   Estos eventos se capturan automáticamente mediante Web SDK o Mobile SDK. Obtenga más información en la descripción general de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es).

1. Seleccione los conjuntos de datos donde se recopilan los eventos de conversión e impresión. Aprenda a crear estos conjuntos de datos en [esta sección](../experience-decisioning/data-collection/create-dataset.md).

   ![Selección de conjuntos de datos para eventos de conversión e impresión](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >En la lista desplegable solo se muestran los conjuntos de datos creados a partir de esquemas asociados con el grupo de campos **[!UICONTROL Evento de experiencia: interacciones de propuesta]** (anteriormente conocido como mixin).

1. &#x200B;<!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->Seleccione los segmentos que se utilizarán para entrenar el modelo de IA.

   >[!NOTE]
   >
   >Puede seleccionar hasta 50 audiencias.

1. Guarde y active el modelo de IA.

El modelo de IA ahora está disponible para su selección al crear una fórmula de clasificación.

## Seleccione un modelo de IA para una fórmula de clasificación {#select-ai-model-for-ranking-formula}

Ahora puede establecer el modelo de IA como referencia para crear una fórmula de clasificación. Siga los pasos a continuación.

1. Cree una fórmula de clasificación. [Descubra cómo](journey-ranking-formulas.md#create-journey-ranking-formula)

1. Utilice el botón **[!UICONTROL Seleccionar modelo de IA]** para seleccionar el modelo de IA que desea utilizar.

   ![panel de detalles de la fórmula de clasificación de Recorridos con selección de modelo de IA](assets/journey-formula-ai-model.png){width="80%"}

1. En al menos una de las secciones **[!UICONTROL Criterion]**, defina una condición y seleccione **[!UICONTROL Puntuación del modelo de IA]** como método de clasificación. Por ejemplo, si el recorrido tiene la etiqueta &quot;Promoción&quot;, la puntuación de clasificación es la puntuación del modelo de IA.

   ![Fórmula de clasificación: la etiqueta de promoción usa la puntuación del modelo de IA](assets/journey-formula-ex-2.png){width="60%"}

1. Haga clic en **[!UICONTROL Crear]** para completar la fórmula de clasificación.

## Asignar el modelo de IA a un conjunto de reglas {#assign-ai-model-to-ruleset}

Para utilizar un modelo de IA para clasificar los recorridos, debe asignar la fórmula que hace referencia a este modelo de IA a un conjunto de reglas.

1. En el menú **[!UICONTROL Reglas de negocio]**, cree un conjunto de reglas que desee usar para el arbitraje de recorrido. [Descubra cómo](rule-sets.md#Create)

1. Asegúrese de seleccionar el dominio **[!UICONTROL Recorrido]**.

1. En las propiedades del conjunto de reglas, establezca el **[!UICONTROL método de clasificación]** en **[!UICONTROL Fórmula]** (en lugar de **[!UICONTROL Prioridad]**).

1. Seleccione la fórmula que utiliza el modelo de IA que ha creado en la lista desplegable.

1. Cree las reglas de límite de recorrido que desee agregar al conjunto de reglas. [Descubra cómo](journey-capping.md#create-rule)

1. Guarde el conjunto de reglas.

Ahora la fórmula que utiliza el modelo de IA se asigna al conjunto de reglas. A continuación, puede aplicar ese conjunto de reglas a los recorridos.

## Aplicación del conjunto de reglas a un recorrido {#assign-rule-set-to-journey}

Para asignar el conjunto de reglas a un recorrido, siga los pasos a continuación.

1. Cree o abra el recorrido al que desee asignar el conjunto de reglas. [Obtenga información sobre cómo crear un recorrido](../building-journeys/journey-gs.md)

1. En las propiedades del recorrido, seleccione el conjunto de reglas en la lista desplegable. [Más información](journey-capping.md#apply-capping).

   >[!NOTE]
   >
   >Solo se puede aplicar un conjunto de reglas a un recorrido a la vez.

1. Guarde el recorrido.

Todos los recorridos que utilicen este conjunto de reglas se clasificarán con la fórmula seleccionada utilizando el modelo de IA cuando se aplique el límite.
