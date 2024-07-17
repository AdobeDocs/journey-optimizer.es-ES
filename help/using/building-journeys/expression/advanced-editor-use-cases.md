---
solution: Journey Optimizer
product: journey optimizer
title: Uso del editor de expresiones avanzadas
description: Aprenda a crear expresiones avanzadas
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: expresión, condición, casos de uso, eventos
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 1%

---

# Ejemplos de expresiones avanzadas{#advanced-expression-examples}

El editor de expresiones avanzadas se puede utilizar para crear condiciones que le permitan filtrar a los usuarios en sus recorridos. Estas condiciones le permiten dirigirse a los usuarios en función del tiempo, la fecha, la ubicación, la duración o las acciones como la compra o el abandono de carros de compras para que se puedan reorientar en el recorrido.

>[!NOTE]
>
>Los eventos comienzan por @, las fuentes de datos con #.

## Creación de condiciones en eventos de experiencia

El editor de expresiones avanzadas es obligatorio para realizar consultas en series temporales como una lista de compras o clics pasados en mensajes. Estas consultas no se pueden realizar con el editor simple.

Los eventos de experiencia se recuperan de Adobe Experience Platform como una colección en orden cronológico inverso, por lo tanto:

* La primera función devolverá el evento más reciente.
* la última función devolverá la más antigua.

Por ejemplo, supongamos que desea dirigirse a los clientes con un abandono del carro de compras en los últimos 7 días para enviarles un mensaje cuando el cliente se acerca a una tienda, con una oferta de los artículos que querían y que están en la tienda.

**Debe generar las siguientes condiciones:**

En primer lugar, los clientes de destino que navegaron por la tienda en línea, pero no finalizaron el pedido en los últimos 7 días.

<!--**This expression looks for a specified value in a string value:**

`In (“addToCart”, #{field reference from experience event})`-->

**Esta expresión busca todos los eventos de este usuario especificados en los últimos siete días:**

A continuación, selecciona todos los eventos del carro de compras que no se transformaron en una compra completa.

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
