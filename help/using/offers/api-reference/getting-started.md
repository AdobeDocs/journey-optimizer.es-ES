---
title: Introducción
description: Obtenga información sobre cómo empezar a utilizar la API de la biblioteca de ofertas para realizar operaciones clave mediante el motor de decisión.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: ccc3ad2b186a64b9859a5cc529fe0aefa736fc00
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 7%

---

# Guía para desarrolladores de API de Administración de decisiones {#decision-management-api-developer-guide}

Esta guía para desarrolladores proporciona pasos para ayudarle a empezar a utilizar [!DNL Offer Library] API. A continuación, la guía proporciona llamadas de API de ejemplo para realizar operaciones clave mediante el motor de toma de decisiones.

➡️ [Obtenga más información sobre los componentes de Administración de decisiones en este vídeo](#video)

## Requisitos previos {#prerequisites}

Esta guía requiere una comprensión práctica de los siguientes componentes de Adobe Experience Platform:

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}: El marco estandarizado mediante el cual [!DNL Experience Platform] organiza los datos de experiencia del cliente.
   * [Conceptos básicos de composición de esquemas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=es){target="_blank"}: Obtenga información acerca de los componentes básicos de los esquemas XDM.
* [Gestión de decisiones](../../../using/offers/get-started/starting-offer-decisioning.md): Explica los conceptos y componentes utilizados para Experience Decisioning en general y para la administración de decisiones en particular. Ilustra las estrategias utilizadas para elegir la mejor opción para presentar durante la experiencia de un cliente.
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}: PQL es un lenguaje potente para escribir expresiones en instancias de XDM. El PQL se utiliza para definir reglas de decisión.

## Leer llamadas de API de muestra {#reading-sample-api-calls}

Esta guía proporciona ejemplos de llamadas API para mostrar cómo dar formato a las solicitudes. Estas incluyen rutas, encabezados obligatorios y cargas de solicitud con el formato correcto. También se proporciona el JSON de muestra devuelto en las respuestas de API. Para obtener información sobre las convenciones utilizadas en la documentación de las llamadas de API de ejemplo, consulte la sección sobre [cómo leer llamadas de API de ejemplo](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} en el [!DNL Experience Platform] guía de solución de problemas.

## Recopilar valores para los encabezados obligatorios {#gather-values-for-required-headers}

Para realizar llamadas a [!DNL Adobe Experience Platform] API, primero debe completar el [tutorial de autenticación](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=es){target="_blank"}. Al completar el tutorial de autenticación, se proporcionan los valores para cada uno de los encabezados necesarios en todas las [!DNL Experience Platform] Llamadas de API, como se muestra a continuación:

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`

Todas las solicitudes que contienen una carga útil (POST, PUT, PATCH) requieren un encabezado adicional:

* `Content-Type: application/json`

## Administración del acceso a un contenedor {#manage-access-to-container}

Un contenedor es un mecanismo de aislamiento para mantener separadas las diferentes preocupaciones. El ID de contenedor es el primer elemento de ruta para todas las API del repositorio. Todos los objetos de toma de decisiones residen en un contenedor.

Un administrador puede agrupar entidades principales, recursos y permisos de acceso similares en perfiles. Esto reduce la carga administrativa y está respaldado por [Adobe Admin Console](https://adminconsole.adobe.com/). Debe ser administrador de productos de Adobe Experience Platform en su organización para crear perfiles y asignarles usuarios. Es suficiente con crear perfiles de producto que coincidan con determinados permisos en un solo paso y luego simplemente añadir usuarios a esos perfiles. Los perfiles actúan como grupos a los que se han concedido permisos y cada usuario real o técnico de ese grupo hereda esos permisos.

Con privilegios de administrador, puede conceder o retirar permisos a los usuarios a través del [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}. For more information, see the [Access control overview](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=es){target="_blank"}.

### Enumerar contenedores accesibles para usuarios e integraciones {#list-containers-accessible-to-users-and-integrations}

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

Una respuesta correcta devuelve información sobre los contenedores de administración de decisiones. Esto incluye un `instanceId` atributo, cuyo valor es su ID de contenedor.

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

Este documento abarcaba los conocimientos previos necesarios para realizar llamadas a la [!DNL Offer Library] API, incluida la adquisición del ID de contenedor. Ahora puede continuar con las llamadas de ejemplo proporcionadas en esta guía para desarrolladores y seguir junto con sus instrucciones.
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## Vídeo explicativo {#video}

El siguiente vídeo tiene como objetivo ayudarle a comprender los componentes de Administración de decisiones.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

