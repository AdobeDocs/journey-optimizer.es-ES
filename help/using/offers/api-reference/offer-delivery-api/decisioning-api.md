---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Entrega de ofertas
description: Gestión de decisiones es una colección de servicios y programas de interfaz de usuario que permite a los especialistas en marketing crear y ofrecer experiencias de oferta personalizadas al usuario final en canales y aplicaciones mediante la lógica empresarial y las reglas de decisión.
badge: label="Heredado" type="Informative"
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 692d0aae-6fa1-40b8-a35f-9845d78317a3
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/jhf2EpgMU35YmRWeatijWUFz3KwwjFfKP8lHtX8eyEU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 1153
ht-degree: 5%

---

# Entrega de ofertas mediante la API de decisiones {#decisioning-api}

>[!TIP]
>
>Decisioning, la nueva funcionalidad de toma de decisiones de [!DNL Adobe Journey Optimizer], ya está disponible a través de los canales de experiencia basada en código y de correo electrónico. [Más información](../../../experience-decisioning/gs-experience-decisioning.md)

Con Administración de decisiones, puede crear y ofrecer experiencias de oferta personalizadas para el usuario final en varios canales y aplicaciones mediante la lógica empresarial y las reglas de decisión. Una oferta es un mensaje de marketing que puede tener reglas asociadas que especifican quién puede ver la oferta.

Puede crear y enviar ofertas realizando una petición POST a la API [!DNL Decisioning].

Este tutorial requiere una comprensión práctica de las API, específicamente en lo que respecta a la administración de decisiones. Para obtener más información, consulte la [Guía para desarrolladores de API de administración de decisiones](../getting-started.md). Este tutorial también requiere que tenga un ID de ubicación único y un valor de ID de decisión disponibles. Si no ha adquirido estos valores, consulte los tutoriales de [creación de una ubicación](../offers-api/placements/create.md) y [creación de una decisión](../activities-api/activities/create.md).

>[!NOTE]
>
>**Pasar datos de contexto en solicitudes de Decisioning**
>
>Puede pasar datos de contexto (como tipo de dispositivo, ubicación o preferencias de usuario) en las solicitudes de Decisioning para crear reglas de elegibilidad dinámicas y entregar ofertas personalizadas basadas en condiciones en tiempo real. [Más información sobre datos de contexto y solicitudes de toma de decisiones](../../context-data-decisioning.md)

## Encabezados obligatorios {#required-headers}

En la tabla siguiente se muestran los valores válidos que comprenden los campos *Content-Type* y *Accept* del encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Aceptar | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |
| Autorización | `Bearer {ACCESS_TOKEN}` |
| x-gw-ims-org-id | `{IMS_ORG}` |
| x-sandbox-name | `{SANDBOX_NAME}` |
| x-api-key | `{API_KEY}` |

* Todas las solicitudes que contienen una carga útil (POST, PUT, PATCH) requieren el encabezado de tipo de contenido


>[!NOTE]
>
>La comprobación de permisos no se aplica a zonas protegidas individuales. Siempre que el llamador presente un token válido, la API de envío se activará.

## Solicitud de API {#request}

### Formato de API

```https
POST /{ENDPOINT_PATH}/decisions
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/ods` |

### Solicitud

```shell
curl -X POST 'https://platform.adobe.io/data/core/ods/decisions' \
-H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
-H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
-H 'Authorization: Bearer {ACCESS_TOKEN}....' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-sandbox-id: {SANDBOX_ID}' \
-H 'x-request-id: e9ac8d7e-3e77-4b38-8726-555ef1737b32-example' \
-d '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:15ded04b1786ea27",
            "xdm:placementId": "dps:offer-placement:15d9bc01d35e1238"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "example@adobe.com",
                        "primary": true
                    }
                ]
            }
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}' 
```

| Propiedad | Descripción | Ejemplo |
| -------- | ----------- | ------- |
| `xdm:propositionRequests` | Este objeto contiene los identificadores de ubicación y decisión. |  |
| `xdm:propositionRequests.xdm:placementId` | El identificador de ubicación único. | `"xdm:placementId": "dps:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | El identificador único de la decisión. | `"xdm:activityId": "dps:offer-activity:ffed0123"` |
| `xdm:itemCount` | Número de ofertas que se van a devolver. El número máximo es 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Este objeto contiene información sobre el perfil para el que se solicita la decisión. Para una solicitud de API, esto contiene un perfil. |  |
| `xdm:profiles.xdm:identityMap` | Este objeto contiene un conjunto de identidades de usuario final basado en el código de integración de área de nombres de la identidad. El mapa de identidad puede llevar más de una identidad de cada área de nombres. Para obtener más información sobre áreas de nombres, vea [esta página](../../../audience/get-started-identity.md). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | El ID generado por el cliente que se puede utilizar para identificar de forma exclusiva una solicitud de decisión de perfil. Este ID se recoge en la respuesta y no influye en el resultado de la decisión. | `"xdm:decisionRequestId": "0AA00002-0000-1224-c0de-cjf98Csj43"` |
| `xdm:allowDuplicatePropositions` | Este objeto define la estructura de control de las reglas de deduplicación. Consiste en una serie de indicadores que indican si la misma opción se puede proponer en una dimensión determinada. Un indicador que se establece en true significa que se permiten duplicados y no deben eliminarse en la categoría indicada por el indicador. Un indicador establecido en false significa que el motor de decisión no debe hacer la misma propuesta en toda la dimensión y elegir la siguiente mejor opción para una de las subdecisiones. |  |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Si se establece en true, es posible que se asignen varias decisiones a la misma opción. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Si se establece en true, es posible que se asignen varias ubicaciones a la misma opción. | `"xdm:acrossPlacements": true` |
| `xdm:enrichedAudience` | Establezca este parámetro en `true` si su objetivo es una audiencia de carga personalizada (CSV) y desea recuperar datos de enriquecimiento en la respuesta de decisión de oferta. [Más información acerca del uso de audiencias CSV para la toma de decisiones](../../custom-upload-decisioning.md#must-read) | `"xdm:enrichedAudience": true` |
| `xdm:mergePolicy.xdm:id` | Identifica la política de combinación por la que se rigen los datos devueltos por el servicio de acceso a perfiles. Si no se especifica uno en la solicitud, Administración de decisiones no transmitirá ningún servicio de acceso a perfiles; de lo contrario, transmitirá el ID proporcionado por el llamador. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Conjunto de indicadores que da formato al contenido de la respuesta. |  |
| `xdm:responseFormat.xdm:includeContent` | Un valor booleano que, si se establece en `true`, incluye contenido en la respuesta. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Un objeto que se utiliza para especificar qué metadatos adicionales se devuelven. Si no se incluye esta propiedad, se devolverán `xdm:id` y `repo:etag` de forma predeterminada. | `name` |
| `xdm:responseFormat.xdm:activity` | Este indicador identifica la información de metadatos específica devuelta para `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | Este indicador identifica la información de metadatos específica devuelta para `xdm:option`. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | Este indicador identifica la información de metadatos específica devuelta para `xdm:placement`. | `name`, `channel`, `componentType` |

### Respuesta

Una respuesta correcta devuelve información sobre la propuesta, incluido su `xdm:propositionId` único.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "dps:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "dps:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "dps:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "dps:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "dps:fallback:ccc0222",
        "repo:etag": 5,
        "@type": "https://ns.adobe.com/experience/decisioning/content-component-imagelink",
        "dc:format": "image/png",
        "xdm:deliveryURL": "https://cdn.adobe.com/content/1445323-1134331.png",
        "xdm:content": "https://www.adobe.com/index2.html"
      }
    }
  ],
  "ode:createDate": 1566497582038
}
```

| Propiedad | Descripción | Ejemplo |
| -------- | ----------- | ------- |
| `xdm:propositionId` | El identificador único de la entidad de propuesta asociada con un DecisionEvent de XDM. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Este objeto contiene una sola propuesta de decisión. Se pueden devolver varias opciones para la decisión. Si no se encuentran opciones, se devuelve la oferta de reserva de la decisión. Las propuestas de decisión única siempre incluyen una propiedad `options` o `fallback`. Cuando está presente, la propiedad `options` no puede estar vacía. |  |
| `xdm:propositions.xdm:activity` | Este objeto contiene el identificador único de una decisión. | `"xdm:id": "dps:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Este objeto contiene el identificador único de la ubicación de una oferta. | `"xdm:id": "dps:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Este objeto contiene una sola opción, incluido su identificador único. Si está presente, este objeto no puede estar vacío. | `xdm:id": "dps:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Define el tipo de componente. `@type` actúa como el contrato de procesamiento para el cliente. Cuando se monta la experiencia, el compositor buscará los componentes que tengan un tipo específico. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | El formato del contenido de respuesta. | El contenido de la respuesta puede ser: `text`, `html block` o `image link` |
| `xdm:score` | La puntuación de una opción que se calcula como resultado de una función de clasificación asociada con la opción o la decisión. La API devolverá este campo si una función de clasificación participa en la determinación de la puntuación de una oferta durante la clasificación. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Este objeto contiene una sola oferta de reserva, incluido su identificador único. | `"xdm:id": "dps:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | La manifestación física o digital del recurso. Normalmente, el formato debe incluir el tipo de medio del recurso. El formato se puede utilizar para determinar el software, hardware u otro equipo necesario para mostrar o utilizar el recurso. Se recomienda seleccionar un valor de un vocabulario controlado, por ejemplo, la lista de [tipos de medios de Internet](https://www.iana.org/assignments/media-types/) que definen formatos de medios de equipo. | `"dc:format": "image/png"` o `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | Una URL opcional para leer el recurso de un punto final de servicio o red de entrega de contenido. Esta URL se utiliza para acceder al recurso públicamente desde un agente de usuario. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | Hora a la que se creó el mensaje de respuesta a la decisión. Esto se representa como tiempo de época. | `"ode:createDate": 1566497582038` |

**Códigos de respuesta**

La siguiente tabla enumera todos los códigos que se pueden devolver en la respuesta:

| Código | Descripción |
|  ---  |  ---  |
| 200 | Correcto. Se tomó una decisión sobre determinadas actividades |
| 400 | Parámetro de solicitud no válido. El servidor no puede entender la solicitud debido a una sintaxis mal formada. |
| 403 | Permisos prohibidos e insuficientes. |
| 422 | Entidad no procesable. La sintaxis de la solicitud es correcta, sin embargo, debido a errores semánticos, no se puede procesar. |
| 429 | Demasiadas solicitudes. El usuario ha enviado demasiadas solicitudes en un período de tiempo determinado. |
| 500 | Error interno del servidor. El servidor encontró una condición inesperada que le impedía cumplir la solicitud. |
| 503 | El servicio no está disponible debido a una sobrecarga del servidor. El servidor no puede gestionar la solicitud debido a una sobrecarga temporal. |

<!--
 
## Tutorial video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/342828/?captions=spa&quality=12)
-->

## Próximos pasos {#next-steps}

Al seguir esta guía de API, ha creado y entregado ofertas mediante la API [!DNL Decisions]. Para obtener más información, consulte la [descripción general de Administración de decisiones](../../../offers/get-started/starting-offer-decisioning.md).
