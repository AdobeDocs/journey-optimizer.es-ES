---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Enumerar ofertas de reserva
description: Se envía una oferta de reserva a los clientes si no cumplen los requisitos para otras ofertas
feature: Decision Management, API
badge: label="Heredado" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: dd95c040-d905-4f5a-8cc5-58e39082e57e
version: Journey Orchestration
source-git-commit: 0b6d41fad9715985ec6418cdda27760f977bbc47
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 14%

---

# Enumerar ofertas de reserva {#list-fallback-offers}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../../../experience-decisioning/gs-experience-decisioning.md)


Se envía una oferta de reserva a los clientes si no cumplen los requisitos para otras ofertas. Los pasos para crear una oferta de reserva consisten en crear una o varias representaciones, como al crear una oferta.

Puede ver una lista de todas las ofertas de reserva realizando una única petición GET a la API [!DNL Offer Library].

**Formato de API**

```http
GET /{ENDPOINT_PATH}/offers?offer-type=fallback&{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | Parámetros de consulta opcionales por los que filtrar los resultados. | `limit=2` |

**Solicitud**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offers?offer-type=fallback&limit=2' \
-H 'Accept: *,application/json' \
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
| `property` | Un filtro de propiedad opcional: <ul><li>Las propiedades se agrupan por operación AND.</li><li>Los parámetros se pueden repetir como se indica a continuación: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] o property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>Las expresiones de propiedad están en el formato `[!]field[op]value`, con `op` en `[==,!=,<=,>=,<,>,~]`, que admite expresiones regulares.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Ordene los resultados por una propiedad específica. Si se agrega un - antes del nombre (orderby=-name), los elementos se ordenarán por nombre en orden descendente (Z-A). Las expresiones de ruta tienen la forma de rutas separadas por puntos. Este parámetro se puede repetir de esta manera: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limite el número de entidades devueltas. | `limit=5` |

**Respuesta**

Una respuesta correcta devuelve una lista de ofertas de reserva a las que tiene acceso.

```json
{
      "results": [
        {
            "created": "2023-06-08T14:04:41.011+00:00",
            "modified": "2023-06-08T14:04:41.011+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "fallbackOffer1234",
            "name": "Fallback Offer Web",
            "description": "Fallback Offer Web Description",
            "status": "draft",
            "representations": [
                {
                    "channel": "https://ns.adobe.com/xdm/channel-types/web",
                    "placement": "offerPlacement5678",
                    "components": [
                        {
                            "type": "imagelink",
                            "format": "image/png",
                            "deliveryURL": "https://mysite.com"
                        }
                    ]
                }
            ]
        },
        {
            "created": "2022-10-07T11:23:55.885+00:00",
            "modified": "2022-10-07T11:23:55.885+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.7"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "fallbackOffer5678",
            "name": "Fallback Offer email",
            "status": "approved",
            "representations": [
                {
                    "channel": "https://ns.adobe.com/xdm/channel-types/email",
                    "placement": "offerPlacement1234",
                    "components": [
                        {
                            "type": "component-text",
                            "format": "text/template",
                            "content": "Get free shipping!"
                        }
                    ]
                }
            ],
            "labels": [
                "core/C1"
            ]
        }
    ],
    "count": 2,
    "total": 3,
    "_links": {
        "self": {
            "href": "/offers?offer-type=fallback&href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offers?offer-type=fallback&href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
