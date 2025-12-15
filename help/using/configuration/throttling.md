---
solution: Journey Optimizer
product: journey optimizer
title: API de limitación
description: Aprenda a trabajar con la API de restricción
feature: Journeys, API
role: Developer
level: Beginner
keywords: externo, API, optimizador, límite
exl-id: b837145b-1727-43c0-a0e2-bf0e8a35347c
source-git-commit: b495462aed9a67ff25c2563288bb2ca57e9b7db7
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 48%

---

# Uso de la API de limitación

La API de restricción le ayuda a crear, configurar y supervisar sus configuraciones de restricción para limitar el número de eventos enviados por segundo.

Esta sección proporciona información global sobre cómo trabajar con la API. Hay disponible una descripción detallada de la API en [Documentación de las API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.

## Lectura obligatoria

* **Una configuración por organización:** Actualmente solo se permite una configuración por organización. Se debe definir una configuración en una zona protegida de producción (dada a través de `x-sandbox-name` en los encabezados).
* **Aplicación de nivel de organización:** Se aplica una configuración en el nivel de organización.
* **Administración de límites de API:** Cuando se alcanza el límite establecido en la API, los eventos adicionales se ponen en cola durante un máximo de 6 horas. Este valor no se puede modificar.
* **`maxHttpConnections`parámetro:** El parámetro `maxHttpConnections` es un parámetro opcional disponible en la API de límite que solo le permite restringir el número de conexiones que Journey Optimizer abrirá en el sistema externo. [Aprenda a trabajar con la API de límite](../configuration/capping.md)

  Si desea restringir el número de conexiones pero también limitar esas llamadas externas, puede configurar dos configuraciones, una de limitación y otra de restricción, en el mismo punto de conexión. Ambas configuraciones pueden coexistir para un extremo. Para establecer &quot;maxHttpConnections&quot; para un extremo limitado, utilice la API de limitación para establecer el umbral de limitación y la API de restricción para establecer &quot;maxHttpConnections&quot;. Al llamar a la API de límite, puede establecer el umbral de límite en algo más alto que el umbral de restricción, de modo que la regla de límite nunca entre en juego.

## Descripción de la API de restricción y colección de Postman {#description}

En la tabla siguiente se enumeran los comandos disponibles para la API de regulación. Encontrará información detallada, incluidos ejemplos de solicitudes, parámetros y formatos de respuesta, en la [documentación de API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling/).

| Método | Ruta | Descripción |
|---|---|---|
| [!DNL POST] | list/throttlingConfigs | Obtención de una lista de las configuraciones de limitación |
| [!DNL POST] | /throttlingConfigs | Creación de una configuración de limitación |
| [!DNL POST] | /throttlingConfigs/`{uid}`/deploy | Implementación de una configuración de limitación |
| [!DNL POST] | /throttlingConfigs/`{uid}`/undeploy | Desimplementación de una configuración de limitación |
| [!DNL POST] | /throttlingConfigs/`{uid}`/canDeploy | Compruebe si una configuración de limitación se puede implementar o no |
| [!DNL PUT] | /throttlingConfigs/`{uid}` | Actualización de una configuración de limitación |
| [!DNL GET] | /throttlingConfigs/`{uid}` | Recuperación de una configuración de limitación |
| [!DNL DELETE] | /throttlingConfigs/`{uid}` | Eliminación de una configuración de limitación |

Además, hay disponible una colección de Postman [aquí](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Throttling-API_postman-collection.json){target="_blank"} que le ayudará en la configuración de las pruebas.

Esta colección se ha configurado para compartir la colección Variable de Postman generada mediante **[Integraciones de la consola de Adobe I/O](https://console.adobe.io/integrations) > Probarla > Descargar para Postman**, que genera un archivo de entorno de Postman con los valores de integraciones seleccionados.

Una vez descargado y cargado en Postman, debe añadir tres variables: `{JO_HOST}`,`{BASE_PATH}` y `{SANDBOX_NAME}`.

* `{JO_HOST}` : URL de puerta de enlace [!DNL Journey Optimizer].
* `{BASE_PATH}` : punto de entrada para la API.
* `{SANDBOX_NAME}`: el encabezado **x-sandbox-name** (por ejemplo, “prod”) correspondiente al nombre de la zona protegida donde se realizarán las operaciones de API. Consulte la [información general sobre las zonas protegidas](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=es){target="_blank"} para obtener más detalles.

## Configuración de limitación {#configuration}

Esta es la estructura de una configuración de limitación. Los atributos **name** y **description** son opcionales.

```json
{
    "name": "<given name - free text>",
    "description": "<given description - free text>"
    "urlPattern": "<endpoint URL - wildcards are allowed>",
    "methods": [ "<HTTP method such as GET, POST, PUT>" ],
    "maxThroughput": <max call throughput>
}
```

Por ejemplo:

```json
{
  "name": "throttling-config-external",
  "description": "example of throttling config for an external endpoint",
  "urlPattern": "https://api.example.org/data/2.5/*",
  "methods": ["POST", "PUT"],
  "maxThroughput": 4000
}
```

>[!IMPORTANT]
>
>La configuración solo estará activa después de llamar al extremo **deploy**.

## Errores

Al crear o actualizar una configuración, el proceso aprueba la dada y devuelve el estado de validación identificado por su ID único, uno de los siguientes:

```json
"ok" or "error"
```

>[!IMPORTANT]
>
>Los atributos **maxThroughput**, **urlPattern** y **methods** son obligatorios.
>
>El valor de **maxThroughput** debe estar en el rango de 200-5000.

Al crear, eliminar o implementar la configuración de limitación, pueden producirse los siguientes errores:

* **ERR_THROTTLING_CONFIG_100**: configuración de limitación: `<mandatory attribute>` obligatorio
* **ERR_THROTTLING_CONFIG_101**: configuración de limitación: maxThroughput es obligatorio y debe ser mayor o igual que 200 y menor o igual que 5.000.
* **ERR_THROTTLING_CONFIG_104**: configuración de limitación: patrón de URL incorrecto
* **ERR_THROTTLING_CONFIG_105**: configuración de limitación: no se permiten comodines en la parte host del patrón de URL
* **ERR_THROTTLING_CONFIG_106**: configuración de limitación: carga útil no válida
* **THROTTLING_CONFIG_DELETE_FORBIDDEN_ERROR: 1456**, “No se puede eliminar una configuración de limitación implementada. Debe desimplementarlo antes de eliminarlo”
* **THROTTLING_CONFIG_DELETE_ERROR: 1457**, “No se puede eliminar la configuración de limitación: se produce un error inesperado”
* **THROTTLING_CONFIG_DEPLOY_ERROR: 1458**, “No se puede implementar la configuración de limitación: se produce un error inesperado”
* **THROTTLING_CONFIG_UNDEPLOY_ERROR: 1459**, “No se puede desimplementar la configuración de limitación: se produce un error inesperado”
* **THROTTLING_CONFIG_GET_ERROR: 1460**, “No se puede obtener la configuración de limitación: se produce un error inesperado”
* **THROTTLING_CONFIG_UPDATE_NOT_ACTIVE_ERROR: 1461**, “No se puede actualizar la configuración de limitación: la versión de tiempo de ejecución no está activa”
* **THROTTLING_CONFIG_UPDATE_ERROR: 1462**, “No se puede actualizar la configuración de limitación: se produce un error inesperado”
* **THROTTLING_CONFIG_NON_PROD_SANDBOX_ERROR: 1463**, “Operación no permitida en la configuración de limitación: la zona protegida no es de producción”
* **THROTTLING_CONFIG_CREATE_ERROR: 1464**, “No se puede crear la configuración de limitación: se produce un error inesperado”
* **THROTTLING_CONFIG_CREATE_LIMIT_ERROR: 1465**, “No se puede crear la configuración de limitación: solo se permite una configuración por organización”
* **THROTTLING_CONFIG_ALREADY_DEPLOYED_ERROR: 14466**, “No se puede implementar la configuración de limitación: ya implementada”
* **THROTTLING_CONFIG_NOT_FOUND_ERROR: 14467**, “Configuración de limitación no encontrada”
* **THROTTLING_CONFIG_NOT_DEPLOYED_ERROR: 14468**, “No se puede anular la implementación de la configuración de limitación: aún no implementada”

**Ejemplos de errores**

Al intentar crear una configuración en una zona protegida que no es de producción:

```json
{
    "status": 400,
    "error": "{\"code\":1463,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Operation not allowed on throttling config: non prod sandbox\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:384\",\"schema\":\"throttlingConfigs$ui-tests\"}",
    "requestId": "5sgnAYXs8mpswwjAFEIaAU2faQYbtyHc"
}
```

En caso de que la zona protegida dada no exista:

```json
{
    "status": 500,
    "error": "{\"code\":4000,\"family\":\"INTERNAL_ERROR\",\"message\":\"INTERNAL ERROR\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.common.exceptions.ApiErrorException:43\"}",
    "requestId": "04ZJ4e5ki4bYs3lfO17a7hovRGewjvdK"
}
```

Al intentar crear otra configuración:

```json
{
    "status": 400,
    "error": "{\"code\":1465,\"family\":\"INPUT_OUTPUT_ERROR\",\"message\":\"Can't create throttling config: only one config allowed per org\",\"service\":\"vyg-authoring-api\",\"version\":\"ed87515\",\"context\":\"com.adobe.voyager.service.authoring.restapis.v1_0.ThrottlingConfigService:108\",\"schema\":\"throttlingConfigs$prod\"}",
    "requestId": "A7ezT8JhOQT4WIAf1Fv7K2wCDA8281qM"
}
```

## Ciclo de vida de configuración en nivel de tiempo de ejecución {#config}

Cuando una configuración se desimplementa, se marca como inactiva en el nivel de tiempo de ejecución y los eventos pendientes se siguen procesando durante 24 horas. A continuación, se elimina en el servicio de tiempo de ejecución.

Una vez que se ha desimplementado una configuración, es posible actualizarla y volver a implementarla. Esto creará una nueva configuración de tiempo de ejecución que se tendrá en cuenta en la próxima ejecución de acciones.

Al actualizar una configuración ya implementada, los nuevos valores se tienen en cuenta de inmediato. Los recursos del sistema subyacentes se adaptan automáticamente. Esto es óptimo, comparado con desimplementar y volver a implementar la configuración.

## Ejemplos de respuestas {#responses}

**Creación: POST**

```json
{
    "canDeploy": {
        "validationStatus": "ok"
    },
    "createdElement": {
        "name": "throttling-config-external",
        "description": "example of throttling config for an external endpoint",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "PUT",
            "POST"
        ],
        "maxThroughput": 4000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T10:48:16.099647Z"
        },
        "state": "created",
        "authoringFormatVersion": "1.0"
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "created"
}
```

**Actualización: PUT**

```json
{
    "updatedElement": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    },
    "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "uri": "/voyager/apis/throttlingConfigs/043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
    "resStatus": "updated",
    "canDeploy": {
        "validationStatus": "ok"
    }
}
```

**Leer (después de la actualización): GET**

```json
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z"
        },
        "state": "updated",
        "authoringFormatVersion": "1.0",
        "hasBeenDeployed": false
    }
}
```

**Leer (después de la implementación): GET**

```json
{
    "result": {
        "_id": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6_8872a010-f91e-11ea-895c-11ef8f98ba52",
        "orgId": "AC202A3A5F615BD30A495FDE@AdobeOrg",
        "sandboxId": "8872a010-f91e-11ea-895c-11ef8f98ba52",
        "sandboxName": "prod",
        "uid": "043a1aea-2dfd-4965-b93a-cb9a1eced0e6",
        "urlPattern": "https://api.example.org/data/2.5/*",
        "methods": [
            "POST"
        ],
        "maxThroughput": 5000,
        "authoringFormatVersion": "1.0",
        "name": "throttling-config-external -- optional",
        "description": "example of throttling config for an external endpoint -- optional",
        "version": "1.0",
        "state": "deployed",
        "metadata": {
            "createdBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "createdById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "createdAt": "2023-03-22T10:48:16.099647Z",
            "lastModifiedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastModifiedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastModifiedAt": "2023-03-22T11:39:14.212983Z",
            "lastDeployedBy": "dacce1c3-d08b-4862-b434-2a4449c7e642@techacct.adobe.com",
            "lastDeployedById": "309F2A46640B0B300A495C83@techacct.adobe.com",
            "lastDeployedAt": "2023-03-22T11:46:07.532648Z"
        },
        "hasBeenDeployed": true
    }
}
```

## Casos de uso {#uc}

En esta sección se enumeran los casos de uso clave para administrar las configuraciones de restricción en [!DNL Journey Optimizer] y los comandos de API asociados necesarios para implementar el caso de uso.

Encontrará detalles sobre cada comando de API en [Descripción de la API y recopilación de Postman](#description).

+++Creación e implementación de una nueva configuración de regulación

Llamadas de API para utilizar:

1. **`list`** - Recupera configuraciones existentes.
1. **`create`** - Crea una nueva configuración.
1. **`candeploy`**: comprueba si se puede implementar la configuración.
1. **`deploy`** - Implementa la configuración.

+++

+++Actualizar e implementar una configuración de limitación (aún no implementada)

Llamadas de API para utilizar:

1. **`list`** - Recupera configuraciones existentes.
1. **`get`**: obtiene detalles de una configuración específica.
1. **`update`** - Modifica la configuración.
1. **`candeploy`** - Comprueba la idoneidad de la implementación.
1. **`deploy`** - Implementa la configuración.

+++

+++Anular la implementación y eliminar una configuración de limitación implementada

Llamadas de API para utilizar:

1. **`list`** - Recupera configuraciones existentes.
1. **`undeploy`** - Anula la implementación de la configuración.
1. **`delete`** - Quita la configuración.

+++

+++Eliminar una configuración de regulación implementada

Solo en una llamada de API puede anular la implementación y eliminar la configuración con el parámetro `forceDelete`.

Llamadas de API para utilizar:

1. **`list`** - Recupera configuraciones existentes.
1. **`delete`(con `forceDelete` parámetro)** - Fuerza la eliminación de una configuración implementada en un solo paso.

+++

+++Actualizar una configuración de restricción ya implementada

>[!NOTE]
>
>No es necesario anular la implementación de la configuración antes de actualizar

Llamadas de API para utilizar:

1. **`list`** - Recupera configuraciones existentes.
1. **`get`**: obtiene detalles de una configuración específica.
1. **`update`** - Modifica la configuración.

+++
