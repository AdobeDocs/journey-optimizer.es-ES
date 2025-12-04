---
solution: Journey Optimizer
product: Journey Optimizer
title: Configurar la captura de eventos
description: Obtenga información sobre cómo configurar el esquema de oferta para capturar eventos
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
version: Journey Orchestration
source-git-commit: f43b1ea0dd2197331329e24cb3d76eef0b5a9e86
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# Configuración de la recopilación de datos {#schema-requirements}

Para poder obtener comentarios sobre tipos de eventos que no sean eventos de decisión, debe establecer el valor correcto para cada tipo de evento en un **evento de experiencia** que se envíe a Adobe Experience Platform.

>[!CAUTION]
>
>Para cada tipo de evento, asegúrese de que el esquema utilizado en el conjunto de datos tenga asociado el grupo de campos **[!UICONTROL Evento de experiencia - Interacciones de propuesta]**. <!--[Learn more](create-dataset.md)-->

A continuación se muestran los requisitos de esquema que debe implementar en el código JavaScript.

## Seguimiento de impresiones {#track-impressions}

Asegúrese de que los campos siguientes estén correctamente configurados:

**Tipo de evento de experiencia:** `decisioning.propositionDisplay`

**propositionEventType:** `_experience.decisioning.propositionEventType.display`

**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o ingesta por lotes

+++**Carga útil de ejemplo:**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "display": 1
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionDisplay",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b219",
  "timestamp": "2025-10-07T20:22:00Z"
}
```

+++

## Seguimiento de clics {#track-clicks}

Asegúrese de que los campos siguientes estén correctamente configurados:

**Tipo de evento de experiencia:** `decisioning.propositionInteract`

**propositionEventType:** `_experience.decisioning.propositionEventType.interact`

**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o ingesta por lotes

Cada oferta de una propuesta incluye un token de seguimiento, que es un identificador único generado por Adobe. Este token debe pasarse exactamente como se recibió (sin alteración) en el evento de clic o impresión correspondiente. La coincidencia de tokens de seguimiento garantiza que Adobe pueda asociar con precisión la acción del usuario con la decisión de oferta correcta, lo que permite la creación de informes descendente y la optimización basada en IA.

+++**Carga útil de ejemplo:**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "interact": 1
      },
      "propositionAction": {
        "tokens": [
          "Vx9fwWXmp6/kyYRVOUZWEQ"
        ]
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionInteract",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b765",
  "timestamp": "2025-10-07T20:50:00Z"
}
```

+++

## Seguimiento de eventos personalizados {#track-custom-events}

Para los eventos personalizados, el esquema utilizado en el conjunto de datos también debe tener asociado el grupo de campos **[!UICONTROL Evento de experiencia - Interacciones de propuesta]**, pero no hay ningún requisito específico sobre el tipo de evento de experiencia que debe usarse para etiquetar estos eventos.

<!--

>[!NOTE]
>
>To have your custom events accounted for in [capping](../items.md#capping), you need to connect the experience event to Adobe Experience Platform endpoints by sending it to either one of these two Edge data collection endpoints:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>If you are using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=es){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=es){target="_blank"}, the connection is made automatically.-->
