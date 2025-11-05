---
product: journey optimizer
title: Funciones de lista
description: Más información sobre las funciones de lista
feature: Journeys
role: Developer
level: Experienced
keywords: lista, funciones, expresión, recorrido, matriz, colección
version: Journey Orchestration
source-git-commit: 0331f8fe2439d41c08ad88a6d0bd95dd150bab90
workflow-type: tm+mt
source-wordcount: '1144'
ht-degree: 9%

---

# Funciones de lista {#list-functions}

Las funciones de lista permiten manipular y trabajar con colecciones de valores dentro de las expresiones de recorrido. Estas funciones son esenciales para filtrar, ordenar, transformar y analizar matrices y listas en los recorridos del cliente.

Utilice las funciones de lista cuando necesite:

* Filtrar y extraer elementos específicos de colecciones en función de criterios
* Ordenar y organizar elementos de lista en orden ascendente o descendente
* Eliminación de duplicados y obtención de valores únicos de las listas
* Comprobar si existen valores dentro de las colecciones
* Limitar el número de elementos devueltos de una lista
* Transformación de listas en diferentes formatos o tipos de datos
* Realizar operaciones de conjunto como buscar elementos comunes entre listas

Las funciones de lista proporcionan potentes herramientas para trabajar con estructuras de datos complejas, lo que permite una manipulación de datos sofisticada y una lógica condicional basada en el contenido de la colección.

## distinct {#distinct}

Devuelve los distintos valores u objetos de una lista determinada. Las entradas nulas se omiten.

+++Sintaxis

`distinct(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para procesar. Para listObject, debe ser una referencia de campo. |
| keyAttributeName | cadena | Este parámetro es opcional y solo para listObject. Si no se proporciona el parámetro, un objeto se considera duplicado si todos los atributos tienen los mismos valores. De lo contrario, un objeto se considera duplicado si el atributo dado tiene el mismo valor. |

+++

+++Firmas y tipos devueltos

`distinct(<listInteger>)`

Devuelve una lista de enteros.

`distinct(<listDecimal>)`

Devuelve una lista de decimales.

`distinct(<listString>)`

Devuelve una lista de cadenas.

`distinct(<listDateTimeOnly>)`

Devuelve una lista de horas de fecha sin tener en cuenta la zona horaria.

`distinct(<listDateTime>)`

Devuelve una lista de fechas y horas.

`distinct(<listDateOnly>)`

Devuelve una lista de fechas.

`distinct(<listBoolean>)`

Devuelve una lista de valores booleanos.

`distinct(<listDuration>)`

Devuelve una lista de duraciones.

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

Devuelve una lista de objetos.

+++

+++Ejemplos

`distinct([10,2,10,null])`

Devuelve `[10, 2]`.

+++

## distinctWithNull {#distinctWithNull}

Devuelve los distintos valores u objetos de una lista determinada. Si la lista tiene al menos una entrada nula, aparecerá una entrada nula en la lista devuelta.

+++Sintaxis

`distinctWithNull(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Lista para procesar. |

+++

+++Firmas y tipos devueltos

`distinctWithNull(<listInteger>)`

Devuelve una lista de enteros.

`distinctWithNull(<listDecimal>)`

Devuelve una lista de decimales.

`distinctWithNull(<listString>)`

Devuelve una lista de cadenas.

`distinctWithNull(<listDateTimeOnly>)`

Devuelve una lista de horas de fecha sin tener en cuenta la zona horaria.

`distinctWithNull(<listDateTime>)`

Devuelve una lista de fechas y horas.

`distinctWithNull(<listDateOnly>)`

Devuelve una lista de fechas.

`distinctWithNull(<listBoolean>)`

Devuelve una lista de valores booleanos.

`distinctWithNull(<listDuration>)`

Devuelve una lista de duraciones.

+++

+++Ejemplos

`distinctWithNull([10,2,10,null])`

Devuelve [10, 2, null]

+++

**Nota:** El parámetro `<listObject>` no se admite en esta función.

## filter {#filter}

Devuelve un listObject con objetos cuyo atributo key coincide con uno de los valores de clave determinados.

+++Sintaxis

`filter(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToFilter | listObject | lista de objetos que se van a filtrar. Debe ser una referencia de campo. |
| keyAttributeName | cadena | nombre del atributo en los objetos de la lista dada, utilizado como clave para el filtrado |
| keyValueList | list | matriz de valores clave para el filtrado |

+++

+++Firmas y tipos devueltos

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Devuelve un listObject.

+++

+++Ejemplos

Este es un ejemplo de una carga útil pasada en un evento entrante &quot;myevent&quot;:

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

Puede utilizar la siguiente expresión:

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Devuelve un listObject que contiene los dos objetos con &quot;product2&quot; y &quot;product3&quot; como id.

+++

## getListItem {#getListItem}

Devuelve el elemento de la lista en el índice dado.

+++Sintaxis

`getListItem(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| list | listString |
| list | listBoolean |
| list | listInteger |
| list | listDecimal |
| list | listDuration |
| list | listDateTime |
| list | listDateTimeOnly |
| list | listDateOnly |
| índice | entero |

+++

+++Firmas y tipo devuelto

`getListItem(<listInteger>,<index>)`

Devuelve un entero.

`getListItem(<listDecimal>,<index>)`

Devuelve un valor decimal.

`getListItem(<listString>,<index>)`

Devuelve una cadena.

`getListItem(<listDateTimeOnly>,<index>)`

Devuelve una fecha y hora sin considerar la zona horaria.

`getListItem(<listDateTime>,<index>)`

Devuelve una fecha y hora.

`getListItem(<listDateOnly>,<index>)`

Devuelve una lista de fechas.

`getListItem(<listBoolean>,<index>)`

Devuelve un valor booleano.

`getListItem(<listDuration>,<index>)`

Devuelve una duración.

+++

+++Ejemplos

`getListItem([10, 2, 3], 1)`

Devuelve &quot;2&quot;

`getListItem(["A", "B", "C"], 2)`

Devuelve &quot;C&quot;

Ejemplos con un campo de evento &quot;event.appVersion&quot; con valor: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Devuelve `["20", "45", "2", "3434"]`

`getListItem(split(@event{event.appVersion}, "\\."), 0)`

Devuelve &quot;20&quot;

+++

## en {#in}

Comprueba si el primer valor del argumento está en la lista. La comprobación se realiza mediante un valor Equal en cada argumento value. Devuelve true si se encuentra el valor del argumento; en caso contrario, devuelve false.

El tipo de `<expression>` debe coincidir con los elementos de la lista. Los tipos de elementos de la lista, como recordatorio, deben coincidir entre sí.

+++Sintaxis

`in(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| Cadena | Cadena |
| Booleano | Booleano |
| Entero | Entero |
| Decimal | Decimal |
| Duración | Duración |
| Fecha/Hora | Fecha/Hora |
| DateTimeOnly | DateTimeOnly |
| Lista | listString |
| Lista | listBoolean |
| Lista | listInteger |
| Lista | listDecimal |
| Lista | listDuration |
| Lista | listDateTime |
| Lista | listDateTimeOnly |
| Lista | listDateOnly |

+++

+++Firma y tipo devuelto

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`in(4,[4,5,3,4])`

Devuelve verdadero.

`in(8,[4,5,3,4])`

Devuelve falso.

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`

+++

## intersect {#intersect}

Devuelve los valores comunes de las dos listas de entrada. Si una de las dos listas es nula, devuelve una lista vacía.

+++Sintaxis

`intersect(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| lista 1 | list |
| lista 2 | list |

+++

+++Firmas y tipos devueltos

`intersect(listString,listString)`: listString

`intersect(listDecimal,listDecimal)`: listDecimal

`intersect(listInteger,listInteger)`: listInteger

`intersect(listDateTime,listDateTime)`: listDateTime

`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly

`intersect(listDateOnly,listDateOnly)`: listDateOnly

`intersect(listDuration,listDuration)`: listDuration

`intersect(listBoolean,listBoolean)`: listBoolean

Devuelve una lista.

+++

+++Ejemplos

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Devuelve [&quot;deportes&quot;, &quot;noticias&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

Devuelve elementos comunes entre atributos de perfil y una lista de categorías determinada.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

Devuelve elementos comunes entre atributos de perfil y un campo de evento determinado.

+++

## límite {#limit}

Devuelve los primeros o últimos elementos N de una lista.

+++Sintaxis

`limit(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista a considerar. Para listObject, debe ser una referencia de campo. |
| numberOfItems | entero | Número de elementos que se van a devolver de la lista determinada. |
| firstOrLastItems | Booleano | Este parámetro es opcional (true de forma predeterminada). true devuelve los primeros elementos. false devuelve los últimos elementos. |

+++

+++Firma y tipo devuelto

`limit(<listString>,<integer>)`

`limit(<listString>,<integer>,<boolean>)`

Devuelve una lista de cadenas.

`limit(<listInteger>,<integer>)`

`limit(<listInteger>,<integer>,<boolean>)`

Devuelve una lista de enteros.

`limit(<listDecimal>,<integer>)`

`limit(<listDecimal>,<integer>,<boolean>)`

Devuelve una lista de decimales.

`limit(<listBoolean>,<integer>)`

`limit(<listBoolean>,<integer>,<boolean>)`

Devuelve una lista de valores booleanos.

`limit(<listDateOnly>,<integer>)`

`limit(<listDateOnly>,<integer>,<boolean>)`

Devuelve una lista de fechas.

`limit(<listDateTimeOnly>,<integer>)`

`limit(<listDateTimeOnly>,<integer>,<boolean>)`

Devuelve una lista de horas de fecha sin tener en cuenta la zona horaria.

`limit(<listDateTime>,integer>)`

`limit(<listDateTime>,<integer>,<boolean>)`

Devuelve una lista de fechas y horas.

`limit(<listDuration>,<integer>)`

`limit(<listDuration>,<integer>,<boolean>)`

Devuelve una lista de duraciones.

`limit(<listObject>,<integer>)`

`limit(<listObject>,<integer>,<boolean>)`

Devuelve una lista de objetos.

+++

+++Ejemplos

`limit(["A", "B", "C", "D", "E"], 3)`

Devuelve `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

Devuelve `["C","D","E"]`.

+++

## listSize {#listSize}

Cuenta el número de elementos de la lista.

+++Sintaxis

`listSize(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para procesar. Para listObject, debe ser una referencia de campo. Un listObject no puede contener un objeto nulo. |

+++

+++Firmas y tipo devuelto

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

Devuelve un entero.

`listSize(<listObject>)`

+++

+++Ejemplos

`listSize([10,2,3])`

Devuelve 3.

`listSize(@event{my_event.productListItems})`

Devuelve el número de objetos de una matriz determinada de objetos (tipo listObject).

+++

## serializeList {#serializeList}

Convierte una lista determinada (cualquier tipo excepto listObject) en una cadena.

+++Sintaxis

`serializeList(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly | Lista para convertir en cadena. |
| separador | cadena | Separador entre cada elemento de lista en la cadena de salida. |
| addQuotes | Booleano | Este parámetro indica si cada elemento de la cadena de salida debe incluir comillas (true) o no (false). |

+++

+++Firma y tipo devuelto

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

Devolver una cadena.

+++

+++Ejemplos

`serializeList(["Hello","World"], " ", false)`

Devuelve &quot;Hello World&quot;.

`serializeList(["Hello", "World"], ",", true)`

Devuelve &quot;Hello&quot;,&quot;World&quot;.

+++

## ordenar {#sort}

Ordena una lista de valores u objetos en orden natural.

+++Sintaxis

`sort(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para ordenar. Para listObject, debe ser una referencia de campo. |
| keyAttributeName | cadena | Este parámetro solo es para listObject. El nombre del atributo en los objetos de la lista dada se utiliza como clave para ordenar. |
| sortingOrder | Booleano | Ascendente (true) o descendente (false) |

+++

+++Firma y tipo devuelto

`sort(<listInteger>,<boolean>)`

Devuelve una lista de enteros.

`sort(<listDecimal>,<boolean>)`

Devuelve una lista de decimales.

`sort(<listString>,<boolean>)`

Devuelve una lista de cadenas.

`sort(<listDateTimeOnly>,<boolean>)`

Devuelve una lista de horas de fecha sin tener en cuenta la zona horaria.

`sort(<listDateTime>,<boolean>)`

Devuelve una lista de fechas y horas.

`sort(<listDateOnly>,<boolean>)`

Devuelve una lista de fechas.

`sort(<listBoolean>,<boolean>)`

Devuelve una lista de valores booleanos.

`sort(<listObject>,<string>,<boolean>)`

Devuelve una lista de objetos.

+++

+++Ejemplos

`sort(["A", "C", "B"], true)`

Devuelve `["A","B","C"]`.

`sort([1, 3, 2], false)`

Devuelve `[3, 2, 1]`.

`sort(@event{my_event.productListItems}, "SKU", true)`

Devuelve el listObject ordenado por atributo SKU (orden ascendente)

+++

