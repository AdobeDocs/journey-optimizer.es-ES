---
title: Actualizar fórmulas de clasificación
description: Las fórmulas de clasificación permiten definir las funciones de puntuación, que se utilizan para clasificar elementos.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 4ef1bfc2-e74f-4b44-b3b5-8a4f2fbd6438
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 9%

---

# Actualizar una fórmula de clasificación {#update-ranking-formula}

Puede modificar o actualizar una fórmula de clasificación realizando una petición PUT a la API de la biblioteca de ofertas.

Para obtener más información sobre JSON PUT, incluidas las operaciones disponibles, consulte la [documentación oficial de JSON PUT](http://jsonpatch.com/).

**Encabezados Accept y Content-Type**

En la tabla siguiente se muestran los valores válidos que comprenden los campos Content-Type del encabezado de la solicitud:

| Nombre del encabezado | Valor |
| --------- | ----------- |
| Content-Type | `application/json` |

**Formato de API**

```http
PUT /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | El ID de la entidad que desea actualizar. | `rankingFormula1234` |

**Solicitud**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "[UPDATED] Test Ranking Function DPS",
    "description": "Ranking  function description",
    "isPure": true,
    "exdFunction": true,
    "returnType": {
        "type": "integer"
    },
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "if(offer.rank.priority.isNotNull(), offer.rank.priority, 0) * if(offer.tags.intersects(boosted.tags), 2, 1)"
    },
    "definedOn": {
        "offer": {
            "schema": {
                "altId": "_experience.offer-management.personalized-offer",
                "version": "0"
            }
        },
        "boosted": {
            "schema": {
                "altId": "_xdm.context.foo",
                "version": "0"
            }
        }
    }
}'
```

| Parámetro | Descripción |
| --------- | ----------- |
| `value` | El nuevo valor con el que desea actualizar el parámetro. |
| `path` | Ruta del parámetro que se va a actualizar. |
| `op` | La llamada de operación utilizada para definir la acción necesaria para actualizar la conexión. Las operaciones incluyen: `add`, `replace`, `remove`, `copy` y `test`. |

**Respuesta**

Una respuesta correcta devuelve los detalles actualizados de la fórmula de clasificación, incluido el ID.

```json
{
    "etag": 2,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
