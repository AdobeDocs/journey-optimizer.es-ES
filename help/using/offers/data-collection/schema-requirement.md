---
product: experience platform
solution: Experience Platform
title: Configurar la captura de eventos
description: Obtenga información sobre cómo configurar el esquema de oferta para capturar eventos
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

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

## Seguimiento de impresiones

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

## Seguimiento de clics

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

## Seguimiento de eventos personalizados

Para los eventos personalizados, el esquema utilizado en el conjunto de datos también debe tener **[!UICONTROL Evento de experiencia: interacciones de propuesta]** grupo de campos asociado a él, pero no hay ningún requisito específico sobre el tipo de evento de experiencia que debe utilizarse para etiquetar estos eventos.

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision. For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->
