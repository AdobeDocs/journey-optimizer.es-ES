---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Actualizar calificadores de colección
description: Los calificadores de colección le permiten organizar y ordenar mejor sus ofertas.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 918927e1-ad7a-4937-b652-2a0932e9efa1
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 11%

---


# Actualización de un cualificador colección {#update-collection-qualifier}

Puede modificar o actualizar un calificador de colección (anteriormente conocido como &quot;etiqueta&quot;) realizando una petición PATCH a la API de la biblioteca de ofertas.

Para obtener más información sobre el parche JSON, incluidas las operaciones disponibles, consulte la [documentación oficial del parche JSON](https://jsonpatch.com/).

## Encabezados Accept y Content-Type {#accept-and-content-type-headers}

La siguiente tabla muestra los valores válidos que comprenden el campo *Content-Type* del encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato de API**

```http
PATCH /{ENDPOINT_PATH}/tags/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | El ID de la entidad que desea actualizar. | `tag1234` |

**Solicitud**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated tag"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated tag description"
    }
]'
```

**Respuesta**

Una respuesta correcta devuelve los detalles actualizados del calificador de recopilación, incluido su exclusivo `id`.

```json
{
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 2,
    "createdDate": "2023-09-07T12:36:26.602Z",
    "lastModifiedDate": "2023-09-07T12:36:26.602Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
