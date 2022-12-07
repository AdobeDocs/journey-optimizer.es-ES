---
solution: Journey Optimizer
product: journey optimizer
title: Diseño de una notificación push
description: Aprenda a diseñar una notificación push en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 11%

---

# Diseño de una notificación push {#design-push-notification}

## Título y cuerpo {#push-title-body}

Para componer el mensaje, haga clic en el botón **[!UICONTROL Título]** y **[!UICONTROL Cuerpo]** campos. Utilice el editor de expresiones para definir contenido, personalizar datos y añadir contenido dinámico. Más información sobre [personalización](../personalization/personalize.md) y [contenido dinámico](../personalization/get-started-dynamic-content.md) en el editor de expresiones.

Utilice la sección de vista previa del dispositivo para visualizar cómo se muestra la notificación push en los dispositivos iOS y Android.

## Comportamiento al hacer clic {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="Acerca del comportamiento al hacer clic"
>abstract="Seleccione el comportamiento cuando un destinatario haga clic en el cuerpo de la notificación push."

Puede seleccionar el comportamiento cuando un usuario haga clic en el cuerpo de la notificación push.

![](assets/title-body-push.png)

* Para abrir la aplicación, seleccione la opción **[!UICONTROL Abrir aplicación]** . La aplicación asociada a la notificación se define en la variable [superficie del canal](../configuration/channel-surfaces.md) (es decir, el ajuste preestablecido de mensaje).
* Para redirigir al usuario a un contenido específico dentro de una aplicación, seleccione la opción **[!UICONTROL Vínculo profundo]** .  El contenido específico puede ser una vista específica, una sección concreta de una página o una ficha determinada. Una vez seleccionada la opción , introduzca el vínculo profundo en el campo asociado.
* Para redirigir al usuario a una URL externa, utilice la variable **[!UICONTROL URL web]** . Una vez seleccionada la opción , introduzca la URL en el campo asociado.

## Añadir medios {#add-media-push}

En la versión iOS de la notificación push, puede añadir una imagen, un vídeo o un GIF que se mostrarán en la notificación.

En la versión de Android, solo puede agregar un icono de imagen y una imagen para notificaciones expandidas.

![](assets/push-config-add-media.png)

Hay dos opciones disponibles. Puede hacer lo siguiente:

* Utilice la variable **[!UICONTROL Añadir medios]** para seleccionar un recurso en **[!DNL Adobe Experience Manager Assets Essentials]**.

   Aprenda a utilizar **[!DNL Adobe Experience Manager Assets Essentials]** en [esta página](../email/assets-essentials.md).

* O introduzca la dirección URL del contenido en el **[!UICONTROL Añadir medios]** campo . En ese caso, puede añadir personalización a la dirección URL.

Una vez añadido, el contenido se muestra a la derecha del cuerpo de notificación.

## Agregar botones {#add-buttons-push}

Cree una notificación procesable añadiendo botones al contenido push.

Si la pantalla del dispositivo está bloqueada, estos botones no se muestran: solo la variable **Título** y **Mensaje** de la notificación están visibles. Si el dispositivo está desbloqueado, los destinatarios verán los botones.

En la versión de iOS, puede añadir hasta cuatro botones. En la versión de Android, puede añadir hasta tres botones.

>[!NOTE]
>
>Para iOS, use la variable **[!UICONTROL Categoría de iOS]** para asociar acciones con una categoría de notificación.

1. Utilice la variable **[!UICONTROL Botón Añadir]** para definir la configuración: la etiqueta y la acción asociada. Las acciones posibles son las mismas que para [comportamiento al hacer clic](#on-click-behavior).

1. Utilice la variable **[!UICONTROL Expandir vista]** bajo la imagen de vista previa central para previsualizar los botones personalizados.

![](assets/push_buttons.png)

## Enviar una notificación silenciosa {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="Acerca de la notificación silenciosa"
>abstract="Envíe notificaciones sin molestar al usuario, las notificaciones no se muestran en el centro de notificaciones ni en la barra de notificaciones."

Una notificación push silenciosa (o notificación en segundo plano) es una instrucción oculta que se envía a la aplicación. Se utiliza, por ejemplo, para notificar a la aplicación la disponibilidad de contenido nuevo o iniciar una descarga en segundo plano.

Seleccione el **[!UICONTROL Notificación silenciosa]** para notificar de forma silenciosa a la aplicación: en este caso, la notificación se transfiere directamente a la solicitud. No se muestra ninguna alerta en la pantalla del dispositivo.

Utilice la variable **[!UICONTROL Datos personalizados]** para agregar pares clave-valor.

## Datos personalizados

En el **[!UICONTROL Datos personalizados]** , puede agregar variables personalizadas a la carga útil, según la configuración de la aplicación móvil. Para obtener más información sobre cómo configurar las notificaciones push en Adobe Experience Platform y Adobe Launch, consulte [esta sección](push-gs.md)

## Opciones avanzadas {#advanced-options-push}

Puede configurar **[!UICONTROL Opciones avanzadas]** para la notificación push. A continuación se enumeran los parámetros disponibles:

| Parámetro | Descripción |
|---------|---------|
| **[!UICONTROL Contraíble]** (iOS/Android) | Un mensaje contraíble es un mensaje que puede reemplazarse por un mensaje nuevo si ha quedado obsoleto. Algunos casos de uso habituales de mensajes contraíbles son los mensajes que se utilizan para indicar a una aplicación móvil que sincronice datos del servidor. Un ejemplo sería una aplicación deportiva que actualiza a los usuarios con la puntuación más reciente. Solo es relevante el mensaje más reciente. Por otro lado, con un mensaje que no se puede contraer, cada mensaje es importante para la aplicación del cliente y debe entregarse. |
| **[!UICONTROL Sonido personalizado]** (iOS/Android) | Sonido que el terminal móvil debe reproducir cuando reciba la notificación. El sonido debe estar incorporado en la aplicación. |
| **[!UICONTROL Distintivos]** (iOS/Android) | Un distintivo se utiliza para mostrar directamente en el icono de la aplicación la cantidad de información nueva no leída. <br/>El valor del distintivo desaparece en cuanto el usuario abra o lea el nuevo contenido de la aplicación. Cuando se recibe una notificación en un dispositivo, puede actualizar o añadir un valor de distintivo para la aplicación relacionada.<br/>Por ejemplo, si está almacenando el número de artículos sin leer de sus clientes, puede aprovechar la personalización para enviar el valor de distintivo de artículos sin leer exclusivo para cada cliente. Para obtener más personalización, consulte [esta sección](../personalization/personalize.md). |
| **[!UICONTROL Grupo de notificaciones]**  (solo iOS) | Asocie un grupo de notificaciones a la notificación push.<br/>A partir de iOS 12, los grupos de notificaciones permiten consolidar los subprocesos de mensajes y los temas de notificación en los ID de subprocesos. Por ejemplo, una marca puede enviar notificaciones de marketing con un ID de grupo, mientras mantiene más notificaciones de tipo operativo con uno o más ID diferentes.<br/>Para ilustrarlo, puede tener groupID: 123 &quot;echa un vistazo a la nueva colección primaveral de suéters&quot; y groupID: 456 Grupos de notificación de &quot;su paquete se entregó&quot;. En este ejemplo, todas las notificaciones de entrega se incluyen en el ID de grupo: 456. |
| **[!UICONTROL Canal de notificación]** (solo Android) | Asocie un canal de notificación a la notificación push.<br/>A partir de Android 8.0 (nivel de API 26), todas las notificaciones deben asignarse a un canal para que se muestre. Para obtener más información, consulte [Documentación para desarrolladores de Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Agregar indicador de disponibilidad de contenido]** (solo iOS) | Envía el indicador de contenido disponible en la carga útil push para garantizar que la aplicación se activa en cuanto recibe la notificación push, lo que significa que la aplicación puede acceder a los datos de carga útil.<br/> Esto funciona incluso si la aplicación se está ejecutando en segundo plano y sin necesidad de interacción del usuario (p. ej., al tocar la notificación push). Sin embargo, esto no se aplica si la aplicación no se está ejecutando. Para obtener más información, consulte la [documentación para desarrolladores de Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Agregar indicador de contenido mutable]** (solo iOS) | Envía el indicador de contenido mutable en la carga útil push y permite que el contenido de la notificación push se modifique con una extensión de aplicación de servicio de notificación proporcionada en el SDK de iOS. Para obtener más información, consulte la [documentación para desarrolladores de Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Puede aprovechar las extensiones de la aplicación móvil para modificar aún más el contenido o la presentación de las notificaciones push entrantes enviadas desde [!DNL Journey Optimizer]. Por ejemplo, los usuarios pueden aprovechar esta opción para descifrar datos, cambiar el texto del cuerpo o el título de una notificación, añadir un identificador de subproceso a una notificación, etc. |
| **[!UICONTROL Visibilidad de la notificación]** (solo Android) | Define la visibilidad de la notificación push. <br/><b>Privado</b> mostrará la notificación en todas las pantallas de seguridad, pero ocultará información confidencial o privada en las pantallas de seguridad. <br/><b>Público</b> mostrará la notificación en su totalidad en todas las pantallas de seguridad. <br/><b>Secreto</b> no revelará ninguna parte de la notificación en una pantalla de bloqueo segura. <br/>Para obtener más información, consulte [Documentación para desarrolladores de Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Prioridad de notificación]** (solo Android) | Define la importancia de la notificación push de Bajo a Máx. Esto determina cuán &quot;intrusiva&quot; será la notificación push cuando se entregue. Para obtener más información, consulte [Documentación para desarrolladores de Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Prioridad de entrega]** (solo Android) | Establece una prioridad alta o normal para las notificaciones push. Para obtener más información sobre la prioridad de los mensajes, consulte la [documentación para desarrolladores de Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |


