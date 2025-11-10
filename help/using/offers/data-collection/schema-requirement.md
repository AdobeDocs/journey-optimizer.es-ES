---
solution: Journey Optimizer
product: Journey Optimizer
title: Configurar la captura de eventos
description: Obtenga información sobre cómo configurar el esquema de oferta para capturar eventos
badge: label="Heredado" type="Informative"
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
version: Journey Orchestration
source-git-commit: 3fa90fa707b562ecf2160ec980520bc8bc267a21
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 2%

---

# Configuración de la recopilación de datos {#schema-requirements}

Para poder obtener comentarios sobre tipos de eventos que no sean eventos de decisión, debe establecer el valor correcto para cada tipo de evento en un **evento de experiencia** que se envíe a Adobe Experience Platform.

>[!CAUTION]
>
>Para cada tipo de evento, asegúrese de que el esquema utilizado en el conjunto de datos tenga asociado el grupo de campos **[!UICONTROL Evento de experiencia - Interacciones de propuesta]**. [Más información](create-dataset.md)

A continuación se muestran los requisitos de esquema que debe implementar en el código JavaScript.

>[!NOTE]
>
>No es necesario enviar los eventos de decisión, ya que Administración de decisiones generará estos eventos automáticamente y los colocará en el conjunto de datos **[!UICONTROL ODE DecisionEvents]**<!--to check--> que se genera automáticamente.

## Seguimiento de impresiones {#track-impressions}

Asegúrese de que el tipo de evento y el origen sean los siguientes:

**Tipo de evento de experiencia:** `decisioning.propositionDisplay`
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o ingesta por lotes
+++**Carga útil de ejemplo:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for "nextBestOffer"
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for "nextBestOffer"
        }
    ]
}
```

+++

## Seguimiento de clics {#track-clicks}

Asegúrese de que el tipo de evento y el origen sean los siguientes:

**Tipo de evento de experiencia:** `decisioning.propositionInteract`
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o ingesta por lotes
+++**Carga útil de ejemplo:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

+++

## Seguimiento de eventos personalizados {#track-custom-events}

Para los eventos personalizados, el esquema utilizado en el conjunto de datos también debe tener asociado el grupo de campos **[!UICONTROL Evento de experiencia - Interacciones de propuesta]**, pero no hay ningún requisito específico sobre el tipo de evento de experiencia que debe usarse para etiquetar estos eventos.

>[!NOTE]
>
>Para que sus eventos personalizados se contabilicen en [límite de frecuencia](../offer-library/add-constraints.md#capping), debe conectar el evento de experiencia a los extremos de Adobe Experience Platform enviándolo a uno de estos dos extremos de recopilación de datos de Edge:
>
>* POST/ee/v2/interaction
>* POST /ee/v2/collect
>
>Si está usando [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es){target="_blank"} o [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=es){target="_blank"}, la conexión se establece automáticamente.
