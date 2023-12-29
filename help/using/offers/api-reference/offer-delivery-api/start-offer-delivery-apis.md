---
title: Introducción a las API de envío de ofertas
description: Obtenga más información sobre las API disponibles para ofrecer ofertas personalizadas.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 91f52af0c2e42556c4456be9b6b0cb84378c2a23
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 4%

---

# Introducción a las API de envío de ofertas {#about-decisioning-apis}

Puede enviar ofertas utilizando las opciones **Decisioning** o el **Edge Decisioning** API. Además, la variable **Toma de decisiones por lotes** La API permite enviar ofertas a todos los perfiles de una audiencia determinada en una llamada. El contenido de la oferta para cada perfil de la audiencia se coloca en un conjunto de datos de Adobe Experience Platform, donde está disponible para flujos de trabajo por lotes personalizados.

En esta página, encontrará información sobre las funcionalidades específicas disponibles con el **Decisioning** y **Edge Decisioning** API. Aunque ambos le permiten enviar ofertas a sus clientes, recomendamos utilizar el **Edge Decisioning** API siempre que sea posible para casos de uso entrantes y para garantizar una mejor latencia y rendimiento en su plataforma.

Para obtener más información sobre cómo trabajar con las API, consulte estas secciones:
* [API de decisiones](decisioning-api.md)
* [API de Edge Decisioning](edge-decisioning-api.md)
* [API de decisiones por lotes](batch-decisioning-api.md)

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

## Funciones de API de Edge Decisioning {#edge}

**Solicitud única de eventos de experiencia y solicitudes de toma de decisiones**

Con la API de Edge Decisioning, puede enviar en una sola solicitud el propio evento de experiencia junto con la solicitud de toma de decisiones, en lugar de tener dos solicitudes diferentes.

Por ejemplo, si un cliente visita su sitio web, la solicitud incluirá el evento de experiencia (la visita del cliente a la página) y recuperará una oferta para rellenar la página visitada.

**Almacenamiento de datos de contexto en Adobe Experience Platform**

Los datos de contexto hacen referencia a datos que solo conoce en el momento en que desea recuperar una oferta. Por ejemplo, el color del artículo comprado, el tiempo en el momento de la compra, etc.

Al pasar datos de contexto con una solicitud de API de Edge Decisioning, los datos se almacenan en el perfil de Adobe Experience Platform, lo que permite su reutilización en el futuro.

>[!NOTE]
>
>Para que se almacenen los datos de contexto, debe tener configurado un esquema XDM dedicado.

## Funciones de API de decisiones {#decisioning}

Las funcionalidades enumeradas a continuación solo están disponibles con la API de Decisioning. Si necesita aprovechar uno de ellos para satisfacer sus necesidades, utilice la API de decisiones. De lo contrario, recomendamos utilizar las API de Edge Decisioning.

* **Contenido y características de la oferta**: puede optar por no devolver el contenido y las características de una oferta mediante una opción dedicada.
* **Metadatos de ofertas**: active una opción para devolver los metadatos de una oferta.
* **Política de combinación**: utilice en la solicitud una política de combinación diferente de la asociada a la zona protegida.
* **Eventos de toma de decisiones y límite de frecuencia**: bloquee la toma de decisiones para que los eventos se cuenten mediante cualquier límite de frecuencia que se produzca.
* **Duplicar propuestas**: active una opción para no deduplicar propuestas.
