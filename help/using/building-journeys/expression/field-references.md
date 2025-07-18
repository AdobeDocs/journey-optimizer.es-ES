---
solution: Journey Optimizer
product: journey optimizer
title: Referencias del campo
description: Obtenga información sobre las referencias de campo en expresiones avanzadas
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: recorrido, campo, expresión, evento
exl-id: 2348646a-b205-4b50-a08f-6625e92f44d7
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 2%

---

# Referencias del campo {#field-references}

Se puede adjuntar una referencia de campo a un evento o a un grupo de campos. La única información significativa es el nombre del campo y su ruta.

Si utiliza caracteres especiales en un campo, debe utilizar comillas dobles o simples. Estos son los casos en los que se necesitan comillas:

* el campo comienza con caracteres numéricos
* el campo comienza con el carácter &quot;-&quot;
* el campo contiene cualquier cosa que no sea: _a_-_z_, _A_-_Z_, _0_-_9_, _, _-_

Por ejemplo, si su campo es _3h_: _#{OpenWeather.weatherData.rain.&#39;3h&#39;} > 0_

```json
// event field
@event{<event name>.<XDM path to the field>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id}

// field group
#{<data source name>.<field group name>.<path to the field>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address}
```

En la expresión, se hace referencia a los campos de evento con &quot;@&quot; y a los campos de fuente de datos con &quot;#&quot;.

Se utiliza un color de sintaxis para distinguir visualmente campos de eventos (verde) de grupos de campos (azul).

## Valores predeterminados para referencias de campo {#default-value}

Se puede asociar un valor predeterminado con un nombre de campo. La sintaxis es la siguiente:

```json
// event field
@event{<event name>.<XDM path to the field>, defaultValue: <default value expression>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue: "example@adobe.com"}
// field group
#{<data source name>.<field group name>.<path to the field>, defaultValue: <default value expression>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address, defaultValue: "example@adobe.com"}
```

>[!NOTE]
>
>El tipo de campo y el valor predeterminado deben ser el mismo. Por ejemplo, `@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue : 2}` no es válido porque el valor predeterminado es un entero, mientras que el valor esperado debe ser una cadena.

Ejemplos:

```json
// for an event 'OrderEvent' having the following payload:
{
    "orderId": "12345"
}
 
expression example:
- @event{OrderEvent.orderId}                                    -> "12345"
- @event{OrderEvent.producdId, defaultValue : "not specified" } -> "not specified" // default value, productId is not a field present in the payload
- @event{OrderEvent.productId}                                  -> null
 
 
// for an entity 'Profile' on datasource 'ACP' having fields person/lastName, with fetched data such as:
{
    "person": {
        "lastName":"Snow"
    },
    "emails": [
        { "email":"john.snow@winterfell.westeros" },
        { "email":"snow@thewall.westeros" }
    ]
}
 
expression examples:
- #{ACP.Profile.person.lastName}                 -> "Snow"
- #{ACP.Profile.emails.at(1).email}              -> "snow@thewall.westeros"
- #{ACP.Profile.person.age, defaultValue : -1}   -> -1 // default value, age is not a field present in the payload
- #{ACP.Profile.person.age}                      -> null
```

Puede agregar cualquier tipo de expresión como valor predeterminado. La única restricción es que la expresión debe devolver el tipo de datos esperado. Cuando se utiliza una función, es necesario encapsular la función con ().

```
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.any.time, defaultValue : (now())} 
== date("2022-02-10T00:00:00Z")
```

## Referencia a un campo dentro de colecciones

Se hace referencia a los elementos definidos dentro de las colecciones mediante las funciones específicas `all`, `first` y `last`. Para obtener más información, consulte [esta página](../expression/collection-management-functions.md).

Ejemplo :

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all()
```

## Referencia a un campo definido en un mapa

### Función `entry`

Para recuperar un elemento en un mapa, utilizamos la función de entrada con una clave determinada. Por ejemplo, se utiliza al definir la clave de un evento, según el área de nombres seleccionada. Para obtener más información, vea [esta página](../../event/about-creating.md#select-the-namespace).

```json
@event{MyEvent.identityMap.entry('Email').first().id}
```

En esta expresión, se obtiene la entrada para la clave &quot;Email&quot; del campo &quot;IdentityMap&quot; de un evento. La entrada &quot;Email&quot; es una colección, de la cual tomamos el &quot;id&quot; en el primer elemento usando &quot;first()&quot;. Para obtener más información, vea [esta página](../expression/collection-management-functions.md).

### Función `firstEntryKey`

Para recuperar la primera clave de entrada de un mapa, utilice la función `firstEntryKey`.

Este ejemplo muestra cómo recuperar la primera dirección de correo electrónico de los suscriptores de una lista específica:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
```

En este ejemplo, la lista de suscripción se denomina `daily-email`. Las direcciones de correo electrónico se definen como claves en el mapa `subscribers`, que está vinculado al mapa de la lista de suscripción.

### Función `keys`

Para recuperar todas las claves de un mapa, utilice la función `keys`.

Este ejemplo muestra cómo recuperar, para un perfil específico, todas las direcciones de correo electrónico asociadas a los suscriptores de una lista específica:

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-mail').subscribers.keys()
```

## Valores de parámetro de una fuente de datos (valores dinámicos de la fuente de datos)

Si selecciona un campo de una fuente de datos externa que requiere que se llame a un parámetro, aparecerá una nueva pestaña a la derecha para que pueda especificar este parámetro. Consulte [esta página](../expression/expressionadvanced.md).

Para casos de uso más complejos, si desea incluir los parámetros del origen de datos en la expresión principal, puede definir sus valores con la palabra clave _params_. Un parámetro puede ser cualquier expresión válida incluso desde otra fuente de datos que también incluya otro parámetro.

>[!NOTE]
>
>Cuando define los valores de parámetro en la expresión, desaparece la pestaña a la derecha.

Utilice la siguiente sintaxis:

```json
#{<datasource>.<field group>.fieldName, params: {<params-1-name>: <params-1-value>, <params-2-name>: <params-2-value>}}
```

* **`<params-1-name>`**: nombre exacto del primer parámetro del origen de datos.
* **`<params-1-value>`**: valor del primer parámetro. Puede ser cualquier expresión válida.

Por ejemplo:

```json
#{Weather.main.temperature, params: {localisation: @event{Profile.address.localisation}}}
#{Weather.main.temperature, params: {localisation: #{GPSLocalisation.main.coordinates, params: {city: @event{Profile.address.city}}}}}
```
