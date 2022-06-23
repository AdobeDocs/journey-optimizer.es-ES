---
title: Creación de un mensaje SMS
description: Obtenga información sobre cómo crear un mensaje SMS en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 67fcddc77ad5493905a0f1894a0cf497b0bfa2f9
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 12%

---

# Creación de un mensaje SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Creación de SMS"
>abstract="Añada el mensaje de texto y comience a personalizarlo con el Editor de expresiones."

>[!AVAILABILITY]
>
>Actualmente, el canal SMS solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, póngase en contacto con el representante del Adobe.

Una vez que [crear un mensaje](get-started-content.md), use el **[!UICONTROL SMS]** para definir la configuración y el contenido del canal SMS.

![](assets/sms_1.png)

Para empezar a personalizar el mensaje SMS, siga estos pasos:

1. Haga clic en el **[!UICONTROL Add text message]** para abrir el editor de expresiones.

   ![](assets/sms_3.png)

1. Utilice el Editor de expresiones para definir el contenido y los datos de personalización. Obtenga más información sobre personalización en el Editor de expresiones en [esta sección](../personalization/personalize.md)

   >[!NOTE]
   >
   > Los mensajes SMS están limitados a una longitud de 160 caracteres.

   ![](assets/sms_2.png)

1. Haga clic en **[!UICONTROL Save]** cuando el mensaje personalizado esté listo.

1. Haga clic en **[!UICONTROL Preview]** para visualizar cómo se mostrará su mensaje SMS en los dispositivos móviles. Para obtener más información, consulte [esta sección](../design/preview.md).

1. Una vez que el mensaje esté listo, puede publicarlo para que esté disponible para la ejecución con la variable **[!UICONTROL Publish]** botón. Esta acción publicará la nueva versión del mensaje que se utilizará para las próximas ejecuciones en sus recorridos.

El mensaje SMS ahora se puede usar en un recorrido. [Obtenga información sobre cómo crear recorridos](../building-journeys/journey-gs.md).

## Inclusión y exclusión{#sms-opt-in-out}

Los destinatarios de SMS pueden responder con palabras clave de inclusión y exclusión. De acuerdo con las normas y regulaciones del sector, Adobe Journey Optimizer procesa automáticamente las siguientes palabras clave en los mensajes entrantes: START, STOP y UNSTOP. Estas palabras clave déclencheur las respuestas estándar automáticas del proveedor de SMS.

**Temas relacionados**

* [Configuración del canal de SMS](../configuration/sms-configuration.md)
* [Informe SMS](../reports/journey-global-report.md#sms-global)
* [Crear un mensaje nuevo](get-started-content.md)
* [Adición de un mensaje en un recorrido](../building-journeys/journeys-message.md)
