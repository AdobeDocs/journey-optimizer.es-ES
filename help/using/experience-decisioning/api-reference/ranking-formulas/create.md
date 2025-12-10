---
title: Crear fórmula de clasificación
description: Las fórmulas de clasificación permiten definir las funciones de puntuación, que se utilizan para clasificar elementos.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 2eb3ca65-f9f2-4483-ac6a-7bd896b0e516
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 16%

---

# Crear fórmula de clasificación {#create-ranking-formula}

Puede crear una fórmula de clasificación realizando una petición POST a la API de la biblioteca de ofertas.

**Encabezados Accept y Content-Type**

En la tabla siguiente se muestran los valores válidos que comprenden los campos Content-Type del encabezado de la solicitud:

| Nombre del encabezado | Valor |
| --------- | ----------- | 
| Content-Type | application/json |

**Formato de API**

```http
POST /{ENDPOINT_PATH}/ranking-formulas 
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps` |

**Solicitud**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/ranking-formulas' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Ranking Function DPS",
    "description": "Ranking  function description",
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

**Respuesta**

Una respuesta correcta devuelve los detalles de la fórmula de clasificación recién creada, incluido el `id`. Puede usar `id` en pasos posteriores para actualizar o eliminar la fórmula de clasificación.

```json
{
    "etag": 1,
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
