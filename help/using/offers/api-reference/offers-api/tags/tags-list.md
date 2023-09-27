---
title: Cualificadores de colección de lista
description: Los calificadores de colección le permiten organizar y ordenar mejor sus ofertas.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 8cee44ed-5569-416c-b463-e75fb20d4c9c
source-git-commit: ce66888c4de157676e7a09f58beed4b4e237dbfc
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 7%

---

# Cualificadores de colección de lista {#list-tags}

Los calificadores de colección (anteriormente conocidos como &quot;etiquetas&quot;) le permiten organizar y ordenar mejor sus ofertas. Por ejemplo, puede etiquetar las ofertas de Black Friday con el calificador de colección Black Friday. A continuación, puede utilizar la funcionalidad de búsqueda de la biblioteca de ofertas para localizar fácilmente todas las ofertas con ese calificador de colección.

Los calificadores de colección también se pueden utilizar para agrupar ofertas en colecciones. Para obtener más información, consulte el tutorial sobre [creación de colecciones](../../../offer-library/creating-collections.md).

Puede ver una lista de todos los calificadores de colección realizando una única solicitud de GET al [!DNL Offer Library] API.

**Formato de API**

```http
GET /{ENDPOINT_PATH}/tags?{QUERY_PARAMS}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |

**Solicitud**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags?limit=2' \
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
| `property` | Un filtro de propiedad opcional: <br> <ul> : las propiedades se agrupan por operación AND. <br><br> - Los parámetros se pueden repetir como se indica a continuación: property=<property-expr>[&amp;property=<property-expr2>...] o property=<property-expr1>[&amp;<property-expr2>...] <br><br> - Las expresiones de propiedad están en formato [!]campo[op]valor, con op in [¡==!=,&lt;=,>=,&lt;,>,~], que admiten expresiones regulares | `property=name!=abc&property=id~.*1234.*&property=description equivalent with property=name!=abc,id~.*1234.*,description.` |
| `orderBy` | Ordene los resultados por una propiedad específica. Si se agrega un - antes del nombre (orderby=-name), los elementos se ordenarán por nombre en orden descendente (Z-A). Las expresiones de ruta tienen la forma de rutas separadas por puntos. Este parámetro se puede repetir de esta manera: `orderby=field1[,-fields2,field3,...]` | `orderby=id`,`-name` |
| `limit` | Limite el número de entidades devueltas. | `limit=5` |

**Respuesta**

Una respuesta correcta devuelve una lista de calificadores de colección que están presentes.

```json
{
                "created": "2022-09-16T19:00:02.070+00:00",
            "modified": "2022-09-16T19:00:02.070+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag1234",
            "name": "Sneakers"
        },
        {
            "created": "2022-09-16T19:55:02.168+00:00",
            "modified": "2022-09-16T19:55:02.168+00:00",
            "etag": 1,
            "schemas": [
                "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
            ],
            "createdBy": "{CREATED_BY}",
            "lastModifiedBy": "{MODIFIED_BY}",
            "id": "tag5678",
            "name": "Black Friday"
        }
    ],
    "count": 2,
    "total": 5,
    "_links": {
        "self": {
            "href": "/tags?href={SELF_HREF}&limit=2",
            "type": "application/json"
        },
        "next": {
            "href": "/tags?href={NEXT_HREF}&limit=2",
            "type": "application/json"
        }
    }
}
```
