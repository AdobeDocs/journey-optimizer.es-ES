---
solution: Journey Optimizer
product: journey optimizer
title: Creación de flujos de trabajo de composición
description: Aprenda a crear flujos de trabajo de composición para combinar y organizar audiencias existentes.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Creación de flujos de trabajo de composición {#create-compositions}

Los flujos de trabajo de composición le permiten combinar y organizar audiencias existentes para crear nuevas audiencias.

## Creación de un flujo de trabajo de composición {#create}

1. Acceda a la **[!UICONTROL Segments]** y seleccione **[!UICONTROL Create Audience]**.

1. Select **[!UICONTROL Compose Audience]**.

   >[!NOTE]
   >
   >La variable **[!UICONTROL Build rule]** el método de creación le permite crear una nueva definición de segmento utilizando el [Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

   ![](assets/audiences-create.png)

1. El lienzo de la composición se muestra con dos actividades predeterminadas:

   * **[!UICONTROL Audience]**: el punto de partida de la composición. Esta actividad le permite seleccionar una o varias audiencias como base para el flujo de trabajo.

   * **[!UICONTROL Save]**: el último paso de la composición. Esta actividad le permite guardar el resultado del flujo de trabajo en una audiencia nueva.
   Para obtener más información sobre cómo configurar actividades en el lienzo del flujo de trabajo de composición, consulte [Trabajo con el lienzo de composición](composition-canvas.md).

1. Abra las propiedades de composición para especificar un título y una descripción.

   Si no se define ningún título en las propiedades, la etiqueta de composición será la que comience **[!UICONTROL Audience]** actividad.

   ![](assets/audiences-properties.png)

1. Configure la composición agregando tantas actividades como sea necesario entre las variables **[!UICONTROL Audience]** y **[!UICONTROL Save]** actividades. [Aprenda a trabajar con el lienzo de composición](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Una vez que la composición esté lista, haga clic en el botón **[!UICONTROL Publish]** para publicar la composición y guardar las audiencias resultantes en Adobe Experience Platform.

   Si se produce algún error durante la publicación, las alertas se mostrarán con información sobre cómo resolver el problema.

   ![](assets/audiences-alerts.png)

1. Se publica la composición. Las audiencias resultantes se guardan en Adobe Experience Platform y están listas para ser segmentadas en las campañas de Journey Optimizer. [Aprenda a trabajar con campañas](../campaigns/get-started-with-campaigns.md)

## Composiciones de acceso {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publicación de la audiencia"
>abstract="Publique la composición para guardar las audiencias resultantes en Adobe Experience Platform."

Se puede acceder a todas las composiciones creadas desde la **[!UICONTROL Compositions]** pestaña . Pueden tener varios estados:

* **[!UICONTROL Draft]**: la composición está en curso y no se ha publicado.
* **[!UICONTROL Published]**: la composición se ha publicado, las audiencias resultantes se han guardado y están disponibles para su uso.
* **[!UICONTROL Archived]**: la composición se ha archivado.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>Puede duplicar o eliminar una composición existente en cualquier momento mediante el botón de elipse de la lista.

Más información:

* [Introducción a la composición de audiencias](get-started-audience-orchestration.md)
* [Trabajo con el lienzo de composición](composition-canvas.md)
* [Acceso y administración de audiencias](access-audiences.md)
