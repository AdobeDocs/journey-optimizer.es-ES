---
solution: Journey Optimizer
product: journey optimizer
title: Funciones de administración de colecciones
description: Obtenga información sobre los tipos de datos en las funciones de administración de colecciones
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: consulta, colecciones, funciones, carga útil, recorrido
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
source-git-commit: 8e020f79e0f44e6fc804fcceb149146f9644c777
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 3%

---

# Funciones de administración de colecciones {#collection-management-functions}


## Acerca de las funciones de recopilación de consultas

El lenguaje de expresión también introduce un conjunto de funciones para consultar colecciones. Estas funciones se explican a continuación.

En el siguiente ejemplo, usemos la carga útil de evento que contiene una colección:

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

## La función all(`<condition>`)

La función **[!UICONTROL all]** habilita la definición de un filtro en una colección determinada mediante una expresión booleana.

```json
<listExpression>.all(<condition>)
```

Por ejemplo, entre todos los usuarios de la aplicación, puede obtener los que usan IOS 13 (expresión booleana &quot;app used == IOS 13&quot;). El resultado de esta función es la lista filtrada que contiene elementos que coinciden con la expresión booleana (ejemplo: usuario de aplicación 1, usuario de aplicación 34, usuario de aplicación 432).

En una actividad de condición de Data Source puede comprobar si el resultado de la función **[!UICONTROL all]** es nulo o no. También puede combinar esta función **[!UICONTROL all]** con otras funciones como **[!UICONTROL count]**. Para obtener más información, consulte [Actividad de la condición de Data Source](../condition-activity.md#data_source_condition).


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
>* Cuando la condición de filtrado de la función **all()** esté vacía, el filtro devolverá todos los elementos de la lista. **Sin embargo, para contar el número de elementos de una colección, no es necesaria la función all.
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
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}`
```

El resultado es `token_2`.