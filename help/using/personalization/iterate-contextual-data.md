---
solution: Journey Optimizer
product: journey optimizer
title: Iteración sobre datos contextuales
description: Aprenda a repetir matrices de varias fuentes de contexto mediante la sintaxis Handlebars
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
hide: true
hidefromtoc: true
keywords: expresión, editor, handlebars, iteration, array, context, personalization
source-git-commit: d3a06e15440dc58267528444f90431c3b32b49f2
workflow-type: tm+mt
source-wordcount: '2704'
ht-degree: 0%

---

# Iteración sobre datos contextuales {#personalization-contexts}

Aprenda a utilizar la sintaxis de la iteración Handlebars para mostrar listas dinámicas de datos de varias fuentes en los mensajes, incluidos eventos, respuestas de acciones personalizadas y otros datos contextuales.

## Información general {#overview}

Journey Optimizer proporciona acceso a datos contextuales de varios orígenes durante la [personalización de mensajes](personalize.md). Puede iterar matrices de estos orígenes utilizando la sintaxis Handlebars en canales nativos ([email](../email/get-started-email-design.md), [push](../push/create-push.md), [SMS](../sms/create-sms.md)) para mostrar contenido dinámico como listas de productos, recomendaciones u otros elementos repetitivos.

**Orígenes de contexto disponibles:**

* **[Eventos](#event-data)**: datos de eventos de recorrido (eventos empresariales, eventos unitarios)
* **[Respuestas de acción personalizada](#custom-action-responses)**: datos devueltos por llamadas de API externas a través de acciones personalizadas
* **[Búsqueda de conjuntos de datos](#dataset-lookup)**: Datos enriquecidos recuperados de conjuntos de datos de Adobe Experience Platform
* **[Propiedades técnicas](#technical-properties)**: metadatos de Recorrido, como identificador de recorrido e identificadores suplementarios
* **[Contexto de Recorrido](#other-contexts)**: se puede obtener acceso a otros datos relacionados con el recorrido durante la ejecución

Esta guía muestra cómo repetir matrices de cada una de estas fuentes en los mensajes, y cómo trabajar con matrices al configurar actividades de recorrido. Comience con [Sintaxis de iteraciones de Handlebars](#syntax) para comprender los conceptos básicos de personalización de mensajes o salte a [Trabaje con matrices en expresiones de Recorrido](#arrays-in-journeys) para aprender a pasar datos de matrices a acciones personalizadas y búsquedas de conjuntos de datos.

## Sintaxis de iteración Handlebars {#syntax}

Handlebars proporciona `{{#each}}` [helper](functions/helpers.md) para iterar en matrices. La sintaxis básica es:

```handlebars
{{#each arrayPath as |item|}}
  <!-- Access item properties here -->
  {{item.property}}
{{/each}}
```

**Puntos clave:**

* Reemplazar `arrayPath` por la ruta a los datos de la matriz
* Reemplazar `item` por cualquier nombre de variable que prefiera (por ejemplo, `product`, `response`, `element`)
* Obtener acceso a las propiedades de cada elemento mediante `{{item.propertyName}}`
* Puede anidar varios bloques de `{{#each}}` para matrices de varios niveles

## Iterar sobre datos de evento {#event-data}

Los datos de evento están disponibles cuando el recorrido se activa mediante un [evento](../event/about-events.md). Esto resulta útil para mostrar los datos capturados en el momento en que comenzó el recorrido, como el contenido del carro de compras, los elementos de pedidos o los envíos de formularios.

>[!TIP]
>
>Puede combinar datos de evento con otras fuentes. Consulte [Combinar varios orígenes de contexto](#combine-sources) para ver ejemplos.

### Ruta de contexto para eventos

```handlebars
context.journey.events.<event_ID>.<fieldPath>
```

* `<event_ID>`: el identificador único del evento, tal como se configuró en el recorrido
* `<fieldPath>`: la ruta de acceso al campo o matriz dentro del esquema de evento

### Ejemplo: Elementos de carro de compras de un evento

Si el [esquema de evento](../event/experience-event-schema.md) incluye una matriz `productListItems` (formato XDM estándar [4&rbrace;), puede mostrar el contenido del carro de compras como se detalla en el ejemplo siguiente.](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target="_blank"}

+++ Ver código de ejemplo

```handlebars
{{#each context.journey.events.event_ID.productListItems as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}
```

+++

### Ejemplo: matrices anidadas en eventos

Para las estructuras anidadas, utilice bloques anidados `{{#each}}`.

+++ Ver código de ejemplo

```handlebars
{{#each context.journey.events.event_ID.categories as |category|}}
  <h2>{{category.name}}</h2>
  <ul>
    {{#each category.items as |item|}}
      <li>{{item.title}}</li>
    {{/each}}
  </ul>
{{/each}}
```

+++

Más información sobre cómo anidar en [Prácticas recomendadas](#best-practices).

## Iterar en respuestas de acciones personalizadas {#custom-action-responses}

Las respuestas de [acción personalizada](../action/about-custom-action-configuration.md) contienen datos devueltos por llamadas a API externas. Esto resulta útil para mostrar información en tiempo real de sus sistemas, como puntos de lealtad, recomendaciones de productos, estados de inventario u ofertas personalizadas.

>[!NOTE]
>
>Las acciones personalizadas deben configurarse con una carga útil de respuesta para utilizar esta función. Obtenga más información en [esta sección](../action/action-response.md#config-response). También puede combinar respuestas de acciones personalizadas con datos de evento o búsquedas de conjuntos de datos. Vea [Combinar varias fuentes de contexto](#combine-sources) para ver ejemplos.

### Ruta de contexto para acciones personalizadas

```handlebars
context.journey.actions.<actionName>.<fieldPath>
```

* `<actionName>`: el nombre de su [acción personalizada](../action/about-custom-action-configuration.md) según la configuración del recorrido
* `<fieldPath>`: la ruta de acceso al campo o matriz dentro de la carga útil de respuesta

### Ejemplo: Recomendaciones de producto desde una API

Para iterar una matriz de recomendaciones de productos devueltas por una acción personalizada y mostrarlas como tarjetas individuales en el mensaje, consulte el ejemplo siguiente.

+++ Ver código de ejemplo

**Respuesta de API:**

```json
{
  "recommendations": [
    {
      "productId": "12345",
      "productName": "Summer Jacket",
      "price": 89.99,
      "imageUrl": "https://example.com/jacket.jpg"
    },
    {
      "productId": "67890",
      "productName": "Running Shoes",
      "price": 129.99,
      "imageUrl": "https://example.com/shoes.jpg"
    }
  ]
}
```

**Personalización de mensaje:**

```handlebars
<h2>Recommended for You</h2>
<div class="recommendations">
  {{#each context.journey.actions.GetRecommendations.recommendations as |item|}}
    <div class="product-card">
      <img src="{{item.imageUrl}}" alt="{{item.productName}}" />
      <h3>{{item.productName}}</h3>
      <p class="price">${{item.price}}</p>
    </div>
  {{/each}}
</div>
```

+++

### Ejemplo: matrices anidadas de acciones personalizadas

Para iterar una respuesta de acción personalizada que contenga matrices anidadas (una matriz de objetos, donde cada objeto contiene otra matriz), vea el ejemplo siguiente. Esto demuestra el uso de bucles `{{#each}}` anidados para acceder a varios niveles de datos.

+++ Ver código de ejemplo

**Respuesta de API:**

```json
{    
  "id": "84632848268632",    
  "responses": [
    { "productIDs": [1111, 2222, 3333] },
    { "productIDs": [4444, 5555, 6666] },
    { "productIDs": [7777, 8888, 9999] }
  ]
}
```

**Personalización de mensaje:**

```handlebars
<h2>Product Groups</h2>
{{#each context.journey.actions.GetProducts.responses as |response|}}
  <div class="product-group">
    <ul>
      {{#each response.productIDs as |productID|}}
        <li>Product ID: {{productID}}</li>
      {{/each}}
    </ul>
  </div>
{{/each}}
```

+++

Para ver patrones de anidación más complejos, consulte [Prácticas recomendadas](#best-practices).

### Ejemplo: Beneficios del nivel de fidelización

Para mostrar los beneficios dinámicos en función del estado de fidelidad, consulte el siguiente ejemplo.

+++ Ver código de ejemplo

**Respuesta de API:**

```json
{
  "loyaltyTier": "gold",
  "benefits": [
    { "name": "Free shipping", "icon": "truck" },
    { "name": "20% discount", "icon": "percent" },
    { "name": "Priority support", "icon": "headset" }
  ]
}
```

**Personalización de mensaje:**

```handlebars
<h2>Your {{context.journey.actions.GetLoyaltyInfo.loyaltyTier}} Member Benefits</h2>
<ul class="benefits">
  {{#each context.journey.actions.GetLoyaltyInfo.benefits as |benefit|}}
    <li>
      <span class="icon-{{benefit.icon}}"></span>
      {{benefit.name}}
    </li>
  {{/each}}
</ul>
```

+++

## Iterar sobre resultados de búsqueda de conjuntos de datos {#dataset-lookup}

La [actividad de búsqueda de conjuntos de datos](../building-journeys/dataset-lookup.md) le permite recuperar datos de [conjuntos de datos de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=es){target="_blank"} durante el tiempo de ejecución del recorrido. Los datos enriquecidos se almacenan como una matriz y se pueden repetir en los mensajes.

>[!AVAILABILITY]
>
>La actividad Búsqueda de conjuntos de datos solo está disponible para un conjunto limitado de organizaciones. Para obtener acceso, póngase en contacto con su representante de Adobe.

Obtenga más información acerca de cómo configurar la actividad Búsqueda de conjuntos de datos en [esta sección](../building-journeys/dataset-lookup.md). La búsqueda de conjuntos de datos es particularmente eficaz cuando se combina con datos de evento. Vea [Ejemplo: Datos de evento enriquecidos con la búsqueda de conjuntos de datos](#combine-sources) para obtener un caso de uso práctico.

### Ruta de contexto para búsquedas de conjuntos de datos

```handlebars
context.journey.datasetLookup.<activityID>.entities
```

* `<activityID>`: ID único de su actividad de búsqueda de conjuntos de datos
* `entities`: matriz de datos enriquecidos recuperados del conjunto de datos

### Ejemplo: Detalles de un producto de un conjunto de datos

Si utiliza una actividad de búsqueda de conjuntos de datos para recuperar información del producto basada en SKU, consulte el siguiente ejemplo.

+++ Ver código de ejemplo

**Configuración de búsqueda de conjuntos de datos:**

* Claves de búsqueda: `list(@event{purchase_event.products.sku})`
* Campos que se van a devolver: `["SKU", "category", "price", "name"]`

**Personalización de mensaje:**

```handlebars
<h2>Product Details</h2>
<table>
  <thead>
    <tr>
      <th>Product Name</th>
      <th>Category</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    {{#each context.journey.datasetLookup.3709000.entities as |product|}}
      <tr>
        <td>{{product.name}}</td>
        <td>{{product.category}}</td>
        <td>${{product.price}}</td>
      </tr>
    {{/each}}
  </tbody>
</table>
```

+++

### Ejemplo: Iteración filtrada con datos del conjunto de datos

Para filtrar los resultados de búsqueda del conjunto de datos durante la iteración y mostrar solo los elementos que coinciden con criterios específicos (por ejemplo, productos de una categoría en particular), utilice instrucciones `{{#if}}` condicionales dentro del bucle `{{#each}}`. Consulte el ejemplo siguiente.

+++ Ver código de ejemplo

```handlebars
<h2>Household Products</h2>
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {{#if product.category = "household"}}
    <div class="product">
      <h3>{{product.name}}</h3>
      <p>Price: ${{product.price}}</p>
    </div>
  {{/if}}
{{/each}}
```

+++

Obtenga más información acerca del filtrado condicional en [Prácticas recomendadas](#best-practices).

### Ejemplo: Calcular totales de búsqueda de conjuntos de datos

Para calcular y mostrar los totales mientras se iteran los resultados de búsqueda del conjunto de datos, vea el ejemplo siguiente.

+++ Ver código de ejemplo

```handlebars
{% let householdTotal = 0 %}
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {%#if product.category = "household"%}
    {% let householdTotal = householdTotal + product.price %}
  {%/if%}
{{/each}}

<p>Your household products total: ${{householdTotal}}</p>
```

+++

## Usar propiedades técnicas del recorrido {#technical-properties}

Las propiedades técnicas de recorrido proporcionan acceso a los metadatos sobre la ejecución de la recorrido, como el ID de recorrido y los identificadores suplementarios. Pueden resultar útiles cuando se combinan con patrones de iteración, especialmente para filtrar matrices basadas en instancias de recorrido específicas.

### Propiedades técnicas disponibles

```handlebars
context.journey.technicalProperties.journeyUID
context.journey.technicalProperties.supplementalId
```

### Ejemplo: Filtrado de elementos de matriz mediante un identificador suplementario

Cuando se utilizan identificadores suplementarios en recorridos activados por eventos con matrices, se puede filtrar para mostrar solo el elemento relevante para la instancia de recorrido actual. Obtenga más información acerca de los identificadores suplementarios en [esta guía](../building-journeys/supplemental-identifier.md).

**Escenario**: se activa un recorrido con varias reservas, pero desea mostrar información solo para la reserva específica (identificada por el ID suplementario) que activó esta instancia de recorrido.

+++ Ver código de ejemplo

```handlebars
{{#each context.journey.events.event_ID.bookingList as |booking|}}
  {%#if booking.bookingInfo.bookingNum = context.journey.technicalProperties.supplementalId%}
    <div class="booking-details">
      <h3>Your Booking: {{booking.bookingInfo.bookingNum}}</h3>
      <p>Destination: {{booking.bookingInfo.bookingCountry}}</p>
      <p>Date: {{booking.bookingInfo.bookingDate}}</p>
    </div>
  {%/if%}
{{/each}}
```

+++

### Ejemplo: Incluir ID de recorrido para el seguimiento

Para incluir el ID de recorrido en el mensaje con fines de seguimiento, consulte el ejemplo siguiente.

+++ Ver código de ejemplo

```handlebars
<footer>
  <p>Journey Reference: {{context.journey.technicalProperties.journeyUID}}</p>
</footer>
```

+++

## Combinación de varias fuentes de contexto {#combine-sources}

Puede combinar datos de diferentes fuentes en el mismo mensaje para crear experiencias personalizadas y enriquecidas. En esta sección se muestran ejemplos prácticos de cómo usar varias fuentes de contexto juntas.

**Orígenes de contexto que se pueden combinar:**

* [Datos de evento](#event-data) + [respuestas de acción personalizada](#custom-action-responses)
* [Datos de evento](#event-data) + [Búsqueda de conjuntos de datos](#dataset-lookup)
* [Múltiples orígenes](#combine-sources) + [propiedades técnicas](#technical-properties)

### Ejemplo: Artículos del carro de compras con inventario en tiempo real

Para combinar datos de evento (contenido del carro de compras) con datos de acción personalizados (estado de inventario), vea el siguiente ejemplo.

+++ Ver código de ejemplo

```handlebars
<h2>Your Cart</h2>
{{#each context.journey.events.cartEvent.productListItems as |product|}}
  <div class="cart-item">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}

<h2>We Also Recommend</h2>
{{#each context.journey.actions.GetRecommendations.items as |recommendation|}}
  <div class="recommendation">
    <h4>{{recommendation.name}}</h4>
    <p>${{recommendation.price}}</p>
    {{#if recommendation.inStock}}
      <span class="badge">In Stock</span>
    {{else}}
      <span class="badge out-of-stock">Out of Stock</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### Ejemplo: datos de evento enriquecidos con la búsqueda de conjuntos de datos

Para combinar [SKU de evento](#event-data) con información detallada del producto a partir de una [búsqueda de conjunto de datos](#dataset-lookup), vea el ejemplo a continuación.

+++ Ver código de ejemplo

```handlebars
<h2>Your Order Details</h2>
{{#each context.journey.events.orderEvent.productListItems as |item|}}
  <div class="order-item">
    <p><strong>SKU:</strong> {{item.SKU}}</p>
    <p><strong>Quantity:</strong> {{item.quantity}}</p>
    
    <!-- Enrich with dataset lookup data -->
    {{#each context.journey.datasetLookup.1234567.entities as |enrichedProduct|}}
      {{#if enrichedProduct.SKU = item.SKU}}
        <p><strong>Product Name:</strong> {{enrichedProduct.name}}</p>
        <p><strong>Category:</strong> {{enrichedProduct.category}}</p>
        <img src="{{enrichedProduct.imageUrl}}" alt="{{enrichedProduct.name}}" />
      {{/if}}
    {{/each}}
  </div>
{{/each}}
```

+++

### Ejemplo: combinación de varias fuentes con propiedades técnicas

Para combinar varias fuentes de contexto (datos de perfil, datos de evento, acciones personalizadas y propiedades técnicas) en un solo mensaje, vea el siguiente ejemplo.

+++ Ver código de ejemplo

```handlebars
<div class="personalized-content">
  <!-- Profile data -->
  <h1>Hello {{profile.person.name.firstName}},</h1>
  
  <!-- Event data iteration -->
  <h2>Your Recent Purchases</h2>
  {{#each context.journey.events.purchaseEvent.items as |purchase|}}
    <div class="purchase">
      <p>{{purchase.productName}} - ${{purchase.price}}</p>
    </div>
  {{/each}}
  
  <!-- Custom action response iteration -->
  <h2>Recommended for You</h2>
  {{#each context.journey.actions.GetPersonalizedRecs.recommendations as |rec|}}
    <div class="recommendation">
      <h3>{{rec.title}}</h3>
      <p>{{rec.description}}</p>
    </div>
  {{/each}}
  
  <!-- Technical properties -->
  <footer>
    <p class="fine-print">Journey ID: {{context.journey.technicalProperties.journeyUID}}</p>
  </footer>
</div>
```

+++

## Otros tipos de contexto {#other-contexts}

Aunque esta guía se centra en la iteración en matrices, otros tipos de contexto están disponibles para la personalización que generalmente no requieren iteración. Se accede a ellas directamente en lugar de hacerlo en bucle:

* **[Atributos de perfil](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=es){target="_blank"}** (`profile.*`): campos de perfil individuales de Adobe Experience Platform
* **[Audiencias](../audience/about-audiences.md)** (`inAudience()`): Comprobaciones de pertenencia a audiencias
* **[Decisiones de oferta](../offers/get-started/starting-offer-decisioning.md)**: ofertas de administración de decisiones
* **[Atributos de destino](../orchestrated/activities/channels.md#add-personalization)** (solo campañas orquestadas): atributos calculados en el lienzo de la campaña
* **Token** (`context.token`): tokens de sesión o autenticación

Para obtener sintaxis de personalización completa y ejemplos con estas fuentes, consulte:

* [Adición de personalización](personalization-build-expressions.md)
* [Sintaxis de personalización](personalization-syntax.md)

## Trabajo con matrices en expresiones de Recorrido {#arrays-in-journeys}

Mientras que las secciones anteriores se centran en repetir matrices en la personalización de mensajes mediante Handlebars, también puede trabajar con matrices al configurar actividades de recorrido. En esta sección se explica cómo utilizar datos de matriz de eventos en expresiones de Recorrido, especialmente al pasar datos a acciones personalizadas o al utilizar matrices con búsquedas de conjuntos de datos.

>[!IMPORTANT]
>
>Las expresiones de recorrido utilizan una sintaxis diferente a la personalización Handlebars. En la configuración del recorrido (como los parámetros o condiciones de acción personalizados), utiliza el [editor de expresiones de Recorrido](../building-journeys/expression/expressionadvanced.md) con funciones como `first`, `all` y `serializeList`. En el contenido del mensaje, se utiliza la sintaxis Handlebars con bucles `{{#each}}`.

### Pasar valores de matriz a parámetros de acción personalizados {#arrays-to-custom-actions}

Al configurar [acciones personalizadas](../action/about-custom-action-configuration.md), a menudo necesita extraer valores de matrices de eventos y pasarlos como parámetros. Esta sección trata sobre patrones comunes.

Obtenga más información sobre cómo pasar colecciones en [Pasar colecciones a parámetros de acción personalizados](../building-journeys/collections.md#passing-collection).

#### Extraer un solo valor de una matriz

**Caso de uso**: obtenga un campo específico de una matriz de eventos para pasarlo como parámetro de consulta en una solicitud GET.

+++ Ver código de ejemplo

**Ejemplo de escenario**: Extraiga el primer SKU con un precio mayor que 0 de una lista de productos.

**Ejemplo de esquema de evento**:

```json
{
  "commerce": {
    "productListItems": [
      { "SKU": "SKU-1", "priceTotal": 10.0 },
      { "SKU": "SKU-2", "priceTotal": 0.0 },
      { "SKU": "SKU-3", "priceTotal": 20.0 }
    ]
  }
}
```

**Configuración de acción personalizada**:

1. En la acción personalizada, configure un parámetro de consulta (por ejemplo, `sku`) con el tipo `string`
2. Márquelo como `Variable` para permitir valores dinámicos

**Expresión de Recorrido en el parámetro de acción**:

```javascript
@event{YourEventName.commerce.productListItems.first(currentEventField.priceTotal > 0).SKU}
```

**Explicación**:

* `@event{YourEventName}`: hace referencia al evento de recorrido
* `.first(currentEventField.condition)`: devuelve el primer elemento de matriz que coincide con la condición
* `currentEventField`: representa cada elemento de la matriz de eventos a medida que se recorre en bucle
* `.SKU`: extrae el campo SKU del elemento coincidente
* Resultado: `"SKU-1"` (una cadena adecuada para el parámetro de acción)

Obtenga más información acerca de la función `first` en [Funciones de administración de colecciones](../building-journeys/expression/collection-management-functions.md).

+++

#### Creación de una lista de valores a partir de una matriz

**Caso de uso**: cree una lista de identificadores separados por comas para pasarlos como parámetro de consulta (por ejemplo, `/products?ids=sku1,sku2,sku3`).

+++ Ver código de ejemplo

**Configuración de acción personalizada**:

1. Configure un parámetro de consulta (por ejemplo, `ids`) con el tipo `string`
2. Marcar como `Variable`

**expresión de Recorrido**:

```javascript
serializeList(
  @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0).SKU},
  ",",
  true
)
```

**Explicación**:

* `.all(currentEventField.condition)`: devuelve todos los elementos de matriz que coinciden con la condición (devuelve una lista)
* `currentEventField`: representa cada elemento de la matriz de eventos a medida que se recorre en bucle
* `.SKU`: proyecta la lista para incluir solamente valores de SKU
* `serializeList(list, delimiter, addQuotes)`: une la lista en una cadena
   * `","`: usar una coma como delimitador
   * `true`: agregar comillas alrededor de cada elemento de cadena
* Resultado: `"SKU-1,SKU-3"` (adecuado para un parámetro de consulta)

Más información sobre:

* [`all`](../building-journeys/expression/collection-management-functions.md)
* [`serializeList`](../building-journeys/functions/list-functions.md#serializeList)

La administración de colecciones para acciones personalizadas se explica en [Pasar colecciones a parámetros de acción personalizados](../building-journeys/collections.md#passing-collection).

+++

#### Pasar una matriz de objetos a una acción personalizada

**Caso de uso**: Envíe una matriz completa de objetos en un cuerpo de solicitud (para POST o GET con cuerpo).

+++ Ver código de ejemplo

**Ejemplo de cuerpo de solicitud**:

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "Product A",
        "price": 20.1,
        "color": "blue"
      }
    ]
  }
}
```

**Configuración de acción personalizada**:

1. En el cuerpo de la solicitud, defina `products` como tipo `listObject`
2. Marcar como `Variable`
3. Defina los campos de objeto: `id`, `name`, `price`, `color` (cada uno se vuelve asignable)

**configuración de lienzo de Recorrido**:

1. En el modo Avanzado, defina la expresión de colección:

   ```javascript
   @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0)}
   ```

1. En la interfaz de usuario de asignación de colecciones:
   * Asignar `id` → `productListItems.SKU`
   * Asignar `name` → `productListItems.name`
   * Asignar `price` → `productListItems.priceTotal`
   * Asignar `color` → `productListItems.color`

Journey Optimizer construye la matriz de objetos que coinciden con la estructura de carga útil de la acción.

>[!NOTE]
>
>Cuando trabaje con matrices de eventos, utilice `currentEventField` para hacer referencia a cada elemento. Para las colecciones de orígenes de datos (Adobe Experience Platform), use `currentDataPackField`. Para las colecciones de respuestas a acciones personalizadas, use `currentActionField`.

Obtenga más información en [Pasar colecciones a parámetros de acción personalizados](../building-journeys/collections.md#passing-collection).

+++

### Usar matrices con búsquedas de conjuntos de datos {#arrays-with-dataset-lookup}

Al usar la [actividad de búsqueda de conjuntos de datos](../building-journeys/dataset-lookup.md), puede pasar una matriz de valores como claves de búsqueda para recuperar datos enriquecidos.

**Ejemplo**: Busca detalles del producto para todos los SKU de una matriz de eventos.

+++ Ver código de ejemplo

**Configuración de búsqueda de conjuntos de datos**:

En el campo de claves de búsqueda, use `list()` para convertir una ruta de matriz en una lista:

```javascript
list(@event{purchaseEvent.productListItems.SKU})
```

Esto crea una lista de todos los valores SKU que se buscarán en el conjunto de datos. Los resultados están disponibles como una matriz en `context.journey.datasetLookup.<activityID>.entities` en la que puede repetir en su mensaje (vea [Iterar en los resultados de búsqueda del conjunto de datos](#dataset-lookup)).

+++

### Limitaciones y patrones {#array-limitations}

Tenga en cuenta estas limitaciones al trabajar con matrices en recorridos:

#### Sin bucles dinámicos en matrices en el flujo de recorrido

Los recorridos no pueden crear bucles dinámicos en los que se ejecuta un nodo de acción varias veces para cada elemento de una matriz. Esto es intencional para evitar problemas de rendimiento fuera de control.

**Lo que no puedes hacer**:

* Ejecutar una acción personalizada una vez por elemento de matriz de forma dinámica
* Crear varias ramas de recorrido en función de la longitud de la matriz

**Patrones recomendados**:

1. **Enviar todos los elementos a la vez**: pase toda la matriz o una lista serializada a una única acción personalizada que procese todos los elementos. Ver [Crear una lista de valores a partir de una matriz](#arrays-to-custom-actions).

2. **Usar agregación externa**: Haga que la API externa acepte varios ID y devuelva resultados combinados en una sola llamada.

3. **Cálculo previo en AEP**: use [atributos calculados](../audience/computed-attributes.md) para precalcular valores de matrices en el nivel de perfil.

4. **Extracción de un solo valor**: Si solo necesita un valor, extráigalo con `first` o `head`. Consulte [Extraer un solo valor de una matriz](#arrays-to-custom-actions).

Obtenga más información en [Protecciones y limitaciones](../start/guardrails.md).

#### Consideraciones de tamaño de matriz

Las cabinas grandes pueden afectar al rendimiento del recorrido:

* **Matrices de eventos**: Mantenga las cargas de eventos por debajo de los 50 KB en total
* **Respuestas de acción personalizada**: las cargas de respuesta deben ser inferiores a 100 KB
* **Resultados de búsqueda de conjuntos de datos**: limitar el número de claves de búsqueda y entidades devueltas

### Ejemplo completo: Matriz de eventos para la acción personalizada. {#complete-example}

Este es un flujo de trabajo completo que muestra cómo utilizar una matriz de eventos con una acción personalizada.

**Escenario**: cuando un usuario abandona el carro, envía los datos del carro a una API de recomendaciones externa para obtener sugerencias personalizadas y luego mostrarlas en un correo electrónico.

+++ Ver código de ejemplo

**Paso 1: Configurar la acción personalizada**

Cree una acción personalizada &quot;GetCartRecommendations&quot;:

* **Método**: POST
* **URL**: `https://api.example.com/recommendations`
* **Cuerpo de solicitud**:

```json
{
  "cartItems": [
    {
      "sku": "string",
      "price": 0,
      "quantity": 0
    }
  ]
}
```

* Marcar `cartItems` como tipo `listObject` y `Variable`
* Definir campos: `sku` (cadena), `price` (número), `quantity` (entero)

Más información en [Configurar una acción personalizada](../action/about-custom-action-configuration.md).

**Paso 2: Configurar carga útil de respuesta**

En la acción personalizada, configure la respuesta:

```json
{
  "recommendations": [
    {
      "productId": "string",
      "productName": "string",
      "price": 0,
      "imageUrl": "string"
    }
  ]
}
```

Obtenga más información en [Usar respuestas de llamadas API](../action/action-response.md).

**Paso 3: Conectar la acción en el recorrido**

1. Después del evento de abandono del carro de compras, agregue la acción personalizada
1. En el modo Avanzado de la colección `cartItems`:

   ```javascript
   @event{cartAbandonment.commerce.productListItems.all(currentEventField.quantity > 0)}
   ```

1. Asigne los campos de recopilación:
   * `sku` → `productListItems.SKU`
   * `price` → `productListItems.priceTotal`
   * `quantity` → `productListItems.quantity`

**Paso 4: usa la respuesta de tu correo electrónico**

En el contenido del correo electrónico, recorra en iteración las recomendaciones:

```handlebars
<h2>We noticed you left these items in your cart</h2>
{{#each context.journey.events.cartAbandonment.productListItems as |item|}}
  <div class="cart-item">
    <p>{{item.name}} - Quantity: {{item.quantity}}</p>
  </div>
{{/each}}

<h2>You might also like</h2>
{{#each context.journey.actions.GetCartRecommendations.recommendations as |rec|}}
  <div class="recommendation">
    <img src="{{rec.imageUrl}}" alt="{{rec.productName}}" />
    <h3>{{rec.productName}}</h3>
    <p>${{rec.price}}</p>
  </div>
{{/each}}
```

**Paso 5: Prueba tu configuración**

Antes de ejecutar un recorrido en directo, pruebe la acción personalizada utilizando la función &quot;Enviar solicitud de prueba&quot; en la configuración de acción para comprobar la solicitud y los valores creados.

1. Usar [modo de prueba de recorrido](../building-journeys/testing-the-journey.md)
2. Déclencheur con datos de evento de ejemplo que incluyen una matriz `productListItems`
3. Compruebe que la acción personalizada recibe la estructura de matriz correcta
4. Comprobar los [registros de prueba de acción](../action/action-response.md#test-mode-logs)
5. Previsualice el correo electrónico para confirmar que ambas matrices se muestran correctamente

Más información en [Solucionar problemas de tus acciones personalizadas](../action/troubleshoot-custom-action.md).

+++

## Prácticas recomendadas {#best-practices}

Siga estas prácticas recomendadas al iterar sobre datos contextuales para crear una personalización mantenible y con rendimiento.

### Uso de nombres de variables descriptivos

Elija nombres de variables que indiquen claramente sobre qué está iterando. Esto hace que su código sea más legible y fácil de mantener. Más información sobre [sintaxis de personalización](personalization-syntax.md):

+++ Ver código de ejemplo

```handlebars
<!-- Good -->
{{#each products as |product|}}
{{#each users as |user|}}
{{#each recommendations as |recommendation|}}

<!-- Less clear -->
{{#each items as |item|}}
{{#each array as |element|}}
```

+++

### Gestión de matrices vacías

Utilice la cláusula `{{else}}` para proporcionar contenido de reserva cuando una matriz esté vacía. Más información sobre [funciones de ayuda](functions/helpers.md):

+++ Ver código de ejemplo

```handlebars
{{#each context.journey.actions.GetRecommendations.items as |item|}}
  <div>{{item.name}}</div>
{{else}}
  <p>No recommendations available at this time.</p>
{{/each}}
```

+++

### Combinación con ayudantes condicionales

Use `{{#if}}` en bucles para contenido condicional. Obtenga más información acerca de [reglas condicionales](create-conditions.md) y vea ejemplos en las secciones [Respuestas de acciones personalizadas](#custom-action-responses) y [Búsqueda de conjuntos de datos](#dataset-lookup).

+++ Ver código de ejemplo

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    {{#if product.onSale}}
      <span class="badge">On Sale!</span>
    {{/if}}
    {{#if product.newArrival}}
      <span class="badge">New</span>
    {{/if}}
  </div>
{{/each}}
```

+++

### Limitar iteración para rendimiento

Para matrices grandes, considere limitar el número de iteraciones:

+++ Ver código de ejemplo

```handlebars
<!-- Display only first 5 items -->
{{#each context.journey.actions.GetProducts.items as |product|}}
  {{#if @index < 5}}
    <div>{{product.name}}</div>
  {{/if}}
{{/each}}
```

+++

### Acceso a metadatos de matriz

Handlebars proporciona variables especiales dentro de bucles que ayudan con los patrones de iteración avanzados:

* `@index`: índice de iteración actual (basado en 0)
* `@first`: True para la primera iteración
* `@last`: True para la última iteración

+++ Ver código de ejemplo

```handlebars
{{#each products as |product|}}
  <div class="product {{#if @first}}featured{{/if}}">
    {{@index}}. {{product.name}}
  </div>
{{/each}}
```

+++

>[!NOTE]
>
>Estas variables Handlebars (`@index`, `@first`, `@last`) solo están disponibles dentro de bucles `{{#each}}` en la personalización de mensajes. Para trabajar con matrices en expresiones de Recorrido (como obtener el primer elemento de una matriz antes de pasar a una acción personalizada), utilice funciones de matriz como [`head`](../personalization/functions/arrays-list.md#head), [`first`](../building-journeys/expression/collection-management-functions.md) o [`all`](../building-journeys/expression/collection-management-functions.md). Consulte [Trabajo con matrices en expresiones de Recorrido](#arrays-in-journeys) para obtener más información.

## Resolución de problemas {#troubleshooting}

¿Tiene problemas con la iteración? Esta sección cubre problemas y soluciones comunes.

### La matriz no se muestra

**Problema**: La iteración de la matriz no muestra ningún contenido.

+++ Ver posibles causas y soluciones

**Posibles causas y soluciones**:

1. **Ruta incorrecta**: compruebe la ruta exacta a la matriz en función del origen de contexto:
   * Para [eventos](#event-data): `context.journey.events.<event_ID>.<fieldPath>`
   * Para [acciones personalizadas](#custom-action-responses): `context.journey.actions.<actionName>.<fieldPath>`
   * Para [búsquedas de conjuntos de datos](#dataset-lookup): `context.journey.datasetLookup.<activityID>.entities`

2. **La matriz está vacía**: agregue una cláusula `{{else}}` para comprobar si la matriz no tiene datos. Consulte [Prácticas recomendadas](#best-practices) para ver ejemplos.

3. **Los datos aún no están disponibles**: Asegúrese de que la acción personalizada, el evento o la actividad de búsqueda del conjunto de datos se haya ejecutado antes de la actividad de mensaje en el flujo de recorrido.

+++

### Errores de sintaxis

**Problema**: Error en la validación de la expresión o no se representa el mensaje.

+++ Ver errores comunes

**Errores comunes**:

* Faltan etiquetas de cierre: Cada `{{#each}}` debe tener un `{{/each}}`. Revise [Sintaxis de iteración de Handlebars](#syntax) para obtener la estructura adecuada.
* Nombre de variable incorrecto: Asegúrese de utilizar de forma coherente el nombre de la variable en todo el bloque. Consulte [Prácticas recomendadas](#best-practices) para conocer las convenciones de nomenclatura.
* Separadores de ruta incorrectos: utilice puntos (`.`), no barras oblicuas ni otros caracteres

+++

### Prueba de las iteraciones

Use [modo de prueba de recorrido](../building-journeys/testing-the-journey.md) para comprobar las iteraciones. Esto es especialmente importante cuando se usan [acciones personalizadas](#custom-action-responses) o [búsquedas de conjuntos de datos](#dataset-lookup):

+++ Ver pasos de prueba

1. Inicie su recorrido en [modo de prueba](../building-journeys/testing-the-journey.md)
2. Almacenar en déclencheur el evento o la acción personalizada con datos de ejemplo
3. Compruebe [message preview](../content-management/preview.md) para verificar que la iteración se muestre correctamente
4. Revise los registros del modo de prueba en busca de errores (consulte [Registros del modo de prueba de acción personalizada](../action/action-response.md#test-mode-logs))

+++

## Temas relacionados {#related-topics}

**Aspectos básicos de Personalization:** [Introducción a la personalización](personalize.md) | [Agregar personalización](personalization-build-expressions.md) | [Sintaxis de Personalization](personalization-syntax.md) | [Funciones de ayuda](functions/helpers.md) | [Crear reglas condicionales](create-conditions.md)

**Configuración del Recorrido:** [Acerca de los eventos](../event/about-events.md) | [Configurar acciones personalizadas](../action/about-custom-action-configuration.md) | [Pasar colecciones a parámetros de acción personalizados](../building-journeys/collections.md#passing-collection) | [Usar respuestas de llamadas API en acciones personalizadas](../action/action-response.md) | [Solucionar problemas de tus acciones personalizadas](../action/troubleshoot-custom-action.md) | [Usar datos de Adobe Experience Platform en recorrido](../building-journeys/dataset-lookup.md) | [Usar identificadores suplementarios en los recorridos](../building-journeys/supplemental-identifier.md) | [Protecciones y limitaciones](../start/guardrails.md) | [Pruebe su recorrido](../building-journeys/testing-the-journey.md)

**Funciones de expresión de Recorrido:** [Editor de expresiones avanzadas](../building-journeys/expression/expressionadvanced.md) | [Funciones de administración de colecciones](../building-journeys/expression/collection-management-functions.md) (primero, todo, último) | [Funciones de lista](../building-journeys/functions/list-functions.md) (serializeList, filter, sort) | [Funciones de matriz](../personalization/functions/arrays-list.md) (cabeza, cola)

**Casos de uso de Personalization:** [Correo electrónico de abandono del carro de compras](personalization-use-case-helper-functions.md) | [Notificación de estado del pedido](personalization-use-case.md)

**Diseño de mensaje:** [Introducción al diseño de correo electrónico](../email/get-started-email-design.md) | [Crear notificaciones push](../push/create-push.md) | [Crear mensajes SMS](../sms/create-sms.md) | [Previsualizar y probar tu contenido](../content-management/preview-test.md)

