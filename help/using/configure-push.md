---
title: Configuración de una notificación push
description: Obtenga información sobre cómo crear una notificación push en Journey Optimizer
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 13%

---

# Configurar una notificación push {#create-push-notification}

![](assets/do-not-localize/badge.png)

Las notificaciones push se configuran al crear un mensaje, en la pestaña **[!UICONTROL Push Notification]** (consulte [Crear un mensaje](create-message.md)).

Puede configurar el contenido de las notificaciones push para los sistemas operativos iOS o Android mediante las pestañas dedicadas.

![](assets/create-content-push.png)

## Título y cuerpo

Para componer el mensaje, haga clic en los campos **[!UICONTROL Title]** y **[!UICONTROL Body]** . Utilice el Editor de expresiones para definir el contenido y los datos de personalización.

Obtenga más información sobre personalización en [esta sección](personalization/personalize.md)

Utilice la sección central para visualizar cómo se muestra la notificación push en los terminales iOS y Android.

>[!NOTE]
>
>La sección **[!UICONTROL Compose Message]** es común para las pestañas **[!UICONTROL iOS]** y **[!UICONTROL Android]** . Cualquier cambio en esta sección se aplicará a ambos sistemas operativos.

## Comportamiento del clic {#on-click-behavior}

Seleccione el comportamiento cuando un destinatario haga clic en el cuerpo de la notificación push:

* Utilice la opción **[!UICONTROL Open app]** para abrir la aplicación asociada al mensaje **[!UICONTROL Preset]**.
* Utilice la opción **[!UICONTROL Deeplink]** para redirigir el destinatario a un contenido específico ubicado dentro de la aplicación. Introduzca el vínculo profundo en el campo asociado.
* Utilice la opción **[!UICONTROL Web URL]** para redirigir el destinatario a una URL externa. Introduzca la dirección URL en el campo asociado.

## Enviar una notificación silenciosa

Una notificación push silenciosa (o notificación en segundo plano) es una instrucción oculta que se envía a la aplicación. Se utiliza, por ejemplo, para notificar a la aplicación la disponibilidad de contenido nuevo o iniciar una descarga en segundo plano.

Seleccione la opción **[!UICONTROL Silent Notification]** para notificar a la aplicación de forma silenciosa: en este caso, la notificación se transfiere directamente a la solicitud. No se muestra ninguna alerta en la pantalla del dispositivo.

Utilice la sección **[!UICONTROL Custom data]** para añadir pares clave/valor.

## Opciones avanzadas

Configure el **[!UICONTROL Advanced options]**. Los parámetros disponibles son:

| Parámetro | Disponibilidad | Descripción |
|---------|----------|---------|
| **[!UICONTROL Collapsible]** | iOS/Android | Un mensaje contraíble es un mensaje que puede reemplazarse por uno nuevo. Por ejemplo, una aplicación que actualiza a los usuarios con las últimas noticias sobre un tema. En ese caso, solo es relevante el mensaje más reciente. Por otro lado, con los mensajes no contraíbles, cada mensaje es importante para la aplicación del cliente y debe enviarse. |
| **[!UICONTROL Custom sound]** | iOS/Android | Sonido que el terminal móvil debe reproducir cuando reciba la notificación. El sonido debe estar incorporado en la aplicación. |
| **[!UICONTROL Badges]** | iOS/Android | Un distintivo se utiliza para mostrar directamente en el icono de la aplicación la cantidad de información nueva no leída. <br/>El valor del distintivo desaparece en cuanto el usuario abra o lea el nuevo contenido de la aplicación. Cuando se recibe una notificación en un dispositivo, puede actualizar o añadir un valor de distintivo para la aplicación relacionada.<br/>Por ejemplo, si está almacenando el número de artículos sin leer de sus clientes, puede aprovechar la personalización para enviar el valor de distintivo de artículos sin leer exclusivo para cada cliente. Para obtener más personalización, consulte [esta sección](personalization/personalize.md). |
| **[!UICONTROL Notification group]** / | iOS | Asocie un grupo de notificaciones a la notificación push.<br/>A partir de iOS 12, los grupos de notificaciones permiten consolidar los subprocesos de mensajes y los temas de notificación en los ID de subprocesos. Por ejemplo, una marca puede enviar notificaciones de marketing con un ID de grupo, mientras mantiene más notificaciones de tipo operativo con uno o más ID diferentes.<br/>Para ilustrarlo, puede tener groupID: 123 &quot;echa un vistazo a la nueva colección primaveral de suéters&quot; y groupID: 456 Grupos de notificación de &quot;su paquete se entregó&quot;. En este ejemplo, todas las notificaciones de entrega se incluyen en el ID de grupo: 456. |
| **[!UICONTROL Notification channel]** | Android | Asocie un canal de notificación a la notificación push.<br/>A partir de Android 8.0 (nivel de API 26), todas las notificaciones deben asignarse a un canal para que se muestre. Para obtener más información, consulte la [documentación para desarrolladores de Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** | iOS | Envía el indicador de contenido disponible en la carga útil push para garantizar que la aplicación se activa en cuanto recibe la notificación push, lo que significa que la aplicación puede acceder a los datos de carga útil.<br/> Esto funciona incluso si la aplicación se está ejecutando en segundo plano y sin necesidad de interacción del usuario (p. ej., al tocar la notificación push). Sin embargo, esto no se aplica si la aplicación no se está ejecutando. Para obtener más información, consulte la [documentación para desarrolladores de Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Add mutable-content flag]** | iOS | Envía el indicador de contenido mutable en la carga útil push y permite que el contenido de la notificación push se modifique con una extensión de aplicación de servicio de notificación proporcionada en el SDK para iOS. Para obtener más información, consulte la [documentación para desarrolladores de Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>A continuación, puede aprovechar las extensiones de la aplicación móvil para modificar aún más el contenido o la presentación de las notificaciones push entrantes enviadas desde  [!DNL Journey Optimizer] Por ejemplo, los usuarios pueden aprovechar esta opción para descifrar datos, cambiar el texto del cuerpo o del título de una notificación, añadir un identificador de subproceso a una notificación, etc. |
| **[!UICONTROL Notification visibility]** | Android | Define la visibilidad de la notificación push. <b></b> privateado mostrará la notificación en todas las pantallas de seguridad, pero ocultará información confidencial o privada en las pantallas de seguridad. <b></b> Publicar mostrará la notificación en su totalidad en todas las pantallas de seguridad. <b></b> El secretario no revelará ninguna parte de la notificación en una pantalla de seguridad. Para obtener más información, consulte la [documentación para desarrolladores de Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** | Android | Define la importancia de la notificación push de Bajo a Máx. Esto determina cuán &quot;intrusiva&quot; será la notificación push cuando se entregue. Para obtener más información, consulte la [documentación para desarrolladores de Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** | Android | Establece una prioridad alta o normal para las notificaciones push. Para obtener más información sobre la prioridad de los mensajes, consulte la [documentación para desarrolladores de Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |

## Datos personalizados

En la sección **[!UICONTROL Custom data]**, puede agregar variables personalizadas a la carga útil, según la configuración de la aplicación móvil. Para obtener más información sobre cómo configurar las notificaciones push en Adobe Experience Platform y Adobe Launch, consulte [esta sección](push-configuration.md)

