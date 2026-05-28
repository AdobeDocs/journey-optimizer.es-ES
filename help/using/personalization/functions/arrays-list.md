---
title: Biblioteca de funciones de matrices
description: Biblioteca de funciones de matrices
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
TQID: https://experienceleague.adobe.com/CUiT5GFH9o4q-oOSWuKC8ZyLbRbH9lj88M92LhMIX9E
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 742
ht-degree: 4%

---

# Funciones de matrices y listas {#arrays}

Utilice estas funciones para facilitar la interacción con matrices, listas y cadenas.

## Contar solo nulo {#count-only-null}

La función `countOnlyNull` se usa para contar el número de valores nulos de una lista.

**Sintaxis**

```sql
{%= countOnlyNull(array) %}
```

**Ejemplo**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Devuelve 3.

## Contar Con Nulo {#count-with-null}

La función `countWithNull` se usa para contar todos los elementos de una lista, incluidos los valores nulos.

**Sintaxis**

```sql
{%= countWithNull(array) %}
```

**Ejemplo**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

Devuelve 6.

## Distinto{#distinct}

La función `distinct` se usa para obtener valores de una matriz o lista con valores duplicados eliminados.

**Sintaxis**

```sql
{%= distinct(array) %}
```

**Ejemplo**

La siguiente operación especifica las personas que han realizado pedidos en más de un almacén.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Recuento distinto con nulo {#distinct-count-with-null}

La función `distinctCountWithNull` se usa para contar el número de valores diferentes en una lista, incluidos los valores nulos.

**Sintaxis**

```sql
{%= distinctCountWithNull(array) %}
```

**Ejemplo**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

Devuelve 3.

## Primer elemento{#head}

La función `head` se usa para devolver el primer elemento de una matriz o lista.

**Sintaxis**

```sql
{%= head(array) %}
```

**Ejemplo**

La siguiente operación devuelve el primero de los cinco pedidos principales con el precio más alto. Encontrará más información sobre la función `topN` en la sección [primeros `n` de la matriz](#first-n).

```sql
{%= head(topN(orders,price, 5)) %}
```

## Ordenar y obtener el primer N en la matriz {#first-n}

La función `topN` ordena una matriz en orden descendente en función de la expresión numérica dada y devuelve los primeros `N` elementos. Si el tamaño de la matriz es menor que `N`, devuelve toda la matriz ordenada.

Esta función
**Sintaxis**

```sql
{%= topN(array, value, amount) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{ARRAY}` | La matriz o lista que se va a ordenar. |
| `{VALUE}` | Propiedad en la que se ordena la matriz o lista. |
| `{AMOUNT}` | Número de elementos que se van a devolver. |

**Ejemplo**

La siguiente operación devuelve los cinco primeros pedidos con el precio más bajo.

```sql
{%= topN(orders,price, 5) %}
```

## Entrada{#in}

La función `in` se usa para determinar si un elemento es miembro de una matriz o lista.

**Sintaxis**

```sql
{%= in(value, array) %}
```

**Ejemplo**

La siguiente operación define a las personas con cumpleaños en marzo, junio o septiembre.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Incluye{#includes}

La función `includes` se usa para determinar si una matriz o lista contiene un elemento determinado.

**Sintaxis**

```sql
{%= includes(array,item) %}
```

**Ejemplo**

La siguiente operación define a las personas cuyo color favorito incluye el rojo.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Intersecciones{#intersects}

La función `intersects` se usa para determinar si dos matrices o listas tienen al menos un miembro común.

**Sintaxis**

```sql
{%= intersects(array1, array2) %}
```

**Ejemplo**

La siguiente operación define a las personas cuyos colores favoritos incluyen al menos uno de rojo, azul o verde.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!--
## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## Ordenar y obtener el último N de la matriz {#last-n}

La función `bottomN` ordena una matriz en orden ascendente en función de la expresión numérica dada y devuelve los primeros `N` elementos. Si el tamaño de la matriz es menor que `N`, devuelve toda la matriz ordenada.

**Sintaxis**

```sql
{%= bottomN(array, value, amount) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{ARRAY}` | La matriz o lista que se va a ordenar. |
| `{VALUE}` | Propiedad en la que se ordena la matriz o lista. |
| `{AMOUNT}` | Número de elementos que se van a devolver. |

**Ejemplo**

La siguiente operación devuelve los últimos cinco pedidos con el precio más alto.

```sql
{%= bottomN(orders,price, 5) %}
```

## No en{#notin}

La función `notIn` se usa para determinar si un elemento no es miembro de una matriz o lista.

>[!NOTE]
>
>La función *also* de `notIn` garantiza que ninguno de los valores es igual a nulo. Por lo tanto, los resultados no son una negación exacta de la función `in`.

**Sintaxis**

```sql
{%= notIn(value, array) %}
```

**Ejemplo**

La siguiente operación define a las personas con cumpleaños que no se celebran en marzo, junio o septiembre.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Subconjunto de{#subset}

La función `subsetOf` se usa para determinar si una matriz específica (matriz A) es un subconjunto de otra matriz (matriz B). En otras palabras, que todos los elementos de la matriz A son elementos de la matriz B.

**Sintaxis**

```sql
{%= subsetOf(array1, array2) %}
```

**Ejemplo**

La siguiente operación define a las personas que han visitado todas sus ciudades favoritas.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Superconjunto de{#superset}

La función `supersetOf` se usa para determinar si una matriz específica (matriz A) es un superconjunto de otra matriz (matriz B). En otras palabras, esa matriz A contiene todos los elementos de la matriz B.

**Sintaxis**

```sql
{%= supersetOf(array1, array2) %}
```

**Ejemplo**

La siguiente operación define a las personas que han comido sushi y pizza al menos una vez.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

## Iteración en una matriz {#each-loop}

Use el asistente del bloque Handlebars `{{#each}}` para recorrer una matriz y procesar el contenido de cada elemento en **contenido personalizado** (correo electrónico, SMS, push).

>[!NOTE]
>
>`{{#each}}` solo está disponible en el **editor de personalización** (cuerpo del correo electrónico, SMS, contenido push). Se admite **no** en la actividad de condición de recorrido. Para filtrar o hacer coincidir elementos de una matriz dentro de una condición de recorrido, use [funciones de administración de colecciones](../../building-journeys/expression/collection-management-functions.md) en su lugar.

**Sintaxis**

```handlebars
{{#each arrayAttribute}}
  {{this}}
{{/each}}
```

+++Ejemplo: enumerar todos los elementos de una matriz

```handlebars
{{#each profile.purchases.items}}
  - {{this.name}}: {{this.price}}€
{{/each}}
```

Salida (ejemplo):

```
- Running shoes: 89€
- Water bottle: 15€
- Gym bag: 45€
```

+++

+++Ejemplo: Acceso al índice de bucle

Use `@index` para acceder a la posición de bucle actual (basada en 0):

```handlebars
{{#each profile.preferences.languages}}
  {{@index}}: {{this}}
{{/each}}
```

Salida (ejemplo):

```
0: English
1: French
2: Spanish
```

+++

+++Ejemplo — Renderización condicional dentro de un bucle

Utilice el bloque `{%#if%}` dentro de `{{#each}}` para procesar contenido solamente cuando se cumpla una condición:

>[!NOTE]
>
>`{% if %}` / `{% endif %}` no son compatibles. En su lugar, use `{%#if%}` / `{%/if%}`. Además, `this.<field>` no funciona dentro de las expresiones de condición PQL; haga referencia al campo directamente usando el nombre del atributo (por ejemplo: `order.status`).

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Your order {{order.id}} is still pending.
  {%/if%}
{{/each}}
```

Este es el patrón recomendado para simular una &quot;interrupción en condición&quot;: solo los elementos que coinciden con la condición generan salida.

+++
