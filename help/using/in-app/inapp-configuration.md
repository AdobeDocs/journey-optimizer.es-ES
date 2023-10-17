---
title: Requisitos previos del canal en la aplicación
description: Aprenda a configurar su entorno para enviar mensajes en la aplicación con Journey Optimizer
role: Admin
feature: In App
level: Intermediate
keywords: en la aplicación, mensaje, configuración, plataforma
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 11%

---

# Requisitos previos del canal en la aplicación {#inapp-configuration}

## Requisitos previos de envío {#delivery-prerequisites}

Para que los mensajes en la aplicación se entreguen correctamente, se debe definir la siguiente configuración:

* En el [Recopilación de datos de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=es){target="_blank"}, asegúrese de que tiene un conjunto de datos definido como en **[!UICONTROL Adobe Experience Platform]** servicio tiene Adobe Experience Platform Edge y **[!UICONTROL Adobe Journey Optimizer]** opción activada.

  Esto garantiza que Adobe Experience Platform Edge gestione correctamente los eventos entrantes de Journey Optimizer. [Más información](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=es){target="_blank"}

  ![](assets/inapp_config_6.png)

* Entrada [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}, make sure you have the default merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Esta política de combinación la utiliza [!DNL Journey Optimizer] canales entrantes para activar y publicar correctamente campañas entrantes en edge. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=es){target="_blank"}

  ![](assets/inapp_config_8.png)

## Requisitos previos de configuración de canal {#channel-prerequisites}

1. Acceda a la **[!UICONTROL Superficies de aplicación]** y haga clic en **[!UICONTROL Crear superficie de aplicación]**.

1. Añada un nombre a su **[!UICONTROL Superficie de aplicación]**.

   ![](assets/inapp_config_2b.png)

1. Desde el **[!UICONTROL Apple iOS]** , configure su aplicación móvil para Apple iOS.

+++ Más información

   1. Escriba su **[!UICONTROL ID de paquete de iOS]**. Consulte [Documentación de Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) para obtener más información sobre **ID de paquete**.

   1. (opcional) Elija la **[!UICONTROL Sandbox]** desde donde desea enviar notificaciones push. Tenga en cuenta que la selección de una zona protegida específica requiere los permisos de acceso necesarios.

      Para obtener más información sobre la administración de zonas protegidas, consulte [esta página](../administration/sandboxes.md#assign-sandboxes).

   1. Habilite la **[!UICONTROL Credenciales push]** opción para arrastrar y soltar el archivo de clave de autenticación .p8 si es necesario.

      También puede activar la variable **[!UICONTROL Introduzca manualmente las credenciales push]** para copiar y pegar la clave de autenticación de APN directamente.

   1. Introduzca su **[!UICONTROL ID de clave]** y **[!UICONTROL Identificador de equipo]**.

      ![](assets/inapp_config_2.png)

+++

1. Desde el **[!UICONTROL Android]** , configure su aplicación móvil para Android.

+++ Más información

   1. Escriba su **[!UICONTROL Nombre del paquete de Android]**. Consulte [Documentación de Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) para obtener más información sobre **Nombre del paquete**.

   1. (opcional) Elija la **[!UICONTROL Sandbox]** desde donde desea enviar notificaciones push. Tenga en cuenta que la selección de una zona protegida específica requiere los permisos de acceso necesarios.

      Para obtener más información sobre la administración de zonas protegidas, consulte [esta página](../administration/sandboxes.md#assign-sandboxes).

   1. Habilite la **[!UICONTROL Credenciales push]** opción para arrastrar y soltar el archivo de clave privada .json si es necesario.

      También puede activar la variable **[!UICONTROL Introduzca manualmente las credenciales push]** para copiar y pegar la clave privada de FCM directamente.

      ![](assets/inapp_config_7.png)

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

## Requisitos previos del experimento de contenido {#experiment-prerequisites}

Para habilitar los experimentos de contenido para el canal en la aplicación, debe asegurarse de que la variable [conjunto de datos](../data/get-started-datasets.md) se utiliza en la implementación en la aplicación [secuencia de datos](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=es){target="_blank"} también se incluye en la configuración de informes.

En otras palabras, al configurar los informes de experimentos, si agrega un conjunto de datos que no está presente en el conjunto de datos web, estos no se mostrarán en los informes de experimentos de contenido.

Aprenda a añadir conjuntos de datos para la creación de informes de experimentos de contenido en [esta sección](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>El conjunto de datos lo utiliza solo lectura el [!DNL Journey Optimizer] sistema de informes de y no afecta a la recopilación ni a la ingesta de datos.

Si es usted **no** utilizando los siguientes elementos predefinidos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target="_blank"} for your dataset schema: `AEP Web SDK ExperienceEvent` and `Consumer Experience Event` (as defined in [this page](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), asegúrese de añadir los siguientes grupos de campos: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details`, y `Web Details`. Estas son necesarias para [!DNL Journey Optimizer] los informes de experimentos de contenido, ya que rastrean en qué experimentos y tratamientos participa cada perfil.

>[!NOTE]
>
>Añadir estos grupos de campos no afecta a la recopilación de datos normal. Solo es aditivo para las páginas en las que se está ejecutando un experimento, dejando el resto del seguimiento intacto.

## Vídeotutoriales{#video}

* El siguiente vídeo muestra cómo asignar el **Administrar configuración de aplicación** permiso para acceder al menú Superficies de la aplicación.

  +++Consulte el vídeo

  >[!VIDEO](https://video.tv.adobe.com/v/3421607)

+++

**Temas relacionados:**

* [Creación de un mensaje en la aplicación ](create-in-app.md)
* [Creación de una campaña](../campaigns/create-campaign.md)
* [Diseño de un mensaje en la aplicación](design-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report.md#inapp-report)

