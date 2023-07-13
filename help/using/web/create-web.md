---
title: Creación de experiencias web
description: Obtenga información sobre cómo crear una página web y editar su contenido en Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 21%

---

# Creación de experiencias web {#create-web}

[!DNL Journey Optimizer] permite personalizar la experiencia web que ofrece a sus clientes a través de campañas web entrantes.

>[!CAUTION]
>
>Actualmente en [!DNL Journey Optimizer] solo puede crear experiencias web mediante **campañas**.

[Obtenga información sobre cómo crear una campaña web en este vídeo](#video)

## Creación de una campaña web {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Definir una superficie web"
>abstract="Una superficie web puede coincidir con una dirección URL de una sola página o varias páginas, lo que permite enviar modificaciones de contenido en una o varias páginas web."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="Creación de páginas que coincidan con una regla"
>abstract="Una regla de coincidencia de páginas permite dirigirse a varias direcciones URL que se ajusten a la misma regla; por ejemplo, si desea aplicar los cambios a un banner principal en todo un sitio web o agregar una imagen superior que se muestre en todas las páginas de producto de un sitio web."

Para empezar a crear una experiencia web a través de una campaña, siga los pasos a continuación.

>[!NOTE]
>
>Si es la primera vez que crea una experiencia web, asegúrese de seguir los requisitos previos descritos en [esta sección](web-prerequisites.md).

1. Creación de una campaña. [Más información](../campaigns/create-campaign.md)

1. Seleccione el **[!UICONTROL Web]** acción.

1. Definir una superficie web.

   >[!NOTE]
   >
   >Una superficie web es una propiedad web identificada por una dirección URL a la que se envía el contenido. Puede coincidir con una dirección URL de una sola página o varias páginas, lo que le permite enviar modificaciones en una o varias páginas web.

   Puede introducir una **[!UICONTROL URL de página]** si desea aplicar los cambios solo a una página.

   ![](assets/web-campaign-surface.png)

1. O puede crear una **[!UICONTROL Regla de coincidencia de páginas]** para dirigirse a varias direcciones URL que coincidan con la misma regla; por ejemplo, si desea aplicar los cambios a un banner a pantalla completa en todo un sitio web o agregar una imagen superior que se muestre en todas las páginas de producto de un sitio web.

   Para ello, seleccione **[!UICONTROL Regla de coincidencia de páginas]** y haga clic en **[!UICONTROL Crear regla]**.

   ![](assets/web-campaign-matching-rule.png)

1. Defina los criterios de **[!UICONTROL Dominio]** y **[!UICONTROL Página]** campos.

   Por ejemplo, si desea editar elementos que se muestran en todas las páginas de productos de sexo femenino del sitio web de Luma, seleccione **[!UICONTROL Dominio]** > **[!UICONTROL Comienza por]** > `luma` y **[!UICONTROL Página]** > **[!UICONTROL Contains]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Guarde los cambios. La regla se muestra en la **[!UICONTROL Crear campaña]** pantalla.

   ![](assets/web-pages-matching-rule-example.png)

1. Una vez definida la superficie web, seleccione **[!UICONTROL Crear]**.

1. Complete los pasos para crear una campaña web, como las propiedades de la campaña, [audiencia](../audience/about-audiences.md), y [programación](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

Para obtener más información sobre cómo configurar una campaña, consulte [esta página](../campaigns/get-started-with-campaigns.md).

## Activación de la campaña web {#activate-web-campaign}

Una vez que haya definido su [configuración de campañas web](#configure-web-campaign) y ha editado el contenido como ha deseado utilizando la variable [diseñador web](author-web.md), puede revisar y activar su campaña web. Complete los siguientes pasos.

>[!NOTE]
>
>También puede previsualizar el contenido de la campaña web antes de activarlo. [Más información](author-web.md#test-web-campaign)

1. En la campaña web, seleccione **[!UICONTROL Revisar para activar]**.

1. Compruebe y edite si es necesario el contenido, las propiedades, la superficie, la audiencia y la programación.

1. Seleccionar **[!UICONTROL Activar]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Después de hacer clic en **[!UICONTROL Activar]**, los cambios en las campañas web pueden tardar hasta 15 minutos en estar disponibles en el sitio web.

La campaña web toma la **[!UICONTROL Activo]** estado y ahora son visibles para la audiencia seleccionada. Cada destinatario de la campaña puede ver las modificaciones agregadas al sitio web mediante el [!DNL Journey Optimizer] diseñador web.

>[!NOTE]
>
>Si ha definido una programación para la campaña web, tiene el **[!UICONTROL Programado]** estado hasta que se alcancen la fecha y la hora de inicio.
>
>Si activa una campaña web que afecte a las mismas páginas que otra campaña que ya está activa, todos los cambios se aplicarán a las páginas web.

Obtenga más información sobre la activación de campañas en [esta sección](../campaigns/review-activate-campaign.md).

## Detener una campaña web {#stop-web-campaign}

Cuando una campaña web está activa, puede detenerla para evitar que la audiencia vea las modificaciones. Complete los siguientes pasos.

1. Seleccione una campaña en directo en la lista.

1. En el menú superior, seleccione **[!UICONTROL Detener campaña]**.

   ![](assets/web-campaign-stop.png)

1. Las modificaciones que ha añadido ya no serán visibles para la audiencia que ha definido.

>[!NOTE]
>
>Una vez detenida una campaña web, no se puede editar ni activar de nuevo. Solo puede duplicarla y activar la campaña duplicada.

## Vídeo explicativo{#video}

El siguiente vídeo muestra cómo crear una campaña web, configurar sus propiedades, revisarla y publicarla.

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)