---
title: API de migración de decisiones
description: Aprenda a utilizar la API del servicio de migración de decisiones para migrar objetos de administración de decisiones entre entornos limitados con resolución de dependencias automatizada y compatibilidad con reversiones.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
source-git-commit: 398d4c2ab3a2312a0af5b8ac835f7d1f49a61b5b
workflow-type: tm+mt
source-wordcount: '1154'
ht-degree: 4%

---


# API de migración de decisiones {#decisioning-migration-api}

La API del servicio de migración de decisiones permite migrar objetos de administración de decisiones de una zona protegida a otra. El proceso de migración se ejecuta como flujos de trabajo asincrónicos que incluyen análisis de dependencia, ejecución y funciones de reversión opcionales.

Esta API le permite realizar una transición sin problemas del contenido de toma de decisiones entre entornos (por ejemplo, de desarrollo a ensayo o de ensayo a producción) a la vez que mantiene la integridad de los datos y las relaciones.

Para obtener más información sobre las ventajas y capacidades de la toma de decisiones en comparación con la administración de decisiones, consulte [esta página](migrate-to-decisioning.md).

## Competencias {#capabilities}

La API del servicio de migración de Decisioning proporciona las siguientes funcionalidades:

* **Análisis de dependencias**: identifique todas las dependencias necesarias entre los entornos limitados de origen y destino, incluidos atributos, segmentos y requisitos de conjuntos de datos.
* **Ámbito de migración flexible**: ejecute migraciones en el nivel de zona protegida, oferta o decisión según sus necesidades.
* **Compatibilidad con reversiones**: revierta una migración completada si se detectan problemas durante la validación.

## Requisitos previos {#prerequisites}

### Permisos necesarios {#permissions}

Para utilizar la API de migración, necesita los permisos adecuados en los entornos limitados de origen y destino:

**Entorno aislado de Source**: acceso de lectura a los objetos de administración de decisiones

**Entorno aislado de Target**: cree y edite el acceso a los objetos de Decisioning

Los permisos habituales incluyen:

* Administrar/Ver decisión
* Administrar/Ver decisiones
* Administración de ofertas
* Administrar estrategias de clasificación
* Administrar campañas (si se migran artefactos relacionados con campañas)
* Administrar/Ver flujos de datos (si se crea un flujo de datos)
* Administrar/Ver esquemas

>[!NOTE]
>
>Aprenda a asignar permisos de toma de decisiones en [esta sección](gs-experience-decisioning.md#steps). Para obtener la lista completa de permisos, consulte la página [Permisos integrados](../administration/ootb-permissions.md#ootb-permissions).

### Preparación de la zona protegida de Target {#target-sandbox-preparation}

Antes de ejecutar una migración, asegúrese de que la zona protegida de Target esté configurada correctamente:

* **Atributos**: compruebe que existan los atributos de perfil y los atributos de contexto necesarios en la zona protegida de destino o prepare asignaciones para ellos.
* **Segmentos**: compruebe que existan los segmentos necesarios en la zona protegida de destino o planee asignarlos mediante el área de nombres y el ID.
* **Conjunto de datos**: identifique un nombre de conjunto de datos para usar en la migración (`dependency.datasetName`).
* **Flujo de datos** - Decida si la migración debe crear un flujo de datos (`createDataStream`).

Para obtener más información sobre la administración de zonas protegidas, consulte [Usar y asignar zonas protegidas](../administration/sandboxes.md).

## Conceptos básicos de la API {#api-basics}

### Direcciones URL base {#base-urls}

Utilice las siguientes direcciones URL base según su entorno:

* **Producción**: `https://platform.adobe.io`
* **Ensayo**: `https://platform-stage.adobe.io`

### Autenticación {#authentication}

Todas las solicitudes de API requieren los siguientes encabezados:

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `x-api-key: <CLIENT_API_KEY>`
* `Content-Type: application/json`

Para obtener instrucciones detalladas sobre cómo configurar la autenticación, consulte la [guía de autenticación de Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

### Modelo de flujo de trabajo {#workflow-model}

Cada llamada de API crea o recupera un recurso de flujo de trabajo. Los flujos de trabajo son operaciones asincrónicas que realizan un seguimiento del progreso y los resultados de las tareas de migración.

Un flujo de trabajo tiene las siguientes propiedades:

* `id` - Identificador único de flujo de trabajo (UUID)
* `status` - Estado actual del flujo de trabajo: `New`, `Running`, `Completed`, `Failed` o `Cancelled`
* `result`: salida del flujo de trabajo cuando se completa (incluye resultados de migración y advertencias)
* `errors`: detalles de error estructurados cuando se produjo un error
* `_etag`: identificador de versión utilizado para operaciones de eliminación (solo usuarios de servicio)
* `_links.self`: URL de flujo de trabajo para recuperar el estado

## Flujo de trabajo migración {#migration-workflow}

El proceso de migración consta de dos pasos principales: analizar las dependencias y ejecutar la migración. Siga estos pasos para garantizar una migración correcta.

### Paso 1: Análisis de dependencias {#analyze-dependencies}

Antes de migrar, utilice el flujo de trabajo de dependencias para identificar qué debe asignarse desde Gestión de decisiones a Decisiones en la zona protegida de destino. Este análisis le ayuda a comprender las relaciones entre los objetos y a preparar las asignaciones necesarias.

#### Creación de un flujo de trabajo de dependencias {#create-dependency-workflow}

Utilice la siguiente llamada de API para crear un flujo de trabajo de análisis de dependencias.

**Formato de API**

```http
POST /migration/service/dependency
```

**Dependencia a nivel de espacio aislado (recomendada primero)**

Comience con un análisis a nivel de zona protegida para obtener una vista completa de todas las dependencias:

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/dependency" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "requestLevel": "sandbox"
  }'
```

**Dependencia de nivel de oferta**

Para analizar solamente las dependencias de ofertas específicas, establezca `requestLevel: "offer"` y proporcione una matriz `offersList` con los identificadores de oferta que desee analizar.

**Dependencia de nivel de decisión**

Para analizar solamente las dependencias para decisiones específicas, establezca `requestLevel: "decision"` y proporcione una matriz `decisionsList` con los identificadores de decisión que desee analizar.

#### Comprobar estado de flujo de trabajo de dependencia {#poll-dependency-status}

Encueste el flujo de trabajo de dependencias para comprobar cuándo se ha completado el análisis.

**Formato de API**

```http
GET /migration/service/dependency/{id}
```

**Solicitud**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/dependency/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

Cuando el campo `status` muestra `Completed`, el análisis de dependencias está listo. Utilice la salida del flujo de trabajo para crear las asignaciones de dependencias de migración:

* **profileAttributeDependency**: asigna atributos de perfil de origen a atributos de perfil de destino
* **contextAttributeDependency**: asigna atributos de contexto de origen a atributos de contexto de destino
* **segmentsDependency**: asigna claves de segmento de origen a identificadores de segmento de destino (`{segmentNamespace, segmentId}`)
* **datasetName**: especifica el nombre del conjunto de datos de destino para la migración

### Paso 2: Ejecución de la migración {#execute-migration}

Una vez que haya analizado las dependencias y preparado las asignaciones, puede ejecutar la migración.

#### Creación de un flujo de trabajo de migración {#create-migration-workflow}

Utilice las asignaciones de dependencias del paso 1 para configurar y ejecutar la migración.

**Formato de API**

```http
POST /migration/service/migrations
```

**Migración a nivel de espacio aislado**

Para migrar todos los objetos de toma de decisiones de una zona protegida a otra:

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/migrations" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributeDependency": {
        "sourceAttr1": "targetAttr1"
      },
      "segmentsDependency": {
        "sourceSegmentKey1": {
          "segmentNamespace": "<TARGET_SEGMENT_NAMESPACE>",
          "segmentId": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributeDependency": {
        "sourceCtx1": "targetCtx1"
      },
      "datasetName": "<TARGET_DATASET_NAME>"
    },
    "requestLevel": "sandbox"
  }'
```

**Migración de nivel de oferta**

Para migrar solo ofertas específicas, use `requestLevel: "offer"` y agregue una matriz `offersList`:

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**Migración de nivel de decisión**

Para migrar únicamente decisiones específicas, use `requestLevel: "decision"` y agregue una matriz `decisionsList`:

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

#### Monitorización del estado de migración {#poll-migration-status}

Encueste el flujo de trabajo de migración para rastrear su progreso.

**Formato de API**

```http
GET /migration/service/migrations/{id}
```

**Solicitud**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/migrations/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

**Resultados de la migración**

Cuando el campo `status` muestra `Completed`, la migración se realizó correctamente. El flujo de trabajo `result` incluye:
* Asignaciones de objetos migrados
* Advertencias encontradas durante la migración

Cuando el campo `status` muestre `Failed`, revise la matriz `errors[]` y el campo `result.error` para obtener detalles sobre qué ha fallado.

## Validación de la migración {#validate-migration}

Una vez completada la migración correctamente, compruebe que todos los objetos se hayan migrado correctamente.

### Lista de comprobación de validación {#validation-checklist}

1. **Segmentos**: compruebe que todos los segmentos a los que se hace referencia se resuelven correctamente en la zona protegida de destino según sus asignaciones.
2. **Atributos**: confirme que todos los atributos de perfil y de contexto existen en la zona protegida de destino y están asignados correctamente.
3. **Objetos de toma de decisiones** - Revisar objetos migrados en la interfaz de usuario de Journey Optimizer:
   * Ofertas (elementos de decisión)
   * Reglas de elegibilidad
   * Fórmulas de clasificación
   * Estrategias de selección
   * Políticas de decisión
4. **Prueba de secuencia de datos**: si se creó una secuencia de datos, pruebe la entrega en tiempo de ejecución mediante la API de Edge Interact.

### Ejemplo {#test-runtime-delivery}

Si la migración ha creado un conjunto de datos, se puede probar la entrega de ofertas con el siguiente ejemplo:

```shell
curl --request POST \
  --url "https://edge.adobedc.net/ee/or2/v1/interact?configId=<DATASTREAM_ID>" \
  --header "Content-Type: application/json" \
  --header "x-request-id: <uuid>" \
  --data '{ "events": [ ... ] }'
```

## Reversión de una migración {#rollback}

Si detecta problemas durante la validación, puede revertir una migración completada para restaurar la zona protegida de destino a su estado anterior.

### Creación de un flujo de trabajo de reversión {#create-rollback-workflow}

Inicie una reversión creando un flujo de trabajo de reversión que haga referencia a la migración que desea revertir.

**Formato de API**

```http
POST /migration/service/rollbacks/{migrationWorkflowId}
```

Reemplace `{migrationWorkflowId}` por el ID del flujo de trabajo de migración que desea revertir.

**Solicitud**

```shell
curl --request POST \
  --url "https://platform.adobe.io/migration/service/rollbacks/<MIGRATION_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

### Monitorizar estado de reversión {#poll-rollback-status}

Encuesta el flujo de trabajo de reversión para rastrear su progreso.

**Formato de API**

```http
GET /migration/service/rollbacks/{rollbackWorkflowId}
```

**Solicitud**

```shell
curl --request GET \
  --url "https://platform.adobe.io/migration/service/rollbacks/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "x-api-key: <CLIENT_API_KEY>"
```

## Gestión de flujos de trabajo simultáneos {#handle-concurrency}

La API de migración solo permite ejecutar un flujo de trabajo a la vez por organización. Si intenta crear un nuevo flujo de trabajo mientras otro está en curso, recibirá una respuesta de error **409 Conflict** (&quot;Ya hay un flujo de trabajo en curso...&quot;).

En este caso, espere a que se complete el flujo de trabajo en curso o recupere el ID de flujo de trabajo y sondee su estado. Una vez finalizado el flujo de trabajo actual, puede crear uno nuevo.

## Referencia de asignación de entidad {#entity-mapping}

Al migrar de Administración de decisiones a Toma de decisiones, las entidades se asignan de la siguiente manera:

| Gestión de decisiones | Toma de decisiones |
|-------------------|-------------|
| Oferta | Elemento de decisión |
| Colección de ofertas | Colección de elementos |
| Regla de elegibilidad | Regla de elegibilidad |
| Fórmula de clasificación | Fórmula de clasificación |
| Decisión | Estrategia de selección + Política de decisión |
| Campaign | Campaña *(solo contenido básico)* |
| Ubicación | Configuración de superficie + canal |
| Etiqueta | Etiqueta unificada |

## Limpieza de flujo de trabajo {#cleanup}

Los usuarios del servicio solo pueden eliminar los recursos de flujo de trabajo. Las operaciones de eliminación requieren un encabezado `If-Match` con el valor `_etag` del flujo de trabajo.

**Operaciones de eliminación disponibles:**

* `DELETE /migration/service/dependency/{id}`
* `DELETE /migration/service/migrations/{id}`
* `DELETE /migration/service/rollbacks/{id}`

>[!NOTE]
>
>La eliminación del flujo de trabajo solo está disponible para las cuentas de servicio con los permisos adecuados. Si necesita eliminar un recurso de flujo de trabajo, póngase en contacto con el administrador del sistema.

## Temas relacionados {#related-topics}

* [Migrar de Administración de decisiones a Toma de decisiones](migrate-to-decisioning.md): comprenda los beneficios y capacidades de migrar a Toma de decisiones
* [Introducción a la toma de decisiones](gs-experience-decisioning.md)
* [Limitaciones y protecciones de decisiones](decisioning-guardrails.md)
* [Comenzar con API de Decisioning](api-reference/getting-started.md)
