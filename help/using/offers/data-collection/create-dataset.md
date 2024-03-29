---
product: experience platform
solution: Experience Platform
title: Crear un conjunto de datos para recopilar eventos
description: Obtenga información sobre cómo crear un conjunto de datos para recopilar eventos
feature: Ranking, Decision Management, Datasets
role: Data Engineer, Developer
level: Experienced
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 7%

---

# Crear un conjunto de datos para recopilar eventos {#create-dataset}

Para recopilar eventos de experiencia, primero debe crear un conjunto de datos al que se envíen estos eventos.

Comience creando el esquema que se utilizará en el conjunto de datos:

1. Desde el **[!UICONTROL Administración de datos]** menú, seleccione **[!UICONTROL Esquema]**.

1. Clic **[!UICONTROL Crear esquema]**, en la parte superior derecha, seleccione **[!UICONTROL Evento de experiencia]** y haga clic en **Siguiente**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Obtenga más información sobre esquemas XDM y grupos de campos en la [Documentación general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

1. Introduzca un nombre y una descripción para el esquema y haga clic en **Finalizar**.
   ![](../assets/ai-ranking-xdm-event-2.png)

1. Desde el **[!UICONTROL Grupos de campos]** en la parte izquierda, seleccione **[!UICONTROL Añadir]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. En el **[!UICONTROL Buscar]** , escriba &quot;interacción de propuesta&quot;.

1. Seleccione el **[!UICONTROL Evento de experiencia: interacciones de propuesta]** y haga clic en **[!UICONTROL Adición de grupos de campos]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >El esquema que se utilizará en el conjunto de datos debe tener el **[!UICONTROL Evento de experiencia: interacciones de propuesta]** grupo de campos asociado a él. De lo contrario, no podrá utilizarlo en su modelo de IA.

1. Guarde el esquema.

>[!NOTE]
>
>Obtenga más información sobre la creación de esquemas en [Conceptos básicos de composición de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#understanding-schemas){target="_blank"}.

Ya está listo para crear un conjunto de datos con este esquema. Para realizar esto, siga los pasos a continuación:

1. Desde el **[!UICONTROL Administración de datos]** menú, seleccione **[!UICONTROL Conjuntos de datos]** y vaya a la **[!UICONTROL Examinar]** pestaña.

1. Clic **[!UICONTROL Crear conjunto de datos]** y seleccione **[!UICONTROL Crear conjunto de datos a partir de esquema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Seleccione el esquema que acaba de crear en la lista y haga clic en **[!UICONTROL Siguiente]**.

1. Proporcione un nombre único para el conjunto de datos en la **[!UICONTROL Nombre]** y haga clic en **[!UICONTROL Finalizar]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Ahora se puede seleccionar este conjunto de datos para recopilar datos de evento cuando [creación de un modelo de IA](../ranking/create-ranking-strategies.md).
