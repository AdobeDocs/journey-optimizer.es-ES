---
solution: Journey Optimizer
product: journey optimizer
title: Integración de proveedor
description: Utilice Integraciones de Adobe Journey Optimizer con cualquier plataforma externa que exponga una API válida, además de patrones de proveedor probados por ingeniería para confiar en usted al diseñar su configuración.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: integración, proveedor, terceros
source-git-commit: 9d839f8ac20b80e4abf5bedb881908f4e24964fc
workflow-type: tm+mt
source-wordcount: '9157'
ht-degree: 5%

---

# Proveedores disponibles

>[!BEGINSHADEBOX]

Tabla de contenido:

* [Trabajo con integraciones](external-sources.md)
* [Introducción a la integración de proveedores](vendor-integration-gs.md)
* **[Proveedores disponibles](vendor-integration.md)**
* [Preguntas más frecuentes](vendor-integration-faq.md)

>[!ENDSHADEBOX]

## Contenido y CMS {#content-and-cms}

### Contentful {#contentful}

>[!BEGINSHADEBOX]

El contenido es un CMS sin encabezado para entradas y recursos estructurados a través de REST o GraphQL, de modo que Journey Optimizer puede extraer contenido en el momento de envío o de apertura.

Los casos de uso típicos incluyen bloques hero localizados, texto alternativo y CTA en correos electrónicos, así como entradas de productos o promociones en módulos dinámicos. Otro patrón común es recuperar una entrada específica por ID para mensajes personalizados.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Contenido.

Se aplican los siguientes requisitos previos:

* Espacio de contenido con acceso a la API de envío y una clave de API de lectura.
* Borre los tipos de contenido y los ID de campo; acceso de administrador en Journey Optimizer para crear integraciones.


Se aplican las siguientes limitaciones y exclusiones:

* Las API de contenido paginadas o de lista amplia no se ajustan bien a este patrón; prefiera las llamadas de recuperación dirigidas a una entrada o recurso específico.
* La sincronización de reescritura o bidireccional está fuera del ámbito de este ejemplo.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la dirección URL de la API de entrega de contenido (CDA): `https://cdn.contentful.com/spaces/{space_id}/environments/{environment_id}/entries/{entry_id}`

1. Seleccione el método HTTP: GET.

1. Añadir encabezado de autenticación:

Autorización: Portador &lt;CONTENTFUL_DELIVERY_TOKEN>

1. Añada variables de ruta si es necesario (por ejemplo, ID de entrada, configuración regional).

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos obligatorios para la personalización.

1. Configure el tiempo de espera y el almacenamiento en caché según sea necesario.

1. Compruebe la conexión y actívela.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Campos de integración de muestra (alinearse con la [API de entrega de contenido](https://www.contentful.com/developers/docs/references/content-delivery-api/){target="_blank"} para su espacio y entorno):

| Campo | Valor |
| -- | -- |
| **Dirección URL** | `https://cdn.contentful.com/spaces/{{spaceID}}/entries/environments/{{environment_id}}` |
| Carga de respuesta | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |
| Política | Configure los detalles del nivel de directiva según sus necesidades. |
| **método HTTP** | `GET` |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `spaceID` | `spaceID` | `<YOUR_SPACE_ID>` |
| `environment_id` | `environment_id` | `<YOUR_ENV_ID>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | `access_token` | `<YOUR_API_KEY>` | Parámetro de consulta |

+++

### Sitecore {#sitecore}

>[!BEGINSHADEBOX]

Sitecore Content Hub y las API de nube relacionadas admiten flujos de metadatos y descargas al estilo DAM; el patrón de ejemplo siguiente se centra en un pedido de descarga por ID.

Los casos de uso habituales incluyen metadatos de recursos o descargas en el contenido del correo electrónico y la alineación con flujos de trabajo de DAM administrados en Sitecore.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Sitecore.

Se aplican los siguientes requisitos previos:

* URL del inquilino y credenciales (portador o token por su superficie de API).
* Acceso de administrador en Journey Optimizer para crear integraciones.

Se aplican las siguientes limitaciones y exclusiones:

* Los nombres de host y las rutas varían según el producto Sitecore. Utilice solo puntos finales que exponga su inquilino.
* Los tokens de acceso, la actualización y las duraciones de OAuth deben seguir la directiva de seguridad de SiteCore.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Configure **GET** en la ruta de orden de descarga, establezca encabezados de autorización por sitio, asigne `id` desde el contexto, pegue el JSON de muestra, asigne campos y ajuste los tiempos de espera para la latencia del recurso.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de Content Hub (por ejemplo: orden de descarga por ID). Ejemplo de patrón de URL:

1. `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{id}`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Utilice los campos siguientes cuando configure esta llamada de ejemplo en Journey Optimizer. Confirme el nombre de host y la versión de la API para su producto (Content Hub, XM Cloud, etc.) en [Documentación de Sitecore](https://doc.sitecore.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{{id}}` |
| **método HTTP** | `GET` |
| Carga de respuesta | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |
| Política | Configure los detalles del nivel de directiva según sus necesidades. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `id` | `id` | `<id_of_download_order>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |
| Autorización | Autorización | Constante | Portador `<token>` | Sí (activado) |
| Si-Modificado-Desde | Si-Modificado-Desde | Variable | 24T14:15:22Z, 08-2019 | No (desactivado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | X-Auth-Token | `<token>` | Encabezado |

+++

### Salsify {#salsify}

>[!BEGINSHADEBOX]

Salsify es un PIM con API para productos, canales y recursos digitales.

Los casos de uso habituales incluyen atributos de producto o URL de medios en el correo electrónico y la mensajería alineados con los datos del catálogo sindicado.

>[!ENDSHADEBOX]

+++ Obtenga más información sobre los requisitos previos y las limitaciones de Salsify.

Se aplican los siguientes requisitos previos:

* Token de API y contexto de organización; ID de producto que se pueden resolver desde el perfil o el contexto.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Catálogos muy grandes: evite los puntos finales de lista masiva si las integraciones esperan la recuperación por entidad.
* La visibilidad de los atributos se puede limitar con los permisos de funciones de Salsify.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Prefiera la recuperación de un solo producto sobre las llamadas masivas al catálogo, establezca la autenticación del portador, pegue el JSON de muestra, asigne campos, pruebe y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de producto de Salsify. Ejemplo de patrón de URL:

1. `https://api.salsify.com/v1/...`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Algunas referencias antiguas reutilizaron una ruta de estilo de orden de descarga para Salsify; en su lugar, el inquilino puede utilizar `https://app.salsify.com/api/v1/orgs/{org_id}/products/{salsify_id}` o similar. Confirme en [Salsify developers](https://developers.salsify.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://app.salsify.com/api/v1/orgs/{{org_id}}/products/{{salsify_id}}` |
| **método HTTP** | `GET` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |
| **Carga de respuesta** | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `org_id` | `org_id` | `<org_id>` |
| `salsify_id` | `salsify_id` | `<salsify_id>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (parámetro predeterminado) | Content-Type | Constante | application/json | Sí (activado) |
| Autorización | Autorización | Constante | `Bearer <YOUR_TOKEN_HERE>` | Sí (activado) |
| Si-Modificado-Desde | Si-Modificado-Desde | Variable | 24T14:15:22Z, 08-2019 | No (desactivado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | `apiKey` | `<your_api_key>` | Encabezado |

+++

### Contentstack {#contentstack}

>[!BEGINSHADEBOX]

Contentstack es una CMS sin encabezado; la entrega REST es típica para la asignación de campos JSON en Journey Optimizer.

Un caso de uso típico es el uso de entradas para titulares o promociones con parámetros que incluyen configuración regional.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Contentstack.

Se aplican los siguientes requisitos previos:

* Apilar clave de API, token de envío, nombre de entorno y UID de tipo de contenido.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Este patrón utiliza el JSON de REST para la asignación de campos; la entrega de GraphQL sigue una ruta de integración diferente.
* Utilice tokens de envío adecuados para la producción; los flujos de vista previa y publicados no son intercambiables.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Agregue ambos encabezados `api_key` y `access_token` según lo requiera Contentstack, incluya el parámetro de consulta `environment`, pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de entrega de contenido. Ejemplo de patrón de URL:

1. `https://cdn.contentstack.io/v3/content_types/{content_type_uid}/entries/{entry_uid}`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Campos de integración de muestra. Consulte [API de entrega de contenido de Contentstack](https://www.contentstack.com/docs/developers/apis/content-delivery-api/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://cdn.contentstack.io/v3/content_types/{{content_type_uid}}/entries/{{entry_uid}}` |
| **método HTTP** | `GET` |
| Carga de respuesta | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |
| Política | Configure los detalles del nivel de directiva según sus necesidades. |
| Encabezados | No se necesitan encabezados adicionales. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `content_type_uid` | Tipo de contenido UID | `<your_content_type_uid>` |
| `entry_uid` | UID de entrada | `<your_entry_uid>` |

**Autenticación**

| Nombre de clave | Valor clave | Añadir a |
| --- | --- | --- |
| `api_key` | `<YOUR_STACK_API_KEY>` | Encabezado |
| `access_token` | `<YOUR_DELIVERY_TOKEN>` | Encabezado |

Contentstack espera **ambas** claves como encabezados para las solicitudes de envío.

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `environment` | Nombre del entorno | Variable | `<your_environment_name>` | Sí (activado) |

+++

### Akeneo {#akeneo}

>[!BEGINSHADEBOX]

Akeneo PIM expone las API de REST para productos, atributos y medios.

Los casos de uso habituales incluyen datos de productos controlados en módulos de correo electrónico y atributos para un canal determinado en recorrido.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Akeneo.

Se aplican los siguientes requisitos previos:

* URL base de PIM y cliente de OAuth; UUID del producto o estrategia del identificador.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Las respuestas de PIM pueden ser grandes. Asigne solo los atributos necesarios para la personalización.
* Las operaciones de escritura están fuera del ámbito de los ejemplos de personalización de solo lectura habituales.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Use **GET** con el token de portador, solicite solo las opciones de atributo necesarias en los indicadores de consulta, pegue el archivo JSON de muestra, asigne un conjunto de atributos mínimo, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de REST de Akeneo. Ejemplo de patrón de URL:

1. `https://{pim-host}/api/rest/v1/...`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Patrón de ejemplo: `https://{pim-host}/api/rest/v1/products-uuid/{uuid}` con `Accept: application/json`. Consulte [API de Akeneo](https://api.akeneo.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://{{your-akeneo-domain}}.com/api/rest/v1/products-uuid/{{uuidProduct}}` |
| **método HTTP** | `GET` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |
| **Carga de respuesta** | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `uuidProduct` | Identificador único universal (UUID) | `<product_uuid>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Autorización | Autorización | Constante | `Bearer <YOUR_TOKEN>` | Sí (activado) |
| Aceptar | Aceptar | Constante | application/json | Sí (activado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `with_attribute_options` | Incluir opciones de atributo | Variable | falso | No (desactivado) |
| `with_quality_scores` | Incluir puntuaciones de calidad | Variable | falso | No (desactivado) |
| `with_completenesses` | Incluir integridad | Variable | falso | No (desactivado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | Autorización | `Bearer <YOUR_ACCESS_TOKEN>` | Encabezado |

+++

### Magnolia {#magnolia}

>[!BEGINSHADEBOX]

Magnolia ofrece puntos finales de entrega REST y sin encabezado según la implementación.

Un caso de uso típico es el envío de nodos de contenido o fragmentos para módulos de marketing.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Magnolia.

Se aplican los siguientes requisitos previos:

* URL de instancia y token para autenticación básica; espacio de trabajo y rutas para envío.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Las direcciones URL de entrega REST dependen de los módulos y la configuración instalados de Magnolia.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Utilice el patrón de URL de entrega pública que exponen sus módulos, autentique según la guía de Magnolia (entrega anónima frente a token para contenido protegido), pegue el JSON de muestra, asigne campos, pruebe y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante Magnolia REST (envío). Ejemplo de patrón de URL:

1. `https://{author-or-public}/.rest/delivery/...`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Patrón de ejemplo: `https://{domain}/magnoliaAuthor/.rest/delivery/...` o direcciones URL de estilo de recorridos de envío públicos. Las rutas dependen de los módulos instalados. Ver [documentación de Magnolia](https://docs.magnolia-cms.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `http://{{your-domain}}/magnoliaAuthor/.rest/delivery/<myEndpoint>/travel/@nodes` |
| **método HTTP** | `GET` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |
| **Carga de respuesta** | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | Constante | application/json | Sí (activado) |
| Aceptar | Aceptar | Constante | application/json | Sí (activado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | Autorización | `<bearer_token>` | Encabezado |

Nota: La API de envío es para utilizar la función rest-anonymous para contenido que no requiera un inicio de sesión. Para un acceso seguro a los datos protegidos, se prefiere un método más robusto como tokens de API o OAuth 2.0

+++


## Lealtad y recompensas {#loyalty-and-rewards}

### Cucherificar {#voucherify}

>[!BEGINSHADEBOX]

Voucherify proporciona promociones y API de REST de fidelidad (campañas, vales, programas de fidelidad).

Los casos de uso habituales incluyen leer la lealtad o el estado de promoción de ofertas en el contenido y mostrar el nivel o el equilibrio cuando corresponda.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Voucherify.

Se aplican los siguientes requisitos previos:

* ID de aplicación y secreto (por región/clúster); claridad sobre a qué extremos de campaña o fidelidad llama.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Evite exponer los identificadores de campañas o promociones internas en errores del cliente o contenido de mensajes.
* Se aplican límites de tasa de nivel de aplicación. Configure los reintentos y el almacenamiento en caché según la guía de Voucherify.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Establezca la dirección URL base para el clúster, agregue los encabezados necesarios (`X-APP-ID`, `X-APP-TOKEN`), restrinja los extremos de la lista con filtros o identificadores, pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante las API de Fidelidad/REST. Ejemplo de patrón de URL:

1. URL base de OpenAPI por cupón para su región

1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Campos de integración de muestra. Referencia completa: [Voucherify API](https://docs.voucherify.io/reference/introduction){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://{{cluster}}.voucherify.io/v1/loyalties/{{campaignId}}/members` |
| **método HTTP** | `GET` |
| Carga de respuesta | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |
| Política | Configure los detalles del nivel de directiva según sus necesidades. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `cluster` | `cluster` | `<your_cluster>` |
| `campaignId` | `campaignId` | `<loyalty_campaign_Id>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |
| X-APP-ID | X-APP-ID | Constante | `<YOUR-APP-ID>` | Sí (activado) |
| X-Voucherify-Channel | X-Voucherify-Channel | Constante | Documentación de Cupón | No (desactivado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `limit` | `limit` | Variable | 10 | No (desactivado) |
| `page` | `page` | Variable | 1 | No (desactivado) |
| `customer` | `customer` | Variable | `<customer_identifier>` | No (desactivado) |
| `created_at` | `created_at` | Variable | `<iso8601_date>` | No (desactivado) |
| `updated_at` | `updated_at` | Variable | `<iso8601_date>` | No (desactivado) |
| `order` | `order` | Variable | `<sort_field>` | No (desactivado) |
| `code` | `code` | Variable | `<loyalty_card_code>` | No (desactivado) |
| `ids` | `ids` | Variable | `<array_of_ids>` | No (desactivado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | X-APP-TOKEN | `<YOUR-APP-TOKEN>` | Encabezado |

+++

### Talon.One {#talon-one}

>[!BEGINSHADEBOX]

Talon.One es un motor de reglas de promoción y lealtad con API de REST para sesiones, efectos y perfiles.

Los casos de uso habituales incluyen promociones a nivel de carro de compras o perfil en contenido personalizado, y progreso de lealtad o visualización de recompensas.

>[!ENDSHADEBOX]

+++ Obtenga más información sobre los requisitos previos y las limitaciones de Talon.One.

Se aplican los siguientes requisitos previos:

* Clave de API y URL base específica de implementación; identificadores para el ámbito de aplicación o campaña.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Los flujos con gran cantidad de sesiones pueden requerir una asignación cuidadosa al modelo de solicitud de integraciones.
* Observe los límites de tasa Talon.One y la guía de idempotencia.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Use **GET** en el perfil o ruta de acceso de logros que necesite, establezca `Authorization: ApiKey-v1 <key>` como documentado, pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de integración de Talon.One. Ejemplo de patrón de URL:

1. `https://{your-domain}.talon.one/v1/...`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://{{your-deployment}}.talon.one/v1/customer_profiles/{{integrationId}}/achievements/{{achievementId}}` |
| **método HTTP** | `GET` |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `your-deployment` | `your-deployment` | `<your_deployment>` |
| `integrationId` | `integrationId` | `<integrationId>` |
| `achievementId` | `achievementId` | `<achievementId>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `progressStatus` | `progressStatus` | Variable | en curso/completado/caducado | No (desactivado) |
| `startDate` | `startDate` | Variable | 29/05/2024 T15:04:05+07:00 | No (desactivado) |
| `endDate` | `endDate` | Variable | 29/05/2024 T15:04:05+07:00 | No (desactivado) |
| `pageSize` | `pageSize` | Variable | `<default_page_size>` | No (desactivado) |
| `skip` | `skip` | Variable | `<items_to_skip>` | No (desactivado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | Autorización | ApiKey-v1 `<YOUR_API_KEY>` | Encabezado |

+++

### Antavo {#antavo}

>[!BEGINSHADEBOX]

Antavo es una plataforma de fidelidad empresarial con API de REST para miembros, recompensas y eventos.

Los casos de uso habituales incluyen puntos, niveles o recompensas en correos electrónicos o push y ofertas impulsadas por el estado de lealtad.

>[!ENDSHADEBOX]

+++ Obtenga más información sobre los requisitos previos y las limitaciones de Antavo.

Se aplican los siguientes requisitos previos:

* Apilar credenciales de URL y API; identificadores de programa o tienda según sea necesario.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* La PII del cliente debe gestionarse según los acuerdos de Antavo y sus políticas de privacidad.
* Confirme las versiones de API y los puntos de conexión estables con Antavo para su entorno.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Configure **GET** con la autenticación del proveedor (por ejemplo, la clave de API en la consulta), evite exponer la PII a la directiva, pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de Antavo Enterprise. Ejemplo de patrón de URL:

1. Dirección URL base de pila por Antavo documentada en el inquilino

1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Los campos de integración de muestra utilizan el host **staging**; la producción utiliza el nombre de host de la pila Antavo. Ver [documentación de Antavo](https://antavo.com/docs/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://api.staging.antavo.com/customers/{{customer_id}}/activities/offers` |
| **método HTTP** | `GET` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |
| **Carga de respuesta** | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `customer_id` | `customer_id` | `<customer_id>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |
| Aceptar | Aceptar | Constante | application/json | No (desactivado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | `api_key` | `<YOUR_API_KEY>` | Parámetros de consulta |

+++

### Lealtad de Salesforce {#salesforce-loyalty}

>[!BEGINSHADEBOX]

Salesforce Loyalty Management expone las API de REST en la plataforma de Salesforce para miembros, programas y transacciones.

Los casos de uso habituales incluyen la aparición de niveles, puntos o ventajas en los recorridos y la alineación de la mensajería con datos de CRM y lealtad.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Lealtad de Salesforce.

Se aplican los siguientes requisitos previos:

* Instancia de Salesforce, aplicación conectada o usuario de integración, y OAuth apropiado para su organización.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Los límites de la API de Salesforce y la actualización de los tokens de OAuth deben diseñarse en su integración.
* Las reglas de seguridad y uso compartido de nivel de campo rigen qué campos aparecen en las respuestas de API.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Utilice el punto final de integración de fidelidad que apruebe su equipo, complete Salesforce OAuth, pegue el JSON de muestra, asigne campos, respete los límites de la API compuesta, pruebe y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el punto final mediante Salesforce Loyalty Management REST. Ejemplo de patrón de URL:

1. `https://{instance}.salesforce.com/services/data/vXX.X/...`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Utilice la operación GET de administración de fidelidad **perfil de miembro** documentada para la versión de API de su organización; las rutas incluyen identificadores de programa y de miembro. Consulte [desarrolladores de Salesforce](https://developer.salesforce.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://{{your-instance}}.my.salesforce.com/services/data/{{version}}/connect/loyalty/management/members` |
| **método HTTP** | `GET` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |
| **Carga de respuesta** | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |
| `version` | `version` | `version` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |
| Aceptar | Aceptar | Constante | application/json | No (desactivado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `membershipNumber` | `membershipNumber` | Variable | `<membership_number>` | No (desactivado) * |
| `membershipId` | `membershipId` | Variable | `<membership_id>` | No (desactivado) * |
| `posMemId` | `posMemId` | Variable | `<pos_mem_id>` | No (desactivado) * |

\* Al menos uno de los tres es obligatorio.

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | Autorización | `<access_token>` | Encabezado |

+++

### Capilar {#capillary}

>[!BEGINSHADEBOX]

Capillary proporciona API de lealtad y participación comunes en las pilas de minoristas.

Los casos de uso habituales incluyen puntos, niveles u ofertas dentro de recorridos personalizados.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Capillary.

Se aplican los siguientes requisitos previos:

* Host y autenticación de API (solicitudes firmadas con frecuencia; siga los documentos de Capillary).
* Identificadores de programa para el extremo.

Se aplican las siguientes limitaciones y exclusiones:

* Los esquemas de autenticación y los hosts regionales varían según la implementación. Confirme con Capillary su pila.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Configure encabezados como `CAP-API-ACCESS-TOKEN` según sea necesario, pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante las API capilares. Ejemplo de patrón de URL:

1. Guía de integración por capilar para su región

1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Ejemplo: `https://ushc.intouch.capillarytech.com/api/v3/rewards/{reward_id}` (el host varía según la región). Valide el host y el esquema de autenticación con [Capillary](https://capillarytech.com/){target="_blank"}.


| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://ushc.intouch.capillarytech.com/api/v3/rewards/{{reward_id}}` |
| **método HTTP** | `GET` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |
| **Carga de respuesta** | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `reward_id` | ID de recompensa | `<your_reward_id>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | Constante | application/json | Sí (activado) |
| CAP-API-ACCESS-TOKEN | Token de acceso | Constante | `<YOUR_ACCESS_TOKEN>` | Sí (activado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | CAP-API-ACCESS-TOKEN | `<YOUR_ACCESS_TOKEN>` | Encabezado |

+++


## Plantillas y mensajería {#templates-and-messaging}

### Stensul {#stensul}

>[!BEGINSHADEBOX]

Stensul es una plataforma de creación de correo electrónico para plantillas aprobadas; Journey Optimizer puede consumir metadatos de plantilla y regiones estructuradas a través de su API.

Los casos de uso habituales incluyen la importación de plantillas aprobadas y la asignación de regiones a atributos de perfil, y la reutilización de bloques controlados para compilaciones de campaña escalables.

>[!ENDSHADEBOX]

+++ Obtenga más información sobre los requisitos previos y las limitaciones de Stensul.

Se aplican los siguientes requisitos previos:

* Cuenta de Stensul con acceso a la API y plantillas publicadas con tokens definidos.
* Acceso de administrador en Journey Optimizer para crear integraciones.

Se aplican las siguientes limitaciones y exclusiones:

* La edición in situ por parte de WYSIWYG de plantillas de Stensul dentro de Journey Optimizer no se trata aquí.
* Las HTML grandes o complejas en cargas útiles de plantilla pueden requerir una revisión de la seguridad y un saneamiento.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración.

1. Configure el extremo mediante la URL de la API de plantillas Stensul (patrón de ejemplo): `https://api.stensul.com/v1/templates/{template_id}`

1. Configure la autenticación (clave de API o documentación de la API de OAuth per Stensul).

1. Defina las variables de ruta (por ejemplo, el ID de plantilla).

1. Pegue una respuesta JSON de muestra para la detección de campos.

1. Asigne los campos de plantilla necesarios a los campos de personalización de Journey Optimizer.

1. Compruebe la conexión y actívela.

### Caléndula {#marigold}

>[!BEGINSHADEBOX]

Marigold expone las API de lealtad y participación; los hosts difieren según la ubicación geográfica (nombres de host del módulo de la UE frente a los de EE. UU.).

Un caso de uso típico es enriquecer los mensajes con datos de lealtad o preferencias de los programas Marigold.

>[!ENDSHADEBOX]

+++ Obtenga más información sobre los requisitos previos y las limitaciones de Marigold.

Se aplican los siguientes requisitos previos:

* Dirección URL base y credenciales del contrato; usuario de API con menos privilegios siempre que sea posible.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Los puntos finales varían según el producto Marigold. Valide con la asistencia de Marigold su implementación.
* Los datos personales en las respuestas deben cumplir con sus políticas de DPA y retención.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Apunte al host Marigold de su región, establezca la autenticación (la muestra siguiente utiliza `X-Api-Key` con clave y secreto), pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de REST de Marigold (extremo según la guía de integración). Ejemplo de patrón de URL:

1. Utilice la dirección URL base y la ruta proporcionadas en la documentación de la API de Marigold

1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

1. Marigold utiliza 2 extremos basados en el área geográfica para la que está activa la instancia de cliente:

1. Europa: https://{{customername}}.module.slgnt.eu
EE.UU.: https://{{customername}}.module.slgnt.us

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

El host base depende de la región (por ejemplo, `https://{{customername}}.module.slgnt.eu` o `https://{{customername}}.module.slgnt.us`). Confirme las rutas con Marigold para su implementación.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://{{customername}}.module.slgnt.{{locale}}/Portal/Api/organizations/{{organization}}/content/{{api_name}}` |
| **método HTTP** | `GET` |
| Carga de respuesta | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |
| Política | Configure los detalles del nivel de directiva según sus necesidades. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `customername` | `customername` | `<your_name>` |
| `locale` | `locale` | `eu` / `us` |
| `organization` | `organization` | `<your_organization>` |
| `api_name` | `api_name` | `<api_name>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | X-Api-Key | `<apiKey>:<apiSecret>` | Encabezado |

+++

### Adobe Target Recommendations {#adobe-target-recommendations}

>[!BEGINSHADEBOX]

Adobe Target incluye Recommendations y API de entrega para experiencias del lado del servidor o integradas, sujetas a derechos.

Los casos de uso habituales incluyen la inyección de recomendaciones en experiencias que crea en Journey Optimizer y la alineación de claves con el perfil o el contexto de Experience Platform.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Adobe Target Recommendations.

Se aplican los siguientes requisitos previos:

* Target con Recommendations; organización de IMS y autenticación admitida.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Las API de recomendación y entrega requieren parámetros específicos (por ejemplo, identificadores de mbox o producto). Siga la documentación de Adobe Target.
* Ajuste la latencia y el almacenamiento en caché para su volumen de envío y caso de uso.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Las llamadas de envío suelen ser **POST** con un cuerpo JSON. Configure OAuth según [Target authentication](https://experienceleague.adobe.com/es/docs/target-dev/developer/api/configure-authentication){target="_blank"}, pegue una respuesta de ejemplo, asigne campos y realice pruebas en el volumen esperado.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante las API de entrega/Recommendations de Target (según la documentación de Adobe para su patrón de integración). Ejemplo de patrón de URL:

1. Consulte la documentación de la API de Adobe Target Recommendations para su caso de uso

1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://{{client}}.tt.omtrdc.net/rest/v1/delivery` |
| Política | Configure los detalles del nivel de directiva según sus necesidades. |
| **método HTTP** | `POST` |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `client` | `client` | `<client_name>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| cliente | cliente | Variable | `<customer_client_code>` | Sí (activado) |
| sessionId | sessionId | Variable | ` <session_identifier>` | Sí (activado) |

**Autenticación**

Consulte [Configuración de autenticación de destino](https://experienceleague.adobe.com/es/docs/target-dev/developer/api/configure-authentication) y agregue JSON a la carga útil.

**Solicitar carga**

```Sample Request Payload JSON
{
  "id": {
    "tntId": "<YOUR_TENANT_ID>"
  },
  "context": {
    "channel": "web",
    "address": {
      "url": "https://example.com/store.html"
    },
    "screen": {
      "width": 1200,
      "height": 1400
    }
  },
  "experienceCloud": {
    "analytics": {
      "logging": "server_side",
      "supplementalDataId": "<supDataId>",
      "trackingServer": "sstats.adobe.com"
    }
  },
  "execute": {
    "pageLoad": {
      "parameters": {
        "pageType": "checkout",
        "preferredCurrency": "$"
      }
    },
    "mboxes": [
      {
        "index": 1,
        "name": "orderConfirmPage"
      }
    ]
  },
  "prefetch": {
    "views": [
      {
        "parameters": {
          "ad": "view"
        }
      }
    ],
    "mboxes": {
      "index": 1,
      "name": "SummerOffer"
    }
  }
}
```

+++


## Datos, tiempo y operaciones {#data-weather-and-operations}

### AccuWeather {#accuweather}

>[!BEGINSHADEBOX]

AccuWeather expone las API de REST de previsión y ubicación para que los mensajes puedan incluir fragmentos según el tiempo.

Los casos de uso habituales incluyen previsiones cortas en mensajes de correo electrónico o push y la personalización del contenido mediante valores de previsión vinculados a un perfil o contexto.

>[!ENDSHADEBOX]

+++ Obtenga más información sobre los requisitos previos y las limitaciones de AccuWeather.

Se aplican los siguientes requisitos previos:

* suscripción y clave de API; clave de ubicación o flujo de búsqueda de la ciudad.
* Acceso de administrador en Journey Optimizer para crear integraciones.

Se aplican las siguientes limitaciones y exclusiones:

* Confirme la forma de respuesta JSON para su nivel de suscripción AccuWeather; las integraciones asignan campos de respuestas JSON.
* Observe los límites de velocidad de AccuWeather y el almacenamiento en caché recomendado.
* La resolución de `locationKey` requiere a menudo una solicitud de geolocalización o búsqueda de ciudad por separado antes de las llamadas de previsión.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Use **GET** a menos que su suscripción requiera lo contrario, adjunte el parámetro de consulta `apiKey` (o como documentado), asigne `locationKey` y otras variables del perfil o contexto, pegue el JSON de muestra, asigne campos y realice pruebas.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de previsiones diarias. Ejemplo de patrón de URL:

1. `https://dataservice.accuweather.com/forecasts/v1/daily/{days}day/{locationKey}`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++Campos de integración de muestra

Campos de integración de muestra. Los detalles y niveles se describen en [API de AccuWeather](https://developer.accuweather.com/apis){target="_blank"}. A menudo, resuelve `locationKey` con una llamada de búsqueda de ubicaciones independiente (por ejemplo, `.../locations/v1/cities/search?q={{cityName}}`).

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://dataservice.accuweather.com/forecasts/v1/daily/{{days}}day/{{locationKey}}` |
| **método HTTP** | `GET` |
| Carga de respuesta | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |
| Política | Configure los detalles del nivel de directiva según sus necesidades. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `days` | `days` | `15` |
| `locationKey` | `locationKey` | `<desired_location_key>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `format` | `format` | Variable | json | No (desactivado) |
| `language` | `language` | Variable | en-US | No (desactivado) |
| `details` | `details` | Variable | False | No (desactivado) |
| `metric` | `metric` | Variable | False | No (desactivado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | `apiKey` | `<YOUR_API_KEY>` | Parámetros de consulta |

+++

### EstaciónBuque {#shipstation}

>[!BEGINSHADEBOX]

ShipStation ofrece API de envío y pedido para operadores, etiquetas y seguimiento.

Los casos de uso habituales incluyen el estado del pedido, los vínculos de seguimiento o los ETA de entrega en mensajes transaccionales.

>[!ENDSHADEBOX]

+++ Obtenga más información sobre los requisitos previos y las limitaciones de ShipStation.

Se aplican los siguientes requisitos previos:

* Clave de API y secreto (autenticación básica por documentos de ShipStation).
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* No exponga las claves API ShipStation en el contenido del mensaje; mantenga las credenciales únicamente en la configuración de integración.
* Los extremos de lista paginados pueden no ser adecuados para las integraciones; prefiera GET de un solo recurso cuando sea posible.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Establezca como objetivo el recurso que necesita (pedidos frente a envíos), autentique por [API ShipStation](https://www.shipstation.com/docs/api/){target="_blank"}, pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el punto final mediante la API ShipStation REST. Ejemplo de patrón de URL:

1. `https://ssapi.shipstation.com/...`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

El siguiente ejemplo de **Obtener temporizador** ilustra una llamada de temporización de automatización de estación de envío. Utilice la ruta y la autenticación exactas de la guía de integración de ShipStation al reproducirla en Journey Optimizer.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://dashboard.sendtric.com/api/v1/timers/{{id}}` |
| **método HTTP** | `POST` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | apiKey | `<your_api_key>` | Encabezado |

**Solicitar carga útil**

```Sample Request Payload
{
    "external_batch_id": "se-28529731",
    "batch_notes": "This is my batch",
    "shipment_ids": [
      "se-28529731"
    ],
    "rate_ids": [
      "se-28529731"
    ]
}
```

+++

### RevenueCat {#revenuecat}

>[!BEGINSHADEBOX]

RevenueCat proporciona API de estado de suscripción y derechos para las aplicaciones.

Un caso de uso típico es reflejar el estado de suscripción en campañas del ciclo vital en las que la directiva lo permite.

>[!ENDSHADEBOX]

+++ Obtenga más información sobre los requisitos previos y las limitaciones de RevenueCat.

Se aplican los siguientes requisitos previos:

* Clave de API secreta e identificadores de aplicación; asignación estable entre perfiles e ID de cliente de RevenueCat.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Proteja las claves API secretas y siga sus políticas de rotación.
* Los datos de suscripciones y autorizaciones son confidenciales. Cumplan los requisitos de privacidad y consentimiento.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Llame al REST **GET** que se muestra a continuación, realice la autenticación con el encabezado de clave secreta, pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de REST de RevenueCat. Ejemplo de patrón de URL:

1. `https://api.revenuecat.com/v1/...`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Patrón de ejemplo: usa **Obtener un producto** de RevenueCat (o un GET de producto/derecho equivalente) de [documentos de RevenueCat](https://docs.revenuecat.com/){target="_blank"} con la URL y la versión base del proyecto.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://api.revenuecat.com/projects/{{project_id}}/products/{{product_id}}` |
| **método HTTP** | `GET` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |
| **Carga de respuesta** | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `project_id` | `project_id` | `<project_id>` |
| `product_id` | `product_id` | `<product_id>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | No (desactivado) |
| `locale` | `locale` | Variable | `<locale_code>` | No (desactivado) |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | No (desactivado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | Autorización | `Bearer <token>` | Encabezado |

+++

### Databricks {#databricks}

>[!BEGINSHADEBOX]

Databricks proporciona API de SQL y REST sobre datos de lakehouse; los borradores anteriores combinaban la guía de ejecución de instrucciones con una muestra de **job/get**.

Un caso de uso típico es el uso de atributos pequeños y desnormalizados de tablas controladas para la personalización con el menor privilegio estricto.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Databricks.

Se aplican los siguientes requisitos previos:

* Host, token o directiva de OAuth por organización de Workspace; entidad de seguridad de servicio con ámbito mínimo.
* Acceso de administrador en Journey Optimizer.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Prefiera rutas de lectura estrechas; si usa la ejecución de instrucciones **POST**, incluya el cuerpo de JSON que requiere la API, pegue una respuesta de éxito de muestra para la asignación, pruebe la latencia con cuidado y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de ejecución de instrucción SQL de Databricks. Ejemplo de patrón de URL:

1. `https://{workspace-host}/api/2.0/sql/statements/...`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++Campos de integración de muestra

El ejemplo del trabajo **GET** que se muestra a continuación es ilustrativo; para la personalización basada en SQL, prefiera el patrón de la [API de ejecución de instrucciones](https://docs.databricks.com/api/workspace/statementexecution){target="_blank"} que admite su espacio de trabajo.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://<databricks-instance>/api/2.0/jobs/get` |
| **método HTTP** | `GET` |
| Carga de respuesta | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |
| Política | Configure los detalles del nivel de directiva según sus necesidades. |
| Autenticación | Oauth |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Aceptar | Aceptar | Constante | application/json | Sí (activado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `job_id` | `job_id` | Variable | `12` | Sí |

+++

## Revisiones, consentimiento y asistencia social {#reviews-consent-and-social}

### Bynder {#bynder}

>[!BEGINSHADEBOX]

Bynder es un DAM con API de REST; las integraciones suelen utilizar OAuth 2.0 para metadatos de solo lectura o URL de recursos.

Algunos casos de uso habituales son la extracción de metadatos de recursos o direcciones URL de entrega en los mensajes y mantener el creativo aprobado en Bynder alineado con los recorridos.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Bynder.

Se aplican los siguientes requisitos previos:

* Dominio de portal y cliente de OAuth (o método de token aprobado).
* Ámbitos para el acceso de solo lectura; acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* La paginación y la actualización de tokens de OAuth deben seguir las reglas de API de Bynder.
* Respuestas paginadas grandes: asigne solo los campos necesarios para la personalización.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Configure **GET** en el extremo elegido (un patrón común es una lista de usuarios), complete OAuth por [Bynder](https://developer.bynder.com/){target="_blank"}, evite extraer páginas de datos innecesarias, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de Bynder v4 (ejemplo: patrón de lista de usuarios). Ejemplo de patrón de URL:

1. `https://{your-bynder-domain}/api/v4/users/`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Campos de integración de muestra. Consulte [Documentación de la API de Bynder](https://developer.bynder.com/){target="_blank"} para obtener detalles de la carga de OAuth 2.0.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://{{your-bynder-domain}}/api/v4/users/` |
| **método HTTP** | `GET` |
| Carga de respuesta | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |
| Política | Configure los detalles del nivel de directiva según sus necesidades. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `your-bynder-domain` | `your-bynder-domain` | `<your-bynder-domain>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |
| Autorización | Autorización | Constante | Portador `<token>` | Sí (activado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `includeInActive` | `includeInActive` | Variable | False | No (desactivado) |
| `limit` | `limit` | Variable | 100 | No (desactivado) |
| `page` | `page` | Variable | 1 | No (desactivado) |

**Autenticación**

| Tipo | Carga útil |
| --- | --- |
| OAuth 2.0 | Carga útil de OAuth 2.0 (consulte la documentación de Bynder) |

```
{
    "type": "oauth2",
    "endpoint": {
        "uri": ""
    },
    "method": "get",
    "response": {
        "type": "json"
    },
    "request": {
        "header": [
            {
                "key": "client_id",
                "value": ""
            },
            {
                "key": "client_secret",
                "value": ""
            }
        ],
        "queryParams": [
            {
                "key": "grant_type",
                "value": ""
            },
            {
                "key": "scope",
                "value": ""
            }
        ],
        "payload": {
            "type": "json",
            "content": {}
        }
    },
    "credentialPaths": [
        "header.client_id",
        "header.client_secret",
        "queryParam.scope"
    ],
    "tokenPath": "message.token",
    "policy": {
        "timeoutInMilliseconds": 30000,
        "cache": {
            "enabled": true,
            "ttlInSeconds": 300
        },
        "retry": {
            "enabled": false
        }
    },
    "locationConfig": {
        "key": "x-token",
        "location": "query"
    }
}
```

+++

### Trustpilot {#trustpilot}

>[!BEGINSHADEBOX]

Trustpilot proporciona API para el negocio y revisa los datos de resumen donde su caso de uso y contrato lo permiten.

Un caso de uso típico es mostrar recuentos de revisiones o clasificaciones en contenido de marketing que cumple con los términos de Trustpilot.

>[!ENDSHADEBOX]

+++ Obtenga más información sobre los requisitos previos y las limitaciones de Trustpilot.

Se aplican los siguientes requisitos previos:

* Clave de API y caso de uso aprobado; identificadores empresariales para consultas.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* El uso de los datos de Trustpilot debe cumplir con las políticas de uso de datos y marca de Trustpilot.
* Los límites de tasa se aplican al resumen de revisión y a los extremos relacionados.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Configure **GET** con la autenticación de consulta requerida, asigne identificadores de perfil o contexto, pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante las API de Trustpilot. Ejemplo de patrón de URL:

1. `https://api.trustpilot.com/v1/...`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Use la operación de listado de categorías de [desarrolladores de Trustpilot](https://developers.trustpilot.com/){target="_blank"} para su patrón de integración; los parámetros varían según el recurso.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://api.trustpilot.com/v1/categories` |
| **método HTTP** | `GET` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |
| **Carga de respuesta** | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | No (desactivado) |
| `locale` | `locale` | Variable | `<locale_code>` | No (desactivado) |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | No (desactivado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | apiKey | `<your_api_key>` | Encabezado |

+++

### Bazaarvoice {#bazaarvoice}

>[!BEGINSHADEBOX]

Bazaarvoice ofrece valoraciones, reseñas y API de UGC.

Un caso de uso típico es mostrar resúmenes de revisión o clasificaciones en correos electrónicos cuando la directiva lo permite.

>[!ENDSHADEBOX]

+++ Obtenga más información sobre los requisitos previos y las limitaciones de Bazaarvoice.

Se aplican los siguientes requisitos previos:

* Clave de paso de API e identificadores de cliente de su contrato.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* La visualización de valoraciones y reseñas debe seguir las políticas de contenido de Bazaarvoice.
* Se aplican límites de velocidad y reglas de almacenamiento en caché por clave de API.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Use **GET** con `passkey` como parámetro de consulta en la API de Conversaciones, establezca `Accept: application/json`, pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de Bazarvoice Conversations. Ejemplo de patrón de URL:

1. `https://api.bazaarvoice.com/...`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Ejemplo de punto de entrada: `https://api.bazaarvoice.com/data/products.json` con parámetros de consulta de versión y filtro. Ver [desarrollador de Bazaarvoice](https://developer.bazaarvoice.com/){target="_blank"}.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://api.bazaarvoice.com/data/products.json` |
| **método HTTP** | `GET` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |
| **Carga de respuesta** | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Aceptar | Aceptar | Constante | application/json | Sí (activado) |

**Autenticación**

| Tipo | Valor clave | Ubicación |
| --- | --- | --- |
| clave de paso | `<YOUR_ACCESS_TOKEN>` | Parámetros de consulta |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `apiversion` | apiversionNumber | Constante | 5,4 | Sí (activado) |
| `filter` | `filter` | Variable | Id.:47950830 | No (desactivado) |
| `stats` | `stats` | Variable | todo | No (desactivado) |

+++

### OneTrust {#onetrust}

>[!BEGINSHADEBOX]

OneTrust expone la privacidad y las API de consentimiento (URL y esquemas específicos del producto).

Un caso de uso típico es la lectura de señales de consentimiento o preferencia para contenido condicional donde la arquitectura y la revisión legal lo permiten.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de OneTrust.

Se aplican los siguientes requisitos previos:

* Credenciales de API y URL base regional; aprobación legal para campos utilizados en mensajería.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Los datos de consentimiento y preferencia están altamente regulados. Coordine con los equipos legales y de privacidad.
* Las rutas de API y las cargas difieren según el producto OneTrust. Utilice la documentación de su suscripción.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Utilice el esquema publicado o la ruta del centro de preferencias de sus documentos de suscripción, complete OAuth si es necesario, pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de OneTrust. Ejemplo de patrón de URL:

1. URL base de portal para desarrolladores de Per OneTrust

1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://customer.my.onetrust.com/api/consentmanager/v2/preferencecenters/{{preferencecenterid}}/schema` |
| **método HTTP** | `GET` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |
| **Carga de respuesta** | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |
| **Autenticación** | Oauth |

**Parámetros de ruta**

| Parámetro | Nombre | Valor |
| --- | --- | --- |
| `preferencecenterid` | `preferencecenterid` | `<pref-id>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Aceptar | Aceptar | Constante | application/json | Sí (activado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `state` | `state` | constante | PUBLICADO | Sí |

+++

#### Esquema del centro de preferencias (publicado)

Patrón de ejemplo (fragmento): `https://{tenant}.my.onetrust.com/api/consentmanager/v2/preferencecenters/{preferencecenterid}/schema?state=PUBLISHED`. Confirme la ruta exacta en [OneTrust Developer](https://developer.onetrust.com/){target="_blank"}.

### Meta {#meta}

>[!BEGINSHADEBOX]

Las API de gráficos y marketing de Meta exponen objetos de catálogo y campaña para integraciones comerciales autorizadas.

Un caso de uso típico es enriquecer contenido con atributos de Meta donde los tokens y las directivas lo permiten.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Meta.

Se aplican los siguientes requisitos previos:

* Token de aplicación o usuario del sistema con los permisos correctos; alineación de Business Manager.
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Los tokens de acceso de corta duración requieren una renovación o una estrategia de larga duración adecuada para las integraciones del lado del servidor.
* Cumplan los términos de la plataforma de Meta; no registren tokens u otros secretos en las cargas útiles de mensajes.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Las llamadas de gráfico suelen ser **GET** con una ruta con versiones; gestione la caducidad del token, pegue el JSON de muestra, asigne campos, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de Meta Graph. Ejemplo de patrón de URL:

1. `https://graph.facebook.com/vXX.X/...`
1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Campos de integración de muestra. Consulte [API de gráficos](https://developers.facebook.com/docs/graph-api){target="_blank"} para ver versiones y tokens de acceso.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://graph.facebook.com/{{API_VERSION}}/{{PRODUCT_CATALOG_ID}}/products` |
| **método HTTP** | `GET` |
| Carga de respuesta | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |
| Política | Configure los detalles del nivel de directiva según sus necesidades. |
| Autenticación | Oauth |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `API_VERSION` | `API_VERSION` | `v19.0` |
| `PRODUCT_CATALOG_ID` | `PRODUCT_CATALOG_ID` | `12345` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Aceptar | Aceptar | Constante | application/json | Sí (activado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `fields` | `fields` | Variable | id | No |
| `filter` | `filter` | Variable | — | No |

+++

### Aprimo {#aprimo}

>[!BEGINSHADEBOX]

Aprimo combina operaciones de marketing y API de DAM para registros, activos y metadatos.

Los casos de uso habituales incluyen campos de recursos o registros aprobados en contenido dinámico y flujos de trabajo de DAM controlados en industrias reguladas.

>[!ENDSHADEBOX]

+++ Obtenga más información acerca de los requisitos previos y las limitaciones de Aprimo.

Se aplican los siguientes requisitos previos:

* URL del inquilino y credenciales (clave de OAuth o API según la configuración).
* Acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* La seguridad de nivel de campo de Aprimo debe alinearse con los atributos que asigne en Journey Optimizer.
* Cargas útiles HAL o JSON grandes: restringir los campos asignados al conjunto mínimo requerido.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). Use **GET** en la ruta de registro que necesite, envíe los encabezados necesarios, como `API-VERSION`, pegue el archivo JSON de muestra (HAL o JSON como devuelto), asigne un conjunto de campos mínimo, realice pruebas y active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API Aprimo DAM/Records. Ejemplo de patrón de URL:

1. Por URL base de API de Aprimo y ruta de recurso para su inquilino

1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://productstrategy1.dam.aprimo.com/api/core/record/{{recordID}}` |
| **método HTTP** | `GET` |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `recordId` | `recordId` | `<record_identifier>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |
| API-VERSION | API-VERSION | Constante | 1 | Sí (activado) |
| Aceptar | Aceptar | Constante | application/hal+json O application/json | No (desactivado) |
| select-record | select-record | Variable | `<selection_type>` | No (desactivado) |
| select-record-fields | select-record-fields | Variable | `<field_list>` | No (desactivado) |
| select-field | select-field | Variable | `<field_selection>` | No (desactivado) |

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | Autorización | Portador `<token>` | Encabezado |

+++

### Épsilon (Epsilon3) {#epsilon}

>[!BEGINSHADEBOX]

Epsilon expone las API por acuerdo empresarial; las URL base y la autenticación provienen del equipo de la cuenta (el ejemplo de la API de eventos que se muestra a continuación es ilustrativo).

Un caso de uso típico es exponer la lealtad o los atributos de oferta a través de las API JSON admitidas.

>[!ENDSHADEBOX]

+++ Obtenga más información sobre los requisitos previos y las limitaciones de Epsilon (Epsilon3).

Se aplican los siguientes requisitos previos:

* Credenciales y puntos de conexión de Epsilon; acceso de administrador en Journey Optimizer.

Se aplican las siguientes limitaciones y exclusiones:

* Los puntos de conexión y hosts son específicos del cliente. No realice la implementación sin la documentación del equipo de cuenta de Epsilon.

+++

Utilice el siguiente procedimiento para configurar esta integración en Journey Optimizer. Consulte **Campos de integración de muestra** para obtener detalles de solicitud de ejemplo y confirme esos valores con la documentación del proveedor para su entorno.

1. Seguir [Trabajar con integraciones](external-sources.md). No adivine las direcciones URL públicas. Utilice la especificación de Epsilon, pegue el JSON de muestra, asigne campos, pruebe, active.

1. En Journey Optimizer, vaya a Configuraciones > Administrar y, a continuación, seleccione Crear integración.

1. Introduzca un nombre de integración sin espacios.

1. Configure el extremo mediante la API de Epsilon (según la especificación de integración). Ejemplo de patrón de URL:

1. Suministrado por Epsilon para su programa

1. Seleccione el método HTTP mostrado en la tabla de configuración (normalmente GET a menos que se indique lo contrario).

1. Configure la autenticación (encabezados, parámetros de consulta u OAuth) exactamente como se especifica en la tabla y en la documentación del proveedor.

1. Defina la ruta, la consulta y los parámetros de encabezado, y asigne variables a datos contextuales o de perfil donde sea necesario.

1. Pegue una respuesta JSON de muestra para que se puedan detectar y asignar los campos.

1. Seleccione los campos necesarios para la personalización en la asignación de carga útil de respuesta.

1. Configure las directivas de tiempo de espera, reintento y almacenamiento en caché en función del volumen esperado.

1. Compruebe la conexión y, a continuación, active la integración.

En la tabla siguiente se muestran valores de ejemplo para esta solicitud de integración.

+++ Campos de integración de muestra

Patrón de ejemplo: `https://{your-instance}.epsilon3.io/api/v1/planning/events` con `start` y `end` parámetros de consulta y clave de API basada en encabezado. Confirme con Epsilon antes de la producción.

| Campo | Valor |
| --- | --- |
| **Dirección URL** | `https://{{your-instance}}.epsilon3.io/api/v1/planning/events` |
| **método HTTP** | `GET` |
| **Directiva** | Configure los detalles del nivel de directiva según sus necesidades. |
| **Carga de respuesta** | Seleccione y configure los campos de respuesta deseados para utilizarlos durante la creación, en función de la respuesta de la API. |

**Parámetros de ruta**

| Parámetro de ruta | Nombre | Valor predeterminado |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |

**Encabezados**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| Tipo de contenido (predeterminado) | Content-Type | Constante | application/json | Sí (activado) |

**Parámetros de consulta**

| Parámetro | Nombre | Tipo | Valor | Obligatorio |
| --- | --- | --- | --- | --- |
| `start` | `start` | Variable | 24T14:15:22Z, 08-2019 | Sí (activado) * |
| `end` | `end` | Variable | 24T14:15:22Z, 08-2019 | Sí (activado) * |
| `eventType` | `eventType` | Variable | programado/no programado | No (desactivado) |
| `exclude_recurrences` | `exclude_recurrences` | Variable | true / false | No (desactivado) |

\* Opcional para `eventType` = `unscheduled` y para `exclude_recurrences` = `true`.

**Autenticación**

| Tipo | Nombre de clave API | Valor de clave API | Ubicación |
| --- | --- | --- | --- |
| Clave de API | `<your_username>` | `<EPSILON3_API_KEY>` | Encabezado |

+++

