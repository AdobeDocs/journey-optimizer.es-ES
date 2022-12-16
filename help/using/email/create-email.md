---
solution: Journey Optimizer
product: journey optimizer
title: Crear un correo electrónico
description: Obtenga información sobre cómo crear correos electrónicos en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 5%

---

# Crear un correo electrónico {#create-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="Creación de correo electrónico"
>abstract="Defina sus parámetros de correo electrónico en solo tres pasos simples."

Para crear un correo electrónico en [!DNL Journey Optimizer], siga los pasos a continuación.

## Creación de un correo electrónico en un recorrido o una campaña {#create-email-journey-campaign}

Agregue un **[!UICONTROL Correo electrónico]** a un recorrido o a una campaña, y siga los pasos a continuación según su caso.

>[!BEGINTABS]

>[!TAB Añadir un correo electrónico a un recorrido]

1. Abra el recorrido y, a continuación, arrastre y suelte una **[!UICONTROL Correo electrónico]** de **[!UICONTROL Acciones]** de la paleta.

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría).

1. Elija la [superficie del correo electrónico](email-settings.md) para usar.

   ![](assets/email_journey.png)

>[!NOTE]
>
>Si envía un correo electrónico desde un recorrido, puede aprovechar la función de optimización del tiempo de envío de Adobe Journey Optimizer para predecir el mejor momento para enviar el mensaje y maximizar la participación en función de las tasas de apertura y clics históricas. [Aprenda a trabajar con la optimización del tiempo de envío](../building-journeys/journeys-message.md#send-time-optimization)

Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md).

>[!TAB Añadir un correo electrónico a una campaña]

1. Cree una nueva campaña programada o activada por la API y seleccione **[!UICONTROL Correo electrónico]** como su acción.

1. Elija la [superficie del correo electrónico](email-settings.md) para usar.

   ![](assets/email_campaign.png)

1. Haga clic en **[!UICONTROL Crear]**.

1. Complete los pasos para crear una campaña de correo electrónico, como las propiedades de la campaña, [audiencia](../segment/about-segments.md)y [programación](../campaigns/create-campaign.md#schedule).

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

Para obtener más información sobre cómo configurar una campaña, consulte [esta página](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Definir el contenido del correo electrónico {#define-email-content}

1. En la pantalla de configuración de recorrido o de campaña, haga clic en el botón **[!UICONTROL Editar contenido]** para configurar el contenido del correo electrónico. [Más información](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

1. En el **[!UICONTROL Encabezado]** de la sección **[!UICONTROL Editar contenido]** de **[!UICONTROL De nombre]**, **[!UICONTROL De correo electrónico]** y **[!UICONTROL CCO]** provienen de la superficie de correo electrónico seleccionada. [Más información](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. Puede añadir una línea de asunto. Escriba texto sin formato directamente en el campo correspondiente o utilice la variable [Editor de expresiones](../personalization/personalization-build-expressions.md) para personalizar la línea de asunto.

1. Haga clic en el **[!UICONTROL Editar cuerpo del correo electrónico]** para empezar a crear contenido con [!DNL Journey Optimizer] Diseñador de correo electrónico. [Más información](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. Si se encuentra en una campaña, también puede hacer clic en el botón **[!UICONTROL Editor de código]** para codificar su propio contenido en el HTML sin formato utilizando la ventana emergente que se muestra.

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >Si ya ha creado o importado contenido a través del Diseñador de correo electrónico, este contenido se mostrará en el HTML.

## Comprobación de alertas {#check-email-alerts}

Al diseñar los mensajes, las alertas se muestran en la interfaz (en la parte superior derecha de la pantalla) cuando falta la configuración de clave.

![](assets/email_journey_alerts_details.png)

>[!NOTE]
>
>Si no ve este botón, no se ha detectado ninguna alerta.

La configuración y los elementos comprobados por el sistema se enumeran a continuación. También encontrará información sobre cómo adaptar la configuración para resolver los problemas correspondientes.

Pueden producirse dos tipos de alertas:

* **Advertencias** consulte las recomendaciones y prácticas recomendadas, como:

   * **[!UICONTROL El vínculo de no participación no está presente en el cuerpo del correo electrónico]**: añadir un vínculo de baja en el cuerpo del correo electrónico es una práctica recomendada. Obtenga información sobre cómo configurarlo en [esta sección](../privacy/opt-out.md#opt-out-management).

      >[!NOTE]
      >
      >Los mensajes de correo electrónico de tipo marketing deben incluir un vínculo de no participación, que no es necesario para los mensajes transaccionales. La categoría del mensaje (**[!UICONTROL Marketing]** o **[!UICONTROL Transaccional]**) se define en la variable [superficie del canal](email-settings.md#email-type) nivel y cuándo [creación del mensaje](#create-email-journey-campaign) desde un recorrido o una campaña.

   * **[!UICONTROL La versión de texto del HTML está vacía]**: no olvide definir una versión de texto del cuerpo del correo electrónico, ya que se utilizará cuando no se pueda mostrar el contenido del HTML. Aprenda a crear la versión de texto en [esta sección](text-version-email.md).

   * **[!UICONTROL El vínculo vacío está presente en el cuerpo del correo electrónico]**: compruebe que todos los vínculos del correo electrónico sean correctos. Obtenga información sobre cómo administrar contenido y vínculos en [esta sección](content-from-scratch.md).

   * **[!UICONTROL El tamaño del correo electrónico ha superado el límite de 100 KB]**: para una entrega óptima, asegúrese de que el tamaño del correo electrónico no supere los 100 KB. Obtenga información sobre cómo editar contenido de correo electrónico en [esta sección](content-from-scratch.md).

* **Errores** evite probar o activar el recorrido o la campaña siempre que no se resuelvan, como:

   * **[!UICONTROL Falta la línea de asunto]**: la línea de asunto del correo electrónico es obligatoria. Obtenga información sobre cómo definirlo y personalizarlo en [esta sección](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL La versión de correo electrónico del mensaje está vacía]**: este error se muestra cuando el contenido del correo electrónico no se ha configurado. Aprenda a diseñar contenido de correo electrónico en [esta sección](get-started-email-design.md).

   * **[!UICONTROL La superficie no existe]**: no puede utilizar el mensaje si la superficie seleccionada se elimina después de la creación del mensaje. Si se produce este error, seleccione otra superficie en el mensaje **[!UICONTROL Propiedades]**. Obtenga más información sobre las superficies de canal en [esta sección](../configuration/channel-surfaces.md).


>[!CAUTION]
>
>Para poder probar o activar el recorrido o la campaña mediante el correo electrónico, debe resolver todos los **error** alertas.

## Previsualice y envíe su correo electrónico

Una vez definido el contenido del mensaje, puede previsualizarlo para controlar la renderización del correo electrónico y comprobar la configuración de personalización con perfiles de prueba. [Más información](preview.md)

![](assets/email_designer_edit_simulate.png)

Cuando el correo electrónico esté listo, complete la configuración de su [recorrido](../building-journeys/journey-gs.md) o [campaign](../campaigns/create-campaign.md)y actívelo para enviar el mensaje.

>[!NOTE]
>
>Para realizar un seguimiento del comportamiento de los destinatarios a través de aperturas de correo electrónico o interacciones, asegúrese de que las opciones dedicadas en la variable **[!UICONTROL Seguimiento]** están activadas en la sección [actividad de correo electrónico](../building-journeys/journeys-message.md) o en el correo electrónico [campaign](../campaigns/create-campaign.md).<!--to move?-->

<!--

## Define your email content {#email-content}

Use [!DNL Journey Optimizer] Email Designer to [design your email from scratch](../email/content-from-scratch.md). If you have an existing content, you can [import it in the Email Designer](../email/existing-content.md), or [code your own content](../email/code-content.md) in [!DNL Journey Optimizer]. 

[!DNL Journey Optimizer] comes with a set of [built-in templates](email-templates.md) to help you start. Any email can also be saved as a template.

Use [!DNL Journey Optimizer] Expression editor to personalize your messages with profiles' data. For more on personalization, refer to [this section](../personalization/personalize.md).

Adapt the content of your messages to the targeted profiles by using [!DNL Journey Optimizer] dynamic content capabilities. [Get started with dynamic content](../personalization/get-started-dynamic-content.md)

## Email tracking {#email-tracking}

If you want to track the behavior of your recipients through openings and/or clicks on links, enable the following options: **[!UICONTROL Email opens]** and **[!UICONTROL Click on email]**. 

Learn more about tracking in [this section](message-tracking.md).

## Validate your email content {#email-content-validate}

Control the rendering of your email, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](preview.md).

![](assets/messages-simple-preview.png)

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. 

-->

