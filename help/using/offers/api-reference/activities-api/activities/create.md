---
title: Crear decisiones
description: Una decisión contiene la lógica que indica la selección de una oferta.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 553501b0-30a9-4795-9a9d-f42df5f4f2ea
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 13%

---

# Crear una decisión {#create-decision}

Puede crear una decisión realizando una solicitud de POST al [!DNL Offer Library] al proporcionar su ID de contenedor.

## Encabezados Accept y Content-Type {#accept-and-content-type-headers}

La tabla siguiente muestra los valores válidos que comprenden el *Content-Type* y *Accept* campos en el encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"` |

**Formato de API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las decisiones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitud**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-activity;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
      "_instance": {
          "xdm:name": "Test API",
          "xdm:startDate": "2022-01-20T16:00:00Z",
          "xdm:endDate": "2022-01-27T16:00:00Z",
          "xdm:status": "live",
          "xdm:criteria": [
              {
                  "xdm:placements": [
                      "xcore:offer-placement:1457f9322f005194"
                  ],
                  "xdm:optionSelection": {
                      "xdm:filter": "xcore:offer-filter:1457f93227d0b6f0"
                  }
              }
          ],
          "xdm:fallback": "xcore:fallback-offer:13c259399d8bf013"
      },
      "_links": {}
  }'
```

**Respuesta**

Una respuesta correcta devuelve información sobre la decisión recién creada, incluido su ID de instancia única y su ubicación `@id`. Puede utilizar el ID de instancia en pasos posteriores para actualizar o eliminar su decisión.

```json
{
    "instanceId": "f88c9be0-1245-11eb-8622-b77b60702882",
    "@id": "xcore:offer-activity:124b79dc3ce2d720",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-19T20:02:09.694067Z",
    "repo:lastModifiedDate": "2020-10-19T20:02:09.694067Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
