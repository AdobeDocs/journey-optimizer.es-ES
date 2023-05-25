---
product: experience platform
solution: Experience Platform
title: Crear un conjunto de datos para recopilar eventos
description: Obtenga información sobre cómo crear un conjunto de datos para recopilar eventos
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 59499dec7d15dd4565c7910d7b454d82243ff011
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 15%

---

# Crear un conjunto de datos para recopilar eventos {#create-dataset}

Para recopilar eventos de experiencia, primero debe crear un conjunto de datos al que se envíen estos eventos.

Comience creando el esquema que se utilizará en el conjunto de datos:

1. Desde el **[!UICONTROL Administración de datos]** menú, seleccione **[!UICONTROL Esquema]** y vaya a la **[!UICONTROL Examinar]** pestaña.

1. Clic **[!UICONTROL Crear esquema]** y elija **[!UICONTROL ExperienceEvent de XDM]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Obtenga más información sobre los esquemas XDM y los grupos de campos en la [Documentación de información general del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

1. Desde el **[!UICONTROL Grupos de campos]** en la parte izquierda, seleccione **[!UICONTROL Añadir]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. En el **[!UICONTROL Buscar]** , escriba &quot;interacción de propuesta&quot;.

1. Seleccione el **[!UICONTROL Evento de experiencia: interacciones de propuesta]** y haga clic en **[!UICONTROL Adición de grupos de campos]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >El esquema que se utilizará en el conjunto de datos debe tener el **[!UICONTROL Evento de experiencia: interacciones de propuesta]** grupo de campos asociado a él. De lo contrario, no podrá utilizarlo en su estrategia de clasificación.

1. Escriba un nombre y guarde el esquema.

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
>Ahora se puede seleccionar este conjunto de datos para recopilar datos de evento cuando [creación de una estrategia de clasificación](#create-ranking-strategy).
