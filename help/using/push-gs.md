---
title: Introducción a la configuración push
description: Comprender el flujo de datos y los componentes de las notificaciones push
feature: Configuración de la aplicación
topic: Push
role: Administrator
level: Intermediate
source-git-commit: 9872df0ac91fff249a7b41ecd99b7c25c25463a9
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 2%

---

# Introducción a la configuración push {#get-started-push}

Las notificaciones push le ayudan a llegar a sus usuarios de aplicaciones móviles en cualquier momento, especialmente cuando no utilizan activamente su aplicación. Las notificaciones push pueden ayudarle a lograr una variedad de casos de uso, como proporcionar actualizaciones sobre el servicio, solicitar al usuario que tome medidas, avisar al usuario de una nueva oferta, etc. Las plataformas de dispositivo requieren la inclusión antes de que los usuarios finales puedan recibir o ver sus notificaciones. La inclusión del usuario puede recibirse tan pronto como se inicia la aplicación por primera vez después de la instalación o en una sesión o flujo de trabajo posterior, según corresponda. [!DNL Journey Optimizer] admite notificaciones push y le ayuda a enviar notificaciones muy relevantes a tasas de rendimiento líderes en el sector. Las notificaciones push pueden incluir personalización y contexto basado en Recorridos para aprovechar la información de datos que su marca tiene con Adobe Experience Cloud.

Esta página le ayudará a configurar y comprender los servicios y flujos de trabajo clave relacionados con las notificaciones push en [!DNL Journey Optimizer].

Los pasos para configurar el canal push en [!DNL Adobe Journey Optimizer] se detallan en [esta página](push-configuration.md).

## Notificaciones push y Adobe Journey Optimizer

En el siguiente gráfico se muestran los sistemas y servicios implicados en los flujos de datos asociados, lo que destaca cómo se entregan las notificaciones push desde un punto de vista de servicio integral.

![](assets/push-flow.png)

1. Registro de su aplicación móvil con marca (Android o iOS) con los servicios de mensajería push APNS y FCM de Google de Apple
1. Los servicios de mensajería generan un token push, que es un identificador que Adobe Journey Optimizer utilizará para dirigirse al dispositivo específico con una notificación push.
1. El token push generado anteriormente se pasa a Adobe Experience Platform y se sincroniza con el perfil del cliente en tiempo real; esto se hace OOTB con un SDK de cliente fácil de integrar
1. Los mensajes push se crean en Adobe Journey Optimizer, los mensajes push se crean con un ajuste preestablecido de mensaje
1. Los mensajes push se pueden incluir en el lienzo de organización de Recorrido
1. Tras la publicación del Recorrido, los perfiles de clientes basados en condiciones de Recorrido están cualificados para recibir notificaciones push, las cargas de mensajería push se personalizan en este paso
1. Las cargas push personalizadas se reenvían a un servicio de entrega de mensajería push interna
1. A continuación, este servicio interno valida las credenciales de la aplicación asociada al mensaje y
1. Envía el mensaje a los servicios de mensajería de Apple y Google para su envío final
1. Se anotan los comentarios de los servicios de mensajería, se registran errores y éxitos para los informes en los informes de Recorrido Live &amp; Global
1. Las notificaciones push se envían a los dispositivos del usuario final
1. Las interacciones de notificaciones push del usuario final se envían como eventos de experiencia desde el cliente del usuario final mediante la integración del SDK

## Funciones de los servicios clave en las notificaciones push

* **Los** proveedores de servicios de notificaciones push son los servicios web de componentes principales que envían notificaciones de servidores remotos a aplicaciones móviles.

   [!DNL Adobe Journey Optimizer]  admite plataformas Android e iOS y, por lo tanto, se integra con lo siguiente:
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging) : para enviar notificaciones a la aplicación móvil de Android
   * [Servicio de notificaciones push de Apple (APNS)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) : para enviar notificaciones a la aplicación móvil iOS

* **Adobe Experience Platform Mobile** SDK, que proporciona API de integración del lado del cliente para sus móviles mediante SDK compatibles con Android y iOS. El SDK proporciona una extensión de Adobe Journey Optimizer que expone una serie de API específicas para la mensajería push y permite el flujo de datos, como registrar el token push o enviar eventos de seguimiento push o cualquier otro evento de experiencia personalizado a Adobe Experience Platform. El SDK también proporciona otras extensiones que habilitan otras funcionalidades de Adobe Experience Cloud, así como de socios de terceros.

   La integración del SDK también requiere la configuración de servicios de recopilación de datos [Adobe Experience Platform](https://experienceleague.adobe.com/docs/launch/using/home.html?lang=es) como:

   * Creación de un conjunto de datos para configurar los conjuntos de datos de evento de perfil y experiencia con los que los datos fluyen a Adobe Experience Platform
   * Creación de una propiedad móvil del lado del cliente y adición de extensiones. El SDK se integra estrechamente con estas extensiones para ofrecer una experiencia de recopilación de datos perfecta.
   * Registro del identificador del paquete de aplicaciones móviles y las credenciales de la aplicación

* **El perfil del cliente en tiempo real de Adobe Experience Platform**  conserva una vista holística de cada cliente al combinar datos de varios canales, incluidos web, móvil, CRM y terceros. El perfil le permite consolidar los datos de sus clientes en una vista unificada que ofrece una cuenta procesable con marca de tiempo de cada interacción con los clientes. El token push de un usuario de aplicación determinado se almacena en el perfil del usuario como datos de registro, mientras que las interacciones del usuario con las notificaciones push se rastrean como datos de eventos de series temporales. [Obtenga más información sobre el Perfil del cliente en tiempo real de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)

* **[!DNL Adobe Journey Optimizer]** : una vez que haya implementado las integraciones de su aplicación móvil con los componentes mencionados y sus perfiles de cliente en Adobe Experience Platform, puede crear y orquestar notificaciones push en Adobe Journey Optimizer para interactuar con los usuarios.

## Ajustes técnicos push y flujos de trabajo de practicantes

En el siguiente tutorial se muestran los distintos pasos, de principio a fin, necesarios para configurar los componentes que forman el esqueleto del flujo de datos push. Los elementos de acción se han clasificado según la función que realiza la configuración y el componente que se está configurando.

![](assets/user-flow.png)
