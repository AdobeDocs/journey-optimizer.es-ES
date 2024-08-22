---
title: Creación de experiencias web
description: Obtenga información sobre cómo crear una página web y editar su contenido en Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 15%

---

# Creación de experiencias web {#create-web}

[!DNL Journey Optimizer] le permite personalizar la experiencia web que entrega a sus clientes a través de campañas web entrantes.

>[!CAUTION]
>
>Actualmente en [!DNL Journey Optimizer] solo puede crear experiencias web mediante **campañas**.

[Obtenga información sobre cómo crear una campaña web en este vídeo](#video)

## Creación de una campaña web {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="Definir una configuración web"
>abstract="Una configuración web puede coincidir con una dirección URL de una sola página o con varias páginas, lo que permite enviar modificaciones de contenido a través de una o varias páginas web."

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="Creación de regla de coincidencia de páginas"
>abstract="Una regla de coincidencia de páginas permite dirigirse a varias direcciones URL que se ajusten a la misma regla; por ejemplo, si desea aplicar los cambios a un banner principal en todo un sitio web o agregar una imagen superior que se muestre en todas las páginas de producto de un sitio web."

Para empezar a crear una experiencia web a través de una campaña, siga los pasos a continuación.

>[!NOTE]
>
>Si es la primera vez que crea una experiencia web, asegúrese de seguir los requisitos previos descritos en [esta sección](web-prerequisites.md).

1. Acceda al menú **[!UICONTROL Campañas]** y haga clic en **[!UICONTROL Crear campaña]**.[Más información](../campaigns/create-campaign.md)


1. Seleccione el tipo de campaña que desea ejecutar

   * **Programado - Marketing**: ejecute la campaña inmediatamente o en una fecha especificada. Las campañas programadas están destinadas a enviar mensajes de marketing. Se configuran y ejecutan desde la interfaz de usuario de.

   * **Activado por API - Marketing/Transaccional**: ejecute la campaña mediante una llamada de API. Las campañas activadas por API están destinadas a enviar mensajes de marketing o transaccionales, es decir, mensajes enviados después de una acción realizada por un individuo: restablecimiento de contraseña, compra en el carro de compras, etc.

1. Complete los pasos para crear una campaña web, como las propiedades de la campaña, [audiencia](../audience/about-audiences.md) y [programación](../campaigns/create-campaign.md#schedule).

1. Seleccione la acción **[!UICONTROL Web]**.

1. Seleccione o cree una nueva configuración. [Más información sobre la configuración web](web-configuration.md)

   ![](assets/web-campaign-steps.png)

Para obtener más información sobre cómo configurar una campaña, consulte [esta página](../campaigns/get-started-with-campaigns.md).

## Prueba de la campaña web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Previsualizar la experiencia web"
>abstract="Obtenga una simulación del aspecto que tendrá su experiencia web."

Una vez que [haya creado su experiencia web](edit-web-content.md) con el diseñador web, puede usar perfiles de prueba para obtener una vista previa de las páginas web modificadas. Si ha insertado contenido personalizado, puede comprobar cómo se muestra este mediante los datos del perfil de prueba.

Para ello, haga clic en **[!UICONTROL Simular contenido]** desde la pantalla de contenido de edición de campañas web o desde el diseñador web. A continuación, añada un perfil de prueba para comprobar la página web mediante los datos del perfil de prueba.

![](assets/web-designer-preview.png)

También puede abrirlo en el explorador predeterminado o copiar la dirección URL de prueba para pegarla en cualquier explorador. Esto le permite compartir el vínculo con su equipo y las partes interesadas, que pueden obtener una vista previa de la nueva experiencia web en cualquier explorador antes de que la campaña se ponga en marcha.

>[!NOTE]
>
>Al copiar la dirección URL de prueba, el contenido mostrado es el personalizado para el perfil de prueba utilizado cuando se generó la simulación de contenido en [!DNL Journey Optimizer].

Encontrará información detallada sobre cómo seleccionar perfiles de prueba y obtener una vista previa del contenido en la sección [Administración de contenido](../content-management/preview-test.md).

## Activación de la campaña web {#activate-web-campaign}

Una vez que haya definido la [configuración de la campaña web](#configure-web-campaign) y haya editado el contenido como desee con el [diseñador web](edit-web-content.md#work-with-web-designer), podrá revisar y activar la campaña web. Siga los pasos a continuación.

<!--
>[!NOTE]
>
>You can also preview your web campaign content before activating it. [Learn more](#test-web-campaign)-->

1. En su campaña web, seleccione **[!UICONTROL Revisar para activar]**.

1. Compruebe y edite si es necesario el contenido, las propiedades, la configuración, la audiencia y la programación.

1. Seleccione **[!UICONTROL Activar]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Después de hacer clic en **[!UICONTROL Activar]**, los cambios de las campañas web pueden tardar hasta 15 minutos en estar disponibles en el sitio web.

La campaña web toma el estado **[!UICONTROL Activo]** y ahora es visible para la audiencia seleccionada. Cada destinatario de la campaña puede ver las modificaciones agregadas al sitio web mediante el diseñador web [!DNL Journey Optimizer].

>[!NOTE]
>
>Si ha definido una programación para su campaña web, tiene el estado **[!UICONTROL Programado]** hasta que se alcance la fecha y la hora de inicio.
>
>Si activa una campaña web que afecte a las mismas páginas que otra campaña que ya está activa, todos los cambios se aplicarán a las páginas web.

Más información sobre cómo activar campañas en [esta sección](../campaigns/review-activate-campaign.md).

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