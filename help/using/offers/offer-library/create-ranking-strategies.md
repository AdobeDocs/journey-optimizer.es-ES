---
product: experience platform
solution: Experience Platform
title: Crear estrategias de clasificación
description: Aprenda a crear estrategias de clasificación en Adobe Experience Platform.
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 6%

---

# Clasificación de IA {#ai-rankings}

## Introducción a las clasificaciones de IA

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can use an trained model system that ranks offers to display for a given profile.

>[!CAUTION]
>
>El uso de la clasificación AI está disponible actualmente en el acceso anticipado solo para usuarios seleccionados.

Esta función le permite crear diferentes **estrategias de clasificación** en función de sus objetivos comerciales. Utilizando estas diferentes estrategias basadas en objetivos en una decisión (anteriormente conocida como actividad de oferta), el sistema de modelos entrenado le ayudará a comprender cómo las diferentes estrategias de clasificación afectan a sus objetivos.

Por ejemplo, puede seleccionar una estrategia de clasificación para el canal de correo electrónico y otra para el canal push. Para cada canal, el sistema de modelos entrenado utilizará múltiples puntos de datos para determinar qué oferta debe presentarse primero para una ubicación determinada, en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas o una fórmula de [clasificación](create-ranking-formulas.md).

<!--This feature is not enabled by default. To be able to use it, reach out to your Adobe contact.-->

Una vez creada una estrategia de clasificación, asígnela a una colocación en una decisión. Obtenga más información en [Configurar la selección de ofertas en decisiones](../offer-activities/configure-offer-selection.md).

## Crear una estrategia de clasificación {#create-ranking-strategy}

Para crear una estrategia de clasificación, siga los pasos a continuación:

1. Acceda al menú **[!UICONTROL Components]** y seleccione la pestaña **[!UICONTROL AI rankings]** .

   ![](../../assets/ai-ranking-list.png)

   Se muestran todas las estrategias de clasificación creadas hasta el momento.

1. Haga clic en el botón **[!UICONTROL Create strategy]**.

1. Complete los campos siguientes:

   ![](../../assets/ai-ranking-fields.png)

   * **[!UICONTROL Name]**: Nombre único que debe proporcionar.

   * **[!UICONTROL Model type]**: Actualmente, el único tipo de modelo admitido es  **[!UICONTROL Auto-optimization]**.<!--More will be supported in the future so the drop-down list will be enabled.-->

   * **[!UICONTROL Optimization metric]**

      Esta opción permite a los especialistas en marketing elegir cómo se debe crear y entrenar el modelo de aprendizaje automático: en función de las ofertas mostradas, las ofertas en las que se hizo clic en el correo electrónico o las ofertas en las que se hizo clic en la web.

      >[!NOTE]
      >
      >Puede seleccionar todos los tipos de métricas si es necesario.

      Existen dos tipos de métricas de optimización:
      * **[!UICONTROL Impression]**: Los eventos de impresión actuales corresponden a todas las ofertas que se muestran.
      * **[!UICONTROL Conversion]**: Los eventos de conversión corresponden a todas las ofertas que resultan en clics a través del correo electrónico o la web.

      Todos los eventos de impresión o de conversión seleccionados se capturarán automáticamente mediante el SDK web o el SDK móvil que se haya proporcionado. Obtenga más información sobre esto en [Información general del SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es).

   * **[!UICONTROL Dataset ID]**: Para la conversión, debe proporcionar un conjunto de datos donde se recopilen los eventos seleccionándolo en la lista desplegable. Aprenda a crear este conjunto de datos en [esta sección](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >En la lista desplegable solo se muestran los conjuntos de datos creados a partir de esquemas asociados con el grupo de campos **[!UICONTROL Experience Event - Proposition Interactions]** (anteriormente conocido como mezcla).

1. Guarde y active la estrategia de clasificación.

   ![](../../assets/ai-ranking-save-activate.png)

Ahora está listo para utilizarse en una decisión para clasificar ofertas aptas para una colocación. Obtenga más información en [esta sección](../offer-activities/configure-offer-selection.md#use-ranking-strategy).<!--TBC?-->

## Crear un conjunto de datos para recopilar eventos {#create-dataset}

Debe crear un conjunto de datos donde se recopilen los eventos de conversión. Comience creando el esquema que se utilizará en el conjunto de datos:

1. En el menú **[!UICONTROL Data Management]**, seleccione **[!UICONTROL Schema]**, vaya a la pestaña **[!UICONTROL Browse]** y haga clic en **[!UICONTROL Create schema]**.

   ![](../../assets/ai-ranking-create-schema.png)

1. Seleccione **[!UICONTROL XDM ExperienceEvent]**.

   ![](../../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    Obtenga más información sobre los esquemas y grupos de campos XDM en la [documentación de información general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es).


1. En el campo **[!UICONTROL Search]**, escriba &quot;interacción de propuesta&quot; y seleccione el grupo de campos **[!UICONTROL Experience Event - Proposition Interactions]**.

   ![](../../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    El esquema que se utilizará en el conjunto de datos debe tener asociado el grupo de campos **[!UICONTROL Experience Event - Proposition Interactions]** . De lo contrario, no podrá utilizarlo en su estrategia de clasificación.

1. Haga clic en **[!UICONTROL Add field groups]**.

   ![](../../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >El grupo de campo se conocía anteriormente como mezcla.


1. Escriba un nombre y guarde el esquema.<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    Obtenga más información sobre la creación de esquemas en [Conceptos básicos de la composición de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas).

Ya está listo para crear un conjunto de datos con este esquema. Para realizar esto, siga los pasos a continuación:

1. En el menú **[!UICONTROL Data Management]**, seleccione **[!UICONTROL Datasets]**, vaya a la pestaña **[!UICONTROL Browse]** y haga clic en **[!UICONTROL Create dataset]**.

   ![](../../assets/ai-ranking-create-dataset.png)

1. Seleccione **[!UICONTROL Create dataset from schema]**.

   ![](../../assets/ai-ranking-create-dataset-from-schema.png)

1. Seleccione el esquema que acaba de crear en la lista.

   ![](../../assets/ai-ranking-dataset-select-schema.png)

1. Haga clic en **[!UICONTROL Next]**.

1. Proporcione un nombre único para el conjunto de datos en el campo **[!UICONTROL Name]** y haga clic en **[!UICONTROL Finish]**.

   ![](../../assets/ai-ranking-dataset-name.png)

El conjunto de datos ya está listo para seleccionarse para recopilar eventos de conversión al [crear una estrategia de clasificación](#create-ranking-strategy).

<!--## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision (previously known as offer activity). For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).-->

