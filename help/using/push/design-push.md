---
solution: Journey Optimizer
product: journey optimizer
title: Diseño de una notificación push
description: Aprenda a diseñar una notificación push en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 14%

---

# Diseño de una notificación push {#design-push-notification}

## Título y cuerpo {#push-title-body}

Para redactar el mensaje, haga clic en el **[!UICONTROL Título]** y **[!UICONTROL Cuerpo]** campos. Utilice el Editor de expresiones para definir contenido, personalizar datos y agregar contenido dinámico. Más información sobre [personalización](../personalization/personalize.md) y [contenido dinámico](../personalization/get-started-dynamic-content.md) en el Editor de expresiones.

Utilice la sección de vista previa del dispositivo para visualizar cómo se muestra la notificación push en dispositivos iOS y Android.

## Comportamiento al hacer clic {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Acerca del comportamiento al hacer clic"
>abstract="Seleccione el comportamiento cuando un destinatario haga clic en el cuerpo de la notificación push."

Puede seleccionar el comportamiento cuando un usuario haga clic en el cuerpo de la notificación push.

![](assets/title-body-push.png)

* Para abrir la aplicación, seleccione **[!UICONTROL Abrir aplicación]** opción. La aplicación asociada a la notificación se define en la variable [superficie de canal](../configuration/channel-surfaces.md) (es decir, ajuste preestablecido de mensaje).
* Para redirigir al usuario a un fragmento de contenido específico dentro de una aplicación, seleccione **[!UICONTROL Vínculo profundo]** opción.  El contenido específico puede ser una vista específica, una sección concreta de una página o una pestaña determinada. Una vez seleccionada la opción, introduzca el vínculo profundo en el campo asociado.
* Para redirigir al usuario a una URL externa, utilice el **[!UICONTROL URL web]** opción. Una vez seleccionada la opción, introduzca la dirección URL en el campo asociado.

## Añadir medios {#add-media-push}

En la versión de iOS de la notificación push, puede añadir una imagen, un vídeo o un GIF que se mostrará en la notificación.

En la versión de Android, solo puede añadir un icono de imagen y una imagen para notificaciones expandidas.

![](assets/push-config-add-media.png)

Hay dos opciones disponibles. Puede hacer lo siguiente:

* Utilice el **[!UICONTROL Añadir medios]** para seleccionar un recurso en **[!DNL Adobe Experience Manager Assets Essentials]**.

  Aprenda a utilizar **[!DNL Adobe Experience Manager Assets Essentials]** in [esta página](../email/assets-essentials.md).

* O introduzca la URL del contenido en la **[!UICONTROL Añadir medios]** field. En ese caso, puede añadir personalización a la dirección URL.

Una vez añadidos, los contenidos se muestran a la derecha del cuerpo de la notificación.

## Añadir botones {#add-buttons-push}

Cree una notificación procesable añadiendo botones al contenido push.

Si la pantalla del dispositivo está bloqueada, estos botones no se muestran: solo el **Título** y el **Mensaje** de la notificación son visibles. Si su dispositivo está desbloqueado, los destinatarios verán los botones.

En la versión de iOS, puede añadir hasta cuatro botones. En la versión de Android, puede añadir hasta tres botones.

>[!NOTE]
>
>Para iOS, utilice el **[!UICONTROL categoría iOS]** para asociar acciones con una categoría de notificación.

1. Utilice el **[!UICONTROL Botón Añadir]** para definir la configuración: etiqueta y acción asociada. Las acciones posibles son las mismas que para [comportamiento al hacer clic](#on-click-behavior).

1. Utilice el **[!UICONTROL Expandir vista]** debajo de la imagen de vista previa central para previsualizar los botones personalizados.

![](assets/push_buttons.png)

## Enviar una notificación silenciosa {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Acerca de la notificación silenciosa"
>abstract="Envíe notificaciones sin molestar al usuario; las notificaciones no se muestran en el centro de notificaciones ni en la barra de notificaciones."

Una notificación push silenciosa (o notificación en segundo plano) es una instrucción oculta que se envía a la aplicación. Se utiliza, por ejemplo, para notificar a la aplicación la disponibilidad de contenido nuevo o iniciar una descarga en segundo plano.

Seleccione el **[!UICONTROL Notificación silenciosa]** opción para notificar a la aplicación de forma silenciosa: en este caso, la notificación se transfiere directamente a la aplicación. No se muestra ninguna alerta en la pantalla del dispositivo.

Utilice el **[!UICONTROL Datos personalizados]** para agregar pares clave-valor.

## Datos personalizados

En el **[!UICONTROL Datos personalizados]** , puede añadir variables personalizadas a la carga útil, según la configuración de la aplicación móvil. Para obtener más información sobre cómo configurar notificaciones push en Adobe Experience Platform y Adobe Launch, consulte [esta sección](push-gs.md)

## Opciones avanzadas {#advanced-options-push}

Puede configurar **[!UICONTROL Opciones avanzadas]** para la notificación push. Los parámetros disponibles se enumeran a continuación:

| Parámetro | Descripción |
|---------|---------|
| **[!UICONTROL Contraíble]** (iOS/Android) | Un mensaje contraíble es un mensaje que puede reemplazarse por uno nuevo si ha quedado obsoleto. Algunos casos de uso comunes de los mensajes contraíbles son los mensajes que se utilizan para indicar a una aplicación móvil que sincronice los datos del servidor. Un ejemplo sería una aplicación deportiva que actualice a los usuarios con la puntuación más reciente. Solo es relevante el mensaje más reciente. Por otro lado, con los mensajes no contraíbles, cada mensaje es importante para la aplicación del cliente y debe entregarse. |
| **[!UICONTROL Sonido personalizado]** (iOS/Android) | Sonido que el terminal móvil debe reproducir cuando reciba la notificación. El sonido debe incluirse en la aplicación. |
| **[!UICONTROL Insignias]** (iOS/Android) | Un distintivo se utiliza para mostrar directamente en el icono de la aplicación la cantidad de información nueva no leída. <br/>El valor del distintivo desaparece en cuanto el usuario abra o lea el nuevo contenido de la aplicación. Cuando se recibe una notificación en un dispositivo, puede actualizar o añadir un valor de distintivo para la aplicación relacionada.<br/>Por ejemplo, si almacena el número de artículos no leídos de sus clientes, puede aprovechar la personalización para enviar el valor de distintivo de artículos no leídos únicos a cada cliente. Para obtener más personalización, consulte [esta sección](../personalization/personalize.md). |
| **[!UICONTROL Grupo de notificación]**  (solo iOS) | Asocie un grupo de notificación a la notificación push.<br/>A partir de iOS 12, los grupos de notificación permiten consolidar subprocesos de mensajes y temas de notificación en ID de subprocesos. Por ejemplo: una marca puede enviar notificaciones de marketing con un ID de grupo, mientras que las notificaciones de tipo más operativas se mantienen con uno o más ID diferentes.<br/>Para ilustrar esto, puede tener grupos de notificación groupID: 123 &quot;echa un vistazo a la nueva colección de primavera de suéters&quot; y groupID: 456 &quot;tu paquete se entregó&quot;. En este ejemplo, todas las notificaciones de envío se agrupan en el ID de grupo: 456. |
| **[!UICONTROL Canal de notificación]** (Solo Android) | Asocie un canal de notificación a la notificación push.<br/>A partir de Android 8.0 (nivel de API 26), todas las notificaciones deben asignarse a un canal para que se muestren. Para obtener más información, consulte [Documentación para desarrolladores de Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Añadir indicador de disponibilidad de contenido]** (solo iOS) | Envía el indicador de contenido disponible en la carga push para garantizar que la aplicación se activa en cuanto recibe la notificación push, lo que significa que la aplicación puede acceder a los datos de carga.<br/> Esto funciona incluso si la aplicación se está ejecutando en segundo plano y sin necesidad de interacción del usuario (por ejemplo, tocando la notificación push). Sin embargo, esto no se aplica si la aplicación no se está ejecutando. Para obtener más información, consulte la [documentación para desarrolladores de Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Añadir indicador de contenido mutable]** (solo iOS) | Envía el indicador de contenido mutable en la carga útil push y permite que el contenido de las notificaciones push se modifique con una extensión de aplicación de servicio de notificaciones proporcionada en el SDK de iOS. Para obtener más información, consulte la [documentación para desarrolladores de Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Puede aprovechar las extensiones de la aplicación móvil para modificar aún más el contenido o la presentación de las notificaciones push entrantes enviadas desde [!DNL Journey Optimizer]. Por ejemplo, los usuarios pueden aprovechar esta opción para descifrar datos, cambiar el texto del cuerpo o del título de una notificación, añadir un identificador de subproceso a una notificación, etc. |
| **[!UICONTROL Visibilidad de notificación]** (Solo Android) | Define la visibilidad de la notificación push. <br/><b>Privado</b> mostrará la notificación en todas las pantallas de bloqueo, pero ocultará la información confidencial o privada en pantallas de bloqueo seguras. <br/><b>Público</b> mostrará la notificación en su totalidad en todas las pantallas de bloqueo. <br/><b>Secreto</b> no revelará ninguna parte de la notificación en una pantalla de bloqueo segura. <br/>Para obtener más información, consulte [Documentación para desarrolladores de Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Prioridad de notificación]** (Solo Android) | Define la importancia de la notificación push de baja a máxima. Esto determina la intrusión que tendrá la notificación push cuando se envíe. Para obtener más información, consulte [Documentación para desarrolladores de Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Prioridad de envío]** (Solo Android) | Establece una prioridad alta o normal para las notificaciones push. Para obtener más información sobre la prioridad de los mensajes, consulte la [documentación para desarrolladores de Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |
