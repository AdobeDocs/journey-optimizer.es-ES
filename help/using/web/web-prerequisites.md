---
title: Requisitos previos de canal web
description: Para poder acceder y crear páginas web en la interfaz de usuario de Journey Optimizer, siga los requisitos previos de esta página
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: 4899dbe71243184b6283a32a4fe7eb2edb82f872
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 6%

---

# Requisitos previos y protecciones {#web-prerequisites}

Para poder acceder y crear páginas web en [!DNL Journey Optimizer] Siga los requisitos previos a continuación:

* Para añadir modificaciones al sitio web, debe tener una implementación específica. [Más información](#implementation-prerequisites)

* Para acceder a [!DNL Journey Optimizer] Diseñador web, debe tener instalada una extensión específica del explorador Google Chrome. [Más información](#visual-authoring-prerequesites)

* Para que la experiencia web se entregue correctamente, asegúrese de definir la configuración detallada de Adobe Experience Platform [aquí](#delivery-prerequisites).

## Notas de precaución {#caution-notes-web}

* Actualmente en [!DNL Journey Optimizer] solo puede crear experiencias web en **campañas**. [Más información](../campaigns/create-campaign.md#configure)

* [!DNL Journey Optimizer] las campañas web se dirigen a nuevos perfiles que no se han utilizado anteriormente en otros canales. Esto aumentará el recuento total de perfiles atractivos, lo que puede tener implicaciones de costes si se supera el número contractual de perfiles atractivos que ha adquirido. Las métricas de licencia de cada paquete se enumeran en la [Descripción del producto de Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"} página.


>[!AVAILABILITY]
>
>Por ahora, el canal Web no está disponible para las organizaciones que han adquirido el Adobe **Healthcare Shield** y **Escudo de seguridad y privacidad** ofertas de complementos.

## Requisitos previos de implementación {#implementation-prerequisites}

Actualmente se admiten dos tipos de implementaciones para habilitar la creación y el envío de campañas de canal web en las propiedades web:

* Solo del lado del cliente: para agregar modificaciones al sitio web, debe implementar la variable [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"} en su sitio web.

  >[!NOTE]
  >
  >Asegúrese de que la versión del SDK web de AEP sea 2.16 o superior.

* Modo híbrido: puede utilizar el [API de servidor de red perimetral AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} to request for personalization server-side; the response is provided to the Adobe Experience Platform Web SDK to render the modifications client-side. Learn more in the Adobe Experience Platform [Edge Network Server API documentation](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html?lang=es){target="_blank"}. You can find out more about the hybrid mode and check some implementation samples in [this blog post](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>Actualmente no se admite la implementación solo del lado del servidor.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## Requisitos previos de creación visual {#visual-authoring-prerequisites}

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Para poder abrir, crear y previsualizar sus páginas web de forma fiable en [!DNL Journey Optimizer] diseñador web, debe tener el [Ayuda de edición visual de Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extensión del explorador instalada en el explorador web.

>[!CAUTION]
>
>Google Chrome y Microsoft Edge son actualmente los únicos exploradores compatibles con la creación de páginas web en [!DNL Journey Optimizer].

### Instale la extensión Ayuda de edición visual {#install-visual-editing-helper}

Para descargar e instalar la extensión del explorador Ayuda de edición visual, siga los pasos a continuación.

1. Abra una pestaña nueva en el explorador (Google Chrome o Microsoft Edge).

1. Vaya a la [Tienda web de Google Chrome](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Si utiliza Microsoft Edge, seleccione **[!UICONTROL Permitir extensiones de otras tiendas]** en el banner superior. Esto le permitirá agregar extensiones de la Chrome Web Store a Microsoft Edge.

1. Busque y vaya al [Ayuda de edición visual de Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extensión del explorador.

1. Haga clic en **[!UICONTROL Añadir a Chrome]** > **[!UICONTROL Añadir extensión]**.

   >[!NOTE]
   >
   >Si utiliza Microsoft Edge, se agregará la extensión a Edge aunque el botón esté etiquetado como **[!UICONTROL Añadir a Chrome]**.

1. Asegúrese de que la extensión del explorador Ayuda de edición visual esté correctamente habilitada en la barra de herramientas del explorador.

   ![](assets/web-visual-editing-extension-edge.png)

El Asistente de edición visual de Adobe Experience Cloud ahora se habilita automáticamente cuando se abre un sitio web en [!DNL Journey Optimizer] [diseñador web](edit-web-content.md#work-with-web-designer) para la creación de contenido.

La extensión no tiene ninguna configuración condicional y administra todas las configuraciones automáticamente, incluida la configuración de cookies de SameSite.

>[!NOTE]
>
>Es posible que algunos sitios web no se abran de forma fiable en [!DNL Journey Optimizer] diseñador web debido a una de las siguientes razones:
>
> * El sitio web tiene normas estrictas de seguridad.
> * El sitio web se encuentra en un iframe.
> * El control de calidad o la fase del cliente no están disponibles para el mundo exterior (el sitio es interno).

### Solucionar problemas de sitio web que no se carga {#troubleshooting}

Al utilizar el Adobe [!DNL Journey Optimizer] diseñador web, si intenta cargar un sitio web que no se puede cargar, aparece un mensaje sugiriendo que instale el [Extensión de explorador Ayuda de edición visual](#install-visual-editing-helper).

1. Asegúrese de que la extensión del explorador Ayuda de edición visual esté instalada correctamente.

1. Si el sitio web sigue comportándose de forma inesperada, asegúrese de que las cookies de terceros estén permitidas en el explorador; de lo contrario, la página web no se puede cargar dentro de [!DNL Journey Optimizer] diseñador web.

En el caso de las páginas que se están autenticando, si la página de inicio de sesión no se puede cargar o si, después de intentar iniciar sesión, aún no ha iniciado sesión:

1. Intente iniciar sesión primero en una nueva pestaña del explorador, vaya a la página deseada, copie la URL e intente abrirla en la [!DNL Journey Optimizer] diseñador web.

2. Si sigue sin poder cargar el sitio web en [!DNL Journey Optimizer] Diseñador web, póngase en contacto con el Servicio de atención al cliente de Adobe para informar del problema. Asegúrese de especificar la dirección URL que falla.

## Requisitos previos de envío {#delivery-prerequisites}

Para que la experiencia web se entregue correctamente, se debe definir la siguiente configuración:

* En el [Recopilación de datos de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=es){target="_blank"}, asegúrese de que tiene un conjunto de datos definido como en **[!UICONTROL Adobe Experience Platform]** servicio que tiene el **[!UICONTROL Adobe Journey Optimizer]** opción activada.

  Esto garantiza que Adobe Experience Platform Edge gestione correctamente los eventos entrantes de Journey Optimizer. [Más información](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=es){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* Entrada [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}, make sure you have one merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Esta política de combinación la utiliza [!DNL Journey Optimizer] canales entrantes para activar y publicar correctamente campañas entrantes en edge. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=es){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

## Requisitos previos del experimento de contenido {#experiment-prerequisites}

Para habilitar los experimentos de contenido para el canal Web, debe asegurarse de que la variable [conjunto de datos](../data/get-started-datasets.md) se utiliza en la implementación web [secuencia de datos](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} también se incluye en la configuración de informes.

En otras palabras, al configurar los informes de experimentos, si agrega un conjunto de datos que no está presente en el conjunto de datos web, estos no se mostrarán en los informes de experimentos de contenido.

Aprenda a añadir conjuntos de datos para la creación de informes de experimentos de contenido en [esta sección](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>El conjunto de datos lo utiliza solo lectura el [!DNL Journey Optimizer] sistema de informes de y no afecta a la recopilación ni a la ingesta de datos.

Si es usted **no** utilizando los siguientes elementos predefinidos [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target="_blank"} for your dataset schema: `AEP Web SDK ExperienceEvent` and `Consumer Experience Event` (as defined in [this page](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), asegúrese de añadir los siguientes grupos de campos: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details`, y `Web Details`. Estas son necesarias para [!DNL Journey Optimizer] los informes de experimentos de contenido, ya que rastrean en qué experimentos y tratamientos participa cada perfil.

>[!NOTE]
>
>Añadir estos grupos de campos no afecta a la recopilación de datos normal. Solo es aditivo para las páginas en las que se está ejecutando un experimento, dejando el resto del seguimiento intacto.

## Dominios de marca para recursos {#branded-domains-for-assets}

Al crear experiencias web, si añade contenido procedente de [Adobe Experience Manager Assets](../content-management/assets.md) , debe configurar el subdominio que se utilizará para publicar este contenido. [Más información](web-delegated-subdomains.md)
