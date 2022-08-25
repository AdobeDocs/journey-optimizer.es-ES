---
title: Creación de un mensaje SMS
description: Obtenga información sobre cómo crear un mensaje SMS en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 9%

---

# Creación de un mensaje SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Creación de SMS"
>abstract="Añada el mensaje de texto y comience a personalizarlo con el editor de expresiones."

Uso [!DNL Journey Optimizer] para enviar mensajes de texto a sus clientes en sus dispositivos móviles. Puede crear, personalizar y previsualizar mensajes en formato de texto desde el editor de SMS.

Se pueden crear envíos de SMS:

* En un **Recorrido**: Una vez que haya agregado una actividad SMS en el recorrido y haya definido la configuración básica, utilice la variable **[!UICONTROL Actions: SMS]** panel derecho para crear el contenido del mensaje SMS.

   Para obtener más información sobre cómo configurar el recorrido, consulte esta [página](../building-journeys/journey-gs.md).

* En un **Campaign**: Una vez que haya creado una campaña, seleccione SMS como su acción y defina la configuración básica.

   Para obtener más información sobre cómo configurar la campaña, consulte esta [página](../campaigns/create-campaign.md#configure).

Si es la primera vez que crea un mensaje SMS, asegúrese de que el canal SMS esté configurado. [Más información](../configuration/sms-configuration.md).

## Definir el contenido del SMS{#sms-content}

Para empezar a personalizar el mensaje SMS, siga estos pasos:

1. Haga clic en el **[!UICONTROL Message]** para abrir el editor de expresiones.

   ![](assets/sms-content.png)

1. Utilice el editor de expresiones para definir el contenido. Puede utilizar cualquier atributo para personalizar el contenido, como el nombre del perfil o la ciudad. Obtenga más información sobre personalización en el editor de expresiones en [esta sección](../personalization/personalize.md).

1. Haga clic en **[!UICONTROL Save]** y compruebe el mensaje en la vista previa.

   ![](assets/sms-content-preview.png)

## Validar el SMS{#sms-preview}

>[!NOTE]
>
> Para mejorar la capacidad de envío, siempre debe utilizar los números de teléfono en los formatos admitidos por el proveedor. Por ejemplo, Twilio y Sinch solo admiten números de teléfono en formato E.164.

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo y probarlo. Si ha insertado [contenido personalizado](../personalization/personalize.md), puede comprobar cómo se muestra este contenido en el mensaje, aprovechando los datos de perfil de prueba.

Para visualizar la visualización de su mensaje SMS en dispositivos móviles, haga clic en el botón **[!UICONTROL Simulate content]** pestaña . Obtenga más información sobre la simulación de contenido en [esta sección](../design/preview.md).

También debe comprobar las alertas en la sección superior del editor.  Algunas de ellas son simples advertencias, pero otras pueden impedir que utilice el mensaje. Obtenga más información en [esta sección](alerts.md).

![](assets/sms-alert-button.png)


## Inclusión y exclusión{#sms-opt-in-out}

Para todos los mensajes de marketing, el SMS debe contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. Una vez cancelada la suscripción, los perfiles se eliminan automáticamente de la audiencia de futuros mensajes de marketing. La adición de un vínculo de baja no es obligatoria para los mensajes transaccionales.

Los destinatarios de SMS pueden responder con palabras clave de inclusión y exclusión. De acuerdo con las normas y regulaciones del sector, Adobe Journey Optimizer procesa automáticamente las siguientes palabras clave en los mensajes entrantes: START, STOP y UNSTOP. Estas palabras clave activan las respuestas estándares automáticas del proveedor de SMS.

Para obtener más información sobre cómo funciona la compatibilidad con palabras clave de entrada nativas (inicio, parada e inparada) para SMS, consulte el siguiente vídeo.

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

<!--
## How-to video

Learn how to configure, author, and include SMS messaging into your customer journeys.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)
-->
**Temas relacionados**

* [Configuración del canal de SMS](../configuration/sms-configuration.md)
* [Informe SMS](../reports/journey-global-report.md#sms-global)
* [Crear un mensaje nuevo](get-started-content.md)
* [Adición de un mensaje en un recorrido](../building-journeys/journeys-message.md)
