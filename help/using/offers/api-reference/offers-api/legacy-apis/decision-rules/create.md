---
title: Crear una regla de decisión
description: Las reglas de decisión son restricciones agregadas a una oferta personalizada y aplicadas a un perfil para determinar la elegibilidad.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 12c49f4c-a1b5-4841-ab98-663b4c771fb6
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 13%

---

# Crear una regla de decisión {#create-decision-rule}

Las reglas de decisión son restricciones agregadas a una oferta personalizada y aplicadas a un perfil para determinar la elegibilidad.

## Encabezados Accept y Content-Type {#accept-and-content-type-headers}

En la tabla siguiente se muestran los valores válidos que comprenden los campos *Content-Type* y *Accept* del encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Aceptar | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"` |

**Formato de API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor donde se encuentran las reglas de decisión. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitud**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "xdm:name": "Sales rule",
    "description": "Decisioning rule for sales",
    "xdm:condition": {
        "xdm:type": "PQL",
        "xdm:format": "pql/text",
        "xdm:value": "profile.person.name.firstName.equals(\"Joe\", false)"
    },
    "xdm:definedOn": {
        "profile": {
            "xdm:schema": {
                "$ref": "https://ns.adobe.com/xdm/context/profile_union",
                "version": "1"
            },
            "xdm:referencePaths": [
                "person.name.firstName"
            ]
        }
    }
}'
```

**Respuesta**

Una respuesta correcta devuelve información sobre la regla de decisión recién creada, incluido su ID de instancia único y la ubicación `@id`. Puede utilizar el ID de instancia en pasos posteriores para actualizar o eliminar la regla de decisión. Puede utilizar la regla de decisión única `@id` en un tutorial posterior para crear ofertas personalizadas.

```json
{
    "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T20:13:43.048666Z",
    "repo:lastModifiedDate": "2023-10-21T20:13:43.048666Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
