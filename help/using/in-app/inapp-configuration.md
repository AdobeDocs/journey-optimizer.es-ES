---
title: Configuración en la aplicación
description: Aprenda a configurar su entorno para enviar mensajes en la aplicación con Journey Optimizer
role: Admin
level: Intermediate
keywords: en la aplicación, mensaje, configuración, plataforma
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 94c4e0e53625fdf20f940e8bfd15d67dba1d0120
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 10%

---

# Configuración del canal en la aplicación {#inapp-configuration}

Antes de enviar mensajes en la aplicación, debe configurar el canal en la aplicación en [!DNL Adobe Experience Platform Data Collection].

1. De su [!DNL Adobe Experience Platform Data Collection] Cuenta de, acceda a **[!UICONTROL Datastream]** y haga clic en **[!UICONTROL Nueva secuencia de datos]**. Para obtener más información sobre la creación de flujos de datos, consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=es).

1. Seleccione el [!DNL Adobe Experience Platform] servicio.

   [!DNL Edge Segmentation] y [!DNL Adobe Journey Optimizer] debe estar seleccionado.

   ![](assets/inapp_config_6.png)

   >[!NOTE]
   >
   >Para habilitar los experimentos de contenido para el canal en la aplicación, debe asegurarse de que la variable [conjunto de datos](../data/get-started-datasets.md) se utiliza en la aplicación [secuencia de datos](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=es){target="_blank"} también está presente en la configuración de creación de informes; de lo contrario, los datos en la aplicación no se mostrarán en los informes de experimento de contenido. [Aprenda a añadir conjuntos de datos](../campaigns/reporting-configuration.md#add-datasets)
   >
   >El conjunto de datos lo utiliza solo lectura el [!DNL Journey Optimizer] sistema de informes de y no afecta a la recopilación ni a la ingesta de datos.

1. A continuación, acceda al **[!UICONTROL Superficies de aplicación]** y haga clic en **[!UICONTROL Crear superficie de aplicación]**.

   >[!NOTE]
   >
   > Necesita el **Administrar configuración de aplicación** permiso para tener acceso a **[!UICONTROL Superficies de aplicación]** menú. Para obtener más información, consulte [este vídeo](#video).

   >[!NOTE]
   >
   > Necesita el **Administrar configuración de aplicación** permiso para tener acceso a **[!UICONTROL Superficies de aplicación]** menú. Para obtener más información, consulte [este vídeo](#video).

   ![](assets/inapp_config_1.png)

1. Añada un nombre a su **[!UICONTROL Superficie de aplicación]**.


1. En la lista desplegable Apple iOS, escriba su **ID de paquete de iOS**. Consulte [Documentación de Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) para obtener más información sobre **ID de paquete**.

   ![](assets/inapp_config_2.png)

1. En la lista desplegable de Android, escriba su **Nombre del paquete de Android**. Consulte [Documentación de Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) para obtener más información sobre **Nombre del paquete**.

1. Clic **[!UICONTROL Guardar]** cuando haya terminado la configuración de su **[!UICONTROL Superficie de aplicación]**.

   ![](assets/inapp_config_3.png)

   Su **[!UICONTROL Superficie de aplicación]** ahora estará disponible al crear una nueva campaña con un mensaje en la aplicación. [Más información](create-in-app.md)

1. Después de crear la superficie de la aplicación, debe crear una propiedad móvil.

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) para el procedimiento detallado.

   ![](assets/inapp_config_4.png)

1. En el menú Extensiones de la propiedad recién creada, instale las siguientes extensiones:

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP Assurance
   * Consentimiento
   * Identidad
   * Mobile Core
   * Perfil

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) para el procedimiento detallado.

   ![](assets/inapp_config_5.png)

El canal en la aplicación ya está configurado. Puede empezar a enviar mensajes en la aplicación a los usuarios.

**Temas relacionados:**

* [Creación de un mensaje en la aplicación ](create-in-app.md)
* [Creación de una campaña](../campaigns/create-campaign.md)
* [Diseño de un mensaje en la aplicación](design-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report.md#inapp-report)


## Vídeotutoriales{#video}

* El siguiente vídeo muestra cómo asignar el **Administrar configuración de aplicación** permiso para acceder al menú Superficies de la aplicación.

  +++Consulte el vídeo

  >[!VIDEO](https://video.tv.adobe.com/v/3421607)

+++


