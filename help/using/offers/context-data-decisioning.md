---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Solicitudes de datos de contexto y toma de decisiones
description: Obtenga información sobre cómo pasar datos de contexto en solicitudes de Decisioning.
badge: label="Heredado" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 45d060ce-0a12-4a6e-a594-ec10cdff8f38
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/QQgN8UHq26U37o902TwS4p33TMYEUPg5A-i2AYLbOwI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: c132d929-fa62-4271-803e-b823be07b914
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 10%

---

# Solicitudes de datos de contexto y toma de decisiones {#context-data-decisioning}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../experience-decisioning/gs-experience-decisioning.md)

Esta sección le guía a través del paso de datos de contexto en solicitudes de Decisioning y su uso en reglas de aceptación.

>[!BEGINSHADEBOX]

Para ir más lejos, también puedes aprovechar el contexto en **fórmulas de clasificación** para aumentar tus ofertas. Hay ejemplos detallados de fórmulas de clasificación que aprovechan los datos de contexto disponibles en [esta sección](../offers/ranking/create-ranking-formulas.md#context-data).

>[!ENDSHADEBOX]

## Paso de datos de contexto en solicitudes de Decisioning

Los datos de contexto en las solicitudes de Decisioning se definen con la clave: `xdm:ContextData`.

Los atributos de datos de contexto no están gobernados por un esquema XDM. Puede pasar cualquier dato de contexto en JSON como parte de la carga útil de la solicitud de Decisioning.

Esta es una solicitud de toma de decisiones de ejemplo con datos de contexto (consulte `xdm:ContextData`):

```
curl --location 'https://platform-stage.adobe.io/data/core/ods/decisions' \
--header 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
--header 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
--header 'Authorization: Bearer eyJhbGciOi....' \
--header 'x-api-key: {{api_key}}' \
--header 'x-gw-ims-org-id: {{ims_org}}' \
--header 'x-sandbox-name: {{sandbox_name}}' \
--header 'x-request-id: {{$guid}}' \
--data-raw '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:19978bf95ebfc8fb",
            "xdm:placementId": "dps:offer-placement:199772e1c90d50ac"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "test@test.com",
                        "primary": true
                    }
                ]
            },
            "xdm:contextData": [
                {
                    "@type": "_xdm.context.additionalParameters;version=1",
                    "xdm:data": {
                        "xdm:channel": "mobile",
                        "xdm:language": "en",
                        "xdm:isThirdParty": true,
                        "xdm:mobileVersion": "3.0.5106",
                        "xdm:mobileVersionMajor": "3",
                        "xdm:mobileVersionMinor": "0",
                        "xdm:mobileVersionPatch": "125",
                        "xdm:deviceType": "iOS",
                        "xdm:features": [
                            "p1000",
                            "p1001"
                        ]
                    }
                }
            ]
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}'
```

## Uso de datos de contexto en reglas de idoneidad

Estos son ejemplos que ilustran cómo utilizar los datos de contexto pasados en las solicitudes de Decisioning en las reglas de elegibilidad.

* Apto si las funciones de datos de contexto contienen un valor determinado:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where contextData.features AND (select personetic from contextData.features where personetic.contains("123"))
  ```

* Apto si el canal no está vacío e es igual a móvil:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where !contextData.channel.isNull() AND contextData.channel!="" AND contextData.channel="mobile"
  ```
