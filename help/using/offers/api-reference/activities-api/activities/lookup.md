---
title: Búsqueda de una decisión
description: Una decisión contiene la lógica que indica la selección de una oferta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ee242f0f-f331-4f41-9418-938b4ca1dda3
source-git-commit: a6ba9632f6de91ed7911012ec4174cb7a01f5f12
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 8%

---

# Búsqueda de una decisión {#look-up-decision}

Puede buscar decisiones específicas realizando una solicitud de GET a [!DNL Offer Library] API que incluye las decisiones `id` en la ruta de solicitud.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | El ID de la entidad que desea buscar. | `offerDecision1234` |

**Solicitud**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve los detalles de la decisión, incluida la información acerca de su decisión única `id`.

```json
{
    "created": "2022-11-15T16:35:06.873+00:00",
    "modified": "2023-05-15T15:00:27.641+00:00",
    "etag": 3,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerDecision1234",
    "name": "Test Decision One",
    "status": "draft",
    "startDate": "2021-08-23T07:00:00.000+00:00",
    "endDate": "2021-08-25T07:00:00.000+00:00",
    "fallback": "fallbackOffer1234",
    "criteria": [
        {
            "placements": [
                "offerPlacement1234",
                "offerPlacement5678"
            ],
            "rank": {
                "priority": 0,
                "order": {
                    "orderEvaluationType": "ranking-strategy",
                    "rankingStrategy": "123456789123"
                }
            },
            "profileConstraint": {
                "profileConstraintType": "none"
            },
            "optionSelection": {
                "filter": "offerCollection1234"
            }
        }
    ]
}
```
