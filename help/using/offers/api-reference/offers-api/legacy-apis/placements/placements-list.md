---
title: Enumerar ubicaciones
description: Las ubicaciones son contenedores que se utilizan para mostrar sus ofertas.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52fbf683-d86f-43c6-be1a-c06141b64b16
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 12%

---

# Enumerar ubicaciones {#list-placements}

Las ubicaciones son contenedores que se utilizan para mostrar sus ofertas. Una ubicación ayuda a garantizar que el contenido de oferta correcto se muestre en la ubicación correcta dentro del mensaje. Al agregar contenido a una oferta, se le pedirá que seleccione una ubicación en la que se pueda mostrar dicho contenido.

Puede ver una lista de todas las ubicaciones dentro de un contenedor realizando una sola petición GET a la API [!DNL Offer Library].

**Formato de API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_PLACEMENT}&{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor donde se encuentran las ubicaciones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `SCHEMA_PLACEMENT}` | Define el esquema asociado a las ubicaciones. | `https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4` |
| `{QUERY_PARAMS}` | Parámetros de consulta opcionales por los que filtrar los resultados. | `limit=2` |

## Uso de parámetros de consulta {#using-query-parameters}

Puede utilizar parámetros de consulta para paginar y filtrar los resultados al enumerar recursos.

### Paginación {#paging}

Los parámetros de consulta más comunes para la paginación incluyen:

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `q` | Una cadena de consulta opcional para buscar en los campos seleccionados. La cadena de consulta debe estar en minúsculas y puede estar rodeada de comillas dobles para evitar que se muestre con tokens y para que salga de los caracteres especiales. Los caracteres `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` tienen un significado especial y se deben aplicar como escape una barra invertida cuando aparezcan en la cadena de consulta. | Sitio web JSON |
| `qop` | Aplica el operador AND u OR a los valores del parámetro de cadena de consulta q. | `AND` / `OR` |
| `field` | Lista opcional de campos para limitar la búsqueda. Este parámetro se puede repetir como se indica a continuación: field=field1[,field=field2,...] y (las expresiones de ruta de acceso tienen la forma de rutas separadas por puntos como _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Ordene los resultados por una propiedad específica. Si se agrega un(a) `-` antes del título (`orderby=-title`), los elementos se ordenarán por título en orden descendente (Z-A). | `-repo:createdDate` |
| `limit` | Limite el número de ubicaciones devueltas. | `limit=5` |

**Solicitud**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2' \
  -H 'Accept: *,application/json' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve una lista de ubicaciones que están presentes dentro del contenedor al que tiene acceso.

```json
{
    "containerId": "e0bd8463-0913-4ca1-bd84-6309134ca1f6",
    "schemaNs": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4",
    "requestTime": "2023-10-21T19:48:51.843067Z",
    "_embedded": {
    "results": [
        {
                "instanceId": "0feb6a80-0f32-11eb-8110-e17787c335b5",
            "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
            ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2023-10-15T22:02:05.480449Z",
                "repo:lastModifiedDate": "2023-10-15T22:13:00.278175Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:name": "New placement name",
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "xdm:description": "Updated placement description",
                    "@id": "xcore:offer-placement:12466ef35fc5baa0"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0feb6a80-0f32-11eb-8110-e17787c335b5",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                    }
            }
        },
        {
                "instanceId": "269192b0-f8f2-11ea-8723-916b9fbadc53",
            "schemas": [
                    "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
                ],
                "productContexts": [
                    "acp"
            ],
                "repo:etag": 1,
                "repo:createdDate": "2023-09-17T14:29:10.107121Z",
                "repo:lastModifiedDate": "2023-09-17T14:29:10.107121Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "xdm:componentType": "https://ns.adobe.com/experience/offer-management/content-component-html",
                    "xdm:name": "demo placement",
                    "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "@id": "xcore:offer-placement:1221fac4e7340521"
                },
                "_links": {
                    "self": {
                        "name": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4#269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/269192b0-f8f2-11ea-8723-916b9fbadc53",
                        "@type": "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4"
            }
                },
                "sandboxName": "ode-prod-va7-edge-testing"
        }
    ],
        "total": 17,
        "count": 2
    },
    "_links": {
        "self": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        },
        "next": {
            "href": "/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?start=269192b0-f8f2-11ea-8723-916b9fbadc53&orderby=instanceId&schema=https://ns.adobe.com/experience/offer-management/offer-placement;version=0.4&limit=2",
            "@type": "https://ns.adobe.com/experience/xcore/hal/results"
        }
    }
}
```
