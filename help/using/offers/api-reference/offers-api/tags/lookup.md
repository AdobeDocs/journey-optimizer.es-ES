---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Buscar un calificador de colección
description: Los calificadores de colección le permiten organizar y ordenar mejor sus ofertas.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: e2d1f093-c1b8-4c4c-a20f-4bd7c2ea5269
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# Buscar un calificador de colección {#look-up-tag}

Puede buscar calificadores de colección específicos (anteriormente conocidos como &quot;etiquetas&quot;) realizando una petición GET a la API de la biblioteca de ofertas que incluya el ID del calificador de colección en la ruta de solicitud.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | El ID de la entidad que desea buscar. | `tag1234` |

**Solicitud**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve los detalles del calificador de recopilación, incluida la información sobre el ID de contenedor, el ID de instancia y el calificador de recopilación único `@id`.

```json
{
    "created": "2022-09-16T19:00:02.070+00:00",
    "modified": "2022-09-16T19:00:02.070+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "tag1234",
    "name": "Sneakers"
}
```
