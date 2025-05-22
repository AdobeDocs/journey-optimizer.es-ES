---
solution: Journey Optimizer
product: journey optimizer
title: API de límite
description: Aprenda a trabajar con la API de límite
feature: Journeys, API
role: User
level: Beginner
keywords: externo, API, optimizador, límite
exl-id: 377b2659-d26a-47c2-8967-28870bddf5c5
source-git-commit: 9f801b1fdcab38bffff851675eca5e2fb61dfbf9
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 6%

---

# Uso de la API de límite {#work}

La API de límite le ayuda a crear, configurar y supervisar sus configuraciones de límite.

Esta sección proporciona información global sobre cómo trabajar con la API. Hay disponible una descripción detallada de la API en [Documentación de las API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/).

## Descripción de la API de límite y colección de Postman {#description}

En la tabla siguiente se enumeran los comandos disponibles para la API de límite. Encontrará información detallada, incluidos ejemplos de solicitudes, parámetros y formatos de respuesta, en la [documentación de API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/).

| Método | Ruta | Descripción |
|---|---|---|
| [!DNL POST] | list/endpointConfigs | Obtenga una lista de las configuraciones de límite de extremos |
| [!DNL POST] | /endpointConfigs | Crear una configuración de límite de extremo |
| [!DNL POST] | /endpointConfigs/`{uid}`/deploy | Implementar una configuración de límite de extremo |
| [!DNL POST] | /endpointConfigs/`{uid}`/undeploy | Anular la implementación de una configuración de límite de extremo |
| [!DNL POST] | /endpointConfigs/`{uid}`/canDeploy | Compruebe si se puede implementar o no una configuración de límite de extremo |
| [!DNL PUT] | /endpointConfigs/`{uid}` | Actualizar una configuración de límite de extremo |
| [!DNL GET] | /endpointConfigs/`{uid}` | Recuperar una configuración de límite de extremo |
| [!DNL DELETE] | /endpointConfigs/`{uid}` | Eliminar una configuración de límite de extremo |

Cuando se crea o actualiza una configuración, se realiza automáticamente una comprobación para garantizar la sintaxis y la integridad de la carga útil.
Si se producen algunos problemas, la operación devuelve advertencias o errores para ayudarle a corregir la configuración.

Además, hay disponible una colección de Postman [aquí](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json) que le ayudará en la configuración de las pruebas.

Esta colección se ha configurado para compartir la colección Variable de Postman generada mediante __[Integraciones de la consola de Adobe I/O](https://console.adobe.io/integrations) > Probarla > Descargar para Postman__, que genera un archivo de entorno de Postman con los valores de integraciones seleccionados.

Una vez descargado y cargado en Postman, debe añadir tres variables: `{JO_HOST}`,`{BASE_PATH}` y `{SANDBOX_NAME}`.
* `{JO_HOST}` : URL de puerta de enlace [!DNL Journey Optimizer].
* `{BASE_PATH}` : punto de entrada para la API.
* `{SANDBOX_NAME}`: el encabezado **x-sandbox-name** (por ejemplo, “prod”) correspondiente al nombre de la zona protegida donde se realizarán las operaciones de API. Consulte la [información general sobre las zonas protegidas](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=es) para obtener más detalles.

## Configuración de extremo

Esta es la estructura básica de una configuración de extremo:

```
{
    "url": "<endpoint URL>",  //wildcards are allowed in the endpoint URL
    "methods": [ "<HTTP method such as GET, POST, >, ...],
    "services": {
        "<service name>": { . //must be "action" or "dataSource" 
            "maxHttpConnections": <max connections count to the endpoint (optional)>
            "rating": {          
                "maxCallsCount": <max calls to be performed in the period defined by period/timeUnit>,
                "periodInMs": <integer value greater than 0>
            }
        },
        ...
    }
}
```

>[!IMPORTANT]
>
>El parámetro **maxHttpConnections** es opcional. Permite restringir el número de conexiones que Journey Optimizer abrirá al sistema externo.
>
>El valor máximo que se puede establecer es 400. Si no se especifica nada, el sistema puede abrir varios miles de conexiones en función del escalado dinámico del sistema.
>
>Cuando se implementa la configuración de límite, si no se ha proporcionado ningún valor &quot;maxHttpConnection&quot;, se agrega un valor predeterminado &quot;maxHttpConnection = -1&quot; a la configuración implementada, lo que significa que Journey Optimizer utilizará el valor predeterminado del sistema.

Por ejemplo:

```
`{
  "url": "https://api.example.org/data/2.5/*",
  "methods": [
    "GET"
  ],
  "services": {
    "dataSource": {
      "rating": {
        "maxCallsCount": 500,
        "periodInMs": 1000
      }
    }
  }
}
```

>[!IMPORTANT]
>
>La configuración solo estará activa después de llamar al extremo **deploy**.

## Advertencia y errores

Cuando se llama a un método **canDeploy**, el proceso valida la configuración y devuelve el estado de validación identificado por su identificador único, ya sea:

```
"ok" or "error"
```

Los posibles errores son:

* **ERR_ENDPOINTCONFIG_100**: configuración de límite: falta URL o no es válida
* **ERR_ENDPOINTCONFIG_101**: configuración de límite: URL mal formada
* **ERR_ENDPOINTCONFIG_102**: configuración de límite: url con formato incorrecto: no se permite el carácter comodín en la dirección URL en host:puerto
* **ERR_ENDPOINTCONFIG_103**: configuración de límite: faltan métodos HTTP
* **ERR_ENDPOINTCONFIG_104**: configuración de límite: no se definió la clasificación de llamadas
* **ERR_ENDPOINTCONFIG_107**: configuración de límite: recuento máximo de llamadas no válido (maxCallsCount)
* **ERR_ENDPOINTCONFIG_108**: configuración de límite: recuento máximo de llamadas no válido (periodInMs)
* **ERR_ENDPOINTCONFIG_111**: configuración de límite: no se puede crear la configuración de extremo: carga útil no válida
* **ERR_ENDPOINTCONFIG_112**: configuración de límite: no se puede crear la configuración de extremo: esperando una carga útil JSON
* **ERR_AUTHORING_ENDPOINTCONFIG_1**: nombre de servicio no válido `<!--<given value>-->`: debe ser &#39;dataSource&#39; o &#39;action&#39;

La advertencia potencial es:

**ERR_ENDPOINTCONFIG_106**: configuración de límite: máximo de conexiones HTTP no definidas: sin limitación de forma predeterminada

## Casos de uso

En esta sección se enumeran los casos de uso clave para administrar las configuraciones de límite en [!DNL Journey Optimizer] y los comandos de API asociados necesarios para implementar el caso de uso.

Encontrará detalles sobre cada comando de API en [Descripción de la API y recopilación de Postman](#description).

+++Cree e implemente una nueva configuración de límite

Llamadas de API para utilizar:

1. **`list`** - Recupera configuraciones existentes.
1. **`create`** - Crea una nueva configuración.
1. **`candeploy`**: comprueba si se puede implementar la configuración.
1. **`deploy`** - Implementa la configuración.

+++

+++Actualizar e implementar una configuración de límite (aún no implementada)

Llamadas de API para utilizar:

1. **`list`** - Recupera configuraciones existentes.
1. **`get`**: obtiene detalles de una configuración específica.
1. **`update`** - Modifica la configuración.
1. **`candeploy`** - Comprueba la idoneidad de la implementación.
1. **`deploy`** - Implementa la configuración.

+++

+++Anule la implementación y elimine una configuración de límite implementada

Llamadas de API para utilizar:

1. **`list`** - Recupera configuraciones existentes.
1. **`undeploy`** - Anula la implementación de la configuración.
1. **`delete`** - Quita la configuración.

+++

+++Elimine una configuración de límite implementada en un paso

Solo en una llamada de API puede anular la implementación y eliminar la configuración con el parámetro `forceDelete`.

Llamadas de API para utilizar:

1. **`list`** - Recupera configuraciones existentes.
1. **`delete`(con `forceDelete` parámetro)** - Fuerza la eliminación de una configuración implementada en un solo paso.

+++

+++Actualizar una configuración de límite ya implementada

>[!NOTE]
>
>Se requiere una nueva implementación después de actualizar una configuración ya implementada.

Llamadas de API para utilizar:
1. **`list`** - Recupera configuraciones existentes.
1. **`get`**: obtiene detalles de una configuración específica.
1. **`update`** - Modifica la configuración.
1. **`undeploy`**: anula la implementación de la configuración antes de aplicar los cambios.
1. **`candeploy`** - Comprueba la idoneidad de la implementación.
1. **`deploy`** - Implementa la configuración actualizada.

+++
