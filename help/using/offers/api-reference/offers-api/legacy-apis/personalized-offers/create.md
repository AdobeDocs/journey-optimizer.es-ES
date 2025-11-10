---
title: Crear una oferta personalizada
description: Una oferta personalizada es un mensaje de marketing personalizable basado en reglas de elegibilidad y restricciones.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 234bee17-c830-4bc0-b258-182804df4cb3
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 11%

---

# Crear una oferta personalizada {#create-personalized-offer}

Una oferta personalizada es un mensaje de marketing personalizable basado en reglas de elegibilidad y restricciones.

Puede crear una oferta personalizada realizando una petición POST a la API [!DNL Offer Library], mientras proporciona su ID de contenedor.

## Encabezados Accept y Content-Type {#accept-and-content-type-headers}

En la tabla siguiente se muestran los valores válidos que comprenden los campos *Content-Type* y *Accept* del encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Aceptar | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**Formato de API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | El contenedor donde se encuentran las ofertas personalizadas. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitud**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
        "xdm:name": "Sale offer",
        "xdm:status": "draft",
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
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
        }
    ],
        "xdm:selectionConstraint": {
            "xdm:startDate": "2023-10-01T16:00:00Z",
            "xdm:endDate": "2021-12-13T16:00:00Z",
            "xdm:eligibilityRule": "xcore:eligibility-rule:124e0faf5b8ee89b"
        },
        "xdm:rank": {
            "xdm:priority": 1
    },
        "xdm:cappingConstraint": {
            "xdm:globalCap": 150
    },
        "xdm:tags": [
            "xcore:tag:124e147572cd7866"
    ]
}'
```

**Respuesta**

Una respuesta correcta devuelve información sobre la oferta personalizada recién creada, incluido su ID de instancia único y la ubicación `@id`. Puede utilizar el ID de instancia en pasos posteriores para actualizar o eliminar la oferta personalizada.

```json
{
    "instanceId": "0f4bc230-13df-11eb-bc55-c11be7252432",
    "@id": "xcore:personalized-offer:124e181c8b0d7878",
    "repo:etag": 1,
    "repo:createdDate": "2023-10-21T20:50:32.018624Z",
    "repo:lastModifiedDate": "2023-10-21T20:50:32.018624Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```

## Limitaciones {#limitations}

Las representaciones de oferta y algunas restricciones de oferta no son compatibles actualmente con los flujos de trabajo móviles [!DNL Experience Edge], por ejemplo `Capping`. El valor del campo `Capping` especifica el número de veces que se puede presentar una oferta entre todos los usuarios. Para obtener más información, consulte [Documentación sobre reglas de elegibilidad de ofertas y restricciones](../../../../offer-library/creating-personalized-offers.md).
