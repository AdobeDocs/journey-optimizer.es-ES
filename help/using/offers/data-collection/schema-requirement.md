---
product: experience platform
solution: Experience Platform
title: Configurar la captura de eventos
description: Obtenga información sobre cómo configurar el esquema de oferta para capturar eventos
feature: Ranking, Datasets, Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 5%

---

# Configuración de la recopilación de datos {#schema-requirements}

Para poder obtener comentarios sobre tipos de eventos que no sean eventos de decisión, debe establecer el valor correcto para cada tipo de evento en una **evento de experiencia** que se envía a Adobe Experience Platform.

>[!CAUTION]
>
>Para cada tipo de evento, asegúrese de que el esquema utilizado en el conjunto de datos tenga la variable **[!UICONTROL Evento de experiencia: interacciones de propuesta]** grupo de campos asociado a él. [Más información](create-dataset.md)

A continuación se muestran los requisitos de esquema que debe implementar en el código JavaScript.

>[!NOTE]
>
>No es necesario enviar los eventos de decisión, ya que la administración de decisiones generará estos eventos automáticamente y los colocará en **[!UICONTROL ODE DecisionEvents]** conjunto de datos<!--to check--> que se genera automáticamente.

## Seguimiento de impresiones {#track-impressions}

Asegúrese de que el tipo de evento y el origen sean los siguientes:

**Tipo de evento de experiencia:** `decisioning.propositionDisplay`
**Fuente:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o ingesta por lotes
+++**Carga útil de ejemplo:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
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
**Fuente:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o ingesta por lotes
+++**Carga útil de ejemplo:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
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

Para los eventos personalizados, el esquema utilizado en el conjunto de datos también debe tener **[!UICONTROL Evento de experiencia: interacciones de propuesta]** grupo de campos asociado a él, pero no hay ningún requisito específico sobre el tipo de evento de experiencia que debe utilizarse para etiquetar estos eventos.

>[!NOTE]
>
>Para que sus eventos personalizados se contabilicen en [restricción de frecuencia](../offer-library/add-constraints.md#capping)Además, debe conectar el evento de experiencia a los extremos de Adobe Experience Platform enviándolo a uno de estos dos extremos de recopilación de datos de Edge:
>
>* POST /ee/v2/interaction
>* POST /ee/v2/collect
>
>Si utiliza el complemento [SDK web de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}, la conexión se establece automáticamente.
