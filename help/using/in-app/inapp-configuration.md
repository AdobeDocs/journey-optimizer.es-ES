---
title: Requisitos previos y configuración del canal en la aplicación
description: Aprenda a configurar su entorno para enviar mensajes en la aplicación con Journey Optimizer
role: Admin
feature: In App
level: Intermediate
keywords: en la aplicación, mensaje, configuración, plataforma
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 9%

---

# Requisitos previos y configuración {#inapp-configuration}

## Pasos de configuración {#inapp-steps}

Para enviar mensajes en la aplicación en sus recorridos y campañas con [!DNL Journey Optimizer], debe seguir los siguientes pasos de configuración.

1. Asegúrese de tener los permisos correctos en las campañas de Journey Optimizer antes de empezar, incluso si planea usar únicamente mensajes en la aplicación en los recorridos. Los permisos de Campaign siguen siendo necesarios. [Más información](../campaigns/get-started-with-campaigns.md#campaign-prerequisites).
Se debe otorgar un permiso específico para acceder al menú **Superficies de la aplicación** en la recopilación de datos de Adobe Experience Platform. Obtenga más información en [este vídeo](#video).
1. Habilite Adobe Journey Optimizer en su secuencia de datos de recopilación de datos de Adobe Experience Platform y compruebe su política de combinación predeterminada en Adobe Experience Platform, tal como se detalla en los [requisitos previos de entrega](#delivery-prerequisites) a continuación.
1. Cree y configure una superficie de aplicación en la recopilación de datos de Adobe Experience Platform, tal como se detalla en [esta sección](#channel-prerequisites).
1. Si está usando experimentos de contenido, asegúrese de seguir los requisitos enumerados en [esta sección](#experiment-prerequisite).

Cuando haya finalizado, podrá crear, configurar y enviar su primer mensaje en la aplicación. Obtenga información sobre cómo enviar mensajes en [esta sección](create-in-app.md).

## Requisitos previos de envío {#delivery-prerequisites}

Para que los mensajes en la aplicación se entreguen correctamente, se debe definir la siguiente configuración:

* En la [recopilación de datos de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=es){target="_blank"}, asegúrese de que tiene un conjunto de datos definido como en el servicio **[!UICONTROL Adobe Experience Platform]**. Tiene habilitadas la opción Adobe Experience Platform Edge y **[!UICONTROL Adobe Journey Optimizer]**.

  Esto garantiza que Adobe Experience Platform Edge gestione correctamente los eventos entrantes de Journey Optimizer. [Más información](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/inapp_config_6.png)

* En [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}, asegúrese de que tiene habilitada la política de combinación predeterminada con la opción **[!UICONTROL Política de combinación activa en Edge]**. Para ello, seleccione una directiva en el menú de Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Perfiles]** > **[!UICONTROL Políticas de combinación]**. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  [!DNL Journey Optimizer] canales entrantes utilizan esta política de combinación para activar y publicar correctamente campañas entrantes en el perímetro de. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=es){target="_blank"}

  >[!NOTE]
  >
  >Cuando use una directiva de combinación personalizada de **[!UICONTROL preferencias del conjunto de datos]**, asegúrese de agregar el conjunto de datos **[!UICONTROL Recorrido entrante]** dentro de la directiva de combinación especificada.

  ![](assets/inapp_config_8.png)

* Para solucionar problemas del envío de experiencias móviles de Journey Optimizer, puedes usar la vista de **Edge Delivery** en **Adobe Experience Platform Assurance**. Este complemento le permite inspeccionar en detalle las llamadas de solicitud, comprobar si las llamadas perimetrales esperadas se producen según lo previsto y examinar los datos de perfil, incluidos los mapas de identidad, las suscripciones a segmentos y la configuración de consentimiento. Además, puede revisar las actividades para las que la solicitud cumple los requisitos e identificar las que no.

  El uso del complemento **Edge Delivery** le ayuda a obtener la información necesaria para comprender y solucionar problemas de las implementaciones entrantes de forma eficaz.

  [Más información en la vista de Edge Delivery](https://experienceleague.adobe.com/es/docs/experience-platform/assurance/view/edge-delivery)

## Requisitos previos de configuración de canal {#channel-prerequisites}

1. Acceda al menú **[!UICONTROL Superficies de la aplicación]** y haga clic en **[!UICONTROL Crear superficie de la aplicación]**.

1. Agregue un nombre a su **[!UICONTROL superficie de aplicación]**.

   ![](assets/inapp_config_2b.png)

1. En el menú desplegable **[!UICONTROL Apple iOS]**, configure su aplicación móvil para Apple iOS.

+++ Más información

   1. Escriba su **[!UICONTROL ID del paquete de iOS]**. Consulte [Documentación de Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) para obtener más información sobre **ID del paquete**.

   1. (opcional) Elija la **[!UICONTROL zona protegida]** desde la que desea enviar notificaciones push. Tenga en cuenta que la selección de una zona protegida específica requiere los permisos de acceso necesarios.

      Para obtener más información sobre la administración de zonas protegidas, consulte [esta página](../administration/sandboxes.md#assign-sandboxes).

   1. Habilite la opción **[!UICONTROL Push credentials]** para arrastrar y soltar el archivo de clave de autenticación .p8 si es necesario.

      También puede habilitar la opción **[!UICONTROL Introducir manualmente las credenciales de inserción]** para copiar y pegar la clave de autenticación de APN directamente.

   1. Escriba su **[!UICONTROL identificador de clave]** y su **[!UICONTROL identificador de equipo]**.

      ![](assets/inapp_config_2.png)

+++

1. En el menú desplegable **[!UICONTROL Android]**, configure su aplicación móvil para Android.

+++ Más información

   1. Escriba su **[!UICONTROL nombre de paquete de Android]**. Consulte [Documentación de Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) para obtener más información sobre **Nombre del paquete**.

   1. (opcional) Elija la **[!UICONTROL zona protegida]** desde la que desea enviar notificaciones push. Tenga en cuenta que la selección de una zona protegida específica requiere los permisos de acceso necesarios.

      Para obtener más información sobre la administración de zonas protegidas, consulte [esta página](../administration/sandboxes.md#assign-sandboxes).

   1. Habilite la opción **[!UICONTROL Credenciales push]** para arrastrar y soltar el archivo de clave privada .json si es necesario.

      También puede habilitar la opción **[!UICONTROL Introducir manualmente credenciales de inserción]** para copiar y pegar la clave privada de FCM directamente.

      ![](assets/inapp_config_7.png)

1. Haga clic en **[!UICONTROL Guardar]** cuando termine de configurar la **[!UICONTROL superficie de la aplicación]**.

   ![](assets/inapp_config_3.png)

   **[!UICONTROL La superficie de la aplicación]** ahora estará disponible al crear una nueva campaña con un mensaje en la aplicación. [Más información](create-in-app.md)

1. Después de crear la superficie de la aplicación, debe crear una propiedad móvil.

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) para ver el procedimiento detallado.

   ![](assets/inapp_config_4.png)

1. En el menú Extensiones de la propiedad recién creada, instale las siguientes extensiones:

   * Edge Network de Adobe Experience Platform
   * Adobe Journey Optimizer
   * AEP Assurance
   * Consentimiento
   * Identidad
   * Mobile Core
   * Perfil

   Consulte [esta página](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) para ver el procedimiento detallado.

   ![](assets/inapp_config_5.png)

El canal en la aplicación ya está configurado. Puede empezar a enviar mensajes en la aplicación a los usuarios.

## Requisitos previos del experimento de contenido {#experiment-prerequisites}

Para habilitar los experimentos de contenido para el canal en la aplicación, debe asegurarse de que el [conjunto de datos](../data/get-started-datasets.md) utilizado en la implementación en la aplicación [secuencia de datos](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} también esté incluido en la configuración de los informes.

En otras palabras, al configurar los informes de experimentos, si agrega un conjunto de datos que no está presente en el conjunto de datos web, estos no se mostrarán en los informes de experimentos de contenido.

Aprenda a agregar conjuntos de datos para los informes de experimentos de contenido en [esta sección](../content-management/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>El sistema de informes [!DNL Journey Optimizer] utiliza el conjunto de datos como de solo lectura y no afecta a la recopilación ni al consumo de datos.

Si **no** usa los siguientes [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target="_blank"} predefinidos para el esquema del conjunto de datos: `AEP Web SDK ExperienceEvent` y `Consumer Experience Event` (según se definen en [esta página](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), asegúrese de agregar los siguientes grupos de campos: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details` y `Web Details`. Los necesita el informe de experimento de contenido [!DNL Journey Optimizer], ya que rastrean en qué experimentos y tratamientos participa cada perfil.

>[!NOTE]
>
>Añadir estos grupos de campos no afecta a la recopilación de datos normal. Solo es aditivo para las páginas en las que se está ejecutando un experimento, dejando el resto del seguimiento intacto.

## Vídeo explicativo{#video}

El siguiente vídeo muestra cómo asignar el permiso **Administrar configuración de la aplicación** para acceder al menú Superficies de la aplicación.

>[!VIDEO](https://video.tv.adobe.com/v/3421607)


**Temas relacionados:**

* [Creación de un mensaje en la aplicación ](create-in-app.md)
* [Creación de una campaña](../campaigns/create-campaign.md)
* [Diseño de un mensaje en la aplicación](design-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report.md#inapp-report)

