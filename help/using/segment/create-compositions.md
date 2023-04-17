---
solution: Journey Optimizer
product: journey optimizer
title: Creación del primer flujo de trabajo de composición
description: Aprenda a crear flujos de trabajo de composición para combinar y organizar audiencias existentes.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
badge: label="Beta" type="Informative"
source-git-commit: 818c3ff2d159ec3a668c55224996b4736f950e5d
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 3%

---

# Creación del primer flujo de trabajo de composición {#create-compositions}

>[!BEGINSHADEBOX]

Lo que encontrará en esta documentación:

* [Introducción a Composición de audiencias](get-started-audience-orchestration.md)
* **[Creación del primer flujo de trabajo de composición](create-compositions.md)**
* [Trabajo con el lienzo de composición](composition-canvas.md)
* [Acceso y administración de audiencias](access-audiences.md)

>[!ENDSHADEBOX]

## Creación de un flujo de trabajo de composición {#create}

Para crear un flujo de trabajo de composición, siga estos pasos:

1. Acceda a la **[!UICONTROL Segmentos]** y seleccione **[!UICONTROL Crear audiencia]**.

1. Select **[!UICONTROL Componer audiencia]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >La variable **[!UICONTROL Generar regla]** el método de creación le permite crear una nueva definición de segmento utilizando el [Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

1. El lienzo de la composición se muestra con dos actividades predeterminadas:

   * **[!UICONTROL Audiencia]**: el punto de partida de la composición. Esta actividad le permite seleccionar una o varias audiencias como base para el flujo de trabajo.

   * **[!UICONTROL Guardar]**: el último paso de la composición. Esta actividad le permite guardar el resultado del flujo de trabajo en una audiencia nueva.
   Para obtener más información sobre cómo configurar actividades en el lienzo del flujo de trabajo de composición, consulte [Trabajo con el lienzo de composición](composition-canvas.md).

1. Abra las propiedades de composición para especificar un título y una descripción.

   Si no se define ningún título en las propiedades, la etiqueta de la composición se establece en &quot;Composición&quot; seguida de su fecha y hora de creación.

   ![](assets/audiences-properties.png)

1. Configure la composición agregando tantas actividades como sea necesario entre las variables **[!UICONTROL Audiencia]** y **[!UICONTROL Guardar]** actividades. [Aprenda a trabajar con el lienzo de composición](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Una vez que la composición esté lista, haga clic en el botón **[!UICONTROL Publicación]** para publicar la composición y guardar las audiencias resultantes en Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Puede publicar hasta 75 composiciones en un entorno limitado determinado. Si ha alcanzado este umbral, debe eliminar una composición para liberar espacio y publicar una nueva.

   Si se produce algún error durante la publicación, las alertas se mostrarán con información sobre cómo resolver el problema.

   ![](assets/audiences-alerts.png)

1. Se publica la composición. Las audiencias resultantes se guardan en Adobe Experience Platform y están listas para ser segmentadas en campañas de Journey Optimizer. [Aprenda a trabajar con campañas](../campaigns/get-started-with-campaigns.md)

## Composiciones de acceso {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publicación de la audiencia"
>abstract="Publique la composición para guardar las audiencias resultantes en Adobe Experience Platform."

Se puede acceder a todas las composiciones creadas desde la **[!UICONTROL Composiciones]** pestaña . Pueden tener varios estados:

* **[!UICONTROL Borrador]**: la composición está en curso y no se ha publicado.
* **[!UICONTROL Publicado]**: la composición se ha publicado, las audiencias resultantes se han guardado y están disponibles para su uso.
* **[!UICONTROL Archivado]**: la composición se ha archivado.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>Puede duplicar o eliminar una composición existente en cualquier momento mediante el botón de elipsis de la lista.
