---
title: Entregar ofertas
description: La administración de decisiones es una colección de servicios y programas de interfaz de usuario que permiten a los especialistas en marketing crear y ofrecer experiencias de oferta personalizadas para el usuario final en canales y aplicaciones mediante lógica empresarial y reglas de decisión.
feature: Ofertas
topic: Integraciones
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 2%

---

# Enviar ofertas mediante la API de decisiones

Con Administración de decisiones, puede crear y ofrecer experiencias de oferta personalizadas para el usuario final en todos los canales y aplicaciones mediante la lógica empresarial y las reglas de decisión. Una oferta es un mensaje de marketing que puede tener reglas asociadas que especifican quién puede ver la oferta.

Puede crear y enviar ofertas realizando una solicitud de POST a la API [!DNL Decisions].

Este tutorial requiere una comprensión práctica de las API, específicamente con respecto a la gestión de decisiones. Para obtener más información, consulte la [guía para desarrolladores de la API de administración de decisiones](../getting-started.md). Este tutorial también requiere que tenga disponible un ID de ubicación y un valor de ID de decisión únicos. Si no ha adquirido estos valores, consulte los tutoriales para [crear una ubicación](../offers-api/placements/create.md) y [crear una decisión](../activities-api/activities/create.md).

![](../../../assets/do-not-localize/how-to-video.png) [Descubra esta función en vídeo](#video)

## Encabezados Accept y Content-Type

La tabla siguiente muestra los valores válidos que comprenden los campos *Content-Type* y *Accept* en el encabezado de la solicitud:

| Nombre del encabezado | Valor |
| ----------- | ----- |
| Accept | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"` |
| Content-Type | `application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"` |

**Formato de API**

```https
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/decisions
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/ode/` |
| `{CONTAINER_ID}` | Contenedor donde se encuentran las decisiones. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Solicitud**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/ode/e0bd8463-0913-4ca1-bd84-6309134ca1f6/decisions' \
  -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
  -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0'
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
  -d '{
        "xdm:propositionRequests": [
            {
              "xdm:placementId": "xcore:offer-placement:ffed0456",
              "xdm:activityId": "xcore:offer-activity:ffed0123",
              "xdm:itemCount": 2
            },
            {
              "xdm:placementId": "xcore:offer-placement:ffed0012",
              "xdm:activityId": "xcore:offer-activity:fffc0789"
            }
        ],
        "xdm:profiles": [
            {
              "xdm:identityMap": {
                "SWCUSTID": [
                {
                    "xdm:id": "123@abc.com"
                }
                ]
            },
            "xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"
            }
        ],
        "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
        },
        "xdm:mergePolicy": {
            "xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"
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
| `xdm:propositionRequests` | Este objeto contiene los identificadores de ubicación y decisión. |
| `xdm:propositionRequests.xdm:placementId` | Identificador de ubicación único. | `"xdm:placementId": "xcore:offer-placement:ffed0456"` |
| `xdm:propositionRequests.xdm:activityId` | Identificador de decisión único. | `"xdm:activityId": "xcore:offer-activity:ffed0123"` |
| `xdm:itemCount` | Número de ofertas que se van a devolver. El número máximo es 30. | `"xdm:itemCount": 2` |
| `xdm:profiles` | Este objeto contiene información sobre el perfil para el que se solicita la decisión. Para una solicitud de API, contendrá un perfil. |
| `xdm:profiles.xdm:identityMap` | Este objeto alberga un conjunto de identidades de usuario final basadas en el código de integración del área de nombres de la identidad. El mapa de identidad puede contener más de una identidad de cada área de nombres. Para obtener más información sobre áreas de nombres, consulte [Identity namespace overview](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html). | `Email: [{"xdm:id": "123@abc.com"}]` |
| `xdm:profiles.xdm:decisionRequestId` | ID generado por el cliente que se puede utilizar para identificar de forma exclusiva una solicitud de decisión de perfil. Este ID se repite en la respuesta y no influye en el resultado de la decisión. | `"xdm:decisionRequestId": "0AA00002-0000-1337-c0de-c0fefec0fefe"` |
| `xdm:allowDuplicatePropositions` | Este objeto define la estructura de control de las reglas de deduplicación. Consiste en una serie de indicadores que indican si se puede proponer la misma opción en una dimensión determinada. Un indicador que se establece en true significa que se permiten duplicados y no se deben eliminar en la categoría indicada por el indicador. Un indicador establecido en false significa que el motor de decisión no debe realizar la misma propuesta en toda la dimensión y, en su lugar, elegir la siguiente mejor opción para una de las subdecisiones. |
| `xdm:allowDuplicatePropositions.xdm:acrossActivities` | Si se establece en true, se puede asignar la misma opción a varias decisiones. | `"xdm:acrossActivities": true` |
| `xdm:allowDuplicatePropositions.xdm:acrossPlacements` | Si se establece en true, se puede asignar la misma opción a varias ubicaciones. | `"xdm:acrossPlacements": true` |
| `xdm:mergePolicy.xdm:id` | Identifica la directiva de combinación por la que se rigen los datos devueltos por el servicio de acceso a perfiles. Si no se especifica una en la solicitud, Administración de decisiones no pasará ningún servicio de acceso a perfiles, de lo contrario pasará el id proporcionado por el llamador. | `"xdm:id": "5f3ed32f-eaf1-456c-b0f0-7b338c4cb18a"` |
| `xdm:responseFormat` | Conjunto de indicadores que da formato al contenido de respuesta. |
| `xdm:responseFormat.xdm:includeContent` | Un valor booleano que, si se establece en `true`, incluye contenido en la respuesta. | `"xdm:includeContent": true` |
| `xdm:responseFormat.xdm:includeMetadata` | Un objeto que se utiliza para especificar qué metadatos adicionales se devuelven. Si esta propiedad no está incluida, se devuelven `xdm:id` y `repo:etag` de forma predeterminada. | `name` |
| `xdm:responseFormat.xdm:activity` | Este indicador identifica la información de metadatos específica devuelta para `xdm:activity`. | `name` |
| `xdm:responseFormat.xdm:option` | Este indicador identifica la información de metadatos específica devuelta para `xdm:option`. | `name`, `characteristics` |
| `xdm:responseFormat.xdm:placement` | Este indicador identifica la información de metadatos específica devuelta para `xdm:placement`. | `name`, `channel`, `componentType` |

**Respuesta**

Una respuesta correcta devuelve información sobre la propuesta, incluida su `xdm:propositionId` única.

```json
{
  "xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8",
  "xdm:propositions": [
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0456",
        "repo:etag": 1
      },
      "xdm:options": [
        {
          "xdm:id": "xcore:personalized-option:ccc0111",
          "repo:etag": 3,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>some html</html>"
        },
        {
          "xdm:id": "xcore:personalized-option:ccc0222",
          "repo:etag": 5,
          "@type": "https://ns.adobe.com/experience/decisioning/content-component-html-template",
          "xdm:content": "<html>hello, world</html>",
          "xdm:score": 45.65
        }
      ]
    },
    {
      "xdm:activity": {
        "xdm:id": "xcore:activity:ffed0123",
        "repo:etag": 4
      },
      "xdm:placement": {
        "xdm:id": "xcore:placement:ffed0789",
        "repo:etag": 2
      },
      "xdm:fallback": {
        "xdm:id": "xcore:fallback:ccc0222",
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
| `xdm:propositionId` | Identificador único de la entidad de propuesta asociada con un evento de decisión XDM. | `"xdm:propositionId": "5d0ffb5e-dfc6-4280-99b6-0bf3131cb8b8"` |
| `xdm:propositions` | Este objeto contiene una única propuesta de decisión. Se pueden devolver varias opciones para la decisión. Si no se encuentran opciones, se devuelve la oferta de reserva de la decisión. Las propuestas de decisión única siempre incluyen una propiedad `options` o una propiedad `fallback`. Cuando está presente, la propiedad `options` no puede estar vacía. |
| `xdm:propositions.xdm:activity` | Este objeto contiene el identificador único para una decisión. | `"xdm:id": "xcore:activity:ffed0123"` |
| `xdm:propositions.xdm:placement` | Este objeto contiene el identificador único de una ubicación de oferta. | `"xdm:id": "xcore:placement:ffed0456"` |
| `xdm:propositions.xdm:options` | Este objeto contiene una sola opción, incluido su identificador único. Si está presente, el objeto no puede estar vacío. | `xdm:id": "xcore:personalized-option:ccc0111` |
| `xdm:propositions.xdm:options.@type` | Define el tipo del componente. `@type` actúa como contrato de procesamiento para el cliente. Cuando se ensambla la experiencia, el compositor buscará los componentes que tengan un tipo específico. | `https://ns.adobe.com/experience/offer-management/content-component-imagelink` |
| `xdm:propositions.xdm:content` | Formato del contenido de respuesta. | El contenido de respuesta puede ser: `text`, `html block` o `image link` |
| `xdm:score` | La puntuación de una opción que se calcula como resultado de una función de clasificación asociada con la opción o la decisión. La API devolverá este campo si una función de clasificación participa en la determinación de la puntuación de una oferta durante la clasificación. | `"xdm:score": 45.65` |
| `xdm:propositions.xdm:fallback` | Este objeto contiene una sola oferta de reserva, incluido su identificador único. | `"xdm:id": "xcore:fallback:ccc0222"` |
| `xdm:propositions.xdm:fallback.dc:format` | La manifestación física o digital del recurso. Normalmente, el formato debe incluir el tipo de medio del recurso. El formato puede utilizarse para determinar el software, el hardware u otro equipo necesario para visualizar o utilizar el recurso. Se recomienda seleccionar un valor de un vocabulario controlado, por ejemplo, la lista de [Internet Media Types](http://www.iana.org/assignments/media-types/) que define los formatos multimedia del equipo. | `"dc:format": "image/png"` O bien `"image/jpeg"` |
| `xdm:propositions.xdm:fallback.xdm:deliveryURL` | Una URL opcional para leer el recurso desde un extremo de red o servicio de entrega de contenido. Esta URL se utiliza para acceder al recurso públicamente desde un agente de usuario. | `https://d37yhxrr0p3l3l.cloudfront.net/0fd0f090-a148-11ea-89e3-f1f2ad52f7e8/urn:aaid:sc:US:a68c86a6-9295-4940-a083-11916b665500/0/40d78a12-f8b6-3f07-8e67-7cb8ae2cc7ec` |
| `ode:createDate` | Hora a la que se creó el mensaje de respuesta de decisión. Esto se representa como hora de época. | `"ode:createDate": 1566497582038` |

## Tutorial en vídeo {#video}

El siguiente vídeo pretende contribuir a su comprensión de los componentes de la gestión de decisiones.

>[!NOTE]
>
>Este vídeo se aplica al servicio de aplicaciones de Offer decisioning creado en Adobe Experience Platform. Sin embargo, proporciona una guía genérica para utilizar Offer en el contexto de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919/?quality=12)

## Pasos siguientes

Al seguir esta guía de API, ha creado y enviado ofertas utilizando la API [!DNL Decisions]. Para obtener más información, consulte la [información general sobre Administración de decisiones](../../../offers/get-started/starting-offer-decisioning.md).
