---
title: Crear un correo electrónico
description: Obtenga información sobre cómo crear un correo electrónico en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 9%

---

# Crear un correo electrónico {#configure-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="Creación de correo electrónico"
>abstract="Defina sus parámetros de correo electrónico en solo tres pasos simples."

Se pueden crear correos electrónicos:

* En un **Recorrido**: Una vez que haya añadido una actividad de correo electrónico en el recorrido y haya definido la configuración básica, utilice la variable **[!UICONTROL Actions: Email]** panel derecho para crear el contenido de las notificaciones push.

   Para obtener más información sobre cómo configurar el recorrido, consulte esta [página](../building-journeys/journey-gs.md).

   ![](assets/email-edit-content.png)

* En un **Campaign**: Una vez creada una campaña, seleccione Correo electrónico como acción y defina la configuración básica.

   Para obtener más información sobre cómo configurar la campaña, consulte esta [página](../campaigns/create-campaign.md#configure).

   ![](assets/email_campaign.png)

## Definir el contenido del correo electrónico{#email-content}

Uso [!DNL Journey Optimizer] Diseñador de correo electrónico para [diseñar el correo electrónico desde cero](../design/create-email-content.md). Si tiene un contenido existente, puede [importarlo en el Diseñador de correo electrónico](../design/existing-content.md)o [codifique su propio contenido](../design/code-content.md) en [!DNL Journey Optimizer].

[!DNL Journey Optimizer] viene con un conjunto de [plantillas integradas](../design/email-templates.md) para ayudarle a empezar. Cualquier correo electrónico también se puede guardar como plantilla.

Uso [!DNL Journey Optimizer] Editor de expresiones para personalizar los mensajes con los datos de los perfiles. Para obtener más información sobre personalización, consulte [esta sección](../personalization/personalize.md).

## Seguimiento de correo electrónico{#email-tracking}

Si desea rastrear el comportamiento de sus destinatarios a través de aperturas o clics en vínculos, habilite las siguientes opciones: **[!UICONTROL Email opens]** y **[!UICONTROL Click on email]**.

Obtenga más información sobre el seguimiento en [esta sección](../design/message-tracking.md).

## Validación del contenido del correo electrónico{#email-content-validate}

Controle la renderización del correo electrónico y compruebe la configuración de personalización con perfiles de prueba mediante la sección de previsualización de la izquierda. Para obtener más información, consulte [esta sección](../design/preview.md).

![](assets/messages-simple-preview.png)


También debe comprobar las alertas en la sección superior del editor.  Algunas de ellas son simples advertencias, pero otras pueden impedir que utilice el mensaje. Obtenga más información en [esta sección](alerts.md).


>[!NOTE]
>
>La variable **[!UICONTROL From email]** y **[!UICONTROL From name]** están determinados por la variable **[!UICONTROL Surface]** que se haya seleccionado al [creación del mensaje](get-started-content.md).

