---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Crear un conjunto de datos para recopilar eventos
description: Obtenga información sobre cómo crear un conjunto de datos para recopilar eventos
badge: label="Heredado" type="Informative"
feature: Ranking, Decision Management, Datasets
role: Developer
level: Experienced
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 13%

---

# Crear un conjunto de datos para recopilar eventos {#create-dataset}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../experience-decisioning/gs-experience-decisioning.md)

Para recopilar eventos de experiencia, primero debe crear un conjunto de datos al que se envíen estos eventos.

Comience creando el esquema que se utilizará en el conjunto de datos:

1. En el menú **[!UICONTROL Administración de datos]**, seleccione **[!UICONTROL Esquema]**.

1. Haga clic en **[!UICONTROL Crear esquema]**, en la esquina superior derecha, seleccione **[!UICONTROL Evento de experiencia]** y haga clic en **Siguiente**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Obtenga más información acerca de esquemas XDM y grupos de campos en la [documentación de información general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

1. Escriba un nombre y una descripción para el esquema y haga clic en **Finalizar**.
   ![](../assets/ai-ranking-xdm-event-2.png)

1. En la sección **[!UICONTROL Grupos de campos]** de la izquierda, seleccione **[!UICONTROL Agregar]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. En el campo **[!UICONTROL Buscar]**, escriba &quot;interacción de propuesta&quot;.

1. Seleccione el grupo de campos **[!UICONTROL Evento de experiencia - Interacciones de propuesta]** y haga clic en **[!UICONTROL Agregar grupos de campos]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >El esquema que se usará en su conjunto de datos debe tener asociado el grupo de campos **[!UICONTROL Evento de experiencia - Interacciones de propuesta]**. De lo contrario, no podrá utilizarlo en su modelo de IA.

1. Guarde el esquema.

>[!NOTE]
>
>Obtenga más información acerca de la creación de esquemas en [Aspectos básicos de la composición de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=es#understanding-schemas){target="_blank"}.

ya está listo para crear un conjunto de datos con este esquema. Para realizar esto, siga los pasos a continuación:

1. En el menú **[!UICONTROL Administración de datos]**, seleccione **[!UICONTROL Conjuntos de datos]** y vaya a la pestaña **[!UICONTROL Examinar]**.

1. Haga clic en **[!UICONTROL Crear conjunto de datos]** y seleccione **[!UICONTROL Crear conjunto de datos a partir del esquema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Seleccione el esquema que acaba de crear en la lista y haga clic en **[!UICONTROL Siguiente]**.

1. Proporcione un nombre único para el conjunto de datos en el campo **[!UICONTROL Nombre]** y haga clic en **[!UICONTROL Finalizar]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Ahora se puede seleccionar este conjunto de datos para recopilar datos de evento al [crear un modelo de IA](../ranking/create-ranking-strategies.md).
