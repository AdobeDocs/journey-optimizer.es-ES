---
title: Buscar una oferta personalizada
description: Una oferta personalizada es un mensaje de marketing personalizable basado en reglas y restricciones de idoneidad.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2e30b155-688b-432b-a703-d09de12ebdfd
source-git-commit: 353aaf2bc4f32b1b0d7bfc2f7f4f48537cc79df4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---

# Buscar una oferta personalizada {#look-up-personalized-offer}

Una oferta personalizada es un mensaje de marketing personalizable basado en reglas y restricciones de idoneidad.

Puede buscar ofertas personalizadas específicas realizando una solicitud de GET al [!DNL Offer Library] API que incluye la oferta personalizada `@id` o el nombre de la oferta personalizada en la ruta de solicitud.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PERSONALIZED_OFFER}&{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las ofertas personalizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_PERSONALIZED_OFFER}` | Define el esquema asociado a ofertas personalizadas. | `https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5` |
| `id` | Una cadena que se usa para hacer coincidir con la variable `@id` propiedad de las entidades. La cadena coincide exactamente. El parámetro &quot;id&quot; y &quot;name&quot; no se puede usar juntos. | `xcore:personalized-offer:124cc332095cfa74` |
| `name` | Cadena que se utiliza para coincidir con la propiedad xdm:name de las entidades. La cadena coincide exactamente, con mayúsculas, pero se pueden utilizar caracteres comodín. Los parámetros `id` y `name` no se puede usar juntos | `Discount offer` |

**Solicitud**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&name=Discount%20offer' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve los detalles de la ubicación, incluida la información sobre el ID del contenedor, el ID de instancia y la oferta personalizada única `@id`.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5",
    "requestTime": "2020-10-21T20:59:16.238585Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 1,
                "repo:createdDate": "2020-10-20T20:01:02.927874Z",
                "repo:lastModifiedDate": "2020-10-20T20:01:02.927874Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_score": 0,
                "_instance": {
                    "xdm:name": "Discount offer",
                    "xdm:representations": [
                        {
                            "xdm:components": [
                                {
                                    "dc:language": [
                                        "en"
                                    ],
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-json",
                                    "dc:format": "application/json"
                                }
                            ],
                            "xdm:placement": "xcore:offer-placement:12428d436d87dc84"
                        }
                    ],
                    "xdm:rank": {
                        "xdm:priority": 1
                    },
                    "xdm:selectionConstraint": {
                        "xdm:startDate": "2020-10-01T16:00:00Z",
                        "xdm:endDate": "2021-12-13T16:00:00Z",
                        "xdm:eligibilityRule": "xcore:eligibility-rule:124cb4511da781fc"
                    },
                    "xdm:status": "draft",
                    "xdm:cappingConstraint": {
                        "xdm:globalCap": 150
                    },
                    "xdm:tags": [
                        "xcore:tag:1246d138ec8cca1f"
                    ],
                    "@id": "xcore:personalized-offer:124cc332095cfa74"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5#fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/fb2aad00-130e-11eb-aa26-21e7b1fa6da6",
                        "@type": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                    }
                }
            }
        ],
        "total": 1,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&name=Discount%20offer",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
