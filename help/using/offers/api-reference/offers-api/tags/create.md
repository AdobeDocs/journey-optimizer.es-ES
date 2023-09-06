---
title: Creación de un cualificador de colección
description: Los calificadores de colección le permiten organizar y ordenar mejor sus ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
source-git-commit: 9b9ca28b185a342d908eeb53d772f9d011105aba
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 14%

---

# Creación de un cualificador de colección {#create-tag}

Puede crear un calificador de colección (anteriormente conocido como &quot;etiqueta&quot;) realizando una solicitud de POST a [!DNL Offer Library] API.

## Encabezados Accept y Content-Type {#accept-and-content-type-headers}

La siguiente tabla muestra los valores válidos que componen la variable *Content-Type* en el encabezado de la solicitud:

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

Una respuesta correcta devuelve información sobre el calificador de recopilación recién creado, incluido su `id`. Puede usarlo en pasos posteriores para actualizar o eliminar el calificador de recopilación. Puede utilizar el calificador de colección único `id` en tutoriales posteriores para crear colecciones y ofertas personalizadas.

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
