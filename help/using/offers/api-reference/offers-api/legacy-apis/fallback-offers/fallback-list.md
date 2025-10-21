---
title: Enumerar ofertas de reserva
description: Se envía una oferta de reserva a los clientes si no cumplen los requisitos para otras ofertas
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 0eb68312-5567-4728-b184-9d40107676a0
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 5%

---

# Enumerar ofertas de reserva {#list-fallback-offers}

Se envía una oferta de reserva a los clientes si no cumplen los requisitos para otras ofertas. Los pasos para crear una oferta de reserva consisten en crear una o varias representaciones, como al crear una oferta.

Puede ver una lista de todas las ofertas de reserva dentro de un contenedor realizando una única petición GET a la API [!DNL Offer Library].

**Formato de API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_FALLBACK_OFFER}&{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las ofertas de reserva. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_FALLBACK_OFFER}` | Define el esquema asociado a las ofertas de reserva. | `https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1` |
| `{QUERY_PARAMS}` | Parámetros de consulta opcionales por los que filtrar los resultados. | `limit=1` |

**Solicitud**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

## Uso de parámetros de consulta {#using-query-parameters}

Puede utilizar parámetros de consulta para paginar y filtrar los resultados al enumerar recursos.

### Paginación {#paging}

Los parámetros de consulta más comunes para la paginación incluyen:

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `q` | Una cadena de consulta opcional para buscar en los campos seleccionados. La cadena de consulta debe estar en minúsculas y puede estar rodeada de comillas dobles para evitar que se muestre con tokens y para que salga de los caracteres especiales. Los caracteres `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` tienen un significado especial y se deben aplicar como escape una barra invertida cuando aparezcan en la cadena de consulta. | `default` |
| `qop` | Aplica el operador AND u OR a los valores del parámetro de cadena de consulta q. | `AND` / `OR` |
| `field` | Lista opcional de campos para limitar la búsqueda. Este parámetro se puede repetir como se indica a continuación: field=field1[,field=field2,...] y (las expresiones de ruta de acceso tienen la forma de rutas separadas por puntos como _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Ordene los resultados por una propiedad específica. Si se agrega un(a) `-` antes del título (`orderby=-title`), los elementos se ordenarán por título en orden descendente (Z-A). | `-repo:createdDate` |
| `limit` | Limite el número de ofertas de reserva devueltas. | `limit=5` |

**Respuesta**

Una respuesta correcta devuelve una lista de ofertas de reserva presentes dentro del contenedor al que tiene acceso.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1",
    "requestTime": "2023-10-22T07:12:30.923768Z",
    "_embedded": {
      "results": [
        {
                "instanceId": "053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
            "schemas": [
                    "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5"
            ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 3,
                "repo:createdDate": "2023-09-17T15:18:20.657299Z",
                "repo:lastModifiedDate": "2023-10-02T02:34:48.034583Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "F1: Web fallback ",
                    "xdm:representations": [
                {
                            "xdm:components": [
                        {
                                    "xdm:content": "aaa",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-json",
                                    "dc:format": "application/json",
                                    "repo:name": "aa"
                        }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122201b2150d98c2"
        },
        {
                            "xdm:components": [
                                {
                                    "xdm:content": "bb",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                                    "dc:format": "text/html",
                                    "repo:name": "bb"
                                }
            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122201c34354a2b4"
                        },
                {
                            "xdm:components": [
                        {
                                    "xdm:deliveryURL": "https://mysite.com",
                                    "@type": "https://ns.adobe.com/experience/offer-management/content-component-imagelink",
                                    "dc:format": "image/png",
                                    "repo:name": "ll"
                        }
                            ],
                            "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                            "xdm:placement": "xcore:offer-placement:122207eddb05205a"
                }
            ],
                    "xdm:status": "approved",
                    "xdm:tags": [],
                    "@id": "xcore:fallback-offer:122206064e0d98df"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5#053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/053bc610-f8f9-11ea-ad6e-775ad2c9b1a1",
                        "@type": "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.5"
                    }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
        }
    ],
        "total": 5,
        "count": 1
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=053bc610-f8f9-11ea-ad6e-775ad2c9b1a1&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1&limit=1",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
