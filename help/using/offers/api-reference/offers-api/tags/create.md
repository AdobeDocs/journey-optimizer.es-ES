---
title: Creación de un cualificador de colección
description: Los calificadores de colección le permiten organizar y ordenar mejor sus ofertas.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 14%

---


# Creación de un cualificador de colección {#create-tag}

Puede crear un calificador de colección (anteriormente conocido como &quot;etiqueta&quot;) realizando una petición POST a la API de la biblioteca de ofertas.

## Encabezados Accept y Content-Type {#accept-and-content-type-headers}

La siguiente tabla muestra los valores válidos que comprenden los campos *Content-Type* del encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato de API**

```http
POST /{ENDPOINT_PATH}/tags
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |

**Solicitud**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/tags' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{        
    "name": "Black Friday",
    "description": "Tag for black friday"
}'
```

**Respuesta**

Una respuesta correcta devuelve información sobre el calificador de colección recién creado, incluido su `id` único. Puede usar `id` en pasos posteriores para actualizar o eliminar el calificador de colección. Puede usar el calificador de colección única `id` en tutoriales posteriores para crear colecciones y ofertas personalizadas.

```json
{
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 1,
    "createdDate": "2023-09-07T12:36:26.602Z",
    "lastModifiedDate": "2023-09-07T12:36:26.602Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
