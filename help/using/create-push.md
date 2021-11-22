---
title: Configuración de una notificación push
description: Obtenga información sobre cómo crear una notificación push en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 13%

---

# Crear una notificación push {#create-push-notification}

Una vez que [crear un mensaje](create-message.md), haga clic en **[!UICONTROL Push Notification]** para definir la configuración y el contenido de la notificación push.

![](assets/create-content-push.png)

Utilice las pestañas dedicadas para definir la configuración de las notificaciones push para **iOS** y **Android** sistemas operativos.

>[!NOTE]
>
>La variable **[!UICONTROL Compose Message]** es común a **[!UICONTROL iOS]** y **[!UICONTROL Android]** pestañas. Cualquier cambio en esta sección se aplicará a ambas pestañas.

## Título y cuerpo

Para componer el mensaje, haga clic en el botón **[!UICONTROL Title]** y **[!UICONTROL Body]** campos. Utilice el Editor de expresiones para definir el contenido y los datos de personalización. Obtenga más información sobre personalización en el Editor de expresiones en [esta sección](personalization/personalize.md)

Utilice la sección de vista previa del dispositivo para visualizar cómo se muestra la notificación push en los dispositivos iOS y Android.

## Comportamiento al hacer clic {#on-click-behavior}

Seleccione el comportamiento cuando un destinatario haga clic en el cuerpo de la notificación push.

![](assets/title-body-push.png)

* Utilice la variable **[!UICONTROL Open app]** para abrir la aplicación asociada al mensaje **[!UICONTROL Preset]**.
* Utilice la variable **[!UICONTROL Deeplink]** para redirigir el destinatario a un contenido específico ubicado dentro de la aplicación. Introduzca el vínculo profundo en el campo asociado.
* Utilice la variable **[!UICONTROL Web URL]** para redirigir el destinatario a una URL externa. Introduzca la dirección URL en el campo asociado.

## Añadir medios

En la versión iOS de la notificación push, puede añadir una imagen, un vídeo o un GIF que se mostrarán en la notificación.

En la versión de Android, solo puede agregar un icono de imagen y una imagen para notificaciones expandidas.

![](assets/push-config-add-media.png)

Hay dos opciones disponibles. Puede:

* Haga clic en el **[!UICONTROL Add media]** para seleccionar un recurso en **[!DNL Adobe Experience Manager Assets Essentials]**.

   Aprenda a utilizar **[!DNL Adobe Experience Manager Assets Essentials]** en [esta página](assets-essentials.md).

* O introduzca la dirección URL del medio haciendo clic en el **[!UICONTROL Add media]** campo . En ese caso, puede añadir personalización.

Una vez añadido, el contenido se muestra a la derecha del cuerpo de notificación.

## Agregar botones

Puede crear una notificación procesable añadiendo botones al contenido push.

Si la pantalla del dispositivo está bloqueada, estos botones no se muestran: solo la variable **Título** y **Mensaje** de la notificación están visibles. Si el dispositivo está desbloqueado, los destinatarios verán los botones.

En la versión de iOS, puede añadir hasta 4 botones. En la versión de Android, puede añadir hasta 3 botones.

>[!NOTE]
>
>Para iOS, use la variable **[!UICONTROL iOS category]** para asociar acciones con una categoría de notificación.

Haga clic en **[!UICONTROL Add button]** para definir la configuración: la etiqueta y la acción asociada. Las acciones posibles son las mismas que para [comportamiento al hacer clic](#on-click-behavior).

Haga clic en **[!UICONTROL Expand view]** para previsualizar los botones personalizados.

![](assets/push_buttons.png)

## Enviar una notificación silenciosa

Una notificación push silenciosa (o notificación en segundo plano) es una instrucción oculta que se envía a la aplicación. Se utiliza, por ejemplo, para notificar a la aplicación la disponibilidad de contenido nuevo o iniciar una descarga en segundo plano.

Seleccione el **[!UICONTROL Silent Notification]** para notificar de forma silenciosa a la aplicación: en este caso, la notificación se transfiere directamente a la solicitud. No se muestra ninguna alerta en la pantalla del dispositivo.

Utilice la variable **[!UICONTROL Custom data]** para agregar pares clave-valor.

## Datos personalizados

En el **[!UICONTROL Custom data]** , puede agregar variables personalizadas a la carga útil, según la configuración de la aplicación móvil. Para obtener más información sobre cómo configurar las notificaciones push en Adobe Experience Platform y Adobe Launch, consulte [esta sección](push-gs.md)

## Opciones avanzadas

Puede configurar **[!UICONTROL Advanced options]** para la notificación push. A continuación se enumeran los parámetros disponibles:

| Parámetro | Descripción |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS/Android) | Un mensaje contraíble es un mensaje que puede reemplazarse por un mensaje nuevo si ha quedado obsoleto. Algunos casos de uso habituales de mensajes contraíbles son los mensajes que se utilizan para indicar a una aplicación móvil que sincronice datos del servidor. Un ejemplo sería una aplicación deportiva que actualiza a los usuarios con la puntuación más reciente. Solo es relevante el mensaje más reciente. Por otro lado, con un mensaje que no se puede contraer, cada mensaje es importante para la aplicación del cliente y debe entregarse. |
| **[!UICONTROL Custom sound]** (iOS/Android) | Sonido que el terminal móvil debe reproducir cuando reciba la notificación. El sonido debe estar incorporado en la aplicación. |
| **[!UICONTROL Badges]** (iOS/Android) | Un distintivo se utiliza para mostrar directamente en el icono de la aplicación la cantidad de información nueva no leída. <br/>El valor del distintivo desaparece en cuanto el usuario abra o lea el nuevo contenido de la aplicación. Cuando se recibe una notificación en un dispositivo, puede actualizar o añadir un valor de distintivo para la aplicación relacionada.<br/>Por ejemplo, si está almacenando el número de artículos sin leer de sus clientes, puede aprovechar la personalización para enviar el valor de distintivo de artículos sin leer exclusivo para cada cliente. Para obtener más personalización, consulte [esta sección](personalization/personalize.md). |
| **[!UICONTROL Notification group]**  (solo iOS) | Asocie un grupo de notificaciones a la notificación push.<br/>A partir de iOS 12, los grupos de notificaciones permiten consolidar los subprocesos de mensajes y los temas de notificación en los ID de subprocesos. Por ejemplo, una marca puede enviar notificaciones de marketing con un ID de grupo, mientras mantiene más notificaciones de tipo operativo con uno o más ID diferentes.<br/>Para ilustrarlo, puede tener groupID: 123 &quot;echa un vistazo a la nueva colección primaveral de suéters&quot; y groupID: 456 Grupos de notificación de &quot;su paquete se entregó&quot;. En este ejemplo, todas las notificaciones de entrega se incluyen en el ID de grupo: 456. |
| **[!UICONTROL Notification channel]** (solo Android) | Asocie un canal de notificación a la notificación push.<br/>A partir de Android 8.0 (nivel de API 26), todas las notificaciones deben asignarse a un canal para que se muestre. Para obtener más información, consulte [Documentación para desarrolladores de Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** (solo iOS) | Envía el indicador de contenido disponible en la carga útil push para garantizar que la aplicación se activa en cuanto recibe la notificación push, lo que significa que la aplicación puede acceder a los datos de carga útil.<br/> Esto funciona incluso si la aplicación se está ejecutando en segundo plano y sin necesidad de interacción del usuario (p. ej., al tocar la notificación push). Sin embargo, esto no se aplica si la aplicación no se está ejecutando. Para obtener más información, consulte la [documentación para desarrolladores de Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Add mutable-content flag]** (solo iOS) | Envía el indicador de contenido mutable en la carga útil push y permite que el contenido de la notificación push se modifique con una extensión de aplicación de servicio de notificación proporcionada en el SDK de iOS. Para obtener más información, consulte la [documentación para desarrolladores de Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Puede aprovechar las extensiones de la aplicación móvil para modificar aún más el contenido o la presentación de las notificaciones push entrantes enviadas desde [!DNL Journey Optimizer]. Por ejemplo, los usuarios pueden aprovechar esta opción para descifrar datos, cambiar el texto del cuerpo o el título de una notificación, añadir un identificador de subproceso a una notificación, etc. |
| **[!UICONTROL Notification visibility]** (solo Android) | Define la visibilidad de la notificación push. <br/><b>Privado</b> mostrará la notificación en todas las pantallas de seguridad, pero ocultará información confidencial o privada en las pantallas de seguridad. <br/><b>Público</b> mostrará la notificación en su totalidad en todas las pantallas de seguridad. <br/><b>Secreto</b> no revelará ninguna parte de la notificación en una pantalla de bloqueo segura. <br/>Para obtener más información, consulte [Documentación para desarrolladores de Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** (solo Android) | Define la importancia de la notificación push de Bajo a Máx. Esto determina cuán &quot;intrusiva&quot; será la notificación push cuando se entregue. Para obtener más información, consulte [Documentación para desarrolladores de Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** (solo Android) | Establece una prioridad alta o normal para las notificaciones push. Para obtener más información sobre la prioridad de los mensajes, consulte la [documentación para desarrolladores de Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |

**Temas relacionados**

<!--
* [Understand push notification flow](push-gs.md)
-->

* [Configurar el canal push](push-gs.md)
* [Crear un nuevo mensaje](create-message.md)
* [Adición de un mensaje en un recorrido](building-journeys/journeys-message.md)
