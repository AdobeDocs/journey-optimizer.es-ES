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
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 4%

---

# Uso de modelos de IA para clasificar recorridos {#journey-ai-models}

>[!AVAILABILITY]
>
>Actualmente, esta función se encuentra en disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

[!DNL Adobe Journey Optimizer] le ayuda a controlar qué recorridos puede introducir un perfil cuando cumplen los requisitos para obtener más de lo que permite el sistema. Para ello, puede usar [conjuntos de reglas](rule-sets.md) para definir límites en la entrada de recorrido o la concurrencia. Cuando un perfil es elegible para recibir más recorridos de los que permite el límite, la prioridad asignada a cada recorrido determina qué recorridos se seleccionan.

En lugar de usar fórmulas de clasificación o de prioridades, puede usar **modelos de IA** para clasificar dinámicamente los recorridos según puntuaciones de modelos entrenados. Puede crear modelos de IA a partir de la sección **[!UICONTROL Clasificación de orquestaciones]** de la interfaz de usuario y utilizarlos en conjuntos de reglas para aplicarlos a los recorridos.

Para obtener una descripción general de los tipos de modelos de IA disponibles en [!DNL Journey Optimizer], consulte [Introducción a los modelos de IA](../experience-decisioning/ranking/ai-models.md#ai-model-types) en la sección Toma de decisiones.

## Creación de un modelo de IA {#create-ai-model}

>[!CAUTION]
>
>Para crear, editar o eliminar modelos de IA, debe tener el permiso **Administrar estrategias de clasificación**. [Más información](../administration/high-low-permissions.md#manage-ranking-strategies)

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

1. La sección **[!UICONTROL Métrica de optimización]** proporciona información sobre el evento de conversión utilizado por el modelo de IA. [!DNL Journey Optimizer] se clasifica según la **tasa de conversión** (tasa de conversión = número total de eventos de conversión / número total de eventos de impresión). La tasa de conversión se calcula mediante:

   * **Eventos de impresión** (elementos que se muestran)
   * **Eventos de conversión** (elementos que resultan en clics o conversiones)

   Estos eventos se capturan automáticamente mediante Web SDK o Mobile SDK. Obtenga más información en la descripción general de [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es).

1. Seleccione los conjuntos de datos donde se recopilan los eventos de conversión e impresión. Aprenda a crear estos conjuntos de datos en [esta sección](../experience-decisioning/data-collection/create-dataset.md).

   ![Selección de conjuntos de datos para eventos de conversión e impresión](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >En la lista desplegable solo se muestran los conjuntos de datos creados a partir de esquemas asociados con el grupo de campos **[!UICONTROL Evento de experiencia: interacciones de propuesta]** (anteriormente conocido como mixin).

1. <!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->Seleccione los segmentos que se utilizarán para entrenar el modelo de IA.

   >[!NOTE]
   >
   >Puede seleccionar hasta cinco audiencias.

1. Guarde y active el modelo de IA.

El modelo de IA ahora está disponible al configurar un conjunto de reglas.

## Asignar el modelo de IA a un conjunto de reglas {#assign-ai-model-to-ruleset}

Para utilizar un modelo de IA para clasificar los recorridos, debe utilizarlo en una fórmula y asignarla a un conjunto de reglas.

1. Cree una fórmula de clasificación con el modelo de IA que ha creado. [Descubra cómo](journey-ranking-formulas.md#create-journey-ranking-formula)

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
