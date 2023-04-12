---
title: Creación de experiencias web
description: Obtenga información sobre cómo crear una página web y editar su contenido en Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
badge: label="Beta" type="Informative"
source-git-commit: c21c0386be33eea6f7053fb891ebad3d9a1154c9
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 8%

---

# Creación de experiencias web {#create-web}

>[!BEGINSHADEBOX]

Lo que encontrará en esta documentación:

* [Introducción al canal web](get-started-web.md)
* **[Creación de experiencias web](create-web.md)**
* [Creación de páginas web](author-web.md)
* [Extensión Ayuda de edición visual](visual-editing-helper.md)
* [Creación de informes web](web-report.md)

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] le permite personalizar la experiencia web que entrega a sus clientes mediante campañas web entrantes.

>[!CAUTION]
>
>Actualmente en [!DNL Journey Optimizer] solo puede crear experiencias web mediante **campañas**.

## Requisitos previos {#prerequesites}

Para poder acceder y crear páginas web en la variable [!DNL Journey Optimizer] interfaz de usuario de , siga los requisitos previos a continuación:

* Para agregar modificaciones al sitio web, debe implementar la variable [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"} en su sitio web.

* Para acceder a la [!DNL Journey Optimizer] diseñador web, debe descargar el [Ayuda de edición visual de Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extensión del explorador en Chrome. [Más información](visual-editing-helper.md)

>[!CAUTION]
>
>Google Chrome es actualmente el único explorador que admite la creación de páginas web en [!DNL Journey Optimizer].

Para que la experiencia web se entregue correctamente, se debe definir la siguiente configuración:

* En el [Recopilación de datos de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=es){target="_blank"}, asegúrese de que tiene un conjunto de datos definido como en la sección **[!UICONTROL Adobe Experience Platform]** tiene ambos **[!UICONTROL Segmentación de Edge]** y **[!UICONTROL Adobe Journey Optimizer]** opciones activadas.

   Esto garantiza que Adobe Experience Platform Edge gestione correctamente los eventos de entrada de Journey Optimizer. [Más información](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=es){target="_blank"}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >La variable **[!UICONTROL Adobe Journey Optimizer]** solo se puede activar cuando **[!UICONTROL Segmentación de Edge]** ya está activada.

* En [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

   Esta directiva de combinación la utiliza [!DNL Journey Optimizer] canales entrantes para activar y publicar correctamente campañas entrantes en el perímetro. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html){target="_blank"}

   ![](assets/web-aep-merge-policy.png)

## Creación de una campaña web {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Definir una superficie web"
>abstract="Una superficie web puede coincidir con una dirección URL de una sola página o con varias páginas, lo que le permite enviar modificaciones de contenido en una o varias páginas web."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="Crear páginas que coincidan con una regla"
>abstract="Una regla de coincidencia de páginas permite dirigirse a varias direcciones URL que coincidan con la misma regla; por ejemplo, si desea aplicar los cambios a un banner a través de todo un sitio web o agregar una imagen superior que se muestre en todas las páginas de producto de un sitio web."

Para comenzar a crear la experiencia web a través de una campaña, siga los pasos a continuación.

1. Creación de una campaña. [Más información](../campaigns/create-campaign.md)

1. Seleccione el **[!UICONTROL Web]** acción.

   ![](assets/web-create-campaign.png)

1. Defina una superficie web.

   >[!NOTE]
   >
   >Una superficie web es una propiedad web identificada por una dirección URL donde se enviará el contenido. Puede coincidir con una dirección URL de una sola página o con varias páginas, lo que le permite enviar modificaciones en una o varias páginas web.

   Puede especificar una **[!UICONTROL Dirección URL de la página]** si desea aplicar los cambios solo a una página única.

   ![](assets/web-campaign-surface.png)

1. O puede crear un **[!UICONTROL Páginas que coinciden con la regla]** para dirigirse a varias direcciones URL que coincidan con la misma regla; por ejemplo, si desea aplicar los cambios a un banner a pantalla completa en todo un sitio web o agregar una imagen superior que se muestre en todas las páginas de producto de un sitio web.

   Para ello, seleccione **[!UICONTROL Páginas que coinciden con la regla]** y haga clic en **[!UICONTROL Crear regla]**.

   ![](assets/web-campaign-matching-rule.png)

1. Defina sus criterios para la variable **[!UICONTROL Dominio]** y **[!UICONTROL Página]** campos.

   Por ejemplo, si desea editar los elementos que se muestran en todas las páginas de producto femeninas de su sitio web de Luma, seleccione **[!UICONTROL Dominio]** > **[!UICONTROL Comienza con]** > `luma` y **[!UICONTROL Página]** > **[!UICONTROL Contiene]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Guarde los cambios. La regla se muestra en la sección **[!UICONTROL Crear campaña]** en el Navegador.

   ![](assets/web-pages-matching-rule-example.png)

1. Una vez definida la superficie web, seleccione **[!UICONTROL Crear]**. Ahora puede configurar las propiedades y la configuración de la campaña.

## Configuración de la campaña web {#configure-web-campaign}

1. En el **[!UICONTROL Propiedades]** , puede editar el nombre de la campaña y agregar una descripción si es necesario.

   ![](assets/web-campaign-properties.png)

1. Para asignar etiquetas de uso de datos principales o personalizadas a la campaña web, seleccione la opción **[!UICONTROL Administrar acceso]** en la parte superior de la pantalla. [Más información sobre Control de acceso a nivel de objeto (OLAC)](../administration/object-based-access.md)

1. Puede seleccionar **[!UICONTROL Experimento de contenido]** para probar los tratamientos de contenido con partes de la audiencia, a fin de determinar qué tratamiento ofrece el mejor rendimiento con respecto a una métrica específica. [Más información](../campaigns/content-experiment.md)

   >[!AVAILABILITY]
   >
   >La variable **Experimento de contenido** Actualmente, esta función solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

1. En el **[!UICONTROL Acción]** de la campaña, seleccione **[!UICONTROL Editar contenido]** para comenzar a crear la campaña web. [Más información](author-web.md)

   ![](assets/web-edit-content.png)

1. En el **[!UICONTROL Audiencia]** , defina quién podrá ver la campaña web. De forma predeterminada, la campaña web será visible para todos los visitantes.

   ![](assets/web-campaign-audience.png)

   También puede seleccionar una audiencia específica. Utilice la variable **[!UICONTROL Seleccionar la audiencia]** para mostrar la lista de segmentos de Adobe Experience Platform disponibles. [Más información sobre los segmentos](../segment/about-segments.md)

   >[!NOTE]
   >
   >Para las campañas activadas por API, la audiencia debe configurarse mediante una llamada a la API. [Más información](../campaigns/api-triggered-campaigns.md)

   ![](assets/web-campaign-select-audience.png)

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado. [Más información sobre áreas de nombres](../event/about-creating.md#select-the-namespace)

1. Defina un **[!UICONTROL Programación]** para su campaña web. [Más información](../campaigns/create-campaign.md#schedule)

   ![](assets/web-campaign-schedule.png)

   De forma predeterminada, se inicia cuando se activa manualmente y finaliza cuando se detiene manualmente, pero también puede definir fechas y horas específicas para que las modificaciones sean visibles.

   ![](assets/web-campaign-schedule-start.png)

## Activación de la campaña web {#activate-web-campaign}

Una vez definido el [configuración de campañas web](#configure-web-campaign) y editó el contenido según sus preferencias utilizando la variable [diseñador web](author-web.md), puede revisar y activar su campaña web. Complete los siguientes pasos.

>[!NOTE]
>
>También puede obtener una vista previa del contenido de la campaña web antes de activarlo. [Más información](author-web.md#test-web-campaign)

1. En la campaña web, seleccione **[!UICONTROL Revisar para activar]**.

   ![](assets/web-campaign-review.png)

1. Revise y edite si es necesario el contenido, las propiedades, la superficie, la audiencia y la programación.

1. Select **[!UICONTROL Activar]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Después de hacer clic en **[!UICONTROL Activar]**, los cambios de las campañas web pueden tardar hasta 15 minutos en estar disponibles en el sitio web.

La campaña web toma la variable **[!UICONTROL Activo]** y ahora es visible para la audiencia seleccionada. Cada destinatario de la campaña puede ver las modificaciones que agregó al sitio web mediante la [!DNL Journey Optimizer] diseñador web.

>[!NOTE]
>
>Si ha definido una programación para su campaña web, tiene la variable **[!UICONTROL Programado]** hasta que se alcancen la fecha y hora de inicio.
>
>Si activa una campaña web que afecte a las mismas páginas que otra campaña que ya está activa, todos los cambios se aplicarán a las páginas web.

Obtenga más información sobre la activación de campañas en [esta sección](../campaigns/review-activate-campaign.md).

## Detener una campaña web {#stop-web-campaign}

Cuando una campaña web está activa, puede detenerla para evitar que la audiencia vea las modificaciones. Complete los siguientes pasos.

1. Seleccione una campaña activa de la lista.

1. En el menú superior, seleccione **[!UICONTROL Detener campaña]**.

   ![](assets/web-campaign-stop.png)

1. Las modificaciones que haya agregado ya no serán visibles para la audiencia que haya definido.

>[!NOTE]
>
>Una vez detenida una campaña web, no puede editarla ni activarla de nuevo. Solo puede duplicarla y activar la campaña duplicada.
