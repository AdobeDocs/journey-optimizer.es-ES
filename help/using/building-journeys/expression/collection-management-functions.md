---
solution: Journey Optimizer
product: journey optimizer
title: Funciones de administración de colecciones
description: Obtenga información sobre los tipos de datos en las funciones de administración de colecciones
feature: Journeys
role: Developer
level: Experienced
keywords: consulta, colecciones, funciones, carga útil, recorrido
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sNFI7l-UMGmRV2wRcvYa56tILLoWFxXeG3N5txgrUiw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1000
ht-degree: 1%

---

# Funciones de administración de colecciones {#collection-management-functions}


## Acerca de las funciones de recopilación de consultas

El lenguaje de expresión también introduce un conjunto de funciones para consultar colecciones. Estas funciones se explican a continuación.

En los ejemplos siguientes, se utiliza un evento denominado &quot;LobbyBeacon&quot; que contiene una colección de tokens de notificaciones push. Los ejemplos de esta página utilizan la estructura de carga útil de evento que se muestra a continuación:

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

>[!NOTE]
>
>En los ejemplos siguientes, se hace referencia a esta carga útil mediante `@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens}`, donde &quot;LobbyBeacon&quot; es el nombre del evento y el resto de la ruta corresponde a la estructura mostrada anteriormente.

## La función all(`<condition>`)

La función **[!UICONTROL all]** habilita la definición de un filtro en una colección determinada mediante una expresión booleana.

```json
<listExpression>.all(<condition>)
```

**Ejemplo conceptual:** Entre todos los usuarios de la aplicación, puede obtener los que usan IOS 13 (expresión booleana &quot;app used == IOS 13&quot;). El resultado de esta función es la lista filtrada que contiene elementos que coinciden con la expresión booleana (ejemplo: usuario de aplicación 1, usuario de aplicación 34, usuario de aplicación 432).

En una actividad de condición de Data Source puede comprobar si el resultado de la función **[!UICONTROL all]** es nulo o no. También puede combinar esta función **[!UICONTROL all]** con otras funciones como **[!UICONTROL count]**. Para obtener más información, consulte [Actividad de la condición de Data Source](../conditions.md#data_source_condition).

**Ejemplos de código que utilizan la carga útil de LobbyBeacon:**

Los ejemplos siguientes utilizan la carga útil de evento que se muestra en la parte superior de esta página.


>[!CAUTION]
>
>No se admite el uso de eventos de experiencia en expresiones/condiciones de recorrido. Si su caso de uso requiere el uso de eventos de experiencia, considere métodos alternativos. [Más información](../exp-event-lookup.md)

### Ejemplo 1

Queremos comprobar si un usuario ha instalado una versión específica de una aplicación. Para esto, obtenemos todos los tokens de notificaciones push asociados con aplicaciones móviles para las que la versión es 1.0. A continuación, realizamos una condición con la función **[!UICONTROL count]** para comprobar que la lista devuelta de tokens contiene al menos un elemento.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

El resultado es true.

### Ejemplo 2

Aquí utilizamos la función **[!UICONTROL count]** para comprobar si hay tokens de notificación push en la colección.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```


El resultado es true.


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

El resultado de la expresión es **3**.


>[!NOTE]
>
>* Cuando la condición de filtrado de la función **all()** esté vacía, el filtro devolverá todos los elementos de la lista. **Sin embargo, para contar el número de elementos de una colección, no se requiere la función all.**
>
>* `currentEventField` solo está disponible al manipular colecciones de eventos, `currentDataPackField` al manipular colecciones de orígenes de datos y `currentActionField` al manipular colecciones de respuestas de acciones personalizadas.
>
>  Al procesar colecciones con `all`, `first` y `last`, realizamos un bucle en cada elemento de la colección uno por uno. `currentEventField`, `currentDataPackField` y `currentActionField` corresponden al elemento que se está reproduciendo en bucle.


## Funciones first(`<condition>`) y last(`<condition>`)

Las funciones **[!UICONTROL first]** y **[!UICONTROL last]** también habilitan la definición de un filtro en la colección al devolver el primer/último elemento de la lista que cumple con el filtro.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

### Ejemplo 1

Esta expresión devuelve el primer token de notificación push asociado a aplicaciones móviles para las que la versión es 1.0.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token}
```

El resultado es `token_1`.

### Ejemplo 2

Esta expresión devuelve el último token de notificación push asociado a aplicaciones móviles para las que la versión es 1.0.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

El resultado es `token_2`.

## Función at(`<index>`)

La función **[!UICONTROL at]** le permite hacer referencia a un elemento específico de una colección según un índice.
El índice 0 es el primer índice de la colección.

_`<listExpression>`.at(`<index>`)_

### Ejemplo

Esta expresión devuelve el segundo token de notificación push de la lista.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

El resultado es `token_2`.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página documenta las funciones de administración de colecciones `all()`, `first()`, `last()` y `at()` utilizadas en el editor de expresiones avanzadas de Recorrido, ilustradas con ejemplos de carga útil de token de notificación push.

**Intenciones:**

* Filtre una colección de campos de evento o de origen de datos con una condición booleana con `all(<condition>)`
* Contar elementos de colección filtrados o sin filtrar usando `count()` combinados con funciones de colección
* Recuperar el primer o último elemento coincidente de una colección utilizando `first()` o `last()`
* Obtener acceso a un elemento de colección en un índice específico basado en cero mediante `at(<index>)`
* Comprenda qué variable de bucle (`currentEventField`, `currentDataPackField`, `currentActionField`) se aplica a cada contexto de colección

**Glosario:**

* **all(condition)**: filtra una colección y devuelve todos los elementos que coinciden con la expresión booleana dada *(product-specific)*
* **first(condition)**: Devuelve el primer elemento (el más reciente para eventos de experiencia) de una colección que coincide con la condición *(específica del producto)*
* **last(condition)**: devuelve el último elemento (el más antiguo para los eventos de experiencia) de una colección que coincide con la condición *(específica del producto)*
* **at(index)**: devuelve el elemento en el índice de base cero especificado de una colección *(específica del producto)*
* **currentEventField**: La variable de bucle solo está disponible cuando se iteran las colecciones de eventos *(específica del producto)*
* **currentDataPackField**: La variable de bucle solo está disponible cuando se iteran las colecciones de orígenes de datos *(específicas del producto)*
* **currentActionField**: La variable de bucle solo está disponible cuando se iteran las colecciones de respuestas de acción personalizada *(específica del producto)*

**Protecciones:**

* No se admite el uso de eventos de experiencia en expresiones/condiciones de recorrido; considere métodos alternativos como atributos calculados
* `currentEventField`, `currentDataPackField` y `currentActionField` solo están disponibles dentro de sus respectivos contextos de colección
* La función `all` no es necesaria para contar los elementos de colección: `count()` se puede aplicar directamente a la ruta de campo
* Cuando se llama a `all()` con una condición vacía, se devuelven todos los elementos de la colección

**Terminología:**

* Nombre canónico: Funciones de administración de colecciones — Acrónimo: none — variantes: funciones de colección, funciones de colección de consultas
* Sinónimos: &quot;all()&quot; = &quot;función de filtro de colección&quot;; &quot;at()&quot; = &quot;descriptor de acceso de índice&quot;
* No confunda: `first()` (evento de experiencia más reciente) ≠ primer elemento insertado en las listas generales

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Cuál es la diferencia entre `all()` con una condición vacía y `all()` con una condición?** — Un `all()` vacío devuelve todos los elementos; un `all()` basado en condiciones devuelve solamente los elementos que coinciden con esa expresión booleana.
* **Q: ¿Cómo cuento los tokens de notificaciones push sin usar `all()`?** — Llamar a `count()` directamente en la ruta del campo de token, p. ej. `count(@event{LobbyBeacon...pushNotificationTokens.token})`.
* **Q: ¿Qué variable se usa para hacer referencia al elemento actual al realizar un bucle en una colección de origen de datos?** — Usar `currentDataPackField` dentro de `all()`, `first()` o `last()` en colecciones de orígenes de datos.
* **Q: ¿Cómo obtengo el segundo elemento de una colección?** — Utilice `at(1)` porque el índice 0 es el primer elemento.
* **Q: ¿Por qué `last()` devuelve el evento de experiencia más antiguo?** — Los eventos de experiencia se almacenan en orden cronológico inverso, de modo que la última posición de la colección corresponde al evento más antiguo.

+++
