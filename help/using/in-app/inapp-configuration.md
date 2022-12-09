---
title: Configuración en la aplicación
description: Aprenda a configurar su entorno para enviar mensajes en la aplicación con Journey Optimizer
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Configuración del canal en la aplicación {#inapp-configuration}

Antes de enviar mensajes en la aplicación, debe configurar el canal en la aplicación en [!DNL Adobe Experience Platform Data Collection].

1. Desde su [!DNL Adobe Experience Platform Data Collection] la cuenta, acceda a la **[!UICONTROL Datastream]** y haga clic en **[!UICONTROL New datastream]**. Para obtener más información sobre la creación de conjuntos de datos, consulte [esta página](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. Seleccione el [!DNL Adobe Experience Platform] servicio.

   [!DNL Edge Segmentation], [!DNL Offer Decisioning] y [!DNL Adobe Journey Optimizer] debe estar seleccionado.

   ![](assets/inapp_config_6.png)

1. A continuación, acceda al **[!UICONTROL App surfaces]** a continuación, haga clic en **[!UICONTROL Create App surface]**.

   ![](assets/inapp_config_1.png)

1. Añada un nombre a su **[!UICONTROL App surface]**.

1. En la lista desplegable Apple iOS , escriba su **ID de paquete de iOS**. Consulte [Documentación de Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) para obtener más información sobre **ID del paquete**.

   ![](assets/inapp_config_2.png)

1. En la lista desplegable de Android, escriba su **Nombre del paquete de Android**. Consulte [Documentación de Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) para obtener más información sobre **Nombre del paquete**.

1. Haga clic en **[!UICONTROL Save]** cuando haya terminado la configuración de su **[!UICONTROL App surface]**.

   ![](assets/inapp_config_3.png)

   Su **[!UICONTROL App surface]** estará disponible al crear una nueva campaña con un mensaje en la aplicación. [Más información](create-in-app.md)

1. Después de crear la superficie de la aplicación, debe crear una propiedad móvil.

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) para el procedimiento detallado.

   ![](assets/inapp_config_4.png)

1. En el menú Extensiones de la propiedad recién creada, instale las siguientes extensiones:

   * Red perimetral de Adobe Experience Platform
   * Adobe Journey Optimizer
   * AEP Assurance
   * Consentimiento
   * Identificar
   * Núcleo móvil
   * Perfil

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en#add-a-new-extension) para el procedimiento detallado.

   ![](assets/inapp_config_5.png)

Ya está configurado el canal en la aplicación. Puede empezar a enviar mensajes en la aplicación a los usuarios.

**Temas relacionados:**

* [Crear un mensaje en la aplicación](create-in-app.md)
* [Creación de una campaña](../campaigns/create-campaign.md)
* [Diseño de mensajes en la aplicación](design-in-app.md)
* [Informe en la aplicación](inapp-report.md)
