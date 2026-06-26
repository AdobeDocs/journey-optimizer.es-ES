---
solution: Journey Optimizer
product: journey optimizer
title: Uso del editor de expresiones avanzadas
description: Aprenda a crear expresiones avanzadas
feature: Journeys
role: Developer
level: Experienced
hide: true
keywords: expresión, condición, casos de uso, eventos
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/UUeCcATC7MFHsLuI8TPoVHqwVe9GOXUq3U3RoAG-a1o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1103
ht-degree: 2%

---

# Ejemplos de expresiones avanzadas{#advanced-expression-examples}

El editor de expresiones avanzadas se puede utilizar para crear condiciones que le permitan filtrar a los usuarios en sus recorridos. Estas condiciones permiten segmentar usuarios en función de la hora, la fecha, la ubicación y la duración, de modo que puedan volver a segmentarse en el recorrido.

>[!CAUTION]
>
>No se admite el uso de eventos de experiencia en expresiones/condiciones de recorrido. Si su caso de uso requiere el uso de eventos de experiencia, considere métodos alternativos. [Más información](../exp-event-lookup.md)


## Creación de condiciones en eventos de experiencia


>[!CAUTION]
>
>No se admite el uso de eventos de experiencia en expresiones/condiciones de recorrido. Si su caso de uso requiere el uso de eventos de experiencia, considere métodos alternativos. [Más información](../exp-event-lookup.md)
>



El editor de expresiones avanzadas es obligatorio para realizar consultas en series temporales como una lista de compras o clics pasados en mensajes. Estas consultas no se pueden realizar con el editor simple.

>[!NOTE]
>
>Los eventos comienzan por @, las fuentes de datos con #.

Los eventos de experiencia se recuperan de Adobe Experience Platform como una colección en orden cronológico inverso, por lo tanto:

* La primera función devolverá el evento más reciente.
* la última función devolverá la más antigua.

Por ejemplo, supongamos que desea dirigirse a los clientes con un abandono del carro de compras en los últimos 7 días para enviarles un mensaje cuando el cliente se acerca a una tienda, con una oferta de los artículos que querían y que están en la tienda.

**Debe generar las siguientes condiciones:**

En primer lugar, los clientes de destino que navegaron por la tienda en línea, pero no finalizaron el pedido en los últimos 7 días.

**Esta expresión busca un valor especificado en un valor de cadena:**

`In ("addToCart", #{field reference from experience event})`

**Esta expresión busca todos los eventos de este usuario especificados en los últimos siete días:**

A continuación, selecciona todos los eventos de agregar al carro de compras que no se transformaron en una compra completa.

>[!NOTE]
>
>Para insertar campos en la expresión rápidamente, haga doble clic en el campo en el panel izquierdo del editor.

La marca de tiempo especificada actúa como valor de fecha y hora; la segunda es el número de días.

```json
        in( "addToCart", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction})
        and
        not(in( "completePurchase", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction}))
```

Esta expresión devuelve un valor booleano.

**Ahora vamos a crear una expresión para comprobar que el producto está disponible**

* En Inventory, esta expresión busca el campo de cantidad de un producto y especifica que debe ser mayor que 0.

`#{Inventory.fieldgroup3.quantity} > 0`

* A la derecha, se especifican los valores necesarios, aquí, necesitamos recuperar la ubicación de la tienda, que está asignada desde la ubicación del evento &quot;ArriveLumaStudio&quot;:

`#{ArriveLumaStudio._acpevangelists1.location.location}`

* Y especifique el SKU, utilizando la función `first` para recuperar la interacción &quot;addToCart&quot; más reciente:

  ```json
      #{ExperiencePlatformDataSource
                      .ExperienceEventFieldGroup
                      .experienceevent
                      .first(
                      currentDataPackField
                      .productData
                      .productInteraction == "addToCart"
                      )
                      .SKU}
  ```

A partir de ahí, puede añadir otra ruta en el recorrido para los casos en los que el producto no esté en la tienda y enviar una notificación con una oferta de participación. Configure los mensajes según corresponda y utilice datos de personalización para mejorar el destinatario de mensajes.

## Filtrado de marcas de tiempo en expresiones

Al hacer referencia a varios eventos de actividad de carro de compras, especifique una ventana de marca de tiempo de inicio y otra de finalización para evitar recoger datos históricos. Por ejemplo:

```json
toDateTimeOnly(currentDataPackField.timestamp) >= toDateTimeOnly(@event{poc_UDXCartAddSavedCheckOutEv.timestamp})
AND
toDateTimeOnly(currentDataPackField.timestamp) < toDateTimeOnly(nowWithDelta(4, "hours"))
```

## Ejemplos de manipulaciones de cadenas con el editor de expresiones avanzadas

**En condiciones**

Esta condición recupera solo los eventos de geovalla activados en &quot;Arlington&quot;:

```json
        @event{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

Explicación: Se trata de una comparación de cadenas estricta (con distinción de mayúsculas y minúsculas), equivalente a una consulta en modo simple que utiliza `equal to` con `Is sensitive` marcado.

La misma consulta con `Is sensitive` sin marcar generará la siguiente expresión en modo avanzado:

```json
        equalIgnoreCase(@event{GeofenceEntry
                        .placeContext
                        .POIinteraction
                        .POIDetail
                        .name}, "Arlington")
```

**En acciones**

La siguiente expresión le permite definir el CRM ID en un campo de personalización de acción:

```json
substr(
   @event{MobileAppLaunch
   ._myorganization
   .identification
   .crmid},
   1, 
   lastIndexOf(
     @event{MobileAppLaunch
     ._myorganization
     .identification
     .crmid},
     '}'
   )
)
```

Explicación: Este ejemplo utiliza las funciones `substr` y `lastIndexOf` para eliminar llaves que encierran el ID de CRM pasado con un evento de inicio de aplicación móvil.


Para obtener más información sobre cómo usar el editor de expresiones avanzadas, vea [este vídeo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/introduction-to-building-a-journey.html?lang=es).

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página proporciona ejemplos prácticos del uso del editor de expresiones avanzadas para generar condiciones de recorrido que filtran a los usuarios por actividad de carro de compras, estado de inventario, eventos de geovalla, manipulaciones de cadenas y ventanas de marca de tiempo.

**Intenciones:**

* Generar una condición de abandono del carro de compras con `in()` y `inLastDays()` para aproximarse a los usuarios que agregaron artículos pero no completaron la compra en un plazo de 7 días
* Filtre las colecciones de eventos de experiencia por ventana de marca de tiempo para evitar capturar datos históricos
* Aplique comparaciones de cadenas que distinguen entre mayúsculas y minúsculas y que no distinguen entre mayúsculas y minúsculas a los campos de eventos de geovalla
* Extraer y manipular los ID de CRM desde eventos de inicio de aplicaciones móviles mediante `substr` y `lastIndexOf`
* Comprobar la disponibilidad del inventario de productos comparando un campo de cantidad con un umbral
* Combinar varias expresiones booleanas utilizando la lógica `and` / `not` en condiciones de recorrido

**Glosario:**

* **Editor de expresiones avanzadas**: La interfaz de Journey Optimizer para escribir expresiones complejas de nivel de código mediante funciones, operadores y referencias de campo *(específico del producto)*
* **currentDataPackField**: una variable de bucle utilizada al iterar colecciones de orígenes de datos dentro de `all()`, `first()` o `last()` funciones *(específicas del producto)*
* **inLastDays(timestamp, N)**: Una función de fecha que devuelve el valor &quot;True&quot; si la marca de tiempo especificada se encuentra dentro de los últimos N días *(específicos del producto)*
* **Eventos de experiencia**: registros de datos de comportamiento de series de tiempo almacenados en Adobe Experience Platform, recuperados en orden cronológico inverso *(específicos del producto)*

**Protecciones:**

* No se admite el uso directo de eventos de experiencia en expresiones/condiciones de recorrido; en su lugar, se deben utilizar métodos alternativos como atributos calculados o segmentos de audiencia
* Se debe utilizar el editor de expresiones avanzadas (no el editor simple) para consultas sobre datos de series temporales como colecciones de compras o clics
* Al hacer doble clic en un campo del panel izquierdo, se inserta rápidamente en la expresión; evite escribir las rutas de campo manualmente para reducir los errores
* Expresiones que consultan eventos de experiencia devuelven un valor booleano; asegúrese de que la lógica descendente espere un tipo booleano.

**Terminología:**

* Nombre canónico: Editor de expresiones avanzadas — Acrónimo: none — variantes: editor de expresiones, editor avanzado
* Sinónimos: &quot;addToCart&quot; = &quot;add to cart interaction&quot;; &quot;completePurchase&quot; = &quot;purchase completion event&quot;
* No confunda: eventos (con el prefijo `@`) ≠ fuentes de datos (con el prefijo `#`)

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Por qué debo usar el editor avanzado en lugar del editor simple para consultas de abandono del carro de compras?** — El editor simple no puede realizar consultas en colecciones de series temporales; se requiere el editor avanzado para las funciones de colección `all()`, `first()` y `last()`.
* **Q: ¿Cómo hago referencia al evento &quot;addToCart&quot; más reciente en una expresión?** — Utilice la función `first()` en la colección de eventos de experiencia filtrada por `productInteraction == "addToCart"`, ya que los eventos se devuelven en orden cronológico inverso.
* **Q: ¿Cómo puedo hacer que una comparación de cadenas no distinga mayúsculas de minúsculas en el editor avanzado?** — Utilice la función `equalIgnoreCase()` en lugar del operador `==`.
* **Q: ¿Cuál es el propósito de agregar una ventana de marca de tiempo al consultar los eventos del carro de compras?** — Especificar una marca de tiempo de inicio y de fin impide que se recojan datos históricos que no entren en la ventana de actividad prevista.
* **Q: ¿Cómo elimino llaves de una cadena de ID de CRM pasada en un evento?** — Use `substr()` combinado con `lastIndexOf()` para extraer el contenido entre llaves.

+++
