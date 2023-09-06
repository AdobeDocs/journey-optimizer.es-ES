---
title: Buscar un calificador de colección
description: Los calificadores de colección le permiten organizar y ordenar mejor sus ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: e2d1f093-c1b8-4c4c-a20f-4bd7c2ea5269
source-git-commit: e8fe3ffd936c4954e8b17f58f1a2628bea0e2e79
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 7%

---

# Buscar un calificador de colección {#look-up-tag}

Puede buscar calificadores de colección específicos (anteriormente conocidos como &quot;etiquetas&quot;) realizando una solicitud de GET a [!DNL Offer Library] API que incluye el calificador de recopilación `id` en la ruta de solicitud.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/dps` |
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

Una respuesta correcta devuelve los detalles del calificador de recopilación, incluida la información sobre el calificador de recopilación único `id`.

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
