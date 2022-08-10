---
title: Alertas en mensajes
description: Obtenga información sobre cómo comprobar la validación del contenido del mensaje y solucionar problemas
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 8%

---

# Comprobar alertas en los mensajes {#messages-alerts}

## Comprobaciones antes de enviar {#message-alerting}

Al diseñar los mensajes, las alertas se muestran en la interfaz cuando falta la configuración clave.

Las alertas se muestran en la parte superior derecha de la pantalla, al editar el contenido del mensaje.

![](assets/alerts-details.png)

>[!NOTE]
>
>Si no ve este botón, no se ha detectado ninguna alerta.

Pueden producirse dos tipos de alertas:

* **Advertencias** consulte recomendaciones y prácticas recomendadas. Por ejemplo, se mostrará un mensaje si falta el vínculo de no participación.

* **Errores** impida que pruebe o active el recorrido mientras no se resuelvan. Por ejemplo, un mensaje le avisará de que falta la línea de asunto.

Se detallan todas las advertencias y errores posibles [below](#alerts-and-warnings).

>[!CAUTION]
>
> Debe resolver todo **error** alertas antes de probar o activar el recorrido mediante el mensaje.

## Lista de advertencias y errores {#alerts-and-warnings}

La configuración y los elementos comprobados por el sistema se enumeran a continuación. También encontrará información sobre cómo adaptar la configuración para resolver los problemas correspondientes.

**Advertencias**:

* **[!UICONTROL The opt-out link is not present in the email body]**: añadir un vínculo de baja en el cuerpo del correo electrónico es una práctica recomendada. Obtenga información sobre cómo configurarlo en [esta sección](consent.md#opt-out-management).

   >[!NOTE]
   >
   >Los mensajes de correo electrónico de tipo marketing deben incluir un vínculo de no participación, que no es necesario para los mensajes transaccionales. La categoría del mensaje (**[!UICONTROL Marketing]** o **[!UICONTROL Transactional]**) se define en la [superficie de canal](../configuration/channel-surfaces.md#email-type) (es decir, nivel de ajuste preestablecido de mensaje) y durante la [creación del mensaje](get-started-content.md#create-new-message).

* **[!UICONTROL Text version of HTML is empty]**: no olvide definir una versión de texto del cuerpo del correo electrónico, ya que se utilizará cuando no se pueda mostrar el contenido del HTML. Aprenda a crear la versión de texto en [esta sección](../design/text-version-email.md).

* **[!UICONTROL Empty link is present in email body]**: compruebe que todos los vínculos del correo electrónico sean correctos. Obtenga información sobre cómo administrar contenido y vínculos en [esta sección](../design/create-email-content.md).

* **[!UICONTROL Email size has exceeded the limit of 100KB]**: para una entrega óptima, asegúrese de que el tamaño del correo electrónico no supere los 100 KB. Obtenga información sobre cómo editar contenido de correo electrónico en [esta sección](../design/create-email-content.md).

**Errores**:

* **[!UICONTROL The subject line is missing]**: la línea de asunto del correo electrónico es obligatoria. Obtenga información sobre cómo definirlo y personalizarlo en [esta sección](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL The push version of the message is empty]**: este error se muestra cuando falta el cuerpo o el título de la notificación push. Aprenda a definir el contenido de las notificaciones push en [esta sección](create-push.md).

* **[!UICONTROL The email version of the message is empty]**: este error se muestra cuando el contenido del correo electrónico no se ha configurado. Aprenda a diseñar contenido de correo electrónico en [esta sección](../design/design-emails.md).

* **[!UICONTROL Surface doesn’t exist]**: no puede utilizar el mensaje si la superficie seleccionada se elimina después de la creación del mensaje. Si se produce este error, seleccione otra superficie en el mensaje **[!UICONTROL Properties]**. Obtenga más información sobre las superficies de canal en [esta sección](../configuration/channel-surfaces.md).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: el tamaño de la notificación push no puede superar los 4 KB. Para respetar este límite, intente reducir el uso de imágenes o emojis. Aprenda a administrar el contenido de las notificaciones push en [esta sección](create-push.md).

>[!CAUTION]
>
> Para poder utilizar el mensaje, debe resolver todos los **error** alertas.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
