---
title: Enumerar ofertas personalizadas
description: Una oferta personalizada es un mensaje de marketing personalizable basado en reglas y restricciones de idoneidad.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 45d51918-1106-4b6b-b383-8ab4d9a4f7af
source-git-commit: 9873af4caf7cd8bc4e9672748414bf78f28ed30b
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 6%

---

# Enumerar ofertas personalizadas {#list-personalized-offers}

Una oferta personalizada es un mensaje de marketing personalizable basado en reglas y restricciones de idoneidad.

Puede ver una lista de todas las ofertas personalizadas dentro de un contenedor realizando una sola solicitud de GET al [!DNL Offer Library] API.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PERSONALIZED_OFFER}&{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las ofertas personalizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_PERSONALIZED_OFFER}` | Define el esquema asociado a ofertas personalizadas. | `https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5` |
| `{QUERY_PARAMS}` | Parámetros de consulta opcionales para filtrar los resultados por. | `limit=1` |

**Solicitud**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&limit=1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Uso de parámetros de consulta {#using-query-parameters}

Puede utilizar parámetros de consulta para filtrar los resultados y la página cuando enumere recursos.

### Paginación {#paging}

Los parámetros de consulta más comunes para la paginación incluyen:

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `q` | Una cadena de consulta opcional para buscar en los campos seleccionados. La cadena de consulta debe estar en minúscula y puede estar rodeada de comillas dobles para evitar que se la toquee y para que escape de caracteres especiales. Los caracteres `+ - = && || > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` tienen un significado especial y deben evitarse con una barra invertida al aparecer en la cadena de consulta. | `discounted offers` |
| `qop` | Aplica el operador AND u OR a los valores del parámetro de cadena de consulta q. | `AND` / `OR` |
| `field` | Lista opcional de campos a los que limitar la búsqueda. Este parámetro se puede repetir de esta manera: field=field1[,campo=campo2,...] y (las expresiones de ruta están en forma de rutas separadas por puntos como _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Ordene los resultados por una propiedad específica. Adición de un `-` antes del título (`orderby=-title`) ordenará los elementos por título en orden descendente (Z-A). | `-repo:createdDate` |
| `limit` | Limite el número de ofertas personalizadas devueltas. | `limit=5` |

**Respuesta**

Una respuesta correcta devuelve una lista de ofertas personalizadas que están presentes dentro del contenedor al que tiene acceso.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5",
    "requestTime": "2020-10-22T20:36:50.408105Z",
    "_embedded": {
        "results": [
            {
                "instanceId": "2cdb4d10-149e-11eb-b1a9-a779d2fe8690",
                "schemas": [
                    "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-10-22T19:38:35.489354Z",
                "repo:lastModifiedDate": "2020-10-22T19:45:43.839088Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "Checking Advanced",
                    "xdm:representations": [
                        {
                            "xdm:components": [
                                {
                                    "dc:format": "image/png",
                                    "repo:id": "urn:aaid:sc:US:7db21be9-89ee-472a-b2c9-91f7a39ada51",
                                    "repo:resolveURL": "https://platform-cs-va6.adobe.io/content/storage/id/urn:aaid:sc:US:7db21be9-89ee-472a-b2c9-91f7a39ada51/:rendition;size=300",
                                    "repo:name": "mobile-check-deposit.png",
                                    "dc:language": [
                                        "en-us"
                                    ],
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-imagelink",
                                    "xdm:deliveryURL": ""
                                }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/offline",
                            "xdm:placement": "xcore:offer-placement:124f4e33724bb15f"
                        },
                        {
                            "xdm:components": [
                                {
                                    "dc:format": "text/html",
                                    "repo:name": "my content",
                                    "dc:language": [
                                        "en-us"
                                    ],
                                    "xdm:content": "{\n\"foo\": \"bar\"\n}",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-html"
                                }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
                        }
                    ],
                    "xdm:rank": {
                        "xdm:priority": 10
                    },
                    "xdm:characteristics": {
                        "PROD": "checking",
                        "offer_code": "CHECK200",
                        "region": "NA"
                    },
                    "xdm:selectionConstraint": {
                        "xdm:startDate": "2020-10-22T07:00:00.000Z",
                        "xdm:endDate": "2020-12-31T08:00:00.000Z",
                        "xdm:eligibilityRule": "xcore:eligibility-rule:124f4f57259caba5"
                    },
                    "xdm:status": "draft",
                    "xdm:cappingConstraint": {
                        "xdm:globalCap": 1000
                    },
                    "xdm:tags": [
                        "xcore:tag:124f4e5c8a00cd92",
                        "xcore:tag:1229cf47455177b1"
                    ],
                    "@id": "xcore:personalized-offer:124f513c290bb16e"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5#2cdb4d10-149e-11eb-b1a9-a779d2fe8690",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/2cdb4d10-149e-11eb-b1a9-a779d2fe8690",
                        "@type": "https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
            }
        ],
        "total": 15,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&orderby=-repo:createdDate&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=1603395515489%2C2cdb4d10-149e-11eb-b1a9-a779d2fe8690&schema=https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5&orderby=-repo%3AcreatedDate%2CinstanceId&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
