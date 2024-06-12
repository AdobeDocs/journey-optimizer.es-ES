---
title: Requisitos previos y protecciones de experiencias basadas en código
description: Para poder editar aplicaciones y páginas web con la función basada en código de Journey Optimizer, siga los requisitos previos de esta página
feature: Code-based Experiences
topic: Content Management
role: Admin
level: Experienced
exl-id: ac901f88-5fde-4220-88c6-fe05433866cc
source-git-commit: 83e93b18a3f5a8e688ad519d3e1c0d70d91dfc9f
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 2%

---

# Mecanismos de protección y requisitos previos {#web-prerequisites}

Para poder usar acciones de experiencia basadas en código en [!DNL Journey Optimizer] y enviar una carga útil de contenido de código que puedan utilizar las aplicaciones, siga los requisitos previos siguientes:

* Para agregar modificaciones a las aplicaciones, debe tener una implementación específica. [Más información](#implementation-prerequisites)

* Para que las experiencias basadas en código se entreguen correctamente, asegúrese de definir la configuración detallada de Adobe Experience Platform [aquí](#delivery-prerequisites).

>[!CAUTION]
>
>* El canal de experiencia basada en código no está disponible para organizaciones que hayan adquirido el Adobe **Healthcare Shield** y **Escudo de seguridad y privacidad** ofertas de complementos.
>
>* Solo puede crear experiencias basadas en código en **campañas**. [Más información](../campaigns/create-campaign.md#configure).


## Requisitos previos de implementación {#implementation-prerequisites}

La experiencia basada en código admite cualquier tipo de implementación del cliente, como se muestra en las opciones siguientes. Puede utilizar un método de implementación del lado del cliente, del lado del servidor o híbrido para sus propiedades:

* Solo del lado del cliente: para agregar modificaciones a sus páginas web o aplicaciones móviles, debe implementar el [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=es){target="_blank"} en su sitio web o [SDK de Adobe Experience Platform Mobile](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} en sus aplicaciones móviles.

* Modo híbrido: puede utilizar el [API de servidor de Edge Network de AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} para solicitar la personalización del lado del servidor; la respuesta se proporciona al SDK web de Adobe Experience Platform para procesar las modificaciones del lado del cliente. Obtenga más información en Adobe Experience Platform [Documentación de API de Edge Network Server](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/overview.html){target="_blank"}. Puede obtener más información sobre el modo híbrido y ver algunos ejemplos de implementación en [esta publicación de blog](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}.

* Del lado del servidor: puede utilizar el [API de servidor de Edge Network de AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html){target="_blank"} para solicitar personalización del lado del servidor. El equipo de desarrollo debe gestionar la respuesta y procesar las modificaciones del lado del cliente en la implementación de la aplicación.

Puede encontrar ejemplos para cada uno de los métodos de implementación anteriores en [esta sección](code-based-implementation-samples.md).

## Requisitos previos de envío {#delivery-prerequisites}

Para que las experiencias basadas en código se entreguen correctamente, se debe definir la siguiente configuración:

* En el [Recopilación de datos de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=es){target="_blank"}, asegúrese de que tiene un conjunto de datos definido como en **[!UICONTROL Adobe Experience Platform]** servicio que tiene el **[!UICONTROL Adobe Journey Optimizer]** opción activada.

  Esto garantiza que Adobe Experience Platform Edge gestione correctamente los eventos entrantes de Journey Optimizer. [Más información](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](../web/assets/web-aep-datastream-ajo.png)

* Entrada [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}, asegúrese de tener una política de combinación con **[!UICONTROL Política de combinación activa en Edge]** opción activada. Para ello, seleccione una política en **[!UICONTROL Cliente]** > **[!UICONTROL Perfiles]** > **[!UICONTROL Políticas de combinación]** menú Experience Platform. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  Esta política de combinación la utiliza [!DNL Journey Optimizer] canales entrantes para activar y publicar correctamente campañas entrantes en edge. [Más información](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=es){target="_blank"}

  ![](../web/assets/web-aep-merge-policy.png)

* Para solucionar los problemas de entrega de las experiencias web de Journey Optimizer, puede usar la variable **Entrega en Edge** ver en **Adobe Experience Platform Assurance**. Este complemento le permite inspeccionar en detalle las llamadas de solicitud, comprobar si las llamadas perimetrales esperadas se producen según lo previsto y examinar los datos de perfil, incluidos los mapas de identidad, las suscripciones a segmentos y la configuración de consentimiento. Además, puede revisar las actividades para las que la solicitud cumple los requisitos e identificar las que no.

  Uso del **Entrega en Edge** Este complemento le ayuda a obtener la información necesaria para comprender y solucionar problemas de las implementaciones entrantes de forma eficaz.

  [Más información sobre la Vista de entrega de Edge](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/view/edge-delivery)

## Requisitos previos del experimento de contenido {#experiment-prerequisites}

Para habilitar experimentos de contenido para el canal basado en código, debe asegurarse de que la variable [conjunto de datos](../data/get-started-datasets.md) se utiliza en la implementación de la aplicación [secuencia de datos](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} también se incluye en la configuración de informes.

En otras palabras, al configurar los informes de experimentos, si agrega un conjunto de datos que no está presente en el conjunto de datos de la aplicación, los datos de la aplicación no se mostrarán en los informes de experimentos de contenido.

Aprenda a añadir conjuntos de datos para la creación de informes de experimentos de contenido en [esta sección](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>El conjunto de datos lo utiliza solo lectura el [!DNL Journey Optimizer] sistema de informes de y no afecta a la recopilación ni a la ingesta de datos.
