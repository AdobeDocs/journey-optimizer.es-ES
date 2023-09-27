---
title: Enumerar ubicaciones
description: Las ubicaciones son contenedores que se utilizan para mostrar sus ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 36030ffe-eb7a-4487-914d-84ccb0a6bf6e
source-git-commit: 8071bcf194a7cbf1ba00011e5deba1e6296cf708
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 17%

---

# Enumerar ubicaciones {#list-placements}

Las ubicaciones son contenedores que se utilizan para mostrar sus ofertas. Una ubicación ayuda a garantizar que el contenido de oferta correcto se muestre en la ubicación correcta dentro del mensaje. Al agregar contenido a una oferta, se le pedirá que seleccione una ubicación en la que se pueda mostrar dicho contenido.

Puede ver una lista de todas las ubicaciones realizando una única solicitud de GET a [!DNL Offer Library] API.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/placements?{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/dps` |

## Uso de parámetros de consulta {#using-query-parameters}

Puede utilizar parámetros de consulta para paginar y filtrar los resultados al enumerar recursos.

### Paginación {#paging}

Los parámetros de consulta más comunes para la paginación incluyen:

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `property` | Un filtro de propiedad opcional: <br> <ul> : las propiedades se agrupan por operación AND. <br><br> - Los parámetros se pueden repetir como se indica a continuación: property=<property-expr>[&amp;property=<property-expr2>...] o property=<property-expr1>[&amp;<property-expr2>...] <br><br> - Las expresiones de propiedad están en formato [!]campo[op]valor, con op in [¡==!=,&lt;=,>=,&lt;,>,~], que admiten expresiones regulares | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Ordene los resultados por una propiedad específica. Si se agrega un - antes del nombre (orderby=-name), los elementos se ordenarán por nombre en orden descendente (Z-A). Las expresiones de ruta tienen la forma de rutas separadas por puntos. Este parámetro se puede repetir de esta manera: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |

**Solicitud**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/placements?limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve una lista de ubicaciones que están presentes y a las que tiene acceso.

```json
{
    "results": [
        {
            "created": "2023-05-15T11:22:50.031+00:00",
            "modified": "2023-05-15T11:22:50.031+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.5"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerPlacement5678",
            "name": "Placement one",
            "description": "Placement description",
            "componentType": "html",
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "itemCount": 1,
            "allowDuplicatePlacements": false,
            "returnContent": false,
            "returnMetaData": {
                "decisionName": true,
                "offerName": true,
                "offerAttributes": true,
                "offerPriority": true,
                "placementName": true,
                "channelType": true,
                "contentType": true
            }
        },
        {
            "created": "2023-05-19T08:29:15.875+00:00",
            "modified": "2023-05-19T08:29:15.875+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-placement;version=0.5"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerPlacement1234",
            "name": "Placement two",
            "description": "Placement description",
            "componentType": "html",
            "channel": "https://ns.adobe.com/xdm/channel-types/email",
            "itemCount": 1,
            "allowDuplicatePlacements": false,
            "returnContent": false,
            "returnMetaData": {
                "decisionName": true,
                "offerName": true,
                "offerAttributes": true,
                "offerPriority": true,
                "placementName": true,
                "channelType": true,
                "contentType": true
            }
        }
    ],
    "count": 2,
    "total": 4,
    "_links": {
        "self": {
            "href": "/placements?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/placements?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
