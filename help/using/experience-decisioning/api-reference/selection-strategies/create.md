---
title: Crear una estrategia de selección
description: Las estrategias de selección consisten en colecciones asociadas con restricciones y métodos de clasificación para determinar ofertas.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 0e35c77b-6741-4c32-b012-36fc3a8b6d7a
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 8%

---

# Crear una estrategia de selección {#create-selection-strategy}

Puede crear una estrategia de selección realizando una petición POST a la API de la biblioteca de ofertas.

**Formato de API**

```http
POST /{ENDPOINT_PATH}/selection-strategies 
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |

**Solicitud**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/selection-strategies' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{    
    "name": "Selection Strategy One",
    "description": "Selection Strategy",
    "rank": {
        "priority": 1,
        "order": {
            "orderEvaluationType": "static"
        }
    },
    "profileConstraint": {
        "profileConstraintType": "eligibilityRule",
        "eligibilityRule": "offerRule1234"
    },
    "optionSelection": {
        "filter": "itemCollection1234",
    }
}'
```

**Respuesta**

Una respuesta correcta devuelve los detalles de la estrategia de selección recién creada, incluido el ID. Puede usar el ID en pasos posteriores para actualizar o eliminar la estrategia de selección.

```json
{
    "etag": 1,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
