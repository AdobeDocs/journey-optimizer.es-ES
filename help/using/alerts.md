---
title: Alertas en mensajes
description: Obtenga información sobre cómo comprobar la validación del contenido del mensaje y solucionar problemas
translation-type: tm+mt
source-git-commit: 03af839084edafbc93188750db1f9f6c8b559d9e
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Alertas en los mensajes {#publish-manage-messages}

![](assets/do-not-localize/badge.png)

## Comprobaciones antes de la publicación {#message-alerting}

Mientras crea el mensaje, las alertas le avisan cuando necesita realizar acciones importantes antes de publicarlo.

Las alertas se muestran en la parte superior derecha de la pantalla, como se muestra a continuación:

![](assets/message-alerts.png)

>[!NOTE]
>
>Si no ve este botón, no se ha detectado ninguna alerta.

Pueden producirse dos tipos de alertas:

* **** Las advertencias se refieren a recomendaciones y prácticas recomendadas. Por ejemplo, se mostrará un mensaje si falta el vínculo de no participación.

* **** Los errores le impiden publicar el mensaje mientras no se hayan resuelto. Por ejemplo, un mensaje le avisará de que falta la línea de asunto.

Todas las advertencias y errores posibles se detallan [a continuación](#alerts-and-warnings).

>[!CAUTION]
>
> Debe resolver todas las alertas **error** antes de la publicación.

## Lista de advertencias y errores {#alerts-and-warnings}

La configuración y los elementos comprobados por el sistema se enumeran a continuación. También encontrará información sobre cómo adaptar la configuración para resolver los problemas correspondientes.

**Advertencias**:

* **[!UICONTROL Opt out link not present in the email body]**: añadir un vínculo de baja en el cuerpo del correo electrónico es una práctica recomendada. Aprenda a configurarlo en [esta sección](consent.md).

* **[!UICONTROL Text version of html is empty]**: no olvide definir una versión de texto del cuerpo del correo electrónico, ya que se utilizará cuando no se pueda mostrar contenido HTML. Aprenda a crear la versión de texto en [esta sección](create-email-content.md#generate-text-version).

* **[!UICONTROL Empty link is present in email body]**: compruebe que todos los vínculos del correo electrónico sean correctos. Aprenda a administrar contenido y vínculos en [esta sección](create-email-content.md).

* **[!UICONTROL Email size has exceeded the limit of 100KB]**: para una entrega óptima, asegúrese de que el tamaño del correo electrónico no supere los 100 KB. Aprenda a editar el contenido del correo electrónico en [esta sección](create-email-content.md).

**Errores**:

* **[!UICONTROL Subject Line Not Present]**: la línea de asunto del correo electrónico es obligatoria. Aprenda a definirlo y personalizarlo en [esta sección](configure-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Push Variant is empty]**: este error se muestra cuando falta el cuerpo o el título de la notificación push. Aprenda a definir el contenido de las notificaciones push en [esta sección](configure-push.md).

* **[!UICONTROL Email Variant is empty]**: este error se muestra cuando el contenido del correo electrónico no se ha configurado. Aprenda a diseñar contenido de correo electrónico en [esta sección](design-emails.md).

* **[!UICONTROL Preset doesn’t exist]**: no puede publicar el mensaje si el ajuste preestablecido seleccionado se elimina después de la creación del mensaje. Si se produce este error, seleccione otro ajuste preestablecido en el mensaje **[!UICONTROL Properties]**. Obtenga más información sobre la promoción de la marca en [esta sección](administration.md#cjm-branding).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: el tamaño de la notificación push no puede superar los 4 KB. Para respetar este límite, intente reducir el uso de imágenes o emojis. Aprenda a administrar el contenido de las notificaciones push en [esta sección](configure-push.md).

>[!CAUTION]
>
> Para poder publicar el mensaje, debe resolver todas las alertas **error**.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
