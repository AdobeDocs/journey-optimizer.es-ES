---
title: Crear una regla de decisión
description: Las reglas de decisión son restricciones agregadas a una oferta personalizada y aplicadas a un perfil para determinar la elegibilidad.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 6a05efca-31bd-46d5-998d-ff3038d9013f
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 15%

---

# Crear una regla de decisión {#create-decision-rule}

Las reglas de decisión son restricciones agregadas a una oferta personalizada y aplicadas a un perfil para determinar la elegibilidad.

## Encabezados Accept y Content-Type {#accept-and-content-type-headers}

La siguiente tabla muestra los valores válidos que comprenden el campo *Content-Type* del encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato de API**

```http
POST /{ENDPOINT_PATH}/offer-rules
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |

**Solicitud**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-rules' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Sales rule",
    "description": "Decisioning rule for sales",
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "profile.person.name.firstName.equals(\"Joe\", false)"
    },
    "definedOn": {
        "profile": {
            "schema": {
                "ref": "https://ns.adobe.com/xdm/context/profile_union",
                "version": "1"
            },
            "referencePaths": [
                "person.name.firstName"
            ]
        }
    }
}'
```

**Respuesta**

Una respuesta correcta devuelve información sobre la regla de decisión `id` recién creada. Puede usar `id` en pasos posteriores para actualizar o eliminar la regla de decisión o usarla en un tutorial posterior para crear decisiones, reglas de decisión y ofertas de reserva.

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
