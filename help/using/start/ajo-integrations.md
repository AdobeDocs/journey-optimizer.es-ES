---
solution: Journey Optimizer
product: journey optimizer
title: Integración con otras soluciones
description: Obtenga más información sobre cómo integrar Journey Optimizer con otras soluciones
feature: Integrations
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: eef253f35bf93edbe5b64b47754e16e4c590f862
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 100%

---

# Integración con otras soluciones {#integration}

Con Adobe Journey Optimizer puede administrar, conservar y exportar fácilmente estos datos a plataformas o sistemas que forman parte de su oferta tecnológica. Estas integraciones le ayudan a abordar casos de uso específicos y a ampliar el ámbito funcional de Adobe Journey Optimizer.

>[!NOTE]
>
> Adobe Journey Optimizer, que se creó en Adobe Experience Platform, está conectado de forma nativa al [perfil del cliente en tiempo real de Adobe](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}. Esta fuente de datos integrada está preconfigurada y diseñada para recuperar y utilizar datos del perfil del cliente en tiempo real (por ejemplo, comprobar si la persona que ha introducido un recorrido es cliente o no). Permite utilizar información del perfil y datos de los eventos de experiencia. [Más información](../datasource/adobe-experience-platform-data-source.md).
>

## Adobe Customer Journey Analytics {#integration-cja}

Puede utilizar Customer Journey Analytics para llevar a cabo análisis avanzados de los datos generados por Journey Optimizer.

Journey Optimizer almacena datos en Adobe Experience Platform y, con Customer Journey Analytics, ofrece una vista integral de todos sus recorridos, campañas y ofertas con una distribución automatizada de informes y visualizaciones personalizadas de los datos.

Después de crear el recorrido en Journey Optimizer, Customer Journey Analytics puede procesar datos de la plataforma para iniciar informes y comprender el impacto de cada interacción que un cliente tiene con sus recorridos.

Más información sobre [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics {#integration-aa}

Ahora puede aprovechar todos los datos de evento de comportamiento de Adobe Analytics que ya está recopilando y transmitiendo a Adobe Experience Platform para activar recorridos en tiempo real y automatizar experiencias para los clientes. Estos datos también pueden servir para crear públicos que se puedan involucrar con Journey Optimizer.

Obtenga más información acerca de [Journey Optimizer + Analytics](../event/about-analytics.md).


## Adobe Experience Manager Assets {#integration-assets}

Una los flujos de trabajo creativos y de marketing usando [!DNL Adobe Experience Manager Assets]. Integrado de forma nativa con [!DNL Adobe Journey Optimizer], acceso [!DNL Adobe Experience Manager Assets] para almacenar, administrar, descubrir y distribuir recursos digitales. Proporciona un único repositorio centralizado de recursos que puede utilizar para completar los mensajes.

[!DNL Adobe Experience Manager Assets] se puede acceder directamente desde [!DNL Adobe Journey Optimizer] a través de la sección del menú de la izquierda **[!UICONTROL Recursos]**.

Más información sobre [Journey Optimizer + Adobe Experience Manager Assets](../content-management/assets.md).


## Adobe Stock {#integration-stock}

El plugin de integración de [!DNL Adobe Stock] y [!DNL Adobe Journey Optimizer] Diseñador de correos electrónicos proporciona a los clientes una forma sencilla de navegar, obtener licencias y guardar imágenes para utilizarlas en la creación de mensajes.

Con [!DNL Adobe Journey Optimizer], puede cargar imágenes en sus correos electrónicos directamente desde [!DNL Adobe Stock] y agregarlos a su carpeta **[!UICONTROL Recursos]** usando la opción **[!UICONTROL Buscar fotos de Adobe Stock]**. Además, la variable **[!UICONTROL Buscar fotos de Stock similares]** le ayuda a encontrar imágenes que coincidan con el contenido, el color y la composición del recurso utilizado en el envío.

Obtenga más información acerca de [Journey Optimizer + Stock](../content-management/stock.md).


## Servicios inteligentes de Adobe {#integration-intelligent-service}

Los servicios inteligentes de Adobe, nativos de la plataforma de datos del cliente en tiempo real, le permiten sacar el máximo provecho del poder que tiene la inteligencia artificial y del aprendizaje automático en casos prácticos de experiencias del cliente. Esto permite a analistas de marketing formular predicciones concretas de las necesidades de una compañía mediante configuraciones de negocio sin necesidad de tener experiencia en la ciencia de datos.

La inteligencia artificial aplicada al cliente permite a las marcas crear puntuaciones de aprendizaje automático de pérdida o conversión que estarán disponibles como atributos de perfil en Adobe Experience Platform y que se pueden utilizar para personalizar un recorrido.

[Más información](../building-journeys/ai-services-overview.md).


## Adobe Campaign {#integration-ac}

Una integración está disponible si tiene Adobe Campaign v7 o v8. Utilice esta integración para enviar correos electrónicos, notificaciones automáticas y SMS mediante las funcionalidades de mensajería transaccional de Adobe Campaign.

Obtenga más información acerca de [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

También puede configurar una integración con Adobe Campaign Standard para enviar mensajes en los recorridos.

Más información sobre [Journey Optimizer + Campaign Standard](../building-journeys/using-adobe-campaign-standard.md).


## Adobe Workfront {#integration-workfront}

Utilice los módulos de Adobe Journey Optimizer en Adobe Workfront para crear, leer, actualizar o eliminar registros, o realizar una llamada de API personalizada a la API de Adobe Journey Optimizer.

Se encuentra disponible una descripción general del paso clave de esta integración [en esta publicación de blog](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/accelerating-go-to-market-how-workfront-workfront-fusion-aep-and/ba-p/653685){target="_blank"}.

Más información sobre Journey Optimizer + Adobe Workfront [en la documentación de Adobe Workfront](https://experienceleague.adobe.com/docs/workfront/using/adobe-workfront-fusion/fusion-apps-and-modules/adobe-journey-optimizer-modules.html?lang=es){target="_blank"}.

## Canales personalizados {#integration-custom}

Si utiliza un sistema de terceros para enviar mensajes o si desea que los recorridos envíen llamadas de API a un sistema de terceros, utilice acciones personalizadas para conectarse a su recorrido. Por ejemplo, puede conectarse a los siguientes sistemas con las acciones personalizadas: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase, etc.

Las acciones personalizadas son acciones adicionales definidas por usuarios técnicos y que se ponen a disposición de los expertos en marketing. Una vez configuradas, aparecen en la paleta izquierda del recorrido en la categoría **[!UICONTROL Acción]**. Obtenga más información en [esta página](../building-journeys/about-journey-activities.md#action-activities).

Más información sobre las [acciones personalizadas](../action/about-custom-action-configuration.md).

## Fuentes de datos externas {#integration-external-systems}

Journey Optimizer le permite configurar conexiones a sistemas externos mediante fuentes de datos y acciones personalizadas. Esto hace que, por ejemplo, pueda enriquecer recorridos con datos procedentes de un sistema de reservas externo.

Aprenda a utilizar fuentes de datos externas para definir una conexión con un sistema de terceros en [esta sección](../datasource/external-data-sources.md).
