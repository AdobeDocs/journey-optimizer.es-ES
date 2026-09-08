---
title: API de migración de la toma de decisiones
description: Aprenda a utilizar la API del servicio de migración de decisiones para migrar objetos de administración de decisiones entre entornos limitados con resolución de dependencias automatizada y compatibilidad con reversiones.
feature: Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 3ec084ca-af9e-4b5e-b66f-ec390328a9d6
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 02ff2d2090fd2271c3b6ffc0832ff66b9fd0f0b7
workflow-type: tm+mt
source-wordcount: 3211
ht-degree: 3%

---

# API de migración de la toma de decisiones {#decisioning-migration-api}

>[!BEGINSHADEBOX]

**En esta página:** Utilice la API del servicio de migración de decisiones para mover objetos de administración de decisiones entre zonas protegidas con análisis de dependencia automatizado y compatibilidad con reversiones, de modo que pueda realizar la transición del contenido de las decisiones entre entornos preservando al mismo tiempo la integridad de los datos.

>[!ENDSHADEBOX]

La API del servicio de migración de decisiones permite migrar objetos de administración de decisiones de una zona protegida a otra. El proceso de migración se ejecuta como flujos de trabajo asincrónicos que incluyen análisis de dependencia, ejecución y funciones de reversión opcionales.

Esta API le permite realizar una transición sin problemas del contenido de toma de decisiones entre entornos <!--(e.g., from development to staging, or staging to production) -->, manteniendo la integridad de los datos y las relaciones.

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

>[!NOTE]
>
>La zona protegida de destino puede ser la misma que la de origen. El proceso de migración gestiona este escenario y garantiza la integridad de los datos independientemente de si los objetos se migran dentro de la misma zona protegida o a una diferente.

### Requisitos previos de migración entre zonas protegidas {#cross-sandbox-prerequisites}

Cuando la zona protegida de origen ≠ la de destino, se requieren los siguientes elementos:

* **Atributos de perfil**: debe existir en la zona protegida de destino o tener asignaciones predefinidas
* **ID de segmento**: debe crearse previamente en la zona protegida de destino con asignaciones → ID antiguas y nuevas
* **Asignación de identidad**: debe configurarse para obtener una resolución de identidad coherente

## Conceptos básicos de la API {#api-basics}

### URL base {#base-url}

Utilice la siguiente URL base:

* **Producción**: `https://decisioning-migration.adobe.io`

### Autenticación {#authentication}

Todas las solicitudes de API requieren los siguientes encabezados:

* `Authorization: Bearer <IMS_ACCESS_TOKEN>`
* `x-gw-ims-org-id: <IMS_ORG_ID>`
* `Content-Type: application/json`

Para obtener instrucciones detalladas sobre cómo configurar la autenticación, consulte la [guía de autenticación de Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

## Flujo de trabajo migración {#migration-workflow}

El proceso de migración consta de dos pasos principales: analizar las dependencias y ejecutar la migración. Siga estos pasos para garantizar una migración correcta.

### Paso 1: Análisis de dependencias {#analyze-dependencies}

Antes de migrar, utilice el flujo de trabajo de dependencias para identificar qué debe asignarse desde Gestión de decisiones a Decisiones en la zona protegida de destino. Este análisis le ayuda a comprender las relaciones entre los objetos y a preparar las asignaciones necesarias.

#### Creación de un flujo de trabajo de dependencias {#create-dependency-workflow}

Utilice la siguiente llamada de API para crear un flujo de trabajo de análisis de dependencias.

**Formato de API**

```http
POST /workflows/generate-dependencies
```

**Dependencia a nivel de espacio aislado (recomendada primero)**

Comience con un análisis a nivel de zona protegida para obtener una vista completa de todas las dependencias:

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies?request-level=sandbox" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" }
  }'
```

**Dependencia de nivel de oferta**

Para analizar dependencias solo para ofertas específicas, llame al mismo extremo con `request-level=offer` en la cadena de consulta y proporcione una matriz `offersList` en el cuerpo con los ID de oferta que desee analizar.

**Dependencia de nivel de decisión**

Para analizar dependencias únicamente para decisiones específicas, use `request-level=decision` en la cadena de consulta y proporcione una matriz `decisionsList` en el cuerpo con los identificadores de decisión que desee analizar.

#### Comprobar estado de flujo de trabajo de dependencia {#poll-dependency-status}

Encueste el flujo de trabajo de dependencias para comprobar cuándo se ha completado el análisis.

**Formato de API**

```http
GET /workflows/generate-dependencies/{id}
```

**Solicitud**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/generate-dependencies/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

Cuando el campo `status` muestra `Completed`, el análisis de dependencias está listo. Utilice la salida del flujo de trabajo para crear las asignaciones de dependencias de migración:

* **profileAttributes**: asigna atributos de perfil de origen a atributos de perfil de destino
* **contextAttributes**: asigna atributos de contexto de origen a atributos de contexto de destino
* **segmentos**: asigna cada clave de segmento de origen a un identificador de segmento de destino (`{namespace, id}`)
* **datasetName**: el conjunto de datos de evento de experiencia de destino utilizado para la migración. Debe adjuntarse a un conjunto de datos habilitado para las llamadas de Journey Optimizer Edge (Web SDK); su esquema se utiliza para agregar los atributos de contexto migrados.

Proporcione estas asignaciones en el objeto `dependency` de la solicitud de migración en el paso 2.

### Paso 2: Ejecución de la migración {#execute-migration}

Una vez que haya analizado las dependencias y preparado las asignaciones, puede ejecutar la migración.

#### Creación de un flujo de trabajo de migración {#create-migration-workflow}

Utilice las asignaciones de dependencias del paso 1 para configurar y ejecutar la migración.

**Formato de API**

```http
POST /workflows/migration
```

**Migración a nivel de espacio aislado**

Para migrar todos los objetos de toma de decisiones de una zona protegida a otra:

```shell
curl --request POST \
  --url 'https://decisioning-migration.adobe.io/workflows/migration?request-level=sandbox' \
  --header 'Authorization: Bearer <IMS_ACCESS_TOKEN>' \
  --header 'Content-Type: application/json' \
  --header 'x-gw-ims-org-id: <IMS_ORG_ID>' \
  --data '{
    "imsOrgId": "<IMS_ORG_ID>",
    "sourceSandboxDetails": { "sandboxName": "<SOURCE_SANDBOX_NAME>" },
    "targetSandboxDetails": { "sandboxName": "<TARGET_SANDBOX_NAME>" },
    "createDataStream": true,
    "dependency": {
      "profileAttributes": {
        "sourceAttr1": "targetAttr1"
      },
      "segments": {
        "sourceSegmentKey1": {
          "namespace": "<TARGET_SEGMENT_NAMESPACE>",
          "id": "<TARGET_SEGMENT_ID>"
        }
      },
      "contextAttributes": {
        "sourceCtx1": "targetCtx1"
      },
      "datasetName": "<TARGET_DATASET_NAME>"
    }
  }'
```

**Migración de nivel de oferta**

Para migrar solamente ofertas específicas, use `request-level=offer` en la cadena de consulta y agregue una matriz `offersList` al cuerpo:

```json
"offersList": ["offer-id-1", "offer-id-2"]
```

**Migración de nivel de decisión**

Para migrar únicamente decisiones específicas, use `request-level=decision` en la cadena de consulta y agregue una matriz `decisionsList` al cuerpo:

```json
"decisionsList": ["decision-id-1", "decision-id-2"]
```

**Campos de solicitud**

* **nivel de solicitud** (consulta) - Ámbito de migración: `sandbox`, `offer` o `decision`.
* **imsOrgId** (obligatorio): su ID de organización de IMS.
* **sourceSandboxDetails.sandboxName** (requerido): zona protegida de Source que contiene entidades de Administración de decisiones.
* **targetSandboxDetails.sandboxName** (requerido): zona protegida de Target donde se crean las entidades de Decisioning.
* **dependencies.datasetName** (obligatorio): conjunto de datos de evento de experiencia de Target. Debe adjuntarse a un conjunto de datos habilitado para las llamadas de Journey Optimizer Edge (Web SDK); su esquema se utiliza para agregar los atributos de contexto migrados.
* **createDataStream** - `true` crea un nuevo conjunto de datos habilitado para Journey Optimizer; `false` vuelve a utilizar el que ya está adjunto al conjunto de datos en `dependency.datasetName`.
* **dependencies.profileAttributes**: asignación de atributos de perfil de origen → destino.
* **dependencies.contextAttributes**: asignación de atributos de contexto de origen → destino.
* **dependencies.segments**: asignación de la clave de segmento de origen → segmento de destino (`{namespace, id}`).
* **offersList[]** / **decisionsList[]**: los identificadores de oferta o decisión que se van a migrar; necesarios cuando `request-level` es `offer` o `decision` respectivamente.

#### Monitorización del estado de migración {#poll-migration-status}

Encueste el flujo de trabajo de migración para rastrear su progreso.

**Formato de API**

```http
GET /workflows/migration/{id}
```

**Solicitud**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/migration/<WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

**Resultados de la migración**

Cuando el campo `status` muestra `Completed`, la migración se realizó correctamente. El flujo de trabajo `result` incluye:
* Asignaciones de objetos migrados
* Advertencias encontradas durante la migración

Cuando el campo `status` muestre `Failed`, revise la matriz `errors[]` y el campo `result.error` para obtener detalles sobre qué ha fallado.

Cada flujo de trabajo (dependencia, migración y reversión) devuelve los mismos campos de recurso:

* **id** - Identificador de flujo de trabajo (UUID); sondear su estado con el `GET /{id}` coincidente.
* **estado** - Estado del ciclo de vida: `New`, `Running`, `Completed` o `Failed`.
* **result** - Presente en `Completed`; la salida del flujo de trabajo (por ejemplo, asignaciones de objetos migrados y advertencias).
* **errores[]** - Presentes en `Failed`; detalles de error estructurados (véase también `result.error`).
* **_links.self**: URL del recurso de flujo de trabajo.

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
POST /workflows/rollback
```

**Solicitud**

```shell
curl --request POST \
  --url "https://decisioning-migration.adobe.io/workflows/rollback" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>" \
  --header "Content-Type: application/json" \
  --data '{ "rollbackWorkflowId": "<MIGRATION_WORKFLOW_ID>" }'
```

Reemplace `<MIGRATION_WORKFLOW_ID>` por el ID del flujo de trabajo de migración que desea revertir.

### Monitorizar estado de reversión {#poll-rollback-status}

Encuesta el flujo de trabajo de reversión para rastrear su progreso.

**Formato de API**

```http
GET /workflows/rollback/{rollbackWorkflowId}
```

**Solicitud**

```shell
curl --request GET \
  --url "https://decisioning-migration.adobe.io/workflows/rollback/<ROLLBACK_WORKFLOW_ID>" \
  --header "Authorization: Bearer <IMS_ACCESS_TOKEN>" \
  --header "x-gw-ims-org-id: <IMS_ORG_ID>"
```

## Gestión de flujos de trabajo simultáneos {#handle-concurrency}

La API de migración solo permite ejecutar un flujo de trabajo a la vez por organización. Si intenta crear un nuevo flujo de trabajo mientras otro está en curso, recibirá una respuesta de error **409 Conflict** (&quot;Ya hay un flujo de trabajo en curso...&quot;).

En este caso, espere a que se complete el flujo de trabajo en curso o recupere el ID de flujo de trabajo y sondee su estado. Una vez finalizado el flujo de trabajo actual, puede crear uno nuevo.

## Alcance y cobertura de la migración {#migration-scope}

Comprender el ámbito de la migración le ayuda a planificar y validar la transición de la gestión de decisiones a la toma de decisiones. En esta sección se describe qué cubre el proceso de migración y qué requiere una acción manual.

### En el ámbito: Aspectos cubiertos {#in-scope}

La API de migración gestiona los siguientes elementos y funcionalidades:

* **Casos de uso**: solo los casos de uso de decisiones de entrada/Edge están en el ámbito. La migración saliente o OD del canal de correo electrónico de Journey Optimizer es compatible, pero requiere actualizaciones manuales.
* **Campañas de experiencias basadas en código**: creadas automáticamente durante la migración, una campaña por ámbito de decisión migrado en la zona protegida de Target.
* **Configuración/Superficie de canal**: configuraciones/superficies de canal creadas por cada ubicación de Administración de decisiones, lo que garantiza el enrutamiento adecuado de las respuestas de toma de decisiones.
* **Tipos de contenido de ofertas**: las ofertas solo se migran si su tipo de contenido es JSON o Texto. Otros tipos de contenido requieren una recreación manual.
* **Características de la oferta** - Conservadas en el grupo de campos `offer_item_custom_attributes` del esquema &quot;Elementos de oferta personalizados - Experience Decisioning&quot;, manteniendo los metadatos personalizados.
* **Atributos de contexto** - Se agregó al esquema de Evento de experiencia en el grupo de campos `custom_context_attributes` para seguimiento y personalización.
* **Ámbitos de decisión**: un ámbito de decisión de administración de decisiones se asigna a una estrategia de selección + una directiva de decisión + una campaña en Toma de decisiones, lo que garantiza la jerarquía de entidades adecuada.
* **Reglas de elegibilidad solo de API**: las reglas de elegibilidad creadas solamente a través de API (no en la IU de Administración de decisiones) se migran y permanecen solo de API en Decisioning. Las reglas creadas por la interfaz de usuario también se migran.

### Fuera del ámbito: elementos que no están cubiertos o que requieren una acción manual {#out-of-scope}

Los siguientes elementos requieren una acción manual o no son compatibles con las herramientas de migración:

* **Posiciones de decisión**: la herramienta de migración no crea ninguna ubicación. Debe crearlos manualmente en Decisioning antes o después de la migración en función de su arquitectura.
* **Límite de nivel de ubicación** - El límite de frecuencia de nivel de ubicación no se migra.
* **Contenido de ofertas no JSON/de texto**: las ofertas con tipos de contenido que no sean JSON o de texto (por ejemplo, HTML, imágenes) NO se migran y requieren recreación manual en Decisioning.
* **Atributos de perfil y segmentos**: las herramientas de migración NUNCA crean ni editan atributos de perfil ni suscripciones a segmentos. Deben existir en la zona protegida de Target antes de ejecutar la migración.
* **Asignación de ID de segmento**: los ID de segmento deben crearse previamente en la zona protegida de destino. Debe proporcionar una asignación de ID antigua→nueva en la solicitud de API de migración para la resolución de segmentos.
* **Cambios en el código de recopilación de datos**: los cambios en el código de seguimiento de eventos del lado del cliente y del lado del servidor NO están automatizados. El equipo de implementación debe actualizar la colección de eventos para utilizar los formatos de solicitud/respuesta de Decisioning y los esquemas de eventos de decisión.

## Referencia de asignación de entidad {#entity-mapping}

Al migrar de Administración de decisiones a Toma de decisiones, las entidades se asignan según la siguiente tabla. Las asignaciones incluyen las entidades Decisioning principales y las entidades asociadas adicionales creadas o utilizadas durante la migración.

### Administración de decisiones para la asignación de entidades de decisiones

| Entidad de gestión de decisiones | Entidad de toma de decisiones | Entidades adicionales |
|-----------|--------------|-------------------|
| Decisión | Estrategia de selección | Recopilación de artículos, Regla de idoneidad, Fórmula de clasificación |
| | Política de decisión | Recuento de elementos, estrategias de selección, elemento de oferta de reserva |
| | Campaña de experiencia basada en código | Política de decisión, Contenido, Configuración de canal, Fragmentos de Journey Optimizer |
| Ubicación | Configuración de canal | — |
| Colección | Colección de elementos | Etiquetas Unificadas, Elementos De Oferta |
| Calificador de colección | Etiquetas unificadas | — |
| Regla | Regla de toma de decisiones | — |
| Fórmula de clasificación | Fórmula de clasificación de decisiones | — |
| Oferta | Artículo de oferta | Regla De Idoneidad, Fragmentos De Journey Optimizer, Etiquetas Unificadas, Límite De Frecuencia |
| | Esquema de elemento de oferta | — |
| | Fragmentos de Journey Optimizer | — |

### Convenciones de nomenclatura

El proceso de migración aplica convenciones de nomenclatura utilizando el prefijo `ExD_` para garantizar la coherencia y evitar conflictos de nomenclatura.

| Objeto Source | Patrón de nombre de administración de decisiones | Patrón de nombre de decisión |
|---------------|-----------------|-------------------|
| Oferta | `<offerName>` | `ExD_<offerName>` |
| Regla de elegibilidad | `<ruleName>` | `ExD_<ruleName>` |
| Fórmula de clasificación | `<formulaName>` | `ExD_<formulaName>` |
| Colección | `<collectionName>` | `ExD_<collectionName>_<placementName>` |
| Estrategia de selección de → de decisión | `<decisionName>` | `ExD_<decisionName>_selection_strategy_<index>` |
| Decisión → política de decisión | `<decisionName>` | `ExD_<decisionName>_<placementName>` |
| Fragmento de Journey Optimizer | `<offerName>` | `ExD_<offerName>_<placementName>_<index>` |
| Superficie de → de posición | `<placementName>` | `ExD_<placementName>` *(espacios/puntos convertidos en guiones bajos)* |
| Etiqueta unificada | `<sourceName>, <targetName>` | `ExDMigration_<sourceName>_<targetName>` |
| Campaña CBE | `<decisionName>, <placementName>` | `Campaign for <decisionName> : <placementName>` |

### Atributos adicionales

| Atributo Source | Ubicación de destino |
|-----------------|-----------------|
| Atributos de oferta | Campo &quot;migratedofferattributes&quot; en el esquema de elemento de oferta personalizada |
| Atributos de contexto | campo &quot;migratedcontextattributes&quot; en el esquema adjunto al conjunto de datos proporcionado durante la migración |

## Modelo de solicitud y respuesta {#request-response-model}

Al migrar de Administración de decisiones a Toma de decisiones, el código de la aplicación debe actualizarse para utilizar los nuevos formatos de solicitud y respuesta. Ambos sistemas utilizan el extremo de Edge Network, pero con diferentes estructuras de carga útil y nombres de campo.

### Solicitud Edge de gestión de decisiones (actual) {#dm-request}

La solicitud de Edge actual de Administración de decisiones sigue esta estructura:

**Punto final:**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**Encabezados:**
&#x200B;- `Authorization: Bearer <IMS_ACCESS_TOKEN>`
&#x200B;- `x-api-key: <API_KEY>` (de Developer Console)
&#x200B;- `x-gw-ims-org-id: <IMS_ORG_ID>` (formato: `{ORG_ID}@AdobeOrg`)
&#x200B;- `x-request-id: <UNIQUE_REQUEST_ID>` (para seguimiento y deduplicación)
&#x200B;- `Content-Type: application/vnd.adobe.xdm+json; schema="…/decision-request;version=1.0"`
&#x200B;- `Accept: application/vnd.adobe.xdm+json; schema="…/decision-response;version=1.0"`
&#x200B;- `x-sandbox-name: <SANDBOX_NAME>` (por ejemplo, prod, dev)

**Parámetros de cuerpo de solicitud:**
&#x200B;- `xdm:dryRun` (true/false): solicitudes de prueba sin informes contaminantes
&#x200B;- `xdm:propositionRequests[]` - Matriz de solicitudes de decisión:
  &#x200B;- `activityId` - Identificador de actividad de decisión
  &#x200B;- `placementId` - Identificador de ubicación
  &#x200B;- `itemCount`: número máximo de ofertas que se devolverán
&#x200B;- `xdm:profiles[].xdm:identityMap`: asignación de identidad (correo electrónico, ECID, etc.)
&#x200B;- `xdm:validateContextData` - Indicador de validación de datos de contexto estricto
&#x200B;- `xdm:responseFormat.xdm:includeContent`: incluir contenido real frente a solo ID

**Cuerpo de solicitud de ejemplo:**

```json
{
  "xdm": {
    "dryRun": false,
    "propositionRequests": [
      { "activityId": "<ACTIVITY_ID>", "placementId": "<PLACEMENT_ID>", "itemCount": 3 }
    ],
    "profiles": [
      { "identityMap": { "ECID": [ { "id": "<ECID>", "primary": true } ] } }
    ],
    "validateContextData": true,
    "responseFormat": { "includeContent": true }
  }
}
```

>[!NOTE]
>Para obtener la referencia completa de solicitud/respuesta de Administración de decisiones (OD), consulte la [API de Edge Decisioning](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/decisioning/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api) (la variante de Web SDK/Edge, que usa `decisionScopes` con codificación base64 que lleva `activityId` y `placementId`).

### Decisión de una solicitud de Edge (después de la migración) {#decisioning-request}

Después de la migración, utilice el formato de solicitud de Decisioning a través del mismo punto de conexión de Edge Network.

**Punto final:**

```
POST https://edge.adobedc.net/ee/v2/interact
```

**Campos de solicitud de clave:**
&#x200B;- `query.identity.fetch`: matriz de tipos de identidad para resolver (por ejemplo, `["ECID"]`)
&#x200B;- `event.xdm.environment.type` - Tipo de entorno: `"browser"`, `"app"` o `"server"`
&#x200B;- `event.xdm.environment.browserDetails` - Metadatos del explorador (`viewportWidth`, `viewportHeight`, `userAgent`)
&#x200B;- `event.xdm.identityMap` - Misma asignación de identidad que Administración de decisiones
&#x200B;- `event.xdm.timestamp` - Marca de tiempo ISO 8601
&#x200B;- `query.personalization.surfaces` - Matriz de superficies de destino (por ejemplo, `["web://site.com/homepage"]`) — reemplaza a `decisionScope`
&#x200B;- `query.personalization.schemas` - Esquemas de contenido para devolver (por ejemplo, `["json-content-item", "html-content-item"]`)
&#x200B;- `data.__adobe.ajo.allowDuplicateDecisionItems` - Control de deduplicación (el valor predeterminado es `true`; establezca `false` de modo que un elemento que cumpla los requisitos para varias superficies se devuelva solo una vez, y las demás superficies recibirán un elemento de reserva o vacío). Reemplaza la Administración de decisiones `allowDuplicatePropositions`.
&#x200B;- `data.__adobe.ajo.dryRun` - Indicador de prueba; suprime los eventos de comentarios tanto para los contadores de informes como de límite. Reemplaza la Administración de decisiones `xdm:dryRun`. Eliminar antes de producción.

**Cuerpo de solicitud de ejemplo (lado del servidor):**

```json
{
  "events": [
    {
      "query": {
        "identity": { "fetch": ["ECID"] },
        "personalization": {
          "surfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"],
          "schemas": [
            "https://ns.adobe.com/personalization/json-content-item",
            "https://ns.adobe.com/personalization/html-content-item"
          ]
        }
      },
      "xdm": {
        "eventType": "decisioning.propositionFetch",
        "environment": {
          "type": "browser",
          "browserDetails": { "viewportWidth": 1280, "viewportHeight": 900, "userAgent": "<USER_AGENT>" }
        },
        "identityMap": {
          "ECID": [ { "id": "<ECID>", "authenticatedState": "ambiguous", "primary": true } ]
        },
        "timestamp": "2025-09-08T12:00:00.000Z"
      },
      "data": {
        "__adobe": { "ajo": { "allowDuplicateDecisionItems": false } }
      }
    }
  ],
  "meta": {
    "state": {
      "domain": "my-web",
      "cookiesEnabled": true,
      "entries": [
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>" },
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>" }
      ]
    }
  }
}
```

>[!NOTE]
>Para obtener la referencia completa de Journey Optimizer Decisioning Web SDK / Edge, consulte [Experiencia basada en código: Implementaciones de decisiones](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations).

### Decidir la respuesta de Edge {#decisioning-response}

La respuesta de Decisioning contiene varios identificadores organizados por tipo de problema: `personalization:decisions` (las ofertas), `locationHint:result` y `state:store` (las cookies que se van a mantener).

**Estructura de respuesta:**

```json
{
  "requestId": "<REQUEST_ID>",
  "handle": [
    {
      "type": "personalization:decisions",
      "eventIndex": 0,
      "payload": [
        {
          "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
          "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
          "scopeDetails": {
            "decisionProvider": "AJO",
            "correlationID": "<CORRELATION_ID>",
            "characteristics": {
              "eventToken": "<base64 message-level event token>",
              "subPropositions": "<base64-encoded array of decision items>"
            },
            "rank": 1,
            "activity": {
              "id": "<campaignId>#<actionId>",
              "priority": 0,
              "matchedSurfaces": ["web://my-web/IP_NLI_HP_GET_LOAN_WIDGET"]
            }
          },
          "items": [
            {
              "id": "36646bab-af1b-44c6-b632-bbfb9c357919",
              "schema": "https://ns.adobe.com/personalization/json-content-item",
              "data": { "content": "{ ...offer JSON... }" }
            }
          ]
        }
      ]
    },
    {
      "type": "locationHint:result",
      "payload": [
        { "scope": "EdgeNetwork", "hint": "ind1", "ttlSeconds": 1800 }
      ]
    },
    {
      "type": "state:store",
      "payload": [
        { "key": "kndctr_<ORG>_AdobeOrg_cluster", "value": "<cluster-cookie>", "maxAge": 1800 },
        { "key": "kndctr_<ORG>_AdobeOrg_identity", "value": "<identity-cookie>", "maxAge": 34128000 }
      ]
    }
  ]
}
```

**Campos de respuesta clave:**
&#x200B;- `handle[].type` - Tipo de identificador (`personalization:decisions`, `locationHint:result`, `state:store`)
&#x200B;- `payload[].id` - ID de instancia de propuesta única — Eco de nuevo en los eventos de visualización/interacción
&#x200B;- `payload[].scope`: URI de superficie para el que se resolvió la propuesta
&#x200B;- `payload[].scopeDetails.decisionProvider` - Confirma que el motor es `AJO`
&#x200B;- `payload[].scopeDetails.correlationID`: vincula la instancia de decisión con el evento de servicio
&#x200B;- `payload[].scopeDetails.rank` / `payload[].scopeDetails.activity` - Metadatos de clasificación, campaña y acción de la propuesta
&#x200B;- `payload[].scopeDetails.characteristics.eventToken` - Token de seguimiento de nivel de mensaje
&#x200B;- `payload[].scopeDetails.characteristics.subPropositions` - **matriz de elementos de decisión** codificada en Base64; cada elemento lleva su propio elemento por elemento `token`. Estos tokens por elemento son lo que se pasa en `propositionAction.tokens` en eventos de visualización/interacción
&#x200B;- `payload[].items[].schema` / `payload[].items[].data.content`: esquema de contenido y contenido de oferta real (JSON/HTML) que se procesarán
&#x200B;- `state:store` carga: las cookies de identidad y de clúster que se mantendrán y reenviarán en solicitudes posteriores (del lado del servidor)

La cadena `characteristics.subPropositions` base64-descodifica la matriz de elementos servidos, cada uno con su valor por elemento `token`:

```json
[
  {
    "id": "1ae75277-8832-4c23-bbbc-09f01cfe6c8b",
    "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
    "scopeDetails": { "decisionProvider": "EXD", "correlationID": "<CORRELATION_ID>-0", "rank": 1 },
    "items": [
      { "id": "dps:<schema>:1be64ff83a612488", "name": "ExD_Personal Loan Offer", "score": 997.0, "token": "CLaefQnVLcLbCtzEXV3Jeg" },
      { "id": "dps:<schema>:1be6516838e1248c", "name": "ExD_Home Loan Offer",     "score": 995.0, "token": "ALlB5KV1B0e+CpHoahi7Ew" },
      { "id": "dps:<schema>:1be650da3cd06e98", "name": "ExD_Auto Loan Offer",     "score": 994.0, "token": "koJTRQcwFkR92AqbZ88ytQ" },
      { "id": "dps:<schema>:1be65612d5a1248d", "name": "ExD_Fallback Offer",      "itemSelection": { "selectionDetail": { "selectionType": "fallback" } }, "token": "GHo4ow7h6iCzBOhYR1+6jg" }
    ]
  }
]
```

## Patrones de implementación {#implementation-patterns}

Decisioning admite tres enfoques de implementación:

### Implementación del lado del cliente (SDK web/SDK móvil) {#client-side}

Web SDK o Mobile SDK gestiona automáticamente todas las solicitudes y la administración de cookies. SDK almacena y reenvía las cookies de identidad y de clúster con cada solicitud.

**Administración de cookies:** Automática: Web SDK administra las cookies `kndctr_<OrgId>_identity` y `kndctr_<OrgId>_cluster`.

### Implementación del lado del servidor (API de Edge Network) {#server-side}

El servidor de aplicaciones realiza POST directamente en Edge Network y debe administrar manualmente el reenvío de cookies. El servidor extrae las cookies del explorador de las solicitudes entrantes, las reenvía a Edge Network a través de `meta.state.entries[]` y, a continuación, devuelve las cookies en la respuesta.

**Administración de cookies:** Manual: el servidor de aplicaciones debe extraer las cookies de la solicitud del explorador, reenviarlas a Edge Network en el cuerpo de la solicitud y configurarlas como respuesta. Las cookies deben reenviarse explícitamente en `meta.state.entries` para mantener la coherencia de la identidad.

### Implementación híbrida {#hybrid}

Combina el procesamiento del lado del servidor (carga inicial de página) con SDK del lado del cliente (interacciones subsiguientes). El servidor procesa el contenido inicial mediante Edge Network y, a continuación, Web SDK asume el control para las solicitudes de personalización posteriores.

**Administración de cookies:** mixta: el lado del servidor requiere el reenvío manual de cookies a Edge Network; el lado del cliente se administra automáticamente mediante Web SDK. Asegúrese de que los tokens de identidad del procesamiento del lado del servidor estén disponibles para SDK del lado del cliente para una resolución de identidad coherente.

## Seguimiento de eventos y recopilación de datos {#event-tracking}

Para atribuir correctamente los resultados de las decisiones, habilitar la restricción de frecuencia y activar la optimización de clasificación basada en IA, debe implementar el seguimiento de eventos mediante el esquema de eventos Decisioning.

### Campos de evento obligatorios {#event-fields}

Se requieren `eventType` y `_experience.decisioning.propositionEventType`. Si falta alguna de las dos, el contador de visualización/interacción correspondiente no se incrementa.

* **`eventType`** - Especifica la categoría del evento:
  &#x200B;- `decisioning.propositionDisplay` — Evento de impresión (oferta mostrada al usuario)
  &#x200B;- `decisioning.propositionInteract`: evento de interacción (el usuario hizo clic o participó en la oferta)

* **`_experience.decisioning.propositionEventType`** - Marca el subtipo de evento. Incluir **exactamente una clave de tipo de evento** establecida en `1` (cada valor es `1` o `0`; no establezca varios tipos de evento en `1` en el mismo objeto):
  &#x200B;- `{ "display": 1 }` — Evento de impresión
  &#x200B;- `{ "interact": 1 }` — evento de interacción
  &#x200B;- Si todos/as los/las `display`/`interact`/`dismiss` son `0` (o `eventType` es cualquier valor distinto de `decisioning.proposition<Display|Interact|Dismiss>`), el evento se trata como un **evento personalizado**.

* **`_experience.decisioning.propositionAction.tokens[]`** - Token(s) por elemento(s) que identifica qué elemento(s) sirvió(n) para incrementar los contadores de:
  &#x200B;- Copie los `token` de cada elemento de la matriz `subPropositions` descodificada — **no** `scopeDetails.characteristics.eventToken`, que es un token de nivel de mensaje diferente.
  &#x200B;- Pase el token exactamente como se recibió, sin modificar.
  &#x200B;- **Eventos de interacción:** proporcionan **exactamente un token** (el elemento donde se hizo clic).
  &#x200B;- **Mostrar eventos:** opcional — proporciona token(s) para incrementar elementos específicos, o **omite** `tokens` para incrementar el contador de **todos** los elementos de `subPropositions`.

* **`_experience.decisioning.propositions[]`**: haga eco de las propuestas servidas, incluidas `id`, `scope` y la `scopeDetails` completa de la respuesta (que lleva `characteristics.subPropositions` y requiere `decisionProvider`). No es necesario que genere una matriz `items[]` explícita.

### Requisitos de esquema {#schema-requirements}

Asocie el grupo de campos Decisioning al esquema del conjunto de datos de evento antes de la migración:

1. En Experience Platform, abra el esquema del conjunto de datos de eventos
2. Agregar el grupo de campos `Experience Event - Proposition Details`
3. Asegúrese de que los siguientes campos estén asignados:
   &#x200B;- `_experience.decisioning.*` campos
   &#x200B;- `_experience.decisioning.propositionAction.tokens`
   &#x200B;- `_experience.decisioning.propositionEventType`

### Administración de tokens de seguimiento {#tracking-token}

El token de seguimiento debe gestionarse de acuerdo con estos requisitos:

* **El token por elemento controla los contadores**; los valores de `propositionAction.tokens` son `token` de cada elemento proporcionado de `subPropositions`, no del nivel de mensaje `characteristics.eventToken`.
* **Eventos de interacción**: proporcione exactamente un token (el elemento donde se hizo clic).
* **Mostrar eventos**: los tokens son opcionales; omita aumentar todos los elementos en `subPropositions` o proporcione tokens específicos para incrementar únicamente esos elementos.
* **No modifique el token**; pase el valor exactamente como se recibió; no lo codifique, analice ni modifique.

## Ejemplos de eventos de decisiones {#event-examples}

Cada ejemplo hace eco de la propuesta servida (incluido su `scopeDetails`, que lleva `characteristics.subPropositions`) y establece `eventType` y `propositionEventType`. Los contadores se incrementan en los elementos de `subPropositions`; `propositionAction.tokens` selecciona qué elementos.

### Mostrar eventos

Mostrar eventos notificar a Decisioning cuando se muestra una oferta a un usuario. Proporcione los token de los elementos mostrados u omita `tokens` para aumentar el contador de visualización de todos los elementos en `subPropositions`:

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionDisplay",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg", "ALlB5KV1B0e+CpHoahi7Ew"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### Eventos de interacción (clic)

Los eventos de interacción rastrean cuándo un usuario hace clic o interactúa con una oferta mostrada. Usted **debe** proporcionar **exactamente un token** que identifique el elemento en el que se hizo clic:

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "source": { "name": "ajo-inbound" }
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "decisioning.propositionInteract",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "interact": 1 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

### Eventos personalizados

Un evento personalizado usa un `eventType` definido por el cliente (cualquier valor que no sea `decisioning.proposition<Display|Interact|Dismiss>`) y establece todo `display`/`interact`/`dismiss` en `0` en `propositionEventType` (clasificado como `OTHER`). Los eventos personalizados se descodifican como eventos de visualización (filtrado de múltiples tokens) con `subPropositions` y se evalúan mediante el PQL configurado:

```json
{
  "header": {
    "imsOrgId": "YOUR_ORG_ID",
    "sandboxId": "sandbox-id",
    "sandboxName": "sandbox-name",
    "originalTimestamp": 1700000
  },
  "body": {
    "xdmEntity": {
      "identityMap": {
        "ECID": [ { "id": "ecid-123", "primary": true } ]
      },
      "eventType": "add-to-cart",
      "_experience": {
        "decisioning": {
          "propositionEventType": { "display": 0, "interact": 0, "dismiss": 0 },
          "propositionAction": {
            "id": "b96f842b-5dd9-4c55-9dae-647d96250028",
            "tokens": ["CLaefQnVLcLbCtzEXV3Jeg"]
          },
          "propositions": [
            {
              "id": "103ae599-e6d8-4631-baf3-51dd8c6ed4c1",
              "scope": "web://my-web/IP_NLI_HP_GET_LOAN_WIDGET",
              "scopeDetails": {
                "decisionProvider": "AJO",
                "characteristics": {
                  "eventToken": "<base64 eventToken from response>",
                  "subPropositions": "<base64 subPropositions from response>"
                }
              }
            }
          ]
        }
      }
    }
  }
}
```

Estos eventos permiten la restricción de frecuencia, la creación de informes predeterminados y la optimización de clasificación impulsada por IA en Decisioning. Para enviar eventos de propuesta con Web SDK, consulte [Experiencia basada en código: Implementaciones de decisiones](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-decisioning-implementations).

## Proceso de migración de extremo a extremo {#migration-process}

1. Validar requisitos previos: asegúrese de que la zona protegida de Target esté preparada y de que todas las dependencias de requisitos previos estén identificadas y listas antes de iniciar la migración (atributos de perfil, ID de segmento, asignación de ID).

1. Llamar a la API de migración: ejecute la API de migración para migrar objetos de administración de decisiones a Decisioning utilizando los requisitos previos y las asignaciones preparados.

1. Generación de entidades de Draft Decisioning: la herramienta crea campañas, políticas de decisión, estrategias de selección, elementos de oferta, etc. en estado de borrador por asignación de entidad. Revise todos los objetos Decisioning generados en la zona protegida de destino. Valide que la nomenclatura, los tipos de entidad y las referencias sean correctos. Todavía no hay nada orientado al cliente, Administración de decisiones sigue sirviendo tráfico en directo.

1. Actualizar código de cliente y servidor: implemente los cambios de código necesarios para utilizar los nuevos formatos de solicitud/respuesta de Decisioning e implemente el seguimiento de eventos con los campos obligatorios.

1. Activar y eliminar: active los objetos de toma de decisiones (estrategias, políticas, campañas y superficies) y desplace el tráfico de Administración de decisiones en su propia cronología.

## Temas relacionados {#related-topics}

* [Migrar de Administración de decisiones a Toma de decisiones](migrate-to-decisioning.md): comprenda los beneficios y capacidades de migrar a Toma de decisiones
* [Introducción a la toma de decisiones](gs-experience-decisioning.md)
* [Limitaciones y protecciones de decisiones](decisioning-guardrails.md)
* [Comenzar con API de Decisioning](api-reference/getting-started.md)