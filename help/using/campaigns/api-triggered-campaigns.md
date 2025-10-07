---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con campañas activadas por API
description: Obtenga información sobre cómo almacenar en déclencheur las campañas mediante las API de Journey Optimizer.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campañas, activadas por API, REST, optimizador, mensajes
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 801b90201c3ffcbfb7b038abac2bf99209a14c7a
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 58%

---


# Trabajo con campañas activadas por API {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Campañas activadas por API"
>abstract="**Campañas activadas por API transaccionales**<br/> Activar mensajes en tiempo real mediante llamadas API <br/><br/>**Mensajes de marketing**<br/> Contenido promocional (requiere inclusión, sujeto a reglas comerciales)<br/><br/>**Mensajes transaccionales**<br/> Contenido relacionado con el servicio (confirmación, alertas, no sujeto al consentimiento de marketing)<br/><br/>**Canales disponibles**<br/> Correo electrónico, SMS, notificaciones push"

## Acerca de las campañas activadas por API {#about}

Las campañas activadas por API permiten que las comunicaciones de marketing lleguen a un público en el momento adecuado o que los mensajes transaccionales/operativos lleguen a una persona, como un restablecimiento de contraseña. Este acto puede implicar una personalización no solo mediante el uso del atributo de perfil, sino también mediante los datos de contexto en tiempo real en el activador, que es una carga útil de API de REST.

Para ello, primero debe crear una campaña activada por API en Journey Optimizer y luego iniciar su ejecución a través de una llamada API usando la [API de REST de ejecución de mensaje interactiva](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

Los canales disponibles para las campañas activadas por API son correo electrónico, SMS y mensajes push.

➡️ [Descubra esta funcionalidad en vídeo](#video)


>[!NOTE]
>
>Los canales admitidos son: [Correo electrónico](../email/get-started-email.md), [SMS/MMS/RCS](../sms/get-started-sms.md), [Notificaciones push](../push/get-started-push.md).
>
>Los canales disponibles varían en función del modelo de licencia y los complementos.

## Pasos clave para la creación de campañas activadas por API {#steps}

Antes de comenzar con las campañas, compruebe los siguientes requisitos previos enumerados [en esta sección](get-started-with-campaigns.md#permissions). Una vez cumplidos estos requisitos previos, puede empezar a crear la campaña:

1. [Definir las propiedades de la campaña](api-triggered-campaign-properties.md)
1. [Configurar la acción de campaña](api-triggered-campaign-action.md)
1. [Edición del contenido de la campaña](api-triggered-campaign-content.md)
1. [Definición del público de la campaña](api-triggered-campaign-audience.md)
1. [Programación de la campaña](api-triggered-campaign-schedule.md)
1. [Revisión y activación de la campaña](review-activate-api-triggered-campaign.md)
1. [Activación de la ejecución de la campaña](trigger-campaigns.md)

## Vídeotutoriales {#video}

Obtenga información sobre cómo crear una campaña y almacenarla en déclencheur desde un sistema externo basado en las interacciones del usuario, mediante la API de REST de ejecución de mensaje interactivo.

>[!VIDEO](https://video.tv.adobe.com/v/3452728?quality=12&captions=spa)
