---
title: Búsqueda de una regla de decisión
description: Las reglas de decisión son restricciones agregadas a una oferta personalizada y aplicadas a un perfil para determinar la elegibilidad.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 3099736d-7109-4c94-aea6-053a9b885278
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 4%

---

# Búsqueda de una regla de decisión {#lookup-decision-rule}

Puede buscar una regla de decisión específica realizando una petición GET a la API [!DNL Offer Library] que incluya la regla de decisión `@id` o el nombre de la regla de decisión en la ruta de solicitud.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ELIGIBILITY_RULE}&{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor donde se encuentran las reglas de decisión. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ELIGIBILITY_RULE}` | Define el esquema asociado a las reglas de decisión. | `https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3` |
| `id` | Cadena utilizada para coincidir con la propiedad `@id` de las entidades. La cadena coincide exactamente. El parámetro `id` y `name` no se pueden usar juntos. | `xcore:eligibility-rule:124e0faf5b8ee89b` |
| `name` | Una cadena utilizada para hacer coincidir la propiedad xdm:name de las entidades. La cadena coincide exactamente, con mayúsculas, pero se pueden utilizar caracteres comodín. Los parámetros `id` y `name` no se pueden usar juntos | `Sales rule` |

**Solicitud**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&name=Sales%20rule' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve los detalles de la regla de decisión específica que buscó, incluida la información acerca de su regla de decisión única `id`.

```json
  {
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3",
    "requestTime": "2023-10-21T20:14:08.153670Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "eaa5af90-13d9-11eb-9472-194dee6dc381",
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
    ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2023-10-21T20:13:43.048666Z",
                "repo:lastModifiedDate": "2023-10-21T20:13:43.048666Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Sales rule",
                    "description": "Decisioning rule for sales",
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
                    },
    "condition": {
                        "format": "pql/text",
        "type": "PQL",
                        "value": "profile.person.name.firstName.equals(\"Joe\", false)"
                    },
                    "@id": "xcore:eligibility-rule:124e0faf5b8ee89b"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3#eaa5af90-13d9-11eb-9472-194dee6dc381",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381",
                        "@type": "https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/eligibility-rule;version=0.3&name=Sales%20rule",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
            }
}
```
