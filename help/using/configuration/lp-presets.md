---
title: Definir ajustes preestablecidos de página de aterrizaje
description: Aprenda a configurar su entorno para crear y utilizar páginas de aterrizaje con Journey Optimizer
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: a036f53b88425d64281d2ac530016d638e2d13c9
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 4%

---

# Definir ajustes preestablecidos de página de aterrizaje {#lp-presets}

When [creación de una página de aterrizaje](../landing-pages/create-lp.md#create-a-lp), debe seleccionar un ajuste preestablecido de página de aterrizaje para poder crear la página de aterrizaje y aprovecharla mediante **[!DNL Journey Optimizer]**.

## Acceso a los ajustes preestablecidos de la página de aterrizaje {#access-lp-presets}

Para acceder a los ajustes preestablecidos de la página de aterrizaje, siga los pasos a continuación.

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Channels]** para abrir el Navegador.

1. Seleccione **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

   ![](assets/lp_presets-access.png)

1. Haga clic en cualquier etiqueta preestablecida para acceder a los detalles del ajuste preestablecido de la página de aterrizaje.

   ![](assets/lp_preset-details.png)

## Crear un ajuste preestablecido de página de aterrizaje {#lp-create-preset}

Para crear un ajuste preestablecido de página de aterrizaje, siga los pasos a continuación.

>[!NOTE]
>
>Para poder crear un ajuste preestablecido, asegúrese de haber configurado previamente al menos un subdominio de página de aterrizaje. [Descubra cómo](lp-subdomains.md)

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Channels]** a continuación, seleccione **[!UICONTROL Branding]** > **[!UICONTROL Landing page presets]**.

1. Seleccione **[!UICONTROL Create landing page preset]**.

   ![](assets/lp_create-preset-temp.png)

1. Introduzca un nombre y una descripción para el ajuste preestablecido.

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar guiones bajos `_`, punto`.` Guión `-` caracteres.

1. Seleccione un subdominio de página de aterrizaje en la lista desplegable.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >Para poder seleccionar un subdominio, asegúrese de haber configurado previamente al menos un subdominio de página de aterrizaje. [Descubra cómo](#lp-subdomains)

   Se muestra la configuración correspondiente al subdominio seleccionado.

1. Si desea seleccionar el subdominio de página de aterrizaje como URL de seguimiento, marque la casilla de verificación **[!UICONTROL Same as landing page subdomain]** . [Más información sobre el seguimiento](../design/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Por ejemplo, si la dirección URL de la página de aterrizaje es &quot;pages.mail.luma.com&quot; y la dirección URL de seguimiento es &quot;data.mail.luma.com&quot;, puede elegir &quot;pages.mail.luma.com&quot; para utilizarla como subdominio de seguimiento.

1. Haga clic en **[!UICONTROL Submit]** para confirmar la creación del ajuste preestablecido de la página de aterrizaje. También puede guardar el ajuste preestablecido como borrador y reanudarlo más adelante.

   ![](assets/lp_preset-subdomain-settings-submit.png)

1. Una vez creado el ajuste preestablecido de la página de aterrizaje, se muestra en la lista con la variable **[!UICONTROL Active]** estado. Está listo para utilizarse para sus páginas de aterrizaje.

   ![](assets/lp-preset-active-temp.png)

Ahora está listo para [crear páginas de aterrizaje](../landing-pages/create-lp.md) en [!DNL Journey Optimizer].

>[!NOTE]
>
>Obtenga información sobre cómo crear ajustes preestablecidos de mensaje para notificaciones push y correos electrónicos en [esta sección](message-presets.md).

**Temas relacionados**:

* [Introducción a las páginas de destino](../landing-pages/get-started-lp.md)
* [Creación de una página de destino](../landing-pages/create-lp.md#create-a-lp)
