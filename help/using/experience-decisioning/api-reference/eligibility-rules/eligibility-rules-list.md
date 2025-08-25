---
title: Enumerar reglas de idoneidad
description: Las reglas de elegibilidad le permiten definir los candidatos elegibles en función de lo que desee segmentar, como atributos de perfil y audiencias.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: c8f88954-a721-4d18-9137-035ee9dc1bcf
source-git-commit: 6378c4a8cb911088c685166b9c1b29a1773d47b7
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 5%

---

# Enumerar reglas de idoneidad {#list-eligibilit-rules}

Una regla de idoneidad consiste en una expresión de regla de PQL que define cómo debe definir la idoneidad.

Puede ver una lista de todas las reglas de idoneidad realizando una sola solicitud de GET a la API de la biblioteca de ofertas.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/offer-rules?{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{QUERY_PARAMS}` | exdRule. | `property=exdRule%3D%3Dtrue` |

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
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-rules?property=exdRule%3D%3Dtrue&limit=2' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve una lista de reglas de idoneidad a las que tiene acceso.

```json
{
    "results": [
        {
            "created": "2024-10-28T01:18:08.506Z",
            "modified": "2024-10-28T01:18:08.506Z",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule"
            ],
            "createdBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "lastModifiedBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "id": "dps:eligibility-rule:19af09a9ae45a8d3",
            "name": "dasdsa",
            "description": "",
            "exdRule": true,
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "personalEmail.address.equals(\"youz@adobe.com\", false)"
            },
            "segmentModel": {
                "lifecycleState": "published",
                "expression": {
                    "isValid": true,
                    "logicalOperator": "and",
                    "profileAttributesContainer": {
                        "exclude": false,
                        "items": [
                            {
                                "comparisonType": "equals",
                                "component": {
                                    "id": "profile.personalEmail.address",
                                    "__entity__": true,
                                    "type": "Sz"
                                },
                                "isCaseSensitive": false,
                                "isPlaceholder": false,
                                "originalLocation": [],
                                "value": [
                                    "youz@adobe.com"
                                ],
                                "itemType": "segmentRule"
                            }
                        ],
                        "logicalOperator": "and",
                        "itemType": "segmentContainer"
                    },
                    "xEventAttributesContainer": {
                        "exclude": false,
                        "items": [],
                        "logicalOperator": "then",
                        "itemType": "eventTypeCardContainer"
                    },
                    "itemType": "segmentDefinition"
                },
                "isMissingAnsibleModel": false,
                "relationalExpression": false,
                "deprecated": {
                    "status": false,
                    "reason": ""
                },
                "description": "",
                "evaluationInfo": {
                    "batch": {
                        "enabled": true
                    },
                    "continuous": {
                        "enabled": false
                    },
                    "synchronous": {
                        "enabled": false
                    }
                },
                "labels": [],
                "tags": [],
                "canHaveFolder": true,
                "mergePolicyId": "24526dbe-d615-4d41-9ebb-fd7f2b3dcdc2",
                "name": "dasdsa",
                "namespace": "ups"
            }
        },
        {
            "created": "2024-10-27T04:01:29.343Z",
            "modified": "2024-10-27T04:33:44.781Z",
            "etag": 2,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/eligibility-rule"
            ],
            "createdBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "lastModifiedBy": "3254197F65569E890A49422F@658557135fa10b860a494019",
            "id": "dps:eligibility-rule:19ade575cf95e584",
            "name": "nick test pes",
            "description": "dasdsad",
            "exdRule": true,
            "condition": {
                "type": "PQL",
                "format": "pql/text",
                "value": "personalEmail.address.equals(\"youz@adobe.com\", false)"
            },
            "segmentModel": {
                "lifecycleState": "published",
                "expression": {
                    "isValid": true,
                    "logicalOperator": "and",
                    "profileAttributesContainer": {
                        "exclude": false,
                        "items": [
                            {
                                "comparisonType": "equals",
                                "component": {
                                    "id": "profile.personalEmail.address",
                                    "__entity__": true,
                                    "type": "Sz"
                                },
                                "isCaseSensitive": false,
                                "isPlaceholder": false,
                                "originalLocation": [],
                                "value": [
                                    "youz@adobe.com"
                                ],
                                "itemType": "segmentRule"
                            }
                        ],
                        "logicalOperator": "and",
                        "itemType": "segmentContainer"
                    },
                    "xEventAttributesContainer": {
                        "exclude": false,
                        "items": [],
                        "logicalOperator": "then",
                        "itemType": "eventTypeCardContainer"
                    },
                    "itemType": "segmentDefinition"
                },
                "isMissingAnsibleModel": false,
                "relationalExpression": false,
                "deprecated": {
                    "status": false,
                    "reason": ""
                },
                "description": "dasdsad",
                "evaluationInfo": {
                    "batch": {
                        "enabled": true
                    },
                    "continuous": {
                        "enabled": false
                    },
                    "synchronous": {
                        "enabled": false
                    }
                },
                "labels": [],
                "tags": [],
                "canHaveFolder": true,
                "mergePolicyId": "24526dbe-d615-4d41-9ebb-fd7f2b3dcdc2",
                "name": "nick test pes",
                "namespace": "ups",
                "estimates": [
                    {
                        "previewId": "MDpTQU1QTEVfUkVJTklUOmJiNjI0MmZkLWUyOGQtNDY0Ni05ZWJjLTc1YmU5NGQ0YjY1Nzow",
                        "addressabilityText": "Of total",
                        "color": "#12805c",
                        "estimateData": {
                            "previewId": "MDpTQU1QTEVfUkVJTklUOmJiNjI0MmZkLWUyOGQtNDY0Ni05ZWJjLTc1YmU5NGQ0YjY1Nzow",
                            "estimatedSize": 0,
                            "totalRows": 62088,
                            "percent": 0,
                            "standardError": 0,
                            "confidenceInterval": "95%",
                            "state": "RESULT_READY",
                            "profilesReadSoFar": 62088,
                            "numRowsToRead": 62088
                        },
                        "state": "RESULT_READY"
                    }
                ]
            }
        }
    ],
    "count": 2,
    "total": 229,
    "_links": {
        "self": {
            "href": "/offer-rules?orderby=-modified&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-rules?orderby=-modified&limit=2&start=2024-10-27T01:24:51.785Z",
            "type": "application/json"
        }
    }
}
```
