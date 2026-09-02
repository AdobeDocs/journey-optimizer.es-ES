---
solution: Journey Optimizer
product: journey optimizer
title: Referencias del campo
description: Obtenga información sobre las referencias de campo en expresiones avanzadas
feature: Journeys
role: Developer
level: Experienced
keywords: recorrido, campo, expresión, evento
exl-id: 2348646a-b205-4b50-a08f-6625e92f44d7
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/G8ooc1R2PwL06V89EBs-jH8Lf43F6q5xj3I4Wl6hDHk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 2%

---

# Referencias del campo {#field-references}

Se puede adjuntar una referencia de campo a un evento o a un grupo de campos. La única información significativa es el nombre del campo y su ruta.

Si utiliza caracteres especiales en un campo, debe utilizar comillas dobles o simples. Estos son los casos en los que se necesitan comillas:

* el campo comienza con caracteres numéricos
* el campo comienza con el carácter &quot;-&quot;
* el campo contiene cualquier cosa que no sea: _a_-_z_, _A_-_Z_, _0_-_9_, _,_-_

Por ejemplo, si el campo es _3h_: _#{OpenWeather.weatherData.rain.&#39;3h&#39;} > 0_

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
- @event{OrderEvent.productId, defaultValue : "not specified" } -> "not specified" // default value, productId is not a field present in the payload
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

Ejemplo:

```json
#{Weather.main.temperature, params: {localisation: @event{Profile.address.localisation}}}
#{Weather.main.temperature, params: {localisation: #{GPSLocalisation.main.coordinates, params: {city: @event{Profile.address.city}}}}}
```

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo hacer referencia a campos de evento y grupos de campos de origen de datos en expresiones de recorrido, incluida la sintaxis de valor predeterminada, las funciones de acceso a mapas (`entry`, `firstEntryKey`, `keys`) y el paso del parámetro de origen de datos en línea con la palabra clave `params`.

**Intenciones:**

* Hacer referencia a un campo de evento en una expresión mediante la sintaxis `@event{eventName.fieldPath}`
* Hacer referencia a un grupo de campos de origen de datos con la sintaxis `#{dataSourceName.fieldGroupName.fieldPath}`
* Asignar un valor predeterminado de reserva a una referencia de campo para que las expresiones no devuelvan un valor nulo
* Recupere una entrada específica de un mapa de identidad o mapa de suscripción mediante la función `entry()`
* Recupere todas las claves de un campo de asignación utilizando la función `keys()`
* Pase valores de parámetro a un origen de datos externo en línea mediante la palabra clave `params`

**Glosario:**

* **Referencia de campo**: sintaxis de expresión que señala a un campo con nombre dentro de una carga útil de evento o un grupo de campos de origen de datos *(específico del producto)*
* **defaultValue**: Expresión de reserva opcional anexada a una referencia de campo que se devuelve cuando el campo está ausente o es nulo *(específico del producto)*
* **entry(key)**: una función de asignación que recupera la entrada de colección asociada con la clave dada *(específica del producto)*
* **firstEntryKey()**: Una función de asignación que devuelve la primera clave de un campo de asignación *(específico del producto)*
* **keys()**: Una función de asignación que devuelve todas las claves de un campo de asignación *(específico del producto)*
* **palabra clave params**: sintaxis en línea para especificar valores de parámetro para campos de origen de datos externos en la expresión principal *(específica del producto)*

**Protecciones:**

* Los nombres de campo que contengan caracteres especiales (que comiencen por un dígito, que contengan `-` o caracteres externos a `a-z A-Z 0-9 _`) deben escribirse entre comillas simples o dobles
* La expresión de valor predeterminada debe devolver el mismo tipo de datos que el campo; los tipos que no coinciden no son válidos
* Cuando se utiliza la palabra clave `params` para definir los valores de parámetros en línea, desaparece la pestaña de parámetros independiente a la derecha del editor
* Las funciones utilizadas como valores predeterminados deben encapsularse entre paréntesis

**Terminología:**

* Nombre canónico: Referencias de campo — Acrónimo: none — variantes: ruta del campo, expresión del campo
* Sinónimos: `@event{...}` = &quot;referencia de campo de evento&quot;; `#{...}` = &quot;referencia de campo de origen de datos&quot;
* No confunda: campos de evento (con el prefijo `@`) ≠ campos de origen de datos (con el prefijo `#`)

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Cómo hago referencia a un campo cuyo nombre comienza con un número?** — escriba el nombre del campo entre comillas simples o dobles, por ejemplo `#{OpenWeather.weatherData.rain.'3h'}`.
* **Q: ¿Qué sucede cuando falta un campo al que se hace referencia en la carga útil de evento y no se establece ningún valor predeterminado?** — La expresión devuelve `null`.
* **Q: ¿Cómo se establece un valor predeterminado dinámico mediante una función?** — ajuste la llamada de función entre paréntesis, p. ej. `defaultValue: (now())`.
* **Q: ¿Cómo puedo recuperar la dirección de correo electrónico almacenada como la primera clave en un mapa de suscriptores?** — Utilice la función `firstEntryKey()` en el campo de asignación de suscriptores.
* **Q: ¿Cómo paso un parámetro a una fuente de datos externa sin usar la ficha del lado derecho?** — Usar la palabra clave `params` en línea: `#{DataSource.group.field, params: {paramName: value}}`.

+++
