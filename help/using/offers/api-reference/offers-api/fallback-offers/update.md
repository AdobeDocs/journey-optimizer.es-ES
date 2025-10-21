---
title: Actualizar una oferta de reserva
description: Se envía una oferta de reserva a los clientes si no cumplen los requisitos para otras ofertas
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 7ff69887-620f-4bc0-b8ff-5144ff30696c
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 12%

---

# Actualizar una oferta de reserva {#update-fallback-offer}

Puede modificar o actualizar una oferta de reserva en su contenedor realizando una petición PATCH a la API [!DNL Offer Library].

Para obtener más información sobre el parche JSON, incluidas las operaciones disponibles, consulte la [documentación oficial del parche JSON](https://jsonpatch.com/).

## Encabezados Accept y Content-Type {#accept-and-content-type-headers}

En la tabla siguiente se muestran los valores válidos que comprenden los campos *Content-Type* y *Accept* del encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato de API**

```http
PATCH /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | El ID de la entidad que desea actualizar. | `fallbackOffer1234` |

**Solicitud**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated fallback offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated fallback offer description"
    }
]'
```

| Parámetro | Descripción |
| --------- | ----------- |
| `op` | La llamada de operación utilizada para definir la acción necesaria para actualizar la conexión. Las operaciones incluyen: `add`, `replace`, `remove`, `copy` y `test`. |
| `path` | Ruta del parámetro que se va a actualizar. |
| `value` | El nuevo valor con el que desea actualizar el parámetro. |

**Respuesta**

Una respuesta correcta devuelve los detalles actualizados de la oferta de reserva, incluido su `id`.

```json
{
    "id": "{ID}",
    "datasetId": "{DATASET_ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 2,
    "createdDate": "2023-09-07T12:47:43.012Z",
    "lastModifiedDate": "2023-09-07T12:47:43.012Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
