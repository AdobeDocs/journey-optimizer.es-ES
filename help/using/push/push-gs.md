---
solution: Journey Optimizer
product: journey optimizer
title: Flujo de notificaciones push en Adobe Journey Optimizer
description: Comprender el flujo y los componentes de los datos de notificaciones push
topic: Mobile
feature: Push, Overview
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: 5758c9db8b1b12367126f4adb8bd1c0bac766514
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 1%

---

# Flujo y componentes de datos de notificaciones push {#get-started-push}

Esta página le ayuda a configurar y comprender los servicios y flujos de trabajo clave relacionados con las notificaciones push en [!DNL Journey Optimizer].


>[!AVAILABILITY]
>
>El nuevo **flujo de trabajo de inicio rápido de la incorporación móvil** ya está disponible. Utilice esta nueva función de producto para configurar rápidamente Mobile SDK para que empiece a recopilar y validar datos de eventos móviles y para enviar notificaciones push móviles. Se puede acceder a esta funcionalidad a través de la página de inicio de la recopilación de datos como una versión beta pública. [Más información](mobile-onboarding-wf.md)
>

Aprenda a crear notificaciones push en [esta página](create-push.md).

Los pasos para configurar el canal push en [!DNL Adobe Journey Optimizer] se detallan en [esta página](push-configuration.md).

La siguiente ilustración muestra los sistemas y servicios involucrados con los flujos de datos asociados, y resalta cómo se entregan las notificaciones push desde un punto de vista de servicio de extremo a extremo.

![](assets/push-flow.png)

1. Registro de la aplicación móvil de marca (Android o iOS) con los servicios de mensajería push APNS y FCM de Google de Apple
1. Los servicios de mensajería generan un token push, que es un identificador que [!DNL Adobe Journey Optimizer] usará para dirigir el dispositivo específico con una notificación push.
1. El token push generado anteriormente se pasa a Adobe Experience Platform y se sincroniza con el perfil del cliente en tiempo real; esto se hace OOTB con un SDK de cliente fácil de integrar

   >[!NOTE]
   >
   >La administración de tokens difiere entre plataformas. En **Android (FCM)**, los tokens se marcan automáticamente como no válidos cuando los usuarios borran la caché de la aplicación o la vuelven a instalar, lo que genera un nuevo token y un ECID. En **iOS (APN)**, los tokens no se marcan de manera consistente como no válidos en estos escenarios. Si un perfil contiene varios ECID con tokens válidos, se enviarán notificaciones push a todos los dispositivos asociados.

1. Los mensajes push se crean en [!DNL Adobe Journey Optimizer] y los mensajes push se crean según una configuración de canal (es decir, un ajuste preestablecido de mensaje)
1. Los mensajes push se pueden incluir en el lienzo de orquestación en los Recorridos
1. Tras la publicación del Recorrido, los perfiles del cliente basados en las condiciones de Recorrido están cualificados para recibir notificaciones push y las cargas de mensajería push se personalizan en este paso
1. Las cargas push personalizadas se reenvían a un servicio de entrega de mensajería push interna
1. A continuación, este servicio interno valida las credenciales de la aplicación asociada al mensaje y
1. Envía el mensaje a los servicios de mensajería de Apple y Google para su envío final
1. Se registran los comentarios de los servicios de mensajería, los errores y los éxitos para la creación de informes en el informe Recorrido Live &amp; Customer Journey Analytics
1. Las notificaciones push se envían a los dispositivos del usuario final
1. Las interacciones de notificación push del usuario final se envían como eventos de experiencia desde el cliente del usuario final a través de la integración de SDK

## Funciones de los servicios clave en las notificaciones push {#roles-of-key-services}

* **Los proveedores de servicios de notificaciones push** son los servicios web de componentes principales que envían notificaciones de servidores remotos a aplicaciones móviles.

  [!DNL Adobe Journey Optimizer] admite plataformas Android y iOS y, en consecuencia, se integra con lo siguiente:
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging): para enviar notificaciones a la aplicación móvil de Android
   * [Servicio de notificaciones push de Apple (APN)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html): para enviar notificaciones a la aplicación móvil de iOS

* **Adobe Experience Platform Mobile SDK** que proporciona API de integración del lado del cliente para sus móviles a través de SDK compatibles con Android y iOS. SDK proporciona una extensión [!DNL Adobe Journey Optimizer] que expone una variedad de API específicas para la mensajería push y habilita el flujo de datos, como el registro del token push o el envío de eventos de seguimiento push o cualquier otro evento de experiencia personalizado a Adobe Experience Platform. SDK también proporciona otras extensiones que habilitan otras funciones de Adobe Experience Cloud y de socios de terceros.

  La integración con SDK también requiere la configuración de los servicios de [recopilación de datos](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=es){target="_blank"} de Adobe Experience Platform, como:

   * Creación de una secuencia de datos para configurar los conjuntos de datos de perfil y evento de experiencia con los que los datos fluyen a Adobe Experience Platform
   * Crear una propiedad móvil del lado del cliente y agregar extensiones. SDK se integra estrechamente con estas extensiones para ofrecer una experiencia de recopilación de datos fluida.
   * Registro del identificador del paquete de aplicaciones móviles y de las credenciales de la aplicación

* **El perfil del cliente en tiempo real de Adobe Experience Platform** mantiene una vista integral de cada cliente individual al combinar datos de varios canales, incluidos web, móvil, CRM y de terceros. El perfil le permite consolidar los datos de sus clientes en una vista unificada, lo que ofrece una cuenta procesable con marca de tiempo de cada interacción con los clientes. El token push de un usuario determinado de la aplicación se almacena en el perfil del usuario como datos de registro, mientras que las interacciones que el usuario realiza con las notificaciones push se rastrean como datos de eventos de series temporales. [Obtenga más información acerca del Perfil del cliente en tiempo real de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}.

* **[!DNL Adobe Journey Optimizer]** : una vez que las integraciones de la aplicación móvil con los componentes mencionados estén implementadas y los perfiles del cliente estén en Adobe Experience Platform, puede crear y organizar notificaciones push en [!DNL Adobe Journey Optimizer] para interactuar con los usuarios.

## Configuración técnica push y flujos de trabajo del profesional {#push-technical-setup}

La siguiente ilustración muestra los distintos pasos, de extremo a extremo, necesarios para configurar los componentes que forman el esqueleto del flujo de datos push. Los elementos de acción se han clasificado según la función que realiza la configuración y el componente que se configura.

![](assets/user-flow.png)

**Temas relacionados**

* [Configuración del canal push](push-configuration.md)
* [Informe de notificaciones push](../reports/journey-global-report-cja-push.md)
* [Crear una notificación push](create-push.md)
* [Añadir un mensaje en un recorrido](../building-journeys/journeys-message.md)
* [Añadir un mensaje en una campaña](../campaigns/create-campaign.md)