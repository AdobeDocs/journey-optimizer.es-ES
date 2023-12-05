---
title: Creación de experiencias web
description: Obtenga información sobre cómo crear una página web y editar su contenido en Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 17%

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
>title="Creación de regla de coincidencia de páginas"
>abstract="Una regla de coincidencia de páginas permite dirigirse a varias direcciones URL que se ajusten a la misma regla; por ejemplo, si desea aplicar los cambios a un banner principal en todo un sitio web o agregar una imagen superior que se muestre en todas las páginas de producto de un sitio web."

Para empezar a crear una experiencia web a través de una campaña, siga los pasos a continuación.

>[!NOTE]
>
>Si es la primera vez que crea una experiencia web, asegúrese de seguir los requisitos previos descritos en [esta sección](web-prerequisites.md).

1. Cree una campaña. [Más información](../campaigns/create-campaign.md)

1. Seleccione el **[!UICONTROL Web]** acción.

1. Defina una superficie web.

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

## Prueba de la campaña web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Previsualizar la experiencia web"
>abstract="Obtenga una simulación del aspecto que tendrá su experiencia web."

Una vez que [ha creado su experiencia web](edit-web-content.md) con el diseñador web, puede utilizar perfiles de prueba para obtener una vista previa de las páginas web modificadas. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este mediante los datos del perfil de prueba.

Para ello, haga clic en **[!UICONTROL Simular contenido]** desde la pantalla editar contenido de la campaña web o el diseñador web, añada un perfil de prueba para comprobar la página web con los datos del perfil de prueba.

![](assets/web-designer-preview.png)

También puede abrirlo en el explorador predeterminado o copiar la dirección URL de prueba para pegarla en cualquier explorador. Esto le permite compartir el vínculo con su equipo y las partes interesadas, que pueden obtener una vista previa de la nueva experiencia web en cualquier explorador antes de que la campaña se ponga en marcha.

>[!NOTE]
>
>Al copiar la dirección URL de prueba, el contenido mostrado es el personalizado para el perfil de prueba utilizado cuando se generó la simulación de contenido en [!DNL Journey Optimizer].

Encontrará información detallada sobre cómo seleccionar perfiles de prueba y previsualizar el contenido en el [Gestión de contenido](../content-management/preview-test.md) sección.

## Activación de la campaña web {#activate-web-campaign}

Una vez que haya definido su [configuración de campañas web](#configure-web-campaign) y ha editado el contenido como ha deseado utilizando la variable [diseñador web](edit-web-content.md#work-with-web-designer), puede revisar y activar su campaña web. Siga los pasos a continuación.

<!--
>[!NOTE]
>
>You can also preview your web campaign content before activating it. [Learn more](#test-web-campaign)-->

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

Cuando una campaña web está activa, puede detenerla para evitar que la audiencia vea las modificaciones. Siga los pasos a continuación.

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