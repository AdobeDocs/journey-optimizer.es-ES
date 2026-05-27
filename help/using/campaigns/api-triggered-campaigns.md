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
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 901ecd19969ea7a79d1fad38c4e3140fea2e01ec
workflow-type: tm+mt
source-wordcount: 293
ht-degree: 38%

---

# Trabajo con campañas activadas por API {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Campañas activadas por API"
>abstract="**Campañas activadas por API transaccionales**<br/> Activar mensajes en tiempo real mediante llamadas API <br/><br/>**Mensajes de marketing**<br/> Contenido promocional (requiere inclusión, sujeto a reglas comerciales)<br/><br/>**Mensajes transaccionales**<br/> Contenido relacionado con el servicio (confirmación, alertas, no sujeto al consentimiento de marketing)<br/><br/>**Canales disponibles**<br/> Correo electrónico, SMS, notificaciones push"

## Acerca de las campañas activadas por API {#about}

Las campañas activadas por API permiten que las comunicaciones de marketing lleguen a una audiencia en el momento adecuado o que los mensajes transaccionales/operativos lleguen a una persona, como un restablecimiento de contraseña, donde la necesidad puede implicar una personalización no solo mediante atributos de perfil, sino también datos de contexto en tiempo real en el déclencheur, que es una carga útil de API de REST.

Para ello, primero debe crear una campaña activada por API en Journey Optimizer y luego iniciar su ejecución a través de una llamada API usando la [API de REST de ejecución de mensaje interactiva](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution).

➡️ [Descubra esta función en vídeo](#video)

>[!NOTE]
>
>Para obtener más información sobre los canales admitidos, consulte la tabla de esta sección: [Canales en recorridos y campañas](../channels/gs-channels.md#channels).
>
>Los canales disponibles varían en función del modelo de licencia y los complementos.

## Pasos clave para la creación de campañas activadas por API {#steps}

Antes de comenzar con las campañas, compruebe los siguientes requisitos previos enumerados [en esta sección](get-started-with-campaigns.md#prerequisites). Una vez cumplidos estos requisitos previos, puede empezar a crear la campaña:

1. [Definir las propiedades de la campaña](api-triggered-campaign-properties.md)
1. [Configurar la acción de campaña](api-triggered-campaign-action.md)
1. [Edición del contenido de la campaña](api-triggered-campaign-content.md)
1. [Definición del público de la campaña](api-triggered-campaign-audience.md)
1. [Programación de la campaña](api-triggered-campaign-schedule.md)
1. [Revisión y activación de la campaña](review-activate-api-triggered-campaign.md)
1. [Activación de la ejecución de la campaña](trigger-campaigns.md)

Obtenga más información sobre [completar el flujo de trabajo de creación de campañas con guías específicas del tipo →](get-started-with-campaigns.md#workflow)

## Vídeotutoriales {#video}

Obtenga información sobre cómo crear una campaña y almacenarla en déclencheur desde un sistema externo basado en las interacciones del usuario, mediante la API de REST de ejecución de mensaje interactivo.

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
