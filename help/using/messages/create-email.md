---
title: Crear un correo electrónico
description: Obtenga información sobre cómo crear un correo electrónico en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 1d0e28583c500d5eddf9f88250f279d188c4784a
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 3%

---

# Crear un correo electrónico {#configure-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="Creación de correo electrónico"
>abstract="Defina sus parámetros de correo electrónico en solo tres pasos simples."

Una vez que [crear un mensaje](get-started-content.md), use el **[!UICONTROL Email]** para definir la configuración y el contenido del canal de correo electrónico.

![](assets/emails-configuration.png)

>[!NOTE]
>
>La variable **[!UICONTROL From email]** y **[!UICONTROL From name]** son de solo lectura y están determinados por la variable **[!UICONTROL Preset]** que se haya seleccionado al [creación del mensaje](get-started-content.md).

Los pasos para configurar un correo electrónico son los siguientes:

1. Especifique el asunto del correo electrónico en la **[!UICONTROL Subject line]** campo . Para ello, haga clic en el botón de la derecha para abrir el editor de expresiones y componer el asunto del correo electrónico. Aprenda a añadir personalización en [esta sección](../personalization/personalize.md)

1. Haga clic en el **[!UICONTROL Email Designer]** para diseñar el correo electrónico. Aprenda a diseñar correos electrónicos en [esta sección](../design/design-emails.md).

1. Si desea rastrear el comportamiento de sus destinatarios a través de aperturas o clics en vínculos, asegúrese de que la variable **[!UICONTROL Open Tracking for email]** y **[!UICONTROL Click Tracking for email]** están activadas. Obtenga más información sobre el seguimiento en [esta sección](../design/message-tracking.md).

>[!NOTE]
>
>Los mensajes de correo electrónico de tipo de marketing deben incluir un [vínculo de no participación](consent.md#opt-out-management), que no es necesario para los mensajes transaccionales. La categoría del mensaje (**[!UICONTROL Marketing]** o **[!UICONTROL Transactional]**) se define en la variable [nivel de mensaje preestablecido](../configuration/message-presets.md#email-type) y cuándo [creación del mensaje](get-started-content.md#create-new-message).
