---
product: experience platform
solution: Experience Platform
title: Crear un conjunto de datos para recopilar eventos
description: Obtenga información sobre cómo crear un conjunto de datos para recopilar eventos
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 15%

---

# Crear un conjunto de datos para recopilar eventos {#create-dataset}

Antes de crear un modelo de IA, debe crear un conjunto de datos donde se recopilen los eventos de conversión. Comience creando el esquema que se utilizará en el conjunto de datos:

1. En el **[!UICONTROL Gestión de datos]** seleccione **[!UICONTROL Esquema]**, vaya a la **[!UICONTROL Examinar]** y haga clic en **[!UICONTROL Crear esquema]**.

   ![](../assets/ai-ranking-create-schema.png)

1. Choose **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Obtenga más información sobre los esquemas XDM y los grupos de campos en la [Documentación de información general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

1. En el **[!UICONTROL Grupos de campo]** a la izquierda, seleccione **[!UICONTROL Agregar]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. En el **[!UICONTROL Buscar]** , escriba &quot;interacción de propuesta&quot; y seleccione la **[!UICONTROL Evento de experiencia: interacciones de propuesta]** grupo de campos.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >El esquema que se utilizará en el conjunto de datos debe tener la variable **[!UICONTROL Evento de experiencia: interacciones de propuesta]** grupo de campos asociado a él. De lo contrario, no podrá utilizarlo en su estrategia de clasificación.

1. Haga clic en **[!UICONTROL Agregar grupos de campos]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >El grupo de campo se conocía anteriormente como mezcla.

1. Escriba un nombre y guarde el esquema.

>[!NOTE]
>
>Obtenga más información sobre la creación de esquemas en [Aspectos básicos de la composición del esquema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target="_blank"}.

Ya está listo para crear un conjunto de datos con este esquema. Para realizar esto, siga los pasos a continuación:

1. En el **[!UICONTROL Gestión de datos]** seleccione **[!UICONTROL Conjuntos de datos]**, vaya a la **[!UICONTROL Examinar]** y haga clic en **[!UICONTROL Crear conjunto de datos]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. Select **[!UICONTROL Crear conjunto de datos a partir del esquema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Seleccione el esquema que acaba de crear en la lista.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. Haga clic en **[!UICONTROL Siguiente]**.

1. Proporcione un nombre único para el conjunto de datos en la variable **[!UICONTROL Nombre]** y haga clic en **[!UICONTROL Finalizar]**.

   ![](../assets/ai-ranking-dataset-name.png)

El conjunto de datos ya está listo para seleccionarse para recopilar datos de evento cuando [creación de una estrategia de clasificación](#create-ranking-strategy).
