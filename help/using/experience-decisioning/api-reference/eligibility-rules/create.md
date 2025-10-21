---
title: Creación de una regla de idoneidad
description: Las reglas de elegibilidad le permiten definir los candidatos elegibles en función de lo que desee segmentar, como atributos de perfil y audiencias.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 39c6e82e-c1b1-4dda-a941-3db6324cef37
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 7%

---

# Creación de una regla de idoneidad {#create-eligibility-rule}

Puede crear una regla de aceptación realizando una petición POST a la API de la biblioteca de ofertas.

**Formato de API**

```http
POST /{ENDPOINT_PATH}/eligibility-rules 
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |

**Solicitud**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-rules' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '
{
    "name": "test dule",
    "description": "xxxxxx",
    "exdRule": true,
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "inSegment(\"849807b6-0a76-4895-96d9-89996477f23b\") and billingAddress.city.equals(\"san jose\", false)"
    }
}'
```

**Respuesta**

Una respuesta correcta devuelve los detalles de la regla de idoneidad recién creada, incluido el ID. Puede usar el ID en pasos posteriores para actualizar o eliminar la regla de elegibilidad.

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
