---
title: Primeros pasos
description: Obtenga información sobre cómo empezar a utilizar la API de biblioteca de ofertas para realizar operaciones clave mediante el motor de gestión de decisiones.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 6%

---

# Guía para desarrolladores de API de administración de decisiones {#decision-management-api-developer-guide}

Esta guía para desarrolladores proporciona los pasos para ayudarle a empezar a usar el [!DNL Offer Library] API. A continuación, la guía proporciona ejemplos de llamadas de API para realizar operaciones clave mediante el motor de gestión de decisiones.

➡️ [Descubra esta función en vídeo](#video)

## Requisitos previos {#prerequisites}

Esta guía requiere conocer los siguientes componentes de Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target=&quot;_blank&quot;}: El marco normalizado por el cual [!DNL Experience Platform] organiza los datos de experiencia del cliente.
   * [Aspectos básicos de la composición del esquema](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=es){target=&quot;_blank&quot;}: Obtenga información sobre los componentes básicos de los esquemas XDM.
* [Administración de decisiones](../../../using/offers/get-started/starting-offer-decisioning.md): Explica los conceptos y componentes utilizados para Experience Decisioning en general y el Offer decisioning en particular. Ilustra las estrategias utilizadas para elegir la mejor opción para presentar durante la experiencia del cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target=&quot;_blank&quot;}: PQL es un lenguaje potente para escribir expresiones en instancias XDM. PQL se utiliza para definir las reglas de decisión.

## Leer llamadas de API de ejemplo {#reading-sample-api-calls}

Esta guía proporciona ejemplos de llamadas a la API para demostrar cómo dar formato a las solicitudes. Estas incluyen rutas de acceso, encabezados necesarios y cargas de solicitud con el formato correcto. También se proporciona el JSON de muestra devuelto en las respuestas de API. Para obtener información sobre las convenciones utilizadas en la documentación para las llamadas de API de ejemplo, consulte la sección sobre [cómo leer llamadas de API de ejemplo](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target=&quot;_blank&quot;} en la sección [!DNL Experience Platform] guía de solución de problemas.

## Recopilar valores para encabezados necesarios {#gather-values-for-required-headers}

Para realizar llamadas a [!DNL Platform] API, primero debe completar la variable [tutorial de autenticación](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target=&quot;_blank&quot;}. Al completar el tutorial de autenticación, se proporcionan los valores para cada uno de los encabezados necesarios en todos los [!DNL Experience Platform] Llamadas de API, como se muestra a continuación:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Todas las solicitudes que contienen una carga útil (POST, PUT, PATCH) requieren un encabezado adicional:

* `Content-Type: application/json`

## Administrar el acceso a un contenedor {#manage-access-to-container}

Un contenedor es un mecanismo de aislamiento para mantener diferentes preocupaciones. El ID de contenedor es el primer elemento de ruta para todas las API de repositorio. Todos los objetos de decisión residen dentro de un contenedor.

Un administrador puede agrupar en perfiles entidades principales, recursos y permisos de acceso similares. Esto reduce la carga de administración y es compatible con [Adobe Admin Console](https://adminconsole.adobe.com/). Debe ser administrador de productos de Adobe Experience Platform en su organización para crear perfiles y asignarles usuarios. Es suficiente crear perfiles de producto que coincidan con determinados permisos en un solo paso y, a continuación, añadir usuarios a dichos perfiles. Los perfiles actúan como grupos a los que se han concedido permisos y todos los usuarios reales o técnicos de ese grupo heredan esos permisos.

Dados privilegios de administrador, puede conceder o retirar permisos a los usuarios a través del [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}. Para obtener más información, consulte la [Información general sobre el control de acceso](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=es){target=&quot;_blank&quot;}.

### Contenedores de lista accesibles para usuarios e integraciones {#list-containers-accessible-to-users-and-integrations}

**Formato de API**

```http
GET /{ENDPOINT_PATH}?product={PRODUCT_CONTEXT}&property={PROPERTY}==decisioning
```

| Parámetro | Descripción | Ejemplo |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Ruta de extremo para las API del repositorio. | `https://platform.adobe.io/data/core/xcore/` |
| `{PRODUCT_CONTEXT}` | Filtra la lista de contenedores por su asociación a contextos de producto. | `acp` |
| `{PROPERTY}` | Filtra el tipo de contenedor que se devuelve. | `_instance.containerType==decisioning` |

**Solicitud**

```shell
curl -X GET \
  'https://platform.adobe.io/data/core/xcore/?product=acp&property=_instance.containerType==decisioning' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Respuesta**

Una respuesta correcta devuelve información sobre los contenedores de administración de decisiones. Esto incluye un `instanceId` , cuyo valor es su ID de contenedor.

```json
{
    "_embedded": {
        "https://ns.adobe.com/experience/xcore/container": [
            {
                "instanceId": "{INSTANCE_ID}",
                "schemas": [
                    "https://ns.adobe.com/experience/xcore/container;version=0.5"
                ],
                "productContexts": [
                    "acp"
                ],
                "repo:etag": 2,
                "repo:createdDate": "2020-09-16T07:54:28.319959Z",
                "repo:lastModifiedDate": "2020-09-16T07:54:32.098139Z",
                "repo:createdBy": "{CREATED_BY}",
                "repo:lastModifiedBy": "{MODIFIED_BY}",
                "repo:createdByClientId": "{CREATED_CLIENT_ID}",
                "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}",
                "_instance": {
                    "containerType": "decisioning",
                    "repo:name": "{REPO_NAME}",
                    "dataCenter": "{DATA_CENTER}",
                    "parentName": "{PARENT_NAME}",
                    "parentId": "{PARENT_ID}"
                },
                "_links": {
                    "self": {
                        "href": "/containers/{INSTANCE_ID}"
                    }
                }
            }
        ]
    },
    "_links": {
        "self": {
            "href": "/?product=acp&property=_instance.containerType==decisioning",
            "@type": "https://ns.adobe.com/experience/xcore/hal/home"
        }
    }
}
```

## Pasos siguientes {#next-steps}

Este documento abarcaba los conocimientos previos necesarios para realizar llamadas al [!DNL Offer Library] , incluida la adquisición del ID de contenedor. Ahora puede continuar con las llamadas de ejemplo que se proporcionan en esta guía para desarrolladores y seguir junto con sus instrucciones.

## Tutorial en vídeo {#video}

El siguiente vídeo pretende contribuir a su comprensión de los componentes de la gestión de decisiones.

>[!NOTE]
>
>Este vídeo se aplica al servicio de aplicaciones de Offer decisioning creado en Adobe Experience Platform. Sin embargo, proporciona una guía genérica para utilizar Offer en el contexto de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)
