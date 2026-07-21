---
solution: Journey Optimizer
product: journey optimizer
title: Guía del transformador de eventos
description: Obtenga información sobre cómo configurar los ajustes de esquema y transformador para las definiciones de eventos de Retos de fidelidad en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: d3ad85f0-7f7e-40ab-b8c4-fc0c1234be87
feature_v2: []
subfeature_v2: []
source-git-commit: 80abca7068e021e52e9c34d9a2fb629ebad70302
workflow-type: tm+mt
source-wordcount: 1731
ht-degree: 1%

---

# Guía del transformador de eventos {#event-transformer-guide}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_event_transformer"
>title="Guía del transformador de eventos"
>abstract="Utilice esta guía para configurar la validación de esquemas y las expresiones del transformador para las definiciones de eventos de Retos de fidelidad."

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
* [Guía de definición de recompensa](reward-definition-guide.md)
* **Guía del transformador de eventos** ◀︎ **Usted está aquí**
* [Datos y conjuntos de datos de fidelización](loyalty-data-and-datasets.md)
* [Referencia de API de retos de fidelización](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta privada**. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad en [!DNL Journey Optimizer], consulte [ciclo de lanzamiento](../rn/releases.md).

Para que una transacción de cliente se pueda aplicar a un desafío de fidelidad, debe tener el formato **Evento de fidelidad de Adobe** que el servicio de desafío entienda. Los eventos del cliente (desde un sistema POS, una aplicación móvil, una plataforma de comercio electrónico o cualquier otra fuente) suelen utilizar el esquema de datos propio del cliente. **Transformadores de eventos** eliminan esta brecha sin requerir ningún cambio en el sistema de flujo ascendente.

## Información general

Una **definición de evento** indica a la plataforma dos cosas:

* **Qué eventos reclamar**: cómo reconocer que un evento entrante pertenece a esta definición (coincidencia)
* **Cómo darles nueva forma**: una expresión [JSONata](https://docs.jsonata.org/overview) que asigna los campos del cliente al formato de Evento de fidelidad (transformación)

Se pueden configurar varias definiciones de evento por organización. La plataforma los evalúa en orden y aplica el primero que coincida. Los eventos que no coinciden con ninguna definición se transfieren a la ingesta nativa (consulte [Reserva — Eventos de fidelidad nativos](#fallback--native-loyalty-events)).

## El formato de evento de fidelización de Adobe

Cada definición de evento debe producir un objeto JSON con el siguiente formato. Esta es la entrada que procesa el servicio de desafío.

```json
{
  "_id":              "string — optional; used for duplicate detection if enabled",
  "event_name":       "string — used for internal metrics and reporting only (e.g. 'purchase', 'visit')",
  "timestamp":        "ISO 8601 date-time string — when the event occurred",
  "utc_offset":       "string — UTC offset of the store or device (e.g. '-07:00'); required for daypart matching",
  "location_id":      "string — optional; store or location identifier",
  "transaction_id":   "string — optional; dedup key for the transaction",
  "loyalty_identity": {
    "id": "string — the member's loyalty ID"
  },
  "item_list": [
    {
      "item_set":   ["string", "..."],  // one or more identifiers — SKU, category, event code, etc.
      "item_name":  "string — optional human-readable label",
      "quantity":   1,                  // integer; how many units
      "unit_price": 4.99,               // float; price per unit
      "sub_total":  4.99                // float; line total (quantity × unit_price)
    }
  ]
}
```

### Notas de campo

| Campo | Requerido | Notas |
|--------------------------------|--------------------|-------|
| `loyalty_identity` | **Sí** | Debe contener `id`: el ID de fidelidad del miembro. |
| `item_list` | **Sí** | Debe tener ≥1 elemento; se rechaza item_list vacío. |
| `item_set` | **Sí** (por elemento) | La tarea de identificadores incluye/excluye listas con las que coincide. |
| `timestamp` | **Sí** | Se utiliza para la evaluación de ventana de fecha. Debe ser ISO 8601. |
| `utc_offset` | Recomendado | Necesario para la coincidencia de días y el recuento de días de racha. |
| `_id` | No | Se utiliza para la desduplicación si org tiene habilitada la detección de duplicados. |
| `sub_total` | No | Las tareas de umbral de gasto utilizan esto; omitir significa no gastar. |

## Campos de definición de evento

| Campo | Tipo | Requerido | Descripción |
|--------------------------------|------------------|----------------------|-------------|
| `guid` | Cadena | No (asignado por el sistema) | ID único asignado por el sistema; solo lectura. |
| `name` | Cadena | **Sí** | Etiqueta legible en lenguaje natural, p. ej. `"Starbucks POS Purchase"`. |
| `xdmSchemaId` | Cadena | **Sí** | Coincide con eventos por ID de esquema XDM (consulte Funcionamiento de la coincidencia). |
| `schema` | Cadena | No | [Esquema JSON](https://json-schema.org/) (como cadena) para validar eventos entrantes. |
| `transformer` | Cadena | **Sí** | Expresión JSONata que asigna el evento al formato de Fidelidad. |

## Funcionamiento de la coincidencia

Los eventos que llegan a través del servicio principal de recopilación de datos (DCCS) llevan una referencia de esquema XDM en su sobre. La plataforma lee el identificador de esquema de `/body/xdmMeta/schemaRef/id` y lo compara con el `xdmSchemaId` de cada definición.

La plataforma recorre las definiciones de evento de la organización **en orden** y aplica la primera coincidencia. Una vez encontrada una coincidencia, el cuerpo `xdmEntity` se pasa al transformador.

## Escritura del transformador

El campo `transformer` es una expresión [JSONata](https://docs.jsonata.org/overview). Recibe el evento JSON entrante como entrada y debe devolver un objeto de evento de fidelidad de Adobe válido.

+++Patrón de asignación básico

Asigne cada campo de nivel superior del formato de destino a la ruta correspondiente en el evento de origen:

```jsonata
{
  "_id":            sourceEvent._id,
  "event_name":     sourceEvent.eventType,
  "timestamp":      sourceEvent.timestamp,
  "utc_offset":     sourceEvent.storeInfo.utcOffset,
  "location_id":    sourceEvent.storeInfo.storeId,
  "transaction_id": sourceEvent.transaction.id,
  "loyalty_identity": {
    "id": sourceEvent.member.loyaltyId
  },
  "item_list": sourceEvent.transaction.items.{
    "item_set":   [itemSku, itemCategory],
    "item_name":  itemDescription,
    "quantity":   quantity,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

+++

+++Codificación del nombre del evento

Si todos los eventos que coinciden con esta definición representan la misma actividad lógica, codifique el `event_name`:

```jsonata
{
  "event_name": "in-store-purchase",
  ...
}
```

`event_name` se usa para informes y métricas internas. No se usa como filtro de tareas: la calificación de tareas está determinada por el contenido de `item_set`, no por el nombre del evento.

+++

+++Asignación de identidad para eventos DCCS/XDM

Para los eventos que llegan a través de la ruta DCCS, la identidad del miembro se suele llevar en el campo XDM estándar `identityMap` en lugar de una propiedad de inquilino personalizada. `identityMap` es un mapa escrito por el área de nombres (la clave en sí es el nombre del área de nombres y el valor es una matriz de objetos de identidad).

```jsonata
"loyalty_identity": {
  "id": identityMap.Email[0].id
}
```

* **Sustitución del área de nombres:** Reemplace `Email` con el área de nombres que su organización utilice para los miembros con lealtad: `Loyalty`, `ECID`, `CRMID`, etc. Lea siempre desde el área de nombres que contiene la identidad principal del perfil de lealtad.

* **Usar siempre `[0]`:** `identityMap.Email` es una matriz. Sin el índice, JSONata devuelve una secuencia en lugar de un valor único si hay más de una identidad y `loyalty_identity.id` se convierte en una lista. Ancléelo al primer elemento con `[0]`.

* **Evitar campos de inquilino personalizados para la identidad:** Los grupos de campos personalizados a veces exponen un campo de aspecto electrónico (p. ej. `_yourtenant.identification.core.email`). En los datos de ejemplo, esto devuelve un valor y tiene un aspecto correcto, pero en los eventos de producción suele estar vacío. La fuente confiable de identidad siempre es `identityMap`.

+++

+++Generando `item_set`

`item_set` es una matriz de identificadores de cadena. Incluya todos los campos por los que puedan filtrar las tareas de desafío:

```jsonata
"item_set": [itemSku, productCategory, departmentCode]
```

Para los eventos no transaccionales (un registro de entrada, una finalización de una encuesta, un déclencheur personalizado), un solo identificador es suficiente:

```jsonata
"item_set": [eventName]
```

+++

+++Asignación `unit_price`

`unit_price` debe ser un precio por unidad. Algunos esquemas de origen almacenan un total de línea (precio × cantidad) en su lugar. Si el campo de origen es un total de línea, divida por cantidad para obtener el precio unitario:

```jsonata
"unit_price": priceTotal / quantity
```

> Dividir solo si el campo de origen es un total de línea. Si ya almacena un precio unitario, asígnelo directamente: si se divide un precio unitario por cantidad, se producirá un valor incorrecto de forma silenciosa.

+++

+++Derivando `transaction_id`

Si el evento de origen no incluye un identificador de transacción, puede derivar uno estable de la marca de tiempo:

```jsonata
"transaction_id": "txn_" & $string($toMillis(timestamp))
```

Esto convierte la marca de tiempo ISO en milisegundos epoch y produce un valor determinístico para un evento determinado. Utilice la función de generación de ID de su propia plataforma si hay una disponible.

+++

+++Uso de funciones JSONata

La biblioteca completa de funciones JSONata está disponible. Ejemplos útiles:

```jsonata
/* String concatenation */
"item_set": [skuId & ':' & categoryId]

/* Number formatting */
"item_set": ["spend:" & $formatNumber(totalAmount, '0.00')]

/* Conditional field */
"event_name": eventType ? eventType : "unknown"

/* Array transformation */
"item_list": items.{ "item_set": [sku], "quantity": qty, "sub_total": price * qty }
```

+++

## Ejemplos

+++Ejemplo 1 — Evento personalizado simple (no transaccional)

**Escenario:** Una aplicación móvil envía un evento de protección. No hay elementos de línea: el evento en sí es la actividad correspondiente.

**Evento entrante:**

```json
{
  "_id":       "evt-001",
  "eventName": "store-checkin",
  "timestamp": "2025-10-15T14:22:00Z",
  "storeId":   "STORE-042",
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**Definición de evento:**

```json
{
  "name":        "Mobile Store Check-In",
  "xdmSchemaId": "https://ns.adobe.com/yourtenant/schemas/store-checkin-v1",
  "transformer": "{\"_id\": _id, \"event_name\": eventName, \"timestamp\": timestamp, \"location_id\": storeId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": [{\"item_set\": [eventName], \"quantity\": 1}]}"
}
```

**Transformador con formato (para facilitar la lectura):**

```jsonata
{
  "_id":        _id,
  "event_name": eventName,
  "timestamp":  timestamp,
  "location_id": storeId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": [
    {
      "item_set": [eventName],
      "quantity": 1
    }
  ]
}
```

**Evento de fidelidad de Adobe de salida:**

```json
{
  "_id":        "evt-001",
  "event_name": "store-checkin",
  "timestamp":  "2025-10-15T14:22:00Z",
  "location_id": "STORE-042",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [{ "item_set": ["store-checkin"], "quantity": 1 }]
}
```

Una tarea de desafío sin restricciones de inclusión/exclusión contará este evento como una visita que cumple los requisitos: la sola entrada `item_set` `["store-checkin"]` coincide con cualquier tarea que permita todos los elementos.

+++

+++Ejemplo 2 — Compra de PDV con artículos de línea

**Escenario:** Un sistema de punto de venta envía una carga útil de transacción. Cada elemento de línea tiene un SKU y pertenece a una categoría. Las tareas de desafío utilizan el SKU y la categoría para determinar qué califica.

**Evento entrante:**

```json
{
  "_id":       "txn-20251015-4492",
  "timestamp": "2025-10-15T14:35:00Z",
  "storeInfo": {
    "storeId":   "STORE-042",
    "utcOffset": "-07:00"
  },
  "transaction": {
    "transactionId": "4492",
    "items": [
      { "sku": "COFFEE-001", "category": "BEVERAGE", "qty": 2, "unitPrice": 4.50, "lineTotal": 9.00 },
      { "sku": "MUFFIN-007", "category": "FOOD",     "qty": 1, "unitPrice": 3.25, "lineTotal": 3.25 }
    ]
  },
  "member": {
    "loyaltyId": "LM-8827361"
  }
}
```

**Definición de evento:**

```json
{
  "name":        "Retail POS Purchase",
  "xdmSchemaId": "https://ns.adobe.com/yourtenant/schemas/retail-pos-purchase-v1",
  "transformer": "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": storeInfo.utcOffset, \"location_id\": storeInfo.storeId, \"transaction_id\": transaction.transactionId, \"loyalty_identity\": {\"id\": member.loyaltyId}, \"item_list\": transaction.items.{\"item_set\": [sku, category], \"quantity\": qty, \"unit_price\": unitPrice, \"sub_total\": lineTotal}}"
}
```

**Transformador con formato:**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     storeInfo.utcOffset,
  "location_id":    storeInfo.storeId,
  "transaction_id": transaction.transactionId,
  "loyalty_identity": {
    "id": member.loyaltyId
  },
  "item_list": transaction.items.{
    "item_set":   [sku, category],
    "quantity":   qty,
    "unit_price": unitPrice,
    "sub_total":  lineTotal
  }
}
```

**Evento de fidelidad de Adobe de salida:**

```json
{
  "_id":            "txn-20251015-4492",
  "event_name":     "purchase",
  "timestamp":      "2025-10-15T14:35:00Z",
  "utc_offset":     "-07:00",
  "location_id":    "STORE-042",
  "transaction_id": "4492",
  "loyalty_identity": { "id": "LM-8827361" },
  "item_list": [
    { "item_set": ["COFFEE-001", "BEVERAGE"], "quantity": 2, "unit_price": 4.50, "sub_total": 9.00 },
    { "item_set": ["MUFFIN-007", "FOOD"],     "quantity": 1, "unit_price": 3.25, "sub_total": 3.25 }
  ]
}
```

Una tarea de desafío con `include: ["BEVERAGE"]` vería que el elemento de línea de café cumple los requisitos (su `item_set` contiene `"BEVERAGE"`) y acumularía $9,00 de gasto en esa tarea. Se excluiría el elemento de línea de magdalena.

+++

+++Ejemplo 3: Evento de experiencia de AEP (coincidencia de esquemas XDM)

**Escenario:** Los eventos fluyen a través de Adobe Journey Optimizer. El evento entrante es un evento de experiencia XDM con un ID de esquema conocido. La plataforma utiliza el ID de esquema para la coincidencia en lugar de una comprobación de ruta/valor.

**Cuerpo de entidad XDM entrante** (el `xdmEntity` extraído del evento AJO):

```json
{
  "_brandname": {
    "identities": {
      "loyaltyId": "LM-8827361"
    },
    "transactions": {
      "transactionId": "TXN-9901",
      "storeNumber":   "042",
      "utcOffset":     "-07:00",
      "lineItems": [
        { "skuNumber": "11143053", "priceAmount": 345, "qty": 1, "category": "BEVERAGE" },
        { "skuNumber": "11161387", "priceAmount": 495, "qty": 1, "category": "FOOD" }
      ],
      "totalAmount": 840
    }
  },
  "_id":       "87c0cccf-5809-38e0-a703-3994e80173ab",
  "timestamp": "2025-07-04T16:03:32.000Z"
}
```

**Definición de evento:**

```json
{
  "name":        "AJO Brand Purchase",
  "xdmSchemaId": "https://ns.adobe.com/brandname/schemas/purchase-event-v1",
  "transformer":  "{\"_id\": _id, \"event_name\": \"purchase\", \"timestamp\": timestamp, \"utc_offset\": _brandname.transactions.utcOffset, \"location_id\": _brandname.transactions.storeNumber, \"transaction_id\": _brandname.transactions.transactionId, \"loyalty_identity\": {\"id\": _brandname.identities.loyaltyId}, \"item_list\": _brandname.transactions.lineItems.{\"item_set\": [skuNumber, category], \"quantity\": qty, \"unit_price\": priceAmount, \"sub_total\": priceAmount * qty}}"
}
```

**Transformador con formato:**

```jsonata
{
  "_id":            _id,
  "event_name":     "purchase",
  "timestamp":      timestamp,
  "utc_offset":     _brandname.transactions.utcOffset,
  "location_id":    _brandname.transactions.storeNumber,
  "transaction_id": _brandname.transactions.transactionId,
  "loyalty_identity": {
    "id": _brandname.identities.loyaltyId
  },
  "item_list": _brandname.transactions.lineItems.{
    "item_set":   [skuNumber, category],
    "quantity":   qty,
    "unit_price": priceAmount,
    "sub_total":  priceAmount * qty
  }
}
```

> **Nota:** Cuando un evento coincide con el ID de esquema XDM, el transformador solo recibe la parte `xdmEntity` del evento, no el sobre exterior de AJO. Todas las rutas de la expresión del transformador son relativas al cuerpo de la entidad XDM.

+++

## Adición de la validación del esquema JSON (opcional)

Si desea que la plataforma valide la estructura de los eventos entrantes antes de intentar la transformación, establezca el campo `schema` en un documento [Esquema JSON](https://json-schema.org/draft-04) codificado como una cadena JSON.

Los eventos que no superan la validación del esquema se rechazan antes de ejecutar la transformación. La respuesta de error incluye el error de validación específico, lo que facilita el diagnóstico de eventos ascendentes con formato incorrecto.

+++Ejemplo de esquema (por ejemplo, el 2 anterior)

```json
{
  "$schema": "http://json-schema.org/draft-04/schema#",
  "type": "object",
  "required": ["_id", "timestamp", "transaction", "member"],
  "properties": {
    "_id":       { "type": "string" },
    "timestamp": { "type": "string", "format": "date-time" },
    "member": {
      "type": "object",
      "required": ["loyaltyId"],
      "properties": {
        "loyaltyId": { "type": "string" }
      }
    },
    "transaction": {
      "type": "object",
      "required": ["items"],
      "properties": {
        "transactionId": { "type": "string" },
        "items": {
          "type": "array",
          "items": {
            "type": "object",
            "required": ["sku", "qty", "lineTotal"],
            "properties": {
              "sku":       { "type": "string" },
              "category":  { "type": "string" },
              "qty":       { "type": "number" },
              "unitPrice": { "type": "number" },
              "lineTotal": { "type": "number" }
            }
          }
        }
      }
    }
  }
}
```

+++

Pase este esquema como una cadena JSON minificada en el campo `schema` de la definición del evento.

## Reserva: eventos de fidelidad nativos

Si ninguna definición de evento coincide con un evento entrante, la plataforma intenta introducirlo directamente como un evento de fidelidad de Adobe nativo. Si la carga útil ya se ajusta al formato de evento de fidelidad descrito anteriormente, no se necesita ningún transformador y el evento se aplica tal cual. Esto permite a los clientes que han formateado previamente sus eventos evitar la transformación por completo.

## Referencia de la API

Todas las operaciones de definición de eventos utilizan la ruta base `/loyalty/metadata/config/events`.

+++Creación de una definición de evento

```http
POST /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":        "Retail POS Purchase",
  "xdmSchemaId": "https://ns.adobe.com/yourtenant/schemas/retail-pos-purchase-v1",
  "transformer": "{ ... }"
}
```

+++

+++Enumerar definiciones de eventos

```http
GET /loyalty/metadata/config/events
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

+++Actualizar una definición de evento

```http
PUT /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
Content-Type: application/json

{
  "name":        "Retail POS Purchase (v2)",
  "transformer": "{ ... updated expression ... }"
}
```

+++

+++Eliminar una definición de evento

```http
DELETE /loyalty/metadata/config/events/{eventId}
x-gw-ims-org-id: {ORG_ID}
x-sandbox-name: {SANDBOX}
```

+++

## Validación del transformador

Las expresiones JSONata se validan para la sintaxis cuando se guarda la definición del evento. Si la expresión no es válida, la API devuelve un error `422` con una descripción del error de análisis.

Para probar un transformador antes de implementarlo, use [JSONata Exerciser](https://try.jsonata.org/): pegue el evento de origen como entrada y la expresión del transformador para comprobar que la salida coincide con el formato de evento de fidelidad esperado.

## Problemas comunes

Todos estos errores se ejecutan sin errores en una carga útil de prueba de un solo elemento, por lo que no se detectan. Antes de su implementación, pruebe siempre el transformador con una carga útil con dos o más productos.

+++Creación de un objeto en lugar de asignarlo a la matriz

El error más frecuente. Si se usa un solo objeto literal con `productListItems.SKU`, se extraen todos los SKU y todas las cantidades en secuencias agrupadas, en lugar de producir un elemento de línea por producto.

**✗Contrae todos los elementos en uno:**

```jsonata
"item_list": [
  {
    "item_set": [ productListItems.SKU ],
    "quantity": productListItems.quantity
  }
]
```

Con dos productos, `item_set` contiene ambos SKU y `quantity` se convierte en una matriz como `[1, 4]`.

**✓Un elemento de línea por producto:**

```jsonata
"item_list": [
  productListItems.{
    "item_set": [SKU],
    "quantity": quantity
  }
]
```

El mapa `.{ }` se ejecuta una vez por producto para que cada uno se convierta en su propia entrada.

+++

+++Olvidando el índice de matriz en la identidad

`identityMap.Email` es una matriz. Sin `[0]`, si un perfil tiene más de una identidad en ese área de nombres, `id` se convierte en una lista de valores en lugar de una sola cadena.

**✗** `identityMap.Email.id`

**✓** `identityMap.Email[0].id`

+++

+++Abastecimiento de identidad desde un campo de inquilino personalizado

Los grupos de campos personalizados a veces exponen un campo de aspecto electrónico como `_yourtenant.identification.core.email`. En los datos de ejemplo, devuelve un valor y tiene un aspecto correcto, pero en los eventos de producción suele estar vacío, lo que provoca que `loyalty_identity.id` salga como nulo. Use siempre `identityMap` como origen de identidad.

+++

+++Una matriz anidada que se filtra en `item_set`

Agregar un campo de categoría a `item_set` parece sencillo, pero si `productCategories` es en sí mismo una matriz, el resultado se amplía de forma impredecible.

**✗puede producir más entradas de las esperadas:**

```jsonata
"item_set": [SKU, productCategories.categoryID]
```

Un producto con tres categorías genera un(a) `item_set` con cuatro valores.

**✓Indexe la matriz anidada para obtener exactamente un valor:**

```jsonata
"item_set": [SKU, productCategories[0].categoryID]
```

+++

+++`item_list` está vacío o falta

Un evento con un `item_list` vacío o ausente se rechazó como no válido. Para los eventos no transaccionales (registros, déclencheur personalizados) no hay elementos de línea naturales, por lo que debe producir uno sintético:

```jsonata
"item_list": [{ "item_set": [eventName], "quantity": 1 }]
```

+++

+++`timestamp` como un entero Unix epoch en lugar de ISO 8601

La plataforma espera una cadena ISO 8601. Si el evento de origen lleva milisegundos desde epoch, conviértalo:

```jsonata
"timestamp": $fromMillis(timestamp)
```

+++

+++`utc_offset` omitido

Sin `utc_offset`, la coincidencia de la ventana de la parte del día y el recuento de rachas de día consecutivo se omiten. Asigne el desplazamiento UTC de la tienda o el dispositivo desde el evento de origen siempre que esté disponible.

+++

+++Rutas del transformador relativas a la envolvente de AJO en un evento de DCCS

Para los eventos de DCCS, el transformador recibe solamente el cuerpo de `xdmEntity`, no el sobre externo de AJO. Todas las rutas deben ser relativas a la raíz de la entidad XDM. Si la expresión hace referencia a campos que residen en el sobre exterior (p. ej. `/body/xdmMeta/...`), no se encontrarán y generarán un valor nulo de forma silenciosa.

+++
