---
title: Introducción a la configuración push
description: Comprender el flujo de datos y los componentes de las notificaciones push
topic: Mobile
feature: Push
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: b43e3432ede1d4985e0a6b57b57c5efc3cf60c50
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 5%

---

# Introducción a la configuración push {#get-started-push}

Esta página le ayudará a configurar y comprender los servicios y flujos de trabajo clave que intervienen en las notificaciones push en [!DNL Journey Optimizer]. Obtenga información sobre cómo crear notificaciones push en [esta página](create-push.md).

Pasos para configurar el canal push en [!DNL Adobe Journey Optimizer] se detallan en [esta página](push-configuration.md).

## Notificaciones push y [!DNL Adobe Journey Optimizer] {#push-notifications-and-journey-optimizer}

En el siguiente gráfico se muestran los sistemas y servicios implicados en los flujos de datos asociados, lo que destaca cómo se entregan las notificaciones push desde un punto de vista de servicio integral.

![](assets/push-flow.png)

1. Registro de su aplicación móvil con marca (Android o iOS) con APNS de Apple y servicios de mensajería push FCM de Google
1. Los servicios de mensajería generan un token push, que es un identificador de [!DNL Adobe Journey Optimizer] se utilizará para dirigir el dispositivo específico con una notificación push.
1. El token push generado anteriormente se pasa a Adobe Experience Platform y se sincroniza con el perfil del cliente en tiempo real; esto se hace OOTB con un SDK de cliente fácil de integrar
1. Los mensajes push se crean en [!DNL Adobe Journey Optimizer], los mensajes push se crean con un ajuste preestablecido de mensaje
1. Los mensajes push se pueden incluir en el lienzo de organización de Recorrido
1. Tras la publicación del Recorrido, los perfiles de clientes basados en condiciones de Recorrido están cualificados para recibir notificaciones push, las cargas de mensajería push se personalizan en este paso
1. Las cargas push personalizadas se reenvían a un servicio de entrega de mensajería push interna
1. A continuación, este servicio interno valida las credenciales de la aplicación asociada al mensaje y
1. Envía el mensaje a los servicios de mensajería de Apple y Google para su envío final
1. Se anotan los comentarios de los servicios de mensajería, se registran errores y éxitos para los informes en los informes de Recorrido Live &amp; Global
1. Las notificaciones push se envían a los dispositivos del usuario final
1. Las interacciones de notificaciones push del usuario final se envían como eventos de experiencia desde el cliente del usuario final mediante la integración del SDK

## Funciones de los servicios clave en las notificaciones push {#roles-of-key-services}

* **Proveedores de servicios de notificaciones push** son los servicios web de componentes principales que envían notificaciones de servidores remotos a aplicaciones móviles.

   [!DNL Adobe Journey Optimizer]  es compatible con las plataformas Android y iOS y, por lo tanto, se integra con lo siguiente:
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging) - para enviar notificaciones a la aplicación móvil de Android
   * [Servicio de notificaciones push de Apple (APNS)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) - para enviar notificaciones a la aplicación móvil de iOS

* **SDK de Adobe Experience Platform Mobile** que proporciona API de integración del lado del cliente para sus móviles mediante SDK compatibles con Android y iOS. El SDK proporciona un [!DNL Adobe Journey Optimizer] que expone una variedad de API específicas para la mensajería push y habilita el flujo de datos, como registrar el token push o enviar eventos de seguimiento push o cualquier otro evento de experiencia personalizada a Adobe Experience Platform. El SDK también proporciona otras extensiones que habilitan otras funcionalidades de Adobe Experience Cloud, así como de socios de terceros.

   La integración del SDK también requiere la configuración de Adobe Experience Platform [Recopilación de datos](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=es){target=&quot;_blank&quot;} servicios como:

   * Creación de un conjunto de datos para configurar los conjuntos de datos de evento de perfil y experiencia con los que los datos fluyen a Adobe Experience Platform
   * Creación de una propiedad móvil del lado del cliente y adición de extensiones. El SDK se integra estrechamente con estas extensiones para ofrecer una experiencia de recopilación de datos perfecta.
   * Registro del identificador del paquete de aplicaciones móviles y las credenciales de la aplicación

* **Perfil del cliente en tiempo real de Adobe Experience Platform**  mantiene una vista integral de cada cliente individual combinando datos de varios canales, incluidos web, móvil, CRM y terceros. El perfil le permite consolidar los datos de sus clientes en una vista unificada que ofrece una cuenta procesable con marca de tiempo de cada interacción con los clientes. El token push de un usuario de aplicación determinado se almacena en el perfil del usuario como datos de registro, mientras que las interacciones del usuario con las notificaciones push se rastrean como datos de eventos de series temporales. [Obtenga más información sobre el Perfil del cliente en tiempo real de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target=&quot;_blank&quot;}.

* **[!DNL Adobe Journey Optimizer]** : una vez que haya implementado las integraciones de su aplicación móvil con los componentes mencionados y sus perfiles de cliente en Adobe Experience Platform, puede crear y orquestar notificaciones push en [!DNL Adobe Journey Optimizer] para interactuar con los usuarios.

## Ajustes técnicos push y flujos de trabajo de practicantes {#push-technical-setup}

En el siguiente tutorial se muestran los distintos pasos, de principio a fin, necesarios para configurar los componentes que forman el esqueleto del flujo de datos push. Los elementos de acción se han clasificado según la función que realiza la configuración y el componente que se está configurando.

![](assets/user-flow.png)
