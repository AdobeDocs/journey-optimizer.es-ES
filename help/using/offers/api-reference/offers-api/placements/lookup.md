---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Búsqueda de una ubicación
description: Las ubicaciones son contenedores que se utilizan para mostrar sus ofertas.
feature: Decision Management, API
badge: label="Heredado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: db337b5c-426a-4695-81e8-3a1b041791f2
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/iCA7zUsyAz-n0zG5hcc7rLrUZtKTgU21oFge-RydV90
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 27%

---

# Búsqueda de una ubicación {#look-up-placement}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../../../experience-decisioning/gs-experience-decisioning.md)


Puede buscar ubicaciones específicas realizando una petición GET a la API [!DNL Offer Library] que incluye la ubicación `id`.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/placements/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | El ID de la entidad que desea buscar. | `offerPlacement1234` |

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve los detalles de la ubicación, incluida la información acerca de la ubicación única `id`.

```json
{
     "created": "2023-05-15T11:22:50.031+00:00",
    "modified": "2023-05-15T11:22:50.031+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.5"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerPlacement1234",
    "name": "Placement",
    "description": "Placement description",
    "componentType": "html",
    "channel": "https://ns.adobe.com/xdm/channel-types/web",
    "itemCount": 1,
    "allowDuplicatePlacements": false,
    "returnContent": false,
    "returnMetaData": {
        "decisionName": true,
        "offerName": true,
        "offerAttributes": true,
        "offerPriority": true,
        "placementName": true,
        "channelType": true,
        "contentType": true
    }
}
```
