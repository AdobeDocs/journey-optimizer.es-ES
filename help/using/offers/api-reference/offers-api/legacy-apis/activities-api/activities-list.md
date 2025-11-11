---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Enumerar decisiones
description: Una decisión contiene la lógica que indica la selección de una oferta.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: e9bd7602-8945-4768-8a56-dc13ade32a0b
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 6%

---

# Enumerar decisiones {#list-decisions}

Una decisión contiene la lógica que indica la selección de una oferta.

Puede ver una lista de todas las decisiones dentro de un contenedor realizando una única petición GET a la API [!DNL Offer Library].

**Formato de API**

```http
GET /{ENDPOINT_PATH}/{CONTAINER_ID}/queries/core/search?schema={SCHEMA_ACTIVITIES}&{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor en el que se encuentran las decisiones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{SCHEMA_ACTIVITIES}` | Define el esquema asociado a las decisiones. | `https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5` |
| `{QUERY_PARAMS}` | Parámetros de consulta opcionales por los que filtrar los resultados. | `limit=2` |

**Solicitud**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/queries/core/search?schema=https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5&limit=2' \
  -H 'Accept: *,application/vnd.adobe.platform.xcore.hal+json; schema="https://ns.adobe.com/experience/xcore/hal/results"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `q` | Una cadena de consulta opcional para buscar en los campos seleccionados. La cadena de consulta debe estar en minúsculas y puede estar rodeada de comillas dobles para evitar que se muestre con tokens y para que salga de los caracteres especiales. Los caracteres `+ - = && \|\| > < ! ( ) { } [ ] ^ \" ~ * ? : \ /` tienen un significado especial y se deben aplicar como escape una barra invertida cuando aparezcan en la cadena de consulta. | `default` |
| `qop` | Aplica el operador AND u OR a los valores del parámetro de cadena de consulta q. | `AND` / `OR` |
| `field` | Lista opcional de campos para limitar la búsqueda. Este parámetro se puede repetir como se indica a continuación: field=field1[,field=field2,...] y (las expresiones de ruta de acceso tienen la forma de rutas separadas por puntos como _instance.xdm:name) | `_instance.xdm:name` |
| `orderBy` | Ordene los resultados por una propiedad específica. Si se agrega un(a) `-` antes del título (`orderby=-title`), los elementos se ordenarán por título en orden descendente (Z-A). | `-repo:createdDate` |
| `limit` | Limite el número de decisiones devueltas. | `limit=5` |

**Respuesta**

Una respuesta correcta devuelve una lista de decisiones que están presentes dentro del contenedor al que tiene acceso.

```json
{
    "results": [
        {
            "created": "2022-07-05T09:02:02.835+00:00",
            "modified": "2022-08-16T21:40:58.573+00:00",
            "etag": 12,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerDecision1234",
            "name": "Test Decision One",
            "status": "live",
            "startDate": "2022-05-18T00:09:57.706+00:00",
            "endDate": "2032-08-13T21:40:58.235+00:00",
            "fallback": "fallbackOffer1234",
            "criteria": [
                {
                    "placements": [
                        "offerPlacement1234",
                        "offerPlacement5678"
                    ],
                    "rank": {
                        "priority": 0,
                        "order": {
                            "orderEvaluationType": "ranking-strategy",
                            "rankingStrategy": "123456789123"
                        }
                    },
                    "profileConstraint": {
                        "profileConstraintType": "none"
                    },
                    "optionSelection": {
                        "filter": "offerCollection1234"
                    }
                }
            ]
        },
        {
            "created": "2022-09-05T14:12:13.773+00:00",
            "modified": "2022-09-05T14:12:13.773+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/offer-activity;version=0.8"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "offerDecision5678",
            "name": "Test Decision Two",
            "status": "live",
            "startDate": "2022-08-31T21:00:00.000+00:00",
            "endDate": "2023-02-03T22:00:00.000+00:00",
            "fallback": "fallbackOffer5678",
            "criteria": [
                {
                    "placements": [
                        "offerPlacement1234"
                    ],
                    "rank": {
                        "priority": 2
                    },
                    "optionSelection": {
                        "filter": "offerCollection5678"
                    }
                },
                {
                    "placements": [
                        "offerPlacement5678"
                    ],
                    "rank": {
                        "priority": 1
                    },
                    "optionSelection": {
                        "filter": "offerCollection1234"
                    }
                }          
            ]
        }
    ],
    "count": 2,
    "total": 21,
    "_links": {
        "self": {
            "href": "/offer-decisions?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/offer-decisions?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
