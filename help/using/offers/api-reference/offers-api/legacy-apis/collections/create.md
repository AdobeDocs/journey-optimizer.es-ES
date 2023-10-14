---
title: Crear una colección
description: Las colecciones son subconjuntos de ofertas basados en condiciones predefinidas definidas definidas por un experto en marketing, como la categoría de la oferta.
feature: Offers, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ea79add2-1ea7-4c5c-ba67-f99d10975c4f
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 10%

---

# Crear una colección {#create-collection}

Las colecciones son subconjuntos de ofertas basados en condiciones predefinidas definidas definidas por un experto en marketing, como la categoría de la oferta.

Puede crear una colección realizando una solicitud de POST a [!DNL Offer Library] API, al tiempo que proporciona su ID de contenedor.

## Encabezados Accept y Content-Type {#accept-and-content-type-headers}

La siguiente tabla muestra los valores válidos que componen la variable *Content-Type* y *Aceptar* campos en el encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"` |

**Formato de API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor donde se encuentran las colecciones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitud**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/offer-filter;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Offer Collection 1",
        "xdm:filterType": "anyTags",
        "xdm:ids": [
            "xcore:tag:124e147572cd7866"
        ]
    }'
```

**Respuesta**

Una respuesta correcta devuelve información sobre la colección recién creada, incluido su ID de instancia y ubicación únicos `@id`. Puede usar el ID de instancia en pasos posteriores para actualizar o eliminar la colección. Puede utilizar su colección única `@id` en un tutorial posterior para crear una decisión.

```json
{
   "@id": "xcore:offer-filter:124e3594ce8b4930",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T22:59:17.345797Z",
    "repo:lastModifiedDate": "2020-10-21T22:59:17.345797Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
