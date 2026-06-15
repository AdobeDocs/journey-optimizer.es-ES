---
solution: Journey Optimizer
product: Journey Optimizer
title: Crear un conjunto de datos para recopilar eventos
description: Obtenga información sobre cómo crear un conjunto de datos para recopilar eventos
feature: Ranking, Datasets, Decisioning
role: Developer
level: Experienced
hide: true
exl-id: 96c1326f-be40-4738-8997-a67dc14872bb
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/U-4AWTYWPOzBhtT3gxE6ORtMI8jNKOZGns-0P3t7-lE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee394c77b226dd35a9c27f4a02e3b8d7a997ccbd
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 8%

---

# Crear un conjunto de datos para recopilar eventos {#create-dataset}

>[!BEGINSHADEBOX]

**En esta página:** Cree el esquema y el conjunto de datos de Experience Event necesarios para capturar interacciones de propuestas, de modo que pueda proporcionar comentarios sobre decisiones en sus modelos de clasificación de IA.

>[!ENDSHADEBOX]

Para recopilar eventos de experiencia, primero debe crear un conjunto de datos al que se envíen estos eventos.

Comience creando el esquema que se utilizará en el conjunto de datos:

1. En el menú **[!UICONTROL Administración de datos]**, seleccione **[!UICONTROL Esquema]**.

1. Haga clic en **[!UICONTROL Crear esquema]**, en la esquina superior derecha, seleccione **[!UICONTROL Evento de experiencia]** y haga clic en **Siguiente**.

   ![](../../offers/assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Obtenga más información acerca de esquemas XDM y grupos de campos en la [documentación de información general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

1. Escriba un nombre y una descripción para el esquema y haga clic en **Finalizar**.
   ![](../../offers/assets/ai-ranking-xdm-event-2.png)

1. En la sección **[!UICONTROL Grupos de campos]** de la izquierda, seleccione **[!UICONTROL Agregar]**.

   ![](../../offers/assets/ai-ranking-fields-groups.png)

1. En el campo **[!UICONTROL Buscar]**, escriba &quot;interacción de propuesta&quot;.

1. Seleccione el grupo de campos **[!UICONTROL Evento de experiencia - Interacciones de propuesta]** y haga clic en **[!UICONTROL Agregar grupos de campos]**.

   ![](../../offers/assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >El esquema que se usará en su conjunto de datos debe tener asociado el grupo de campos **[!UICONTROL Evento de experiencia - Interacciones de propuesta]**. De lo contrario, no podrá utilizarlo en su modelo de IA.

1. Guarde el esquema.

>[!NOTE]
>
>Obtenga más información acerca de la creación de esquemas en [Aspectos básicos de la composición de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#understanding-schemas){target="_blank"}.

Ya está listo para crear un conjunto de datos con este esquema. Para realizar esto, siga los pasos a continuación:

1. En el menú **[!UICONTROL Administración de datos]**, seleccione **[!UICONTROL Conjuntos de datos]** y vaya a la pestaña **[!UICONTROL Examinar]**.

1. Haga clic en **[!UICONTROL Crear conjunto de datos]** y seleccione **[!UICONTROL Crear conjunto de datos a partir del esquema]**.

   ![](../../offers/assets/ai-ranking-create-dataset-from-schema.png)

1. Seleccione el esquema que acaba de crear en la lista y haga clic en **[!UICONTROL Siguiente]**.

1. Proporcione un nombre único para el conjunto de datos en el campo **[!UICONTROL Nombre]** y haga clic en **[!UICONTROL Finalizar]**.

   ![](../../offers/assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Ahora se puede seleccionar este conjunto de datos para recopilar datos de evento al crear un [modelo de IA](../ranking/create-ai-models.md).
