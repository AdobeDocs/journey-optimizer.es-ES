---
title: Crear una oferta de reserva
description: Se envía una oferta de reserva a los clientes si no cumplen los requisitos para otras ofertas
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 1a9c074a-187a-45b1-9ad0-378aeef0d03d
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 12%

---

# Crear una oferta de reserva {#create-fallback-offer}

Puede crear una oferta de reserva realizando una solicitud de POST a [!DNL Offer Library] API, al tiempo que proporciona su ID de contenedor.

## Encabezados Accept y Content-Type {#accept-and-content-type-headers}

La siguiente tabla muestra los valores válidos que componen la variable *Content-Type* y *Aceptar* campos en el encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Aceptar | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"` |

**Formato de API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las ofertas de reserva. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitud**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/fallback-offer;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:status": "approved",
        "xdm:name": "Fallback for sales",
        "xdm:representations": [
            {
                "xdm:components": [
                    {
                        "dc:language": [
                            "en"
                        ],
                        "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                        "dc:format": "text/html"
                    }
                ],
                "xdm:channel": "https://ns.adobe.com/xdm/channel-types/web",
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
            }
        ]
}'
```

**Respuesta**

Una respuesta correcta devuelve información sobre la oferta de reserva recién creada, incluido su ID de instancia y ubicación únicos `@id`. Puede usar el ID de instancia en pasos posteriores para actualizar o eliminar la oferta de reserva. Puede utilizar su oferta de reserva única `@id` en un tutorial posterior para crear una decisión.


```json
{
    "instanceId": "b3966680-13ec-11eb-9c20-8323709cfc65",
    "@id": "xcore:fallback-offer:124e2e764b1ac1b9",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T22:28:11.111732Z",
    "repo:lastModifiedDate": "2023-10-21T22:28:11.111732Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
