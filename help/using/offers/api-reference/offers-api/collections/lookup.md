---
title: Buscar una colección
description: Las colecciones son subconjuntos de ofertas basados en condiciones predefinidas definidas definidas por un especialista en marketing, como la categoría de la oferta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 723daab2-5590-4c44-acb6-93a77f2e7877
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---

# Buscar una colección

Las colecciones son subconjuntos de ofertas basados en condiciones predefinidas definidas definidas por un especialista en marketing, como la categoría de la oferta.

Puede buscar colecciones específicas realizando una solicitud de GET al [!DNL Offer Library] API que incluye la colección `@id` o el nombre de la colección en la ruta de solicitud.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FILTER}&{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las colecciones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FILTER}` | Define el esquema asociado a las colecciones. | `https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1` |
| `id` | Una cadena que se usa para hacer coincidir con la variable `@id` propiedad de las entidades. La cadena coincide exactamente. Los parámetros `id` y `name` no se puede usar juntos. | `xcore:offer-filter:124bd44648f17ec1` |
| `name` | Cadena que se utiliza para coincidir con la propiedad xdm:name de las entidades. La cadena coincide exactamente, con mayúsculas, pero se pueden utilizar caracteres comodín. Los parámetros `id` y `name` no se puede usar juntos | `Mobile demo` |

**Solicitud**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&id=xcore:offer-filter:124bd44648f17ec1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve los detalles de la ubicación, incluida la información sobre el ID del contenedor, el ID de instancia y la recopilación única `@id`.

```json
{
    "containerId": "ab574eca-f7a9-38d0-b3d9-297376ca9ee2",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1",
    "requestTime": "2020-10-21T21:29:27.329070Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-20T02:37:11.263718Z",
                "repo:lastModifiedDate": "2020-10-20T02:37:11.263718Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:ids": [
                        "xcore:tag:124bd3de7f598dd8"
                    ],
                    "xdm:name": "Mobile Demo",
                    "xdm:filterType": "anyTags",
                    "@id": "xcore:offer-filter:124bd44648f17ec1"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3#27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "href": "/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances/27c92e00-127d-11eb-b9fe-5bcfb5d7ef36",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.3"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/ab574eca-f7a9-38d0-b3d9-297376ca9ee2/instances?schema=https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1&id=xcore:offer-filter:124bd44648f17ec1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
