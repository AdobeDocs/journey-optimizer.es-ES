---
title: Requisitos previos de canal web
description: Para poder acceder y crear páginas web en la interfaz de usuario de Journey Optimizer, siga los requisitos previos de esta página
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 9509fd67-6d12-4440-aad8-59690936be97
source-git-commit: 22e1f08f434a3ceb4be6c539d4007178062cba9e
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 10%

---

# Requisitos previos y protecciones {#web-prerequisites}

Para poder acceder y crear páginas web en la interfaz de usuario de [!DNL Journey Optimizer], siga los requisitos previos siguientes:

* Para añadir modificaciones al sitio web, debe tener una implementación específica. [Más información](#implementation-prerequisites)

* Para tener acceso al diseñador web [!DNL Journey Optimizer], debe tener instalada una extensión específica del explorador Google Chrome. [Más información](#visual-authoring-prerequisites)

* Para que la experiencia web se entregue correctamente, asegúrese de definir la configuración de Adobe Experience Platform detallada [aquí](#delivery-prerequisites).

* Para habilitar los informes para el canal web, debe asegurarse de que el conjunto de datos utilizado en el conjunto de datos de implementación web también se incluya en la configuración de informes. [Más información](#experiment-prerequisites)

>[!IMPORTANT]
>
>* Las campañas web de [!DNL Journey Optimizer] se dirigen a nuevos perfiles que no han interactuado anteriormente en otros canales. Esto aumenta su recuento total de [Perfiles atractivos](../audience/license-usage.md), lo que puede tener implicaciones de costo si se supera el número contractual de Perfiles atractivos que compró. Las métricas de licencia de cada paquete se enumeran en la página [Descripción del producto de Journey Optimizer](https://helpx.adobe.com/es/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Puede comprobar el número de perfiles atractivos en [tablero de uso de licencias](../audience/license-usage.md).
>
>* Al segmentar perfiles seudónimos (visitantes no autenticados) con sus páginas web, considere la posibilidad de establecer un tiempo de vida (TTL) para la eliminación automática de perfiles a fin de administrar el recuento de perfiles atractivos y los costes asociados. [Más información](../start/guardrails.md#profile-management-inbound)

## Requisitos previos de implementación {#implementation-prerequisites}

Se admiten dos tipos de implementaciones para habilitar la creación y el envío de campañas de canal web en las propiedades web:

* Solo del lado del cliente: para agregar modificaciones al sitio web, debe implementar [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"} en el sitio web.

  >[!NOTE]
  >
  >Compruebe que su [versión de Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/release-notes){target="_blank"} sea la 2.16 o superior.

* Modo híbrido: puede utilizar la [API de servidor de AEP Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=es){target="_blank"} para solicitar la personalización del lado del servidor; la respuesta se proporciona al SDK web de Adobe Experience Platform para procesar las modificaciones del lado del cliente. Obtenga más información en la [Documentación de la API de Edge Network Server de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}. Puede obtener más información sobre el modo híbrido y ver algunos ejemplos de implementación en [esta publicación de blog](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

>[!NOTE]
>
>Actualmente, la implementación solo del lado del servidor no es compatible con el canal Web. Si solo tiene una implementación del lado del servidor para sus páginas web, puede usar el [canal de experiencia basado en código](../code-based/get-started-code-based.md) en su lugar.

<!--If the Adobe Experience Platform Web SDK is not yet implemented on the website, a message displays in the web designer suggesting that you install the Visual Editing Helper browser extension and implement the [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target="_blank"}.-->

## Requisitos previos para la creación visual {#visual-authoring-prerequisites}

>[!CONTEXTUALHELP]
>id="ajo_web_browser_extension"
>title="Creación de páginas que coincidan con una regla"
>abstract="Para tener acceso al diseñador web de [!DNL Journey Optimizer], debe tener instalada una extensión de explorador específica: el asistente para la edición visual de Adobe Experience Cloud, que solo está disponible en Google Chrome o Microsoft Edge."

<!--In order to rapidly author and preview your web experiences, the Adobe Experience Cloud Visual Editing Helper browser extension for Google Chrome lets you load websites reliably within the Adobe [!DNL Journey Optimizer] web designer.-->

Para poder abrir, crear y obtener una vista previa de las páginas web de forma fiable en el diseñador web de [!DNL Journey Optimizer], debe tener instalada la extensión de explorador [Ayuda de edición visual de Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} en el explorador web.

>[!CAUTION]
>
>Google Chrome y Microsoft Edge son los únicos exploradores que admiten la creación de páginas web en [!DNL Journey Optimizer].

### Instale la extensión Ayuda de edición visual {#install-visual-editing-helper}

Para descargar e instalar la extensión del explorador Ayuda de edición visual, siga los pasos a continuación.

1. Abra una pestaña nueva en el explorador (Google Chrome o Microsoft Edge).

1. Vaya a [Google Chrome Web Store](https://chrome.google.com/webstore/category/extensions){target="_blank"}.

1. Si usas Microsoft Edge, selecciona **[!UICONTROL Permitir extensiones de otras tiendas]** en el banner superior. Esto le permitirá agregar extensiones de la Tienda web de Chrome a Microsoft Edge.

1. Busque y navegue hasta la extensión de explorador [Ayuda de edición visual de Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"}.

1. Haga clic en **[!UICONTROL Añadir a Chrome]** > **[!UICONTROL Añadir extensión]**.

   >[!NOTE]
   >
   >Si usa Microsoft Edge, esto agregará la extensión a Edge aunque el botón esté etiquetado como **[!UICONTROL Agregar a Chrome]**.

1. Asegúrese de que la extensión del explorador Ayuda de edición visual esté correctamente habilitada en la barra de herramientas del explorador.

   ![](assets/web-visual-editing-extension-edge.png)

La Ayuda de edición visual de Adobe Experience Cloud ahora se habilita automáticamente cuando se abre un sitio web en el [!DNL Journey Optimizer] [diseñador web](web-visual-editor.md) para la creación avanzada.

La extensión no tiene ninguna configuración condicional y administra todas las configuraciones automáticamente, incluida la configuración de cookies de SameSite.

>[!NOTE]
>
>Es posible que algunos sitios web no se abran de forma fiable en el diseñador web [!DNL Journey Optimizer] por uno de los siguientes motivos:
>
> * El sitio web tiene normas estrictas de seguridad.
> * El sitio web se encuentra en un iframe.
> * El control de calidad o la fase del cliente no están disponibles para el mundo exterior (el sitio es interno).

### Solucionar problemas de sitio web que no se carga {#troubleshooting}

Al usar el diseñador web de Adobe [!DNL Journey Optimizer], si intenta cargar un sitio web que no se puede cargar, aparece un mensaje sugiriendo que instale la extensión de explorador [Ayuda de edición visual](#install-visual-editing-helper).

1. Asegúrese de que la extensión del explorador Ayuda de edición visual esté instalada correctamente.

1. Si el sitio web sigue comportándose de forma inesperada, asegúrese de que las cookies de terceros están permitidas en el explorador; de lo contrario, la página web no se podrá cargar dentro del diseñador web de [!DNL Journey Optimizer].

En el caso de las páginas que se están autenticando, si la página de inicio de sesión no se puede cargar o si, después de intentar iniciar sesión, aún no ha iniciado sesión:

1. Intente iniciar sesión primero en una nueva ficha del explorador y navegar a la página deseada. A continuación, copie la dirección URL e intente abrirla en el diseñador web [!DNL Journey Optimizer].

2. Si sigue sin poder cargar el sitio web en el diseñador web [!DNL Journey Optimizer], póngase en contacto con el Servicio de atención al cliente de Adobe para informar del problema y asegúrese de especificar la dirección URL que produce el error.

## Requisitos previos de envío {#delivery-prerequisites}

Para que la experiencia web se entregue correctamente, se debe definir la siguiente configuración:

* En la [recopilación de datos de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=es){target="_blank"}, asegúrese de que tiene un conjunto de datos definido como en el servicio **[!UICONTROL Adobe Experience Platform]** para el que tiene habilitada la opción **[!UICONTROL Adobe Journey Optimizer]**.

  Esto garantiza que Adobe Experience Platform Edge gestione correctamente los eventos entrantes de Journey Optimizer. [Más información](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/web-aep-datastream-ajo.png)

* En [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}, asegúrese de tener habilitada una política de combinación con la opción **[!UICONTROL Política de combinación activa en Edge]**. Para ello, seleccione una directiva en el menú de Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Perfiles]** > **[!UICONTROL Políticas de combinación]**. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  [!DNL Journey Optimizer] canales entrantes utilizan esta política de combinación para activar y publicar correctamente campañas entrantes en el perímetro de. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=es){target="_blank"}

  ![](assets/web-aep-merge-policy.png)

* Para solucionar problemas del envío de experiencias web de Journey Optimizer, puedes usar la vista de **Edge Delivery** en **Adobe Experience Platform Assurance**. Este complemento le permite inspeccionar en detalle las llamadas de solicitud, comprobar si las llamadas perimetrales esperadas se producen según lo previsto y examinar los datos de perfil, incluidos los mapas de identidad, las suscripciones a segmentos y la configuración de consentimiento. Además, puede revisar las actividades para las que la solicitud cumple los requisitos e identificar las que no.

  El uso del complemento **Edge Delivery** le ayuda a obtener la información necesaria para comprender y solucionar problemas de las implementaciones entrantes de forma eficaz.

  [Más información sobre la vista Edge Delivery](https://experienceleague.adobe.com/es/docs/experience-platform/assurance/view/edge-delivery)

## Requisitos previos de informes {#experiment-prerequisites}

Para habilitar la creación de informes para el canal web, debe asegurarse de que el [conjunto de datos](../data/get-started-datasets.md) utilizado en la implementación web [secuencia de datos](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} también esté incluido en la configuración de la creación de informes.

Es decir, al configurar los informes, si agrega un conjunto de datos que no está presente en el conjunto de datos web, estos no se mostrarán en los informes.

Aprenda a agregar conjuntos de datos para informes en [esta sección](../reports/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>El sistema de informes [!DNL Journey Optimizer] utiliza el conjunto de datos como de solo lectura y no afecta a la recopilación ni al consumo de datos.

Si **no** usa los siguientes [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target="_blank"} predefinidos para el esquema del conjunto de datos: `AEP Web SDK ExperienceEvent` y `Consumer Experience Event` (según se definen en [esta página](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}), asegúrese de agregar los siguientes grupos de campos: `Experience Event - Proposition Interactions`, `Application Details`, `Commerce Details` y `Web Details`. Los necesita el sistema de informes [!DNL Journey Optimizer], ya que rastrean en qué campañas y recorridos participa cada perfil.

[Más información sobre la configuración de informes](../reports/reporting-configuration.md)

>[!NOTE]
>
>Añadir estos grupos de campos no afecta a la recopilación de datos normal. Solo es aditivo para las páginas donde se ejecuta una campaña o un recorrido, dejando el resto del seguimiento intacto.

## Dominios de marca para recursos {#branded-domains-for-assets}

Al crear experiencias web, si agrega contenido proveniente de la biblioteca [Adobe Experience Manager Assets](../integrations/assets.md), debe configurar el subdominio que se utilizará para publicar este contenido. [Más información](web-delegated-subdomains.md)
