---
title: Crear una oferta personalizada
description: Una oferta personalizada es un mensaje de marketing personalizable basado en reglas de elegibilidad y restricciones.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 97dc9af3-ca31-4512-aad2-f959dfc9ad0b
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 10%

---

# Crear una oferta personalizada {#create-personalized-offer}

Una oferta personalizada es un mensaje de marketing personalizable basado en reglas de elegibilidad y restricciones.

Puede crear una oferta personalizada realizando una solicitud de POST a [!DNL Offer Library] API.

## Encabezados Accept y Content-Type {#accept-and-content-type-headers}

La siguiente tabla muestra los valores válidos que componen la variable *Content-Type* en el encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato de API**

```http
POST /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API de persistencia. | `https://platform.adobe.io/data/core/dps/` |

**Solicitud**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offers?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test personalized offer with frequency constraint",
    "status": "draft",
    "representations": [
        {
            "channel": "https://ns.adobe.com/xdm/channel-types/web",
            "placement": "offerPlacement1234",
            "components": [
                {
                    "type": "html",
                    "format": "text/html",
                    "language": [
                        "en-us"
                    ],
                    "content": "Hello You qualify for our Discount of 60%"
                }
            ]
        }
    ],
    "selectionConstraint": {
        "startDate": "2022-07-27T05:00:00.000+00:00",
        "endDate": "2023-07-29T05:00:00.000+00:00",
        "profileConstraintType": "none"
    },
    "rank": {
        "priority": 0
    },
    "cappingConstraint": {},
    "frequencyCappingConstraints": [
        {
            "enabled": false,
            "limit": 1,
            "startDate": "2023-05-15T14:25:49.622+00:00",
            "endDate": "2023-05-25T14:25:49.622+00:00",
            "scope": "global",
            "entity": "offer",
            "repeat": {
                "enabled": false,
                "unit": "month",
                "unitCount": 1
            }
        }
    ]
}'
```

**Respuesta**

Una respuesta correcta devuelve los detalles de la oferta personalizada recién creada, incluido el ID. Puede usar el complemento `id` en pasos posteriores para actualizar o eliminar la oferta personalizada.

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

## Limitaciones {#limitations}

Actualmente, las representaciones de oferta y algunas restricciones de oferta no son compatibles con Mobile [!DNL Experience Edge] flujos de trabajo, por ejemplo `Capping`. El `Capping` el valor del campo especifica el número de veces que se puede presentar una oferta entre todos los usuarios. Para obtener más información, consulte [Documentación de restricciones y reglas de idoneidad de ofertas](../../../../offers/offer-library/creating-personalized-offers.md).