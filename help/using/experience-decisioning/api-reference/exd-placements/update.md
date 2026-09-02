---
title: Actualizar ubicación ext
description: La ubicación de Exd consiste en colecciones asociadas con restricciones y métodos de clasificación para determinar ofertas.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
exl-id: 74e090e1-4dbe-484b-a482-ef43e082e7b1
TQID: https://experienceleague.adobe.com/6RpNeMQUn2qEfAzQ-Q7f7PgBRJCLqp7WnsoKx0xr12s
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 7%

---

# Actualización de una ubicación externa {#update-exd-placement}

Puede modificar o actualizar una ubicación realizando una petición PUT a la API de la biblioteca de ofertas.

Para obtener más información sobre JSON PUT, incluidas las operaciones disponibles, consulte la documentación oficial de JSON PUT.

**Encabezados Accept y Content-Type**

En la tabla siguiente se muestran los valores válidos que comprenden los campos Content-Type del encabezado de la solicitud:

| Parámetro | Descripción |
| --------- | ----------- |
| Content-Type | `application/json` |

**Formato de API**

```http
PUT /{ENDPOINT_PATH}/exd-placements/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | El ID de la entidad que desea actualizar. | `placement1234` |

**Solicitud**

```shell
curl --location --request PUT 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19aca09b0a456e57' \
--H 'Content-Type: application/json' \
--H 'x-gw-ims-org-id: {IMS_ORG}' \
--H 'x-sandbox-name: {SANDBOX_NAME}' \
--H 'x-api-key: {API_KEY}' \
--H 'Authorization: Bearer {ACCESS_TOKEN}' \
--X '{
  "id":"dps:exd-placement:19aca09b0a456e57",
  "description": "Keyboard application",
  "status":"archived"
}'
```

| Parámetro | Descripción |
| --------- | ----------- |
| `value` | El nuevo valor con el que desea actualizar el parámetro. |
| `path` | Ruta del parámetro que se va a actualizar. |
| `op` | La llamada de operación utilizada para definir la acción necesaria para actualizar la conexión. Las operaciones incluyen: `add`, `replace`, `remove`, `copy` y `test`. |

**Respuesta**

Una respuesta correcta devuelve los detalles actualizados de la ubicación de salida, incluido el ID.

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
