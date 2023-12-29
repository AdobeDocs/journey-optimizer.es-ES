---
solution: Journey Optimizer
product: journey optimizer
title: Creación del primer flujo de trabajo de composición
description: Aprenda a crear flujos de trabajo de composición para combinar y organizar audiencias existentes.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 2344d53a331cb883a81a051ce1e06e8c42824cb7
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 16%

---

# Creación del primer flujo de trabajo de composición {#create-compositions}

>[!BEGINSHADEBOX]

Esta documentación proporciona información detallada sobre cómo trabajar con la composición de públicos en Adobe Journey Optimizer. Si no utiliza Adobe Journey Optimizer, [haga clic aquí](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=es){target="_blank"}.

>[!ENDSHADEBOX]

## Crear un flujo de trabajo de composición {#create}

Para crear un flujo de trabajo de maquetación, siga estos pasos:

1. Acceda a la **[!UICONTROL Audiencias]** y seleccione **[!UICONTROL Crear audiencia]**.

1. Seleccionar **[!UICONTROL Componer audiencia]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >El **[!UICONTROL Generar regla]** método de creación le permite crear una nueva definición de segmento utilizando [Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=es).

1. El lienzo de composición se muestra con dos actividades predeterminadas:

   * **[!UICONTROL Audiencia]**: el punto de partida de la composición. Esta actividad le permite seleccionar una o varias audiencias como base para el flujo de trabajo,

   * **[!UICONTROL Guardar]**: el último paso de la composición. Esta actividad le permite guardar el resultado del flujo de trabajo en una nueva audiencia.

   Para obtener más información sobre cómo configurar actividades en el lienzo del flujo de trabajo de composición, consulte [Trabajo con el lienzo de composición](composition-canvas.md).

1. Abra las propiedades de la composición para especificar un título y una descripción.

   Si no se define ningún título en las propiedades, la etiqueta de la composición se define en &quot;Composición&quot; seguida de su fecha y hora de creación.

   ![](assets/audiences-properties.png)

1. Configure la composición añadiendo tantas actividades como sea necesario entre las etiquetas **[!UICONTROL Audiencia]** y **[!UICONTROL Guardar]** actividades. [Aprenda a trabajar con el lienzo de composición](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Una vez que la composición esté lista, haga clic en **[!UICONTROL Publish]** para publicar la maquetación y guardar las audiencias resultantes en Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Puede publicar hasta 10 composiciones en una zona protegida determinada. Si ha alcanzado este umbral, debe eliminar una composición para liberar espacio y publicar una nueva.

   Si se produce algún error durante la publicación, las alertas se mostrarán con información sobre cómo resolver el problema.

   ![](assets/audiences-alerts.png)

1. La composición se publica. Las audiencias resultantes se guardan en Adobe Experience Platform y están listas para segmentarse en campañas de Journey Optimizer. [Descubra cómo trabajar con campañas](../campaigns/get-started-with-campaigns.md)

## Acceso a composiciones {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publicar la audiencia"
>abstract="Publique la composición para guardar las audiencias resultantes en Adobe Experience Platform."

Se puede acceder a todas las composiciones creadas desde el **[!UICONTROL Composiciones]** pestaña. Puede duplicar o eliminar una composición existente en cualquier momento mediante el botón de puntos suspensivos de la lista.

Las composiciones pueden tener varios estados:

* **[!UICONTROL Borrador]**: la composición está en curso y no se ha publicado.
* **[!UICONTROL Publicado]**: la composición se ha publicado, las audiencias resultantes se han guardado y están disponibles para su uso.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>La composición de audiencia no está integrada actualmente con la capacidad de restablecimiento de la zona protegida. Antes de iniciar el restablecimiento de una zona protegida, debe eliminar las composiciones manualmente para asegurarse de que los datos de audiencia asociados se limpien correctamente. Encontrará información detallada en Adobe Experience Platform [Documentación de zona protegida](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html#delete-audience-compositions)
