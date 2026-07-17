---
solution: Journey Optimizer
product: journey optimizer
title: Guía de definición de recompensa
description: Aprenda a configurar las definiciones de recompensas para los proveedores de recompensas de Retos de fidelidad en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: 9b0fd9d8-18d1-4a51-8b6f-b2e2a4c6f1d7
feature_v2: []
subfeature_v2: []
source-git-commit: 00c24e9b97b4f6597048731858f3bfbcb39a0030
workflow-type: tm+mt
source-wordcount: 1206
ht-degree: 3%

---

# Guía de definición de recompensa {#reward-definition-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_reward_definition"
>title="Guía de definición de recompensa"
>abstract="Utilice esta guía para configurar las definiciones de recompensas para los proveedores de recompensas de fidelidad, incluidos los campos de comportamiento de definición predeterminada y carga útil de cumplimiento."

>[!BEGINSHADEBOX]

**Tabla de contenido**

[Introducción a los retos de fidelización](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Crear y administrar desafíos**

* [Acceder y administrar desafíos y tareas](access-loyalty-challenges.md)
* [Crear desafíos](create-challenges.md)
* [Creación de tareas](create-tasks.md)
* [Monitorización del rendimiento del desafío de fidelidad](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configurar e integrar**

* [Configuración de desafíos de lealtad](loyalty-admin.md)
* **Guía de definición de recompensa** ◀︎ **Usted está aquí**
* [Guía del transformador de eventos](event-transformer-guide.md)
* [Datos y conjuntos de datos de fidelización](loyalty-data-and-datasets.md)
* [Referencia de API de retos de fidelización](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta privada**. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad en [!DNL Journey Optimizer], consulte [ciclo de lanzamiento](../rn/releases.md).

Cuando una tarea, hito o desafío de desafío completa **y tiene configurado un valor de recompensa**, la plataforma emite un incentivo llamando al extremo HTTP del proveedor de recompensas con una carga útil JSON. Una **definición de recompensa** describe qué recompensa emitir y proporciona una expresión [JSONata](https://docs.jsonata.org/overview) — `rewardJsonata` — que define la carga útil exacta que espera su proveedor.

Esta guía explica cómo configurar un proveedor de recompensas, crear definiciones de recompensas, escribir la expresión `rewardJsonata` y comprender qué contexto está disponible en el momento de la evaluación.

## Modelo de dos niveles

Las recompensas se organizan en dos niveles:

```
Reward Provider  (endpoint, auth, headers)
└── Reward Definition  (denomination, rewardJsonata)
└── Reward Definition
└── ...
```

Un **proveedor de recompensas** representa un único sistema de recompensas externo; contiene la dirección URL del extremo de entrega, la autenticación y cualquier encabezado HTTP personalizado. Un proveedor puede tener varias **definiciones de recompensa**, cada una de las cuales describe un tipo de recompensa o una denominación distinta que ofrece ese proveedor (por ejemplo, &quot;50 estrellas&quot;, &quot;estrellas dobles&quot;, &quot;artículo gratis&quot;).

Un desafío hace referencia al proveedor y a la definición por GUID. Cuando se emite una recompensa, la plataforma evalúa la expresión `rewardJsonata` de la definición y PUBLICA el resultado en el extremo del proveedor.

## Campos de definición y proveedor de recompensas

+++Campos del proveedor de recompensas

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>Campo</th><th>Tipo</th><th>Requerido</th><th>Descripción</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>No (asignado por el sistema)</td><td>Identificador único. Sólo lectura.</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>Sí</strong></td><td>Nombre para mostrar, único dentro de la organización.</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>No</td><td>Descripción legible en lenguaje natural del proveedor.</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>No</td><td>Cuando <code>false</code>, la entrega de recompensa se<br>suspende para todas las definiciones de este proveedor.</td></tr>
<tr><td><code>url</code></td><td><code>String</code></td><td><strong>Sí</strong></td><td>Punto final HTTP que recibe la carga útil de recompensa.<br>La plataforma publica el resultado evaluado<br><code>rewardJsonata</code> en esta dirección URL.</td></tr>
<tr><td><code>additionalHeaders</code></td><td><code>Object</code></td><td>No</td><td>Encabezados HTTP personalizados para incluirlos en cada <br>solicitud de envío (p. ej. claves de API,<br>invalidaciones de tipo de contenido).</td></tr>
<tr><td><code>maxRatePerSecond</code></td><td><code>Integer</code></td><td>No</td><td>Límite de tarifa opcional por proveedor (1-5000).<br>Nulo significa ilimitado.</td></tr>
<tr><td><code>enableMTLS</code></td><td><code>Boolean</code></td><td>No</td><td>Si el punto de conexión requiere TLS mutuo.</td></tr>
</table>

+++

+++Campos de definición de recompensa

<table>
<colgroup>
<col style="width:160px">
<col style="width:80px">
<col style="width:160px">
<col>
</colgroup>
<tr><th>Campo</th><th>Tipo</th><th>Requerido</th><th>Descripción</th></tr>
<tr><td><code>guid</code></td><td><code>String</code></td><td>No (asignado por el sistema)</td><td>Identificador único. Sólo lectura.</td></tr>
<tr><td><code>name</code></td><td><code>String</code></td><td><strong>Sí</strong></td><td>Nombre para mostrar, único dentro del proveedor.</td></tr>
<tr><td><code>denomination</code></td><td><code>String</code></td><td>No</td><td>La unidad del premio, usada en la pantalla <br> y disponible en expresiones como <br><code>reward.denomination</code><br> (p. ej. <code>"Stars"</code>, <code>"Points"</code>, <code>"Miles"</code>).</td></tr>
<tr><td><code>desc</code></td><td><code>String</code></td><td>No</td><td>Descripción del premio, disponible<br>en expresiones como <code>reward.desc</code>.</td></tr>
<tr><td><code>enabled</code></td><td><code>Boolean</code></td><td>No</td><td>Cuando <code>false</code>, esta definición está inactiva<br> y no emitirá recompensas.</td></tr>
<tr><td><code>isDefault</code></td><td><code>Boolean</code></td><td>No</td><td>Marca esto como la definición de recompensa predeterminada para toda la zona protegida <br>. Solo puede haber una definición predeterminada <br>en todos los proveedores a la vez;<br>al establecer una nueva definición predeterminada se borra la anterior.<br>Se usa para rellenar automáticamente los detalles de recompensa en <br>desafíos personalizados en el momento de la publicación.</td></tr>
<tr><td><code>rewardJsonata</code></td><td><code>String</code></td><td><strong>Sí</strong></td><td>Expresión JSONata evaluada en <br>momento de recompensa por el problema. Recibe el contexto de recompensa <br>completo y debe devolver la carga útil JSON<br>para POST al proveedor.</td></tr>
</table>

+++

## El contexto de recompensa

Cuando se evalúa `rewardJsonata`, recibe un único objeto raíz que contiene todo lo conocido sobre el evento de recompensa. Todas las rutas de la expresión son relativas a esta raíz.

```json
{
  "rewardContext": {
    "rewardValue": "50",
    "source":      "challenge"
  },
  "reward": {
    "name":         "500 Stars",
    "desc":         "Issue 500 Stars to the member",
    "denomination": "Stars",
    "enabled":      true
  },
  "task": { ... },
  "milestone": { ... },
  "challenge": { ... },
  "timestamp": "2026-02-10T00:29:22.538+00:00"
}
```

+++ Campos de contexto

| Campo | Descripción |
|----------------------------------------|-------------|
| `rewardContext.rewardValue` | Cadena de valor de recompensa configurada en el desafío, tarea o hito que activó esta emisión. |
| `rewardContext.source` | Qué activó la recompensa: `"task"`, `"challenge"` o `"milestone"`. |
| `reward` | La propia RewardDefinition: `name`, `desc`, `denomination`. |
| `task` | La tarea de finalización, incluidos sus `accumulators`, `schedule` y `reward`. |
| `task.accumulators.spend` | Gasto total correspondiente acumulado por la tarea. |
| `task.accumulators.qty` | Recuento total de artículos aptos acumulado por la tarea. |
| `task.accumulators.item_list` | Todos los elementos aptos aplicados a la tarea. Cada entrada tiene `item`, `transactionId`, `timestamp`, `utcOffset`, `locationId`. |
| `task.accumulators.item_list[-1]` | El elemento aplicado más recientemente (índice negativo de JSONata). Útil para obtener el último ID de transacción o la última marca de tiempo. |
| `task.schedule.currentStreak` | Recuento de racha de visitas consecutivas actuales (para desafíos de racha). |
| `task.schedule.currentVisits` | Recuento total de visitas (para los desafíos de visita). |
| `milestone` | El hito que generó esta recompensa o `null`, si no es una recompensa de hito. Incluye `count` y `reward.rewardValue`. |
| `challenge.profileId` | ID de fidelidad del miembro. |
| `challenge.kvpCustom` | Pares de clave-valor personalizados configurados en el desafío. Un patrón común para pasar ID de campaña, nombres de productos o metadatos específicos de proveedores. |
| `challenge.name` | Nombre del desafío. |
| `challenge._id` | ID de desafío. |
| `timestamp` | Marca de tiempo ISO 8601 de la emisión de recompensa. |

+++

## Escritura de la expresión de premio Jsonata

La expresión recibe el contexto de recompensa como entrada y debe devolver un objeto JSON (la carga útil POST) al extremo del proveedor. La forma de ese objeto depende totalmente de la API del proveedor; los campos de contexto se asignan a la estructura que el proveedor espere.

+++Carga útil fija simple

El caso más sencillo: el proveedor necesita un recuento de puntos y un ID de miembro, ambos conocidos a partir del contexto.

```jsonata
{
  "memberId":   challenge.profileId,
  "points":     $number(rewardContext.rewardValue),
  "currency":   reward.denomination
}
```

**Salida:**

```json
{
  "memberId": "ADB-0000030",
  "points":   50,
  "currency": "Stars"
}
```

> `rewardContext.rewardValue` siempre es una cadena. Use `$number()` para convertirlo si su proveedor espera un valor numérico.

+++

+++Usando `kvpCustom` para metadatos específicos del proveedor

Los proveedores suelen requerir campos como ID de campaña o códigos de sistema de origen específicos para cada desafío ejecutado. Almacénelos en `challenge.kvpCustom` cuando cree el desafío y luego haga referencia a ellos en la expresión, para que la expresión se pueda reutilizar en todas las campañas.

```jsonata
{
  "memberId":         challenge.profileId,
  "points":           $number(rewardContext.rewardValue),
  "campaignId":       challenge.kvpCustom.campaignId,
  "transactionSource": "AJO"
}
```

También puede usar `reward.kvpCustom` para constantes fijas para un determinado tipo de recompensa en lugar de por desafío.

+++

+++Usar datos del acumulador de tareas

Los acumuladores de tareas mantienen un registro de cada evento correspondiente. Use `item_list[-1]` para acceder al elemento aplicado más recientemente; sus `transactionId` y `timestamp` son útiles para las pistas de auditoría y la deduplicación en el lado del proveedor.

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "transactionId":  task.accumulators.item_list[-1].transactionId,
  "transactionDate": task.accumulators.item_list[-1].timestamp
}
```

+++

+++Construcción de un mensaje de texto

Para los proveedores basados en notificaciones (Slack, SMS, correo electrónico), puede crear una cadena de mensaje directamente mediante el operador de concatenación `&` de JSONata:

```jsonata
{
  "text": "You just earned " & rewardContext.rewardValue & " " & reward.denomination & "!"
}
```

**Salida:**

```json
{
  "text": "You just earned 50 Stars!"
}
```

+++

## Ejemplos

+++Ejemplo 1 — Proveedor de puntos simple

**Escenario:** Una API básica de puntos de fidelidad espera un ID de miembro y una cantidad de puntos.

**Definición de recompensa:**

```json
{
  "name":         "Standard Points",
  "denomination": "Points",
  "desc":         "Award loyalty points",
  "enabled":      true,
  "rewardJsonata": "{\"memberId\": challenge.profileId, \"pointQuantity\": $number(rewardContext.rewardValue), \"denomination\": reward.denomination}"
}
```

**Expresión con formato:**

```jsonata
{
  "memberId":      challenge.profileId,
  "pointQuantity": $number(rewardContext.rewardValue),
  "denomination":  reward.denomination
}
```

**Carga útil POSTed al proveedor:**

```json
{
  "memberId":      "ADB-0000030",
  "pointQuantity": 50,
  "denomination":  "Points"
}
```

+++

+++Ejemplo 2: Carga útil del proveedor con metadatos de campaña

**Escenario:** El proveedor requiere un registro de asignación estructurado que incluya campos de auditoría, referencias de campaña y descripción de miembro. Los valores específicos de campaña se almacenan en `challenge.kvpCustom`, por lo que la misma definición de recompensa funciona en todas las campañas sin editar la expresión.

**Desafío`kvpCustom`** (establecido al crear el desafío):

```json
{
  "parentCampaignId": "CAMP-2026-Q1",
  "productName":      "Loyalty Program"
}
```

**Definición de recompensa:**

```json
{
  "name":         "Stars — Campaign Award",
  "denomination": "Stars",
  "desc":         "Issue Stars for completing a qualifying purchase",
  "enabled":      true,
  "rewardJsonata": "{\"awardPoints\":[{\"idType\":\"externalId\",\"id\":challenge.profileId,\"transactionId\":task.accumulators.item_list[-1].transactionId,\"transactionDate\":task.accumulators.item_list[-1].timestamp,\"originalTransactionId\":task.accumulators.item_list[-1].transactionId,\"transactionSource\":\"AJO\",\"channelSource\":\"Web\",\"parentCampaignId\":challenge.kvpCustom.parentCampaignId,\"productName\":challenge.kvpCustom.productName,\"memberAwardDescription\":reward.desc,\"pointQuantity\":$number(rewardContext.rewardValue)}]}"
}
```

**Expresión con formato:**

```jsonata
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    challenge.profileId,
      "transactionId":         task.accumulators.item_list[-1].transactionId,
      "transactionDate":       task.accumulators.item_list[-1].timestamp,
      "originalTransactionId": task.accumulators.item_list[-1].transactionId,
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      challenge.kvpCustom.parentCampaignId,
      "productName":           challenge.kvpCustom.productName,
      "memberAwardDescription": reward.desc,
      "pointQuantity":         $number(rewardContext.rewardValue)
    }
  ]
}
```

**Carga útil POSTed al proveedor:**

```json
{
  "awardPoints": [
    {
      "idType":                "externalId",
      "id":                    "ADB-0000030",
      "transactionId":         "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionDate":       "2026-02-08T00:12:00.000+00:00",
      "originalTransactionId": "b4fa0e89-f4bb-41ce-b370-fb97f9c52f1a",
      "transactionSource":     "AJO",
      "channelSource":         "Web",
      "parentCampaignId":      "CAMP-2026-Q1",
      "productName":           "Loyalty Program",
      "memberAwardDescription": "Issue Stars for completing a qualifying purchase",
      "pointQuantity":         50
    }
  ]
}
```

+++

+++Ejemplo 3 — Recompensa de hito

**Escenario:** Un desafío de racha emite un premio hito cada N visitas. La expresión incluye el recuento de hitos y la racha actual para el contexto del lado del proveedor.

**Expresión con formato:**

```jsonata
{
  "memberId":       challenge.profileId,
  "points":         $number(rewardContext.rewardValue),
  "milestoneCount": milestone.count,
  "currentStreak":  task.schedule.currentStreak,
  "denomination":   reward.denomination,
  "source":         rewardContext.source
}
```

**Carga útil publicada en el proveedor** (en el segundo hito de visita):

```json
{
  "memberId":       "ADB-0000030",
  "points":         20,
  "milestoneCount": 2,
  "currentStreak":  2,
  "denomination":   "Stars",
  "source":         "milestone"
}
```

> Cuando `rewardContext.source` es `"milestone"`, el objeto `milestone` se rellena con `count` y `reward.rewardValue`. Cuando el origen es `"task"` o `"challenge"`, `milestone` es `null`.

+++

## Referencia de la API

+++Proveedores de recompensas

```http
POST   /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers
GET    /loyalty/metadata/config/rewards/providers/{providerId}
PUT    /loyalty/metadata/config/rewards/providers/{providerId}
DELETE /loyalty/metadata/config/rewards/providers/{providerId}
```

Todas las solicitudes requieren `x-gw-ims-org-id` y `x-sandbox-name` encabezados.

**Crear un proveedor:**

```http
POST /loyalty/metadata/config/rewards/providers
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":    "My Points Provider",
  "desc":    "Issues loyalty points via REST",
  "enabled": true,
  "url":     "https://rewards.example.com/award",
  "additionalHeaders": {
    "x-api-key": "YOUR_API_KEY"
  }
}
```

+++

+++Definiciones de recompensa

```http
POST   /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}
GET    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
PUT    /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
DELETE /loyalty/metadata/config/rewards/definitions/{providerId}/{rewardId}
```

**Crear una definición de recompensa:**

```http
POST /loyalty/metadata/config/rewards/definitions/{providerId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":         "50 Stars",
  "denomination": "Stars",
  "desc":         "Award 50 Stars on task completion",
  "enabled":      true,
  "rewardJsonata": "{ \"memberId\": challenge.profileId, \"points\": $number(rewardContext.rewardValue) }"
}
```

+++

## Validación de expresión

Se validaron las expresiones `rewardJsonata` para la sintaxis en el momento de la publicación. Si la expresión no es válida, la API devuelve un error `422` con una descripción del error de análisis.

Para desarrollar y probar una expresión antes de publicarla, use [JSONata Exerciser](https://try.jsonata.org/). Pegue el JSON de contexto de recompensa como documento de entrada y la expresión para verificar que la salida coincida con lo que espera el proveedor. En los ejemplos anteriores se muestra un contexto de recompensa representativo para cada tipo de déclencheur (`task`, `milestone`, `challenge`).

## Errores comunes

| Error | Efecto | Corregir |
|---------|--------|-----|
| `rewardContext.rewardValue` se usó como número sin conversión | El tipo no coincide si el proveedor valida el campo como numérico | Ajustar con `$number(rewardContext.rewardValue)` |
| `challenge.kvpCustom.someKey` devuelve nulo | La clave no se establece en el desafío en el momento de la creación | Asegúrese de que la clave esté presente en `kvpCustom` en todos los desafíos que utilicen esta definición |
| `task.accumulators.item_list[-1]` es nulo | No se aplicó ningún artículo antes de la recompensa emitida (evento sin compra) | Protéjase con un condicional o use `timestamp` del contexto en su lugar |
| Se accedió a `milestone` cuando el origen es `"task"` o `"challenge"` | `milestone` es nulo; la expresión emite o produce campos nulos | Compruebe `rewardContext.source` antes de acceder a `milestone` o use `milestone` solamente en las definiciones adjuntas a las recompensas de hito |
| La expresión devuelve una matriz en lugar de un objeto | El proveedor recibe una estructura de carga útil inesperada | Agrupar expresiones que devuelven matrices en un objeto externo: `{ "items": [...] }` |
