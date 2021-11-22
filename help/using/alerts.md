---
title: Alertas en mensajes
description: Obtenga información sobre cómo comprobar la validación del contenido del mensaje y solucionar problemas
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Alertas en los mensajes {#publish-manage-messages}

## Comprobaciones antes de la publicación {#message-alerting}

Mientras crea el mensaje, las alertas le avisan cuando necesita realizar acciones importantes antes de publicarlo.

Las alertas se muestran en la parte superior derecha de la pantalla, como se muestra a continuación:

![](assets/message-alerts.png)

>[!NOTE]
>
>Si no ve este botón, no se ha detectado ninguna alerta.

Pueden producirse dos tipos de alertas:

* **Advertencias** consulte recomendaciones y prácticas recomendadas. Por ejemplo, se mostrará un mensaje si falta el vínculo de no participación.

* **Errores** impida la publicación del mensaje mientras no se resuelvan. Por ejemplo, un mensaje le avisará de que falta la línea de asunto.

Se detallan todas las advertencias y errores posibles [below](#alerts-and-warnings).

>[!CAUTION]
>
> Debe resolver todo **error** alertas antes de la publicación.

## Lista de advertencias y errores {#alerts-and-warnings}

La configuración y los elementos comprobados por el sistema se enumeran a continuación. También encontrará información sobre cómo adaptar la configuración para resolver los problemas correspondientes.

**Advertencias**:

* **[!UICONTROL Opt out link not present in the email body]**: añadir un vínculo de baja en el cuerpo del correo electrónico es una práctica recomendada. Obtenga información sobre cómo configurarlo en [esta sección](consent.md).

* **[!UICONTROL Text version of html is empty]**: no olvide definir una versión de texto del cuerpo del correo electrónico, ya que se utilizará cuando no se pueda mostrar el contenido del HTML. Aprenda a crear la versión de texto en [esta sección](create-email-content.md#generate-text-version).

* **[!UICONTROL Empty link is present in email body]**: compruebe que todos los vínculos del correo electrónico sean correctos. Obtenga información sobre cómo administrar contenido y vínculos en [esta sección](create-email-content.md).

* **[!UICONTROL Email size has exceeded the limit of 100KB]**: para una entrega óptima, asegúrese de que el tamaño del correo electrónico no supere los 100 KB. Obtenga información sobre cómo editar contenido de correo electrónico en [esta sección](create-email-content.md).

**Errores**:

* **[!UICONTROL Subject Line Not Present]**: la línea de asunto del correo electrónico es obligatoria. Obtenga información sobre cómo definirlo y personalizarlo en [esta sección](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Push Variant is empty]**: este error se muestra cuando falta el cuerpo o el título de la notificación push. Aprenda a definir el contenido de las notificaciones push en [esta sección](create-push.md).

* **[!UICONTROL Email Variant is empty]**: este error se muestra cuando el contenido del correo electrónico no se ha configurado. Aprenda a diseñar contenido de correo electrónico en [esta sección](design-emails.md).

* **[!UICONTROL Preset doesn’t exist]**: no puede publicar el mensaje si el ajuste preestablecido seleccionado se elimina después de la creación del mensaje. Si se produce este error, seleccione otro ajuste preestablecido en el mensaje **[!UICONTROL Properties]**. Obtenga más información sobre la promoción de la marca en [esta sección](configuration/about-subdomain-delegation.md).

* **[!UICONTROL Push iOS/Android payload has exceeded limit of 4KB]**: el tamaño de la notificación push no puede superar los 4 KB. Para respetar este límite, intente reducir el uso de imágenes o emojis. Aprenda a administrar el contenido de las notificaciones push en [esta sección](create-push.md).

>[!CAUTION]
>
> Para poder publicar el mensaje, debe resolver todos los **error** alertas.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
