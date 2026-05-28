---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Búsqueda de una decisión
description: Una decisión contiene la lógica que indica la selección de una oferta.
feature: Decision Management, API
badge: label="Heredado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 99159704-fa39-47ff-b445-0cd6b325007d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/UwFOIpfuJbo4x80iXItfzzZt58RGnZcyOtYSdwEiJKk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 15%

---

# Búsqueda de una decisión {#look-up-decision}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../../../../experience-decisioning/gs-experience-decisioning.md)


Puede buscar decisiones específicas realizando una petición GET a la API [!DNL Offer Library] que incluya las decisiones `@id` o el nombre de la decisión en la ruta de solicitud.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ACTIVITIES}&{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor en el que se encuentran las decisiones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ACTIVITIES}` | Define el esquema asociado a las decisiones. | `https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5` |
| `id` | Cadena utilizada para coincidir con la propiedad `@id` de las entidades. La cadena coincide exactamente. Los parámetros `id` y `name` no se pueden usar juntos. | `xcore:offer-activity:124527ab00b2ebbc` |
| `name` | Una cadena utilizada para hacer coincidir la propiedad xdm:name de las entidades. La cadena coincide exactamente, con mayúsculas, pero se pueden utilizar caracteres comodín. Los parámetros &quot;id&quot; y &quot;name&quot; no se pueden usar juntos | `LBAR` |

**Solicitud**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&id=xcore:offer-activity:124527ab00b2ebbc' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve los detalles de la ubicación, incluida la información sobre el ID de contenedor, el ID de instancia y la decisión única `@id`.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5",
    "requestTime": "2023-10-19T19:50:08.047489Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
    "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                ],
                "productContexts": [
                    "acp"
    ],
                "repo:etag": 1,
                "repo:createdDate": "2023-10-14T22:12:10.300775Z",
                "repo:lastModifiedDate": "2023-10-14T22:12:10.300775Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:fallback": "xcore:fallback-offer:1233160780eaa2ef",
                    "xdm:name": "LBAR",
                    "xdm:endDate": "2021-02-28T08:00:00.000Z",
                    "xdm:startDate": "2023-10-14T07:00:00.000Z",
                    "xdm:status": "live",
                    "xdm:criteria": [
        {
                            "xdm:placements": [
                                "xcore:offer-placement:122204529514a2c0"
                            ],
                            "xdm:optionSelection": {
                                "xdm:filter": "xcore:offer-filter:122a120f234dac7f"
                            }
                        }
            ],
                    "@id": "xcore:offer-activity:124527ab00b2ebbc"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5#4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/4e0206d0-0e6a-11eb-884a-c1a1104e3d7d",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"
                }
            },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 1,
        "count": 1
            },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&id=xcore:offer-activity:124527ab00b2ebbc",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
            }   
        }
}
```
