---
title: Buscar una ubicación de exd
description: La ubicación de Exd consiste en colecciones asociadas con restricciones y métodos de clasificación para determinar ofertas.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 8%

---

# Buscar una ubicación de exd {#list-exd-placement}

Puede buscar un reemplazo específico realizando una petición GET a la API de la biblioteca de ofertas que incluya el ID en la ruta de solicitud.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/exd-placements/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | El ID de la entidad que desea buscar. | `placement1234` |

**Solicitud**

```shell
curl --location 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19c5fa7448c6fcab' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}'
```

**Respuesta**

Una respuesta correcta devuelve los detalles de la ubicación de salida.

```json
{
    "created": "2024-11-14T20:56:45.540Z",
    "modified": "2024-11-14T20:56:45.540Z",
    "etag": 1,
    "schemas": [
        "exd-placement"
    ],
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "id": "dps:exd-placement:19c5fa7448c6fcab",
    "name": "Test Exd Placement1 Car",
    "description": "brand panel",
    "tags": [
        "3d75b849-b344-402b-9d9e-5d750bd46884"
    ],
    "channel": "https://ns.adobe.com/xdm/channel-types/email",
    "channelConfiguration": "530b76f9-dcd6-4fd5-8c52-38e29b04a60a",
    "status": "active"
}            
```
