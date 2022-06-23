---
title: Creación de un mensaje SMS
description: Obtenga información sobre cómo crear un mensaje SMS en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 47b1c2832f82a5c168cd03f1d1b43a9223c945b3
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 9%

---

# Creación de un mensaje SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Creación de SMS"
>abstract="Añada el mensaje de texto y comience a personalizarlo con el Editor de expresiones."

Una vez que [crear un mensaje](get-started-content.md), use el **[!UICONTROL SMS]** para definir la configuración y el contenido del mensaje SMS.


>[!AVAILABILITY]
>
>Actualmente, el canal SMS solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, póngase en contacto con el representante del Adobe.

![](assets/sms_1.png)

Si es la primera vez que crea un mensaje SMS, asegúrese de que el canal SMS esté configurado. [Más información](../configuration/sms-configuration.md).

## Definir el contenido del SMS{#sms-content}

Para empezar a personalizar el mensaje SMS, siga estos pasos:

1. Haga clic en el **[!UICONTROL Add text message]** para abrir el editor de expresiones.

   ![](assets/sms_3.png)

1. Utilice el Editor de expresiones para definir el contenido. Puede utilizar cualquier atributo para personalizar el contenido, como el nombre del perfil o la ciudad. Obtenga más información sobre personalización en el Editor de expresiones en [esta sección](../personalization/personalize.md)

   >[!NOTE]
   >
   > Un mensaje SMS puede tener hasta 160 caracteres, incluidos espacios y saltos de línea.

   ![](assets/sms_2.png)

1. Haga clic en **[!UICONTROL Save]** cuando el mensaje esté listo.

## Validar el SMS{#sms-preview}

Una vez definido el contenido del mensaje, puede utilizar perfiles de prueba para previsualizarlo y probarlo. Si ha insertado [contenido personalizado](../personalization/personalize.md), puede comprobar cómo se muestra este contenido en el mensaje, aprovechando los datos de perfil de prueba.

Para visualizar la visualización de su mensaje SMS en dispositivos móviles, vaya a la **[!UICONTROL Preview]** pestaña .

Para obtener más información, consulte [esta sección](../design/preview.md).

## Publicar su SMS {#sms-publish}

Una vez que el mensaje esté listo, puede publicarlo para que esté disponible para la ejecución con la variable **[!UICONTROL Publish]** botón. Esta acción publica la nueva versión del mensaje que se utilizará para las próximas ejecuciones en sus recorridos.

El mensaje SMS ahora se puede usar en un recorrido. [Obtenga información sobre cómo crear recorridos](../building-journeys/journey-gs.md).

## Inclusión y exclusión{#sms-opt-in-out}

Para todos los mensajes de marketing, el SMS debe contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. Una vez cancelada la suscripción, los perfiles se eliminan automáticamente de la audiencia de futuros mensajes de marketing. La adición de un vínculo de baja no es obligatoria para los mensajes transaccionales.

Los destinatarios de SMS pueden responder con palabras clave de inclusión y exclusión. De acuerdo con las normas y regulaciones del sector, Adobe Journey Optimizer procesa automáticamente las siguientes palabras clave en los mensajes entrantes: START, STOP y UNSTOP. Estas palabras clave déclencheur las respuestas estándar automáticas del proveedor de SMS.

**Temas relacionados**

* [Configuración del canal de SMS](../configuration/sms-configuration.md)
* [Informe SMS](../reports/journey-global-report.md#sms-global)
* [Crear un mensaje nuevo](get-started-content.md)
* [Adición de un mensaje en un recorrido](../building-journeys/journeys-message.md)
