---
title: Enumerar fórmulas de clasificación
description: Las fórmulas de clasificación permiten definir las funciones de puntuación, que se utilizan para clasificar elementos.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8b07be08-b37c-4535-82d8-3304340cbcad
source-git-commit: 6378c4a8cb911088c685166b9c1b29a1773d47b7
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 5%

---

# Enumerar fórmulas de clasificación {#list-ranking-formulas}

Una fórmula de clasificación consiste en una función de clasificación que define cómo debe clasificarse.

Puede ver una lista de todas las fórmulas de clasificación realizando una sola solicitud de GET a la API de la biblioteca de ofertas.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/ranking-formulas?{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | exdFunction. | `property=exdFunction%3D%3Dtrue` |

## Uso de parámetros de consulta {#using-query-parameters}

Puede utilizar parámetros de consulta para paginar y filtrar los resultados al enumerar recursos.

### Paginación {#paging}

Los parámetros de consulta más comunes para la paginación incluyen:

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `property` | Un filtro de propiedad opcional: <ul><li>Las propiedades se agrupan por operación AND.</li><li>Los parámetros se pueden repetir como se indica a continuación: property={PROPERTY_EXPR}[&amp;property={PROPERTY_EXPR2}...] o property={PROPERTY_EXPR1}[,{PROPERTY_EXPR2}...]</li><li>Las expresiones de propiedad están en el formato `[ !]field[op]value`, con `op` en `[==,!=,<=,>=,<,>,~]`, que admite expresiones regulares.</li></ul> | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Ordene los resultados por una propiedad específica. Si se agrega un - antes del nombre (orderby=-name), los elementos se ordenarán por nombre en orden descendente (Z-A). Las expresiones de ruta tienen la forma de rutas separadas por puntos. Este parámetro se puede repetir de esta manera: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limite el número de entidades devueltas. | `limit=5` |

**Solicitud**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/ranking-formulas?property=exdFunction%3D%3Dtrue&limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve una lista de fórmulas de clasificación a las que tiene acceso.

```json
{
    "results": [
        {
            "created": "2024-08-08T23:45:15.380Z",
            "modified": "2024-10-22T18:15:05.909Z",
            "etag": 36,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/ranking-function"
            ],
            "createdBy": "71486D7B5F4011980A494030@AdobeID",
            "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
            "id": "dps:ranking-function:1947f5372cc4ed74",
            "name": "[Do not delete] - Cypress e2e - edit",
            "description": "some description",
            "returnType": {
                "type": "INTEGER"
            },
            "exdFunction": true,
            "expression": {
                "type": "PQL",
                "format": "pql/text",
                "value": "42 = 11"
            }
        },
        {
            "created": "2024-05-03T13:06:22.361Z",
            "modified": "2024-10-18T22:47:35.396Z",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/ranking-function;version=0.3"
            ],
            "createdBy": "FD62391F5B44DF970A494124@AdobeID",
            "lastModifiedBy": "6F8A6FF05F4011C40A494005@AdobeID",
            "id": "xcore:ranking-function:18ca80c5b15c5e11",
            "name": "doc test exd",
            "description": "",
            "returnType": {
                "type": "INTEGER"
            },
            "exdFunction": true,
            "expression": {
                "type": "PQL",
                "format": "pql/text",
                "value": "false"
            }
        }
    ],
    "count": 2,
    "total": 50,
    "_links": {
        "self": {
            "href": "/ranking-formulas?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/ranking-formulas?orderby=-modified&limit=2&start=2024-10-18T22:22:35.048Z",
            "type": "application/json"
        }
    }
}
```
