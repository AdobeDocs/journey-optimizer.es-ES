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
source-git-commit: fd89412703d015fa173f58fa117f65323b954fec
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 25%

---

# Uso de la API de límite {#work}

La API de límite le ayuda a crear, configurar y supervisar sus configuraciones de límite.

Esta sección proporciona información global sobre cómo trabajar con la API. Hay disponible una descripción detallada de la API en [Documentación de las API de Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/).

## Descripción de API de límite

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

### Por ejemplo:

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

En esta sección, encontrará los cinco casos de uso principales que puede realizar para administrar la configuración de límite en [!DNL Journey Optimizer].

Para ayudarle en las pruebas y la configuración, hay una colección de Postman disponible [aquí](https://github.com/AdobeDocs/JourneyAPI/blob/master/postman-collections/Journeys_Capping-API_postman-collection.json).

Esta colección de Postman se ha configurado para compartir la colección de variables de Postman generada mediante __[Integraciones de la consola de Adobe I/O](https://console.adobe.io/integrations) > Pruébelo > Descargar para Postman__, que genera un archivo de entorno de Postman con los valores de integraciones seleccionados.

Una vez descargado y cargado en Postman, debe añadir tres variables: `{JO_HOST}`,`{BASE_PATH}` y `{SANDBOX_NAME}`.
* `{JO_HOST}`: URL de puerta de enlace de [!DNL Journey Optimizer]
* `{BASE_PATH}` : punto de entrada para la API.
* `{SANDBOX_NAME}`: el encabezado **x-sandbox-name** (por ejemplo, “prod”) correspondiente al nombre de la zona protegida donde se realizarán las operaciones de API. Consulte la [información general sobre las zonas protegidas](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=es) para obtener más detalles.

En la siguiente sección, encontrará la lista ordenada de llamadas a la API de REST para ejecutar el caso de uso.

Caso de uso n.º 1: **Creación e implementación de una nueva configuración de límite**

1. list
1. create
1. candeploy
1. deploy

Caso de uso n.º 2: **Actualizar e implementar una configuración de límite aún no implementada**

1. list
1. get
1. update
1. candeploy
1. deploy

Caso de uso n.º 3: **Anule la implementación y elimine una configuración de límite implementada**

1. list
1. undeploy
1. delete

Caso de uso n.º 4: **Eliminar una configuración de límite implementada.**

En una sola llamada de API, puede anular la implementación y eliminar la configuración con el uso del parámetro forceDelete.
1. list
1. eliminar, con el parámetro forceDelete

Caso de uso n.º 5: **Actualizar una configuración de límite ya implementada**

>[!NOTE]
>
>Debe volver a implementar si actualiza una configuración ya implementada.

1. list
1. get
1. update
1. undeploy
1. candeploy
1. deploy
