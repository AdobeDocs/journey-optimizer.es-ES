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
source-git-commit: e539d694e8fb91b6a8c7ba7ff5a2bb0905651f81
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 1%

---

# Ejemplos de expresiones avanzadas{#advanced-expression-examples}

La editor expresión Avanzadas se puede utilizar para crear condiciones que le permitan filtrar usuarios en sus viajes. Estas condiciones le permiten destino a los usuarios sobre hora, fecha, ubicación, duración o acciones como la compra o el abandono de carritos para que puedan ser redirigidos en el viaje.

>[!CAUTION]
>
>Se admite el uso de eventos de experiencia en expresiones o condiciones de recorrido, pero no se recomienda. Si su caso de uso requiere el uso de eventos de experiencia, considere métodos alternativos como [atributos calculados o crear un segmento usar los eventos e incorporar ese segmento en [`inAudience` las expresiones](../../building-journeys/functions/functioninaudience.md).](../../audience/computed-attributes.md)


## Condiciones de construcción en eventos de experiencia

El editor expresión avanzado es obligatorio para realizar consultas en series temporales como un lista de compras o clics anteriores en mensajes. Dichas consultas no se pueden realizar con el editor simple.

>[!NOTE]
>
>Los eventos empiezan por @ y los orígenes de datos por #.

Los eventos experiencia se recuperan de Adobe Experience Platform como un colección en orden cronológico inverso, por lo tanto:

* La primera función devolverá el evento más reciente.
* la última función devolverá la más antigua.

Por ejemplo, supongamos que desea dirigirse a los clientes con un abandono del carro de compras en los últimos 7 días para enviarles un mensaje cuando el cliente se acerca a una tienda, con una oferta de los artículos que querían y que están en la tienda.

**Debe versión las siguientes condiciones:**

En primer lugar, destino clientes que navegaron por el en línea tienda pero no finalizaron el pedido en los últimos 7 días.

<!--**This expression looks for a specified value in a string value:**

`In ("addToCart", #{field reference from experience event})`-->

**Este expresión busca todos los eventos de la usuario especificada en los últimos 7 días:**

Luego selecciona todos los eventos addtocart que no se transformaron en completePurchase.

>[!NOTE]
>
>Para insertar campos en el expresión rápidamente, haga clic doble el campo en el panel izquierdo del editor.

La marca de tiempo especificada actúa como el valor de fecha y hora, el segundo es el número de días.

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

Este expresión devuelve un booleano.

**Ahora vamos a versión un expresión comprobar que el producto está en stock**

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

Desde allí puede agregar otra ruta en su viaje para cuando el producto no esté en tienda y enviar notificación con participación oferta. Configure los mensajes en consecuencia y utilice personalización datos para mejorar la destino del mensaje.

## Ejemplos de manipulaciones de cadenas con el editor expresión avanzado

**En condiciones**

Esta condición recupera solo los eventos de geovalla activados en &quot;Arlington&quot;:

```json
        @event{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

Explicación: Se trata de una comparación estricta de cadenas (con distinción de mayúsculas y minúsculas), equivalente a un consulta en modo simple que utiliza `equal to` con `Is sensitive` elementos marcados.

La misma consulta con `Is sensitive` sin marcar generará el siguiente expresión en modo avanzado:

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
