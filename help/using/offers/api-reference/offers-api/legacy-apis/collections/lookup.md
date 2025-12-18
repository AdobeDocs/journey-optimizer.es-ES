---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Búsqueda de una colección
description: Las colecciones son subconjuntos de ofertas basados en condiciones predefinidas definidas definidas por un experto en marketing, como la categoría de la oferta.
feature: Decision Management, API, Collections
badge: label="Heredado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 91317c46-d8b6-456e-8282-aef1169941af
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 12%

---

# Búsqueda de una colección {#look-up-collection}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../../../../experience-decisioning/gs-experience-decisioning.md)


Las colecciones son subconjuntos de ofertas basados en condiciones predefinidas definidas definidas por un experto en marketing, como la categoría de la oferta.

Puede buscar colecciones específicas realizando una petición GET a la API [!DNL Offer Library] que incluya la colección `@id` o el nombre de la colección en la ruta de solicitud.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FILTER}&{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor donde se encuentran las colecciones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FILTER}` | Define el esquema asociado a las colecciones. | `https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1` |
| `id` | Cadena utilizada para coincidir con la propiedad `@id` de las entidades. La cadena coincide exactamente. Los parámetros `id` y `name` no se pueden usar juntos. | `xcore:offer-filter:124bd44648f17ec1` |
| `name` | Una cadena utilizada para hacer coincidir la propiedad xdm:name de las entidades. La cadena coincide exactamente, con mayúsculas, pero se pueden utilizar caracteres comodín. Los parámetros `id` y `name` no se pueden usar juntos | `Mobile demo` |

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

Una respuesta correcta devuelve los detalles de la ubicación, incluida la información sobre el ID de contenedor, el ID de instancia y la colección única `@id`.

```json
{
    "containerId": "ab574eca-f7a9-38d0-b3d9-297376ca9ee2",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1",
    "requestTime": "2023-10-21T21:29:27.329070Z",
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
                "repo:createdDate": "2023-10-20T02:37:11.263718Z",
                "repo:lastModifiedDate": "2023-10-20T02:37:11.263718Z",
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
