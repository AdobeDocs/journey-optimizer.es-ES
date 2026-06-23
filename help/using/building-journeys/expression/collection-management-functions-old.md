---
solution: Journey Optimizer
product: journey optimizer
title: Funciones de administración de colecciones
description: Obtenga información sobre los tipos de datos en las funciones de administración de colecciones
feature: Journeys
hide: true
role: Developer
level: Experienced
keywords: consulta, colecciones, funciones, carga útil, recorrido
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1222
ht-degree: 1%

---

# Funciones de administración de colecciones

El lenguaje de expresión también introduce un conjunto de funciones para consultar colecciones.

Estas funciones se explican a continuación. En el siguiente ejemplo, usemos la carga útil de evento que contiene una colección:

```json
                { 
   "_experience":{ 
      "campaign":{ 
         "message":{ 
            "profile":{ 
               "pushNotificationTokens":[ 
                  { 
                     "token":"token_1",
                     "application":{ 
                        "_id":"APP1",
                        "name":"MarltonMobileApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_2",
                     "application":{ 
                        "_id":"APP2",
                        "name":"MarketplaceApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_3",
                     "application":{ 
                        "_id":"APP3",
                        "name":"VendorApp",
                        "version":"2.0"
                     }
                  }
               ]
            }
         }
      }
   },
   "timestamp":"1536160728"
}
```

**La función &quot;all(`<condition>`)&quot;**

La función **[!UICONTROL all]** habilita la definición de un filtro en una colección determinada mediante una expresión booleana.

```json
<listExpression>.all(<condition>)
```

Por ejemplo, entre todos los usuarios de la aplicación, puede obtener los que usan IOS 13 (expresión booleana &quot;app used == IOS 13&quot;). El resultado de esta función es la lista filtrada que contiene elementos que coinciden con la expresión booleana (ejemplo: usuario de aplicación 1, usuario de aplicación 34, usuario de aplicación 432).

En una actividad de condición de Data Source puede comprobar si el resultado de la función **[!UICONTROL all]** es nulo o no. También puede combinar esta función **[!UICONTROL all]** con otras funciones como **[!UICONTROL count]**. Para obtener más información, consulte [Actividad de la condición de Data Source](../conditions.md#data_source_condition).


## Ejemplos

>[!CAUTION]
>
>Se admite el uso de eventos de experiencia en expresiones/condiciones de recorrido, pero no se recomienda. Si su caso de uso requiere el uso de eventos de experiencia, considere métodos alternativos como [atributos calculados](../../audience/computed-attributes.md) o la creación de un segmento utilizando los eventos e incorporando ese segmento en [`inAudience` expresiones](../../building-journeys/functions/functioninaudience.md).

**Ejemplo 1:**

Queremos comprobar si un usuario ha instalado una versión específica de una aplicación. Para esto, obtenemos todos los tokens de notificaciones push asociados con aplicaciones móviles para las que la versión es 1.0. A continuación, realizamos una condición con la función **[!UICONTROL count]** para comprobar que la lista devuelta de tokens contiene al menos un elemento.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

El resultado es true.

**Ejemplo 2:**

Aquí utilizamos la función **[!UICONTROL count]** para comprobar si hay tokens de notificación push en la colección.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```

El resultado será true.

<!--
Alternatively, you can check if there is no token in the collection:

   ```json
   count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) == 0
   ```

The result will be false.

Here we use the count function in a condition to count the number of push notification tokens in the event.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token})`

The result is true.

Note that when the condition in the **all()** function is empty, the filter will return all the elements in the list. Hence, the expression above is equivalent to:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.application.name})`

In both cases, the result of the expression is **3**.

A query of experience events recorded on the Adobe Experience Platform may or may not include the current event that triggered the current Journey. This will depend on the relative processing time with which [!DNL Journey Orchestration] sees an event and started evaluating conditions, versus the time it takes for that event to be ingested into the Adobe Experience Platform. For example, when using the .all() syntax to query experience events from the Adobe Experience Platform, we recommend enforcing the exclusion of the current event (by requiring an
earlier timestamp) in order to only consider prior events.
-->

>[!NOTE]
>
>Cuando la condición de filtrado de la función **all()** esté vacía, el filtro devolverá todos los elementos de la lista. **Sin embargo, para contar el número de elementos de una colección, no se requiere la función all.**


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

El resultado de la expresión es **3**.

**Ejemplo 3:**

Aquí comprobamos si una persona no ha recibido ninguna comunicación en las últimas 24 horas. Filtramos la colección de eventos de experiencia recuperados de la fuente de datos de Experience Platform, utilizando dos expresiones basadas en dos elementos de la colección. En particular, la marca de tiempo del evento se compara con el valor dateTime devuelto por la función **[!UICONTROL nowWithDelta]**.

```json
count(#{ExperiencePlatform.MarltonExperience.experienceevent.all(
   currentDataPackField.directMarketing.sends.value > 0 and
   currentDataPackField.timestamp > nowWithDelta(-1, "days")).timestamp}) == 0
```

El resultado es true si no hay ningún evento de experiencia que coincida con las dos condiciones.

**Ejemplo 4:**

Aquí deseamos comprobar si un individuo ha iniciado al menos una aplicación en los últimos 7 días, para, por ejemplo, almacenar en déclencheur una notificación push que le invite a iniciar un tutorial.

```json
count(
 #{ExperiencePlatform.AnalyticsData.experienceevent.all(
 nowWithDelta(-7,"days") <= currentDataPackField.timestamp
 and currentDataPackField.application.firstLaunches.value > 0
)._id}) > 0
```

<!--
**"All + Count" example 4:** here we use the count function in a boolean expression to see if there is push notification tokens in the collection.

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) > 0`

The result will be:

`true`

Alternatively, you can check if there is NO token in the collection:

`count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) =0`

The result will be:

`false`
-->

>[!NOTE]
>
>**[!UICONTROL currentEventField]** solo está disponible al manipular colecciones de eventos, **[!UICONTROL currentDataPackField]** al manipular colecciones de fuentes de datos y **[!UICONTROL currentActionField]** al manipular colecciones de respuestas de acciones personalizadas.
>
>Al procesar colecciones con **[!UICONTROL all]**, **[!UICONTROL first]** y **[!UICONTROL last]**, realizamos un bucle en cada elemento de la colección uno por uno. **[!UICONTROL currentEventField]**, **currentDataPackField** y **[!UICONTROL currentActionField]** corresponden al elemento que se está realizando un bucle.

**Las funciones &quot;first(`<condition>`)&quot; y &quot;last(`<condition>`)&quot;**

Las funciones **[!UICONTROL first]** y **[!UICONTROL last]** también habilitan la definición de un filtro en la colección al devolver el primer/último elemento de la lista que cumple con el filtro.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

**Ejemplo 1:**

Esta expresión devuelve el primer token de notificación push asociado a aplicaciones móviles para las que la versión es 1.0.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token
```

El resultado es &quot;token_1&quot;.

**Ejemplo 2:**

Esta expresión devuelve el último token de notificación push asociado a aplicaciones móviles para las que la versión es 1.0.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

El resultado es &quot;token_2&quot;.

>[!NOTE]
>
>Los eventos de experiencia se recuperan de Adobe Experience Platform como una colección en orden cronológico inverso, por lo tanto:
>
>* **[!UICONTROL primera]** función devolverá el evento más reciente
>* **[!UICONTROL última]** función devolverá la más antigua.

**Ejemplo 3:**

Comprobamos si el primer evento de Adobe Analytics (el más reciente) con un valor distinto de cero para el ID de DMA tiene un valor igual a 602.

```json
#{ExperiencePlatform.AnalyticsProd_EvarsProps.experienceevent.first(
currentDataPackField.placeContext.geo.dmaID > 0).placeContext.geo.dmaID} == 602
```

**La función &quot;at(`<index>`)&quot;**

La función **[!UICONTROL at]** le permite hacer referencia a un elemento específico de una colección según un índice.
El índice 0 es el primer índice de la colección.

_`<listExpression>`.at(`<index>`)_

**Ejemplo:**

Esta expresión devuelve el segundo token de notificación push de la lista.

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

El resultado es &quot;token_2&quot;.

**Otros ejemplos**

Esta expresión devuelve los nombres de producto en función del valor SKU. La lista de estos productos se incluye en la lista de eventos, con la condición de que sea el ID de evento.

```json
#{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.all(currentDataPackField._aepgdcdevenablement2.purchase_event.receipt_nbr == "10-337-4016"). 
_aepgdcdevenablement2.purchase_event.productListItems.all(currentDataPackField.SKU == "AB17 1234 1775 19DT B4DR 8HDK 762").name}
```

Esta expresión recupera el nombre del último producto de la lista de productos de un evento de comercio donde el tipo de evento es productListAdds y el precio total es superior o igual a 150.

```json
 #{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.last(
currentDataPackField.eventType == "commerce.productListAdds").productListItems.last(currentDataPackField.priceTotal >= 150).name}
```

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explican las funciones de administración de colecciones `all()`, `first()`, `last()` y `at()` disponibles en el lenguaje de expresión de Recorrido, con ejemplos que utilizan cargas útiles de token de notificación push y datos de evento de experiencia.

**Intenciones:**

* Filtre una colección con una condición booleana con `all(<condition>)` para recuperar los elementos coincidentes
* Contar elementos en una colección utilizando la función `count()` combinada con `all()`
* Recuperar el primer o último elemento de una colección filtrada usando `first()` o `last()`
* Obtener acceso a un elemento específico de una colección mediante el índice mediante `at(<index>)`
* Combinar consultas de colección anidadas para buscar nombres de productos por SKU o por tipo de evento y umbral de precio

**Glosario:**

* **all(condition)**: Función de colección que filtra una lista y devuelve elementos que coinciden con la expresión booleana dada *(product-specific)*
* **first(condition)**: función de colección que devuelve el primer elemento (el más reciente, para eventos de experiencia) que coincide con la condición *(específica del producto)*
* **last(condition)**: función de colección que devuelve el último elemento (el más antiguo, para eventos de experiencia) que coincide con la condición *(específica del producto)*
* **at(index)**: función de colección que devuelve el elemento en un índice específico basado en cero *(específico del producto)*
* **currentEventField**: variable de bucle disponible al iterar colecciones de eventos dentro de `all()`, `first()` o `last()` *(específico del producto)*
* **currentDataPackField**: variable de bucle disponible al iterar colecciones de orígenes de datos *(específica del producto)*
* **currentActionField**: variable de bucle disponible al iterar en colecciones de respuestas de acción personalizada *(específica del producto)*

**Protecciones:**

* Se admite el uso de eventos de experiencia en expresiones/condiciones de recorrido, pero no se recomienda; considere los atributos calculados o segmentos de audiencia como alternativas
* `currentEventField` solo está disponible para colecciones de eventos; `currentDataPackField` para colecciones de orígenes de datos; `currentActionField` para colecciones de respuestas de acciones personalizadas
* La función `all` no es necesaria para contar elementos de una colección: `count()` se puede aplicar directamente al campo de colección
* Los eventos de experiencia se recuperan en orden cronológico inverso: `first()` devuelve el evento más reciente, `last()` devuelve el más antiguo

**Terminología:**

* Nombre canónico: Funciones de administración de colecciones — Acrónimo: none — variantes: funciones de colección, funciones de colección de consultas
* Sinónimos: &quot;all()&quot; = &quot;función de filtro&quot;; &quot;first()&quot; = &quot;función de elemento más reciente&quot; (para eventos de experiencia)
* No confunda: `first()` (evento de experiencia más reciente) ≠ primer elemento por orden de inserción

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Qué devuelve `all()` cuando la condición está vacía?** — Devuelve todos los elementos de la lista, lo que equivale a no aplicar ningún filtro.
* **Q: ¿Cómo cuento el número de tokens de notificaciones push en una colección?** — Utilice `count()` directamente en la ruta del campo de token sin requerir `all()`, p. ej. `count(@event{...pushNotificationTokens.token})`.
* **Q: ¿Cómo obtengo el segundo elemento de una colección?** — Utilice `at(1)`, ya que el índice 0 es el primer elemento.
* **Q: ¿Por qué `first()` devuelve el evento de experiencia más reciente?** — Los eventos de experiencia se recuperan de Adobe Experience Platform en orden cronológico inverso, por lo que `first()` elige el elemento superior (más reciente).
* **Q: ¿Cómo compruebo si un usuario no ha recibido ninguna comunicación en las últimas 24 horas?** — Filtre la colección de eventos de experiencia con `nowWithDelta(-1, "days")` como límite inferior de marca de tiempo y use `count(...) == 0`.

+++
