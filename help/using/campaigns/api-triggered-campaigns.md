---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 17%

---
No se concedieron los permisos de la herramienta wiki. Procederé usando la información detallada del ticket en sí, que contiene las especificaciones clave (500 TPS por defecto, 1000/1500 TPS niveles a través de Performance Add-on, Push-solamente, admite aumentos de ráfaga/duración limitada).

&#x200B;---

solución: Journey Optimizer
producto: optimizador de recorrido
title: Trabajo con campañas activadas por API
description: Descubra cómo almacenar en déclencheur las campañas de mediante las API de Journey Optimizer.
Función: Campañas, API
Tema: Administración de contenido
función: Desarrollador
level: Con experiencia
palabras clave: campañas, activadas por API, REST, optimizador, mensajes
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2:
- id: cb954087-f4fc-4456-afb9-e939cabcdc79
internal-label: Journey Optimizer
feature_v2:
- id: a653cc2e-bc85-4353-a306-399e5b247978
internal-label: campañas de Journey Optimizer
subfeature_v2:
- id: f7479fa1-474b-479d-8c98-f6cee5865a38
internal-label: campañas activadas por API
- id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
internal-label: Administración de campañas
role_v2:
- id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label: Desarrollador
topic_v2:
- id: e0eb8757-182f-49f3-94a4-1587d16f5094
internal-label: Personalization

Este es el archivo Markdown completo actualizado:

&#x200B;---

```
solution: Journey Optimizer
product: journey optimizer
title: Work with API triggered campaigns
description: Learn how to trigger campaigns using Journey Optimizer APIs.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campaigns, API-triggered, REST, optimizer, messages
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
    internal-label: Journey Optimizer campaigns
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
    internal-label: API triggered campaigns
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
    internal-label: Campaign management
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
```

# Trabajo con campañas activadas por API {#trigger-campaigns}

>[!BEGINSHADEBOX]

**En esta página:** Cree e inicie campañas activadas por API mediante una llamada a la API de REST para que pueda enviar mensajes transaccionales y de marketing en tiempo real utilizando datos contextuales y de perfil.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Campañas activadas por API"
>abstract="**Campañas activadas por API transaccionales**<br/> Activar mensajes en tiempo real mediante llamadas API <br/><br/>**Mensajes de marketing**<br/> Contenido promocional (requiere inclusión, sujeto a reglas comerciales)<br/><br/>**Mensajes transaccionales**<br/> Contenido relacionado con el servicio (confirmación, alertas, no sujeto al consentimiento de marketing)<br/><br/>**Canales disponibles**<br/> Correo electrónico, SMS, notificaciones push"

## Acerca de las campañas activadas por API {#about}

Las campañas activadas por API permiten que las comunicaciones de marketing lleguen a una audiencia en el momento adecuado o que los mensajes transaccionales/operativos lleguen a una persona, como un restablecimiento de contraseña, donde la necesidad puede implicar una personalización no solo mediante atributos de perfil, sino también datos de contexto en tiempo real en el déclencheur, que es una carga útil de API de REST.

Para ello, primero debe crear una campaña activada por API en Journey Optimizer y luego iniciar su ejecución a través de una llamada API usando la [API de REST de ejecución de mensaje interactiva](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution).

➡️ [Descubra esta funcionalidad en vídeo](#video)

>[!NOTE]
>
>Para obtener más información sobre los canales admitidos, consulte la tabla de esta sección: [Canales en recorridos y campañas](../channels/gs-channels.md#channels).
>
>Los canales disponibles varían en función del modelo de licencia y los complementos.

## Rendimiento de notificaciones push {#push-throughput}

De manera predeterminada, las campañas activadas por API admiten hasta **500 transacciones por segundo (TPS)** para la entrega de notificaciones push. Las organizaciones con requisitos de mensajería operativa de gran volumen pueden aumentar este límite con el **complemento de rendimiento**.

El complemento Rendimiento proporciona dos niveles de rendimiento más altos para las notificaciones push:

| Nivel | Rendimiento |
|------|-----------|
| Estándar | 500 TPS (incluidos para todos los clientes) |
| Complemento de rendimiento - Nivel 1 | 1.000 TPS |
| Complemento de rendimiento - Nivel 2 | 1.500 TPS |

Un mayor rendimiento está disponible como un aumento contractual permanente y por una duración **limitada** para admitir escenarios temporales de gran volumen, como lanzamientos de productos o campañas a gran escala.

>[!NOTE]
>
>Los niveles de rendimiento aumentados se aplican al **canal de notificaciones push solamente** para campañas activadas por API. Los canales de correo electrónico y SMS no están en el ámbito de este complemento.
>
>Póngase en contacto con el equipo de su cuenta de Adobe para habilitar un nivel de rendimiento más alto para su organización.

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

&#x200B;---

La adición clave es la nueva sección **Rendimiento de notificaciones push** (`## Push notification throughput {#push-throughput}`) colocada entre &quot;Acerca de&quot; y &quot;Pasos clave&quot;, que documenta:
- El TPS 500 predeterminado incluido para todos los clientes
- Los dos niveles del complemento Rendimiento (1000 y 1500 TPS)
- La compatibilidad con aumentos permanentes y de duración limitada
- Ámbito limitado solo al canal push
- Una nota que dirige a los clientes a su equipo de cuenta de Adobe