---
title: Introducción a la configuración push
description: Comprender el flujo de datos y los componentes de las notificaciones push
hide: true
hidefromtoc: true
source-git-commit: a2eee802f82552e56ced00f93e5e4c8a7b3feb7a
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%

---

# Introducción a la configuración push {#get-started-push}

![](assets/do-not-localize/badge.png)

Las notificaciones push sirven como canal de comunicación rápida que le permite transmitir mensajes, ofertas u otra información a los usuarios de la aplicación móvil. Normalmente, el usuario final debe incluirse en para recibir notificaciones push; la inclusión suele tener lugar durante el proceso de instalación y los usuarios finales disponen de una forma de administrar las notificaciones si cambian de opinión más adelante. Una ventaja importante de las notificaciones push en la computación móvil es que la tecnología no requiere que se abran aplicaciones específicas en un dispositivo móvil para recibir un mensaje. Esto permite que un smartphone reciba y muestre notificaciones incluso cuando la pantalla del dispositivo está bloqueada y la aplicación móvil está en segundo plano o cerrada.

**[!DNL Adobe Journey Optimizer]**  le permite enviar mensajes push personalizados, relevantes y que distinguen el tiempo a gran escala. Se puede segmentar un segmento de perfiles de clientes para recibir notificaciones push enriquecidas en sus dispositivos móviles iOS y Android. Estos segmentos se pueden crear en función de eventos de experiencia de usuario pasados o activos, datos de registro de usuarios o una combinación de interacciones de usuarios y datos. Una vez que un recorrido está activo, puede ver informes detallados sobre la cantidad de mensajes enviados, fallidos por el motivo y también información de seguimiento push como el número de usuarios que hicieron clic en ellos.

Este documento le guiará por un flujo de datos de extremo a extremo básico de las notificaciones push mediante [!DNL Journey Optimizer] y un diagrama de flujo de usuario para explicar cómo cada función cumple sus responsabilidades y colabora para unir el flujo de datos push.


## Componentes y servicios implicados

* **Los** proveedores de Cloud Messaging son servicios de terceros que nos permiten enviar notificaciones desde servidores remotos a aplicaciones móviles.

   [!DNL Adobe Journey Optimizer]  admite plataformas Android e iOS y gestiona dos servicios principales de mensajería en la nube:
   * Firebase Cloud Messaging (FCM): para enviar notificaciones a la aplicación móvil de Android
   * Servicio de notificaciones push de Apple (APNS): para enviar notificaciones a la aplicación móvil de iOS

* **Aplicación móvil integrada con el** SDK móvil de Adobe, que ayuda a integrar sus aplicaciones móviles con las soluciones de Adobe Experience Cloud. El SDK de Mobile se compone de varias extensiones de solución de Experience Cloud para proporcionar funciones específicas del servicio que representan. Estas extensiones exponen varias API para habilitar el flujo de datos, como registrar el token push o enviar eventos de seguimiento push o cualquier otro evento de experiencia personalizado a Adobe Experience Platform.

* **Adobe Launch**  (o Recopilación de datos) es la nueva generación de funcionalidades de administración de SDK móviles que permite el flujo de datos desde el SDK móvil a  [!DNL Adobe Experience Platform]. Proporciona funciones para registrar extensiones, crear reglas y elementos de datos para enviar datos desde la aplicación móvil a las soluciones de Adobe Experience Cloud. Con respecto al flujo de datos de las notificaciones push, las configuraciones principales necesarias en Launch de Adobe son:

   * Creación de un conjunto de datos para configurar los conjuntos de datos de evento de perfil y experiencia con los que los datos fluyen a experience platform.
   * Creación de una propiedad móvil del lado del cliente y adición de extensiones. El SDK de Mobile se integra estrechamente con estas extensiones para ofrecer una experiencia de recopilación de datos perfecta.
   * Registro del identificador del paquete de aplicaciones móviles y las credenciales de la aplicación que ayudarían a identificar y validar de forma exclusiva la coherencia de la aplicación en el momento de enviar la notificación push.

* **El perfil del cliente en tiempo** real es el componente de Adobe Experience Platform que le permite ver una vista holística de cada cliente combinando datos de varios canales, incluidos la web, dispositivos móviles, CRM y terceros. El perfil le permite consolidar los datos de sus clientes en una vista unificada que ofrece una cuenta procesable con marca de tiempo de cada interacción con los clientes. Los datos estáticos que identifican al usuario de la aplicación móvil, como un token push, se almacenan en el perfil del usuario como datos de registro, mientras que las interacciones que el usuario realiza con las notificaciones push se rastrean como datos de eventos de series temporales.

* **[!DNL Adobe Journey Optimizer]** : una vez que haya implementado las integraciones de su aplicación móvil con los componentes mencionados y los perfiles de cliente estén disponibles como perfiles de cliente en tiempo real, puede aprovechar las potentes capacidades de segmentación de audiencia en  [!DNL Adobe Journey Optimizer]  para garantizar una experiencia óptima para cada persona.


## Flujo de datos push

Este diagrama muestra un flujo de datos de mensajería push básico y ofrece una vista previa de los distintos productos de Adobe y componentes involucrados en el flujo.

![](assets/push-flow.png)


1. El cliente desarrolla una aplicación móvil en Android o iOS que entregaría a sus usuarios. Para utilizar la capacidad push proporcionada por los proveedores push (es decir, APNS por Apple y FCM por Google), la aplicación móvil se registra a sí misma y habilita la capacidad push.
1. Los proveedores push generan y envían un token push a la aplicación móvil. Un token push es un identificador que los remitentes utilizan para dirigirse a dispositivos específicos con una notificación push.
1. La aplicación móvil está integrada con el SDK de Adobe Mobile, que expone varias extensiones y API. La extensión Messaging expone una API para registrar el token push en Adobe Experience Platform con el perfil del cliente.
1. Una vez que la aplicación móvil está lista, se configura en **[!DNL Journey Launch]** `>` **Configuraciones de la aplicación** junto con las credenciales.
El especialista en marketing ahora crea una notificación push en **[!DNL Adone Journey Optimizer]** `>` **Messages** en la aplicación móvil registrada.
1. El especialista en marketing organiza un recorrido de cliente que define el flujo de eventos y acciones. Para enviar una notificación push en una fase del recorrido, el especialista en marketing añade una acción de tipo &quot;Mensaje&quot; y la asocia al mensaje creado en el paso anterior.
1. Siempre que un perfil de cliente reúne los requisitos para recibir la notificación push por cualquier motivo, como en déclencheur de un evento o en la calificación de un segmento, el mensaje se personaliza según el perfil, si corresponde.
1. El mensaje push personalizado se envía para su procesamiento posterior al servicio de entrega push.
1. El servicio de envío push valida las credenciales de la aplicación asociada al mensaje.
1. El mensaje se envía a los proveedores push para su envío a la aplicación móvil con las credenciales y el token push específicos.
1. Los proveedores de mensajes push envían comentarios sugiriendo si el mensaje se entregó correctamente al proveedor o no. En caso contrario, el mensaje de error relevante forma parte de los comentarios. Estos comentarios se envían a los informes de Adobe para que el cliente los vea en su Recorrido [Live](reports/live-report.md) y [Global Reports](reports/global-report.md).
1. Mientras tanto, los proveedores push envían de forma asíncrona la notificación push correcta a la aplicación móvil.
1. A medida que el cliente interactúa con la notificación, las impresiones como clic/apertura se pueden rastrear como **Eventos de experiencia**. La extensión de mensajería expone las API para enviar eventos de seguimiento a Adobe Experience Platform con respecto al perfil del cliente.

## Flujo de usuario push

Este diagrama muestra los distintos pasos necesarios para configurar los componentes que forman el esqueleto del flujo de datos push. Los elementos de acción se han clasificado según la función que realiza la configuración y el componente que se está configurando. Como puede ver, antes de empezar a enviar notificaciones push con **[!DNL Adobe Journey Optimizer]** , debe asegurarse de que las configuraciones y las integraciones estén implementadas en la aplicación móvil, **[!DNL Adobe Launch]** y **[!DNL Adobe Experience Platform]**.

![](assets/user-flow.png)

Los pasos detallados para configurar el canal push y habilitar las notificaciones push en [!DNL Journey Optimizer] están disponibles en [esta página](push-configuration.md).