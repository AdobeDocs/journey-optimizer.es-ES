---
title: Actualización de un elemento de decisión
description: Los elementos de decisión son ofertas de marketing que se pueden crear y organizar en colecciones y catálogos.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: b924b7d0-bbed-409e-8173-0685fc41d7de
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 6%

---

# Actualización de un elemento de decisión {#update-decision-items}

Puede modificar o actualizar un elemento de decisión realizando una petición PATCH a la API de la biblioteca de ofertas.

Para obtener más información sobre el parche JSON, incluidas las operaciones disponibles, consulte la [documentación oficial del parche JSON](https://jsonpatch.com/).

**Formato de API**

```http
PATCH /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | El ID de la entidad que desea actualizar. | `offerItem1234` |

**Solicitud**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}' \
-d '[
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemName",
        "value": "Updated offer item"
    },
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemDescription",
        "value": "Updated offer item description"
    }
]'
```

| Parámetro | Descripción |
| --------- | ----------- |
| `value` | El nuevo valor con el que desea actualizar el parámetro. |
| `path` | Ruta del parámetro que se va a actualizar. |
| `op` | Tipo de operación que se va a realizar. Las operaciones incluyen: `add`, `replace`, `remove`, `copy` y `test`. |

**Respuesta**

Una respuesta correcta devuelve los detalles del elemento actualizado, incluido el ID. Puede utilizar el ID en pasos posteriores para actualizar o eliminar el elemento de decisión.

```json
{
    "etag": 2,
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
