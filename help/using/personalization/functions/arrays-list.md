---
title: Biblioteca de funciones de matrices
description: Biblioteca de funciones de matrices
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 6%

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

## Recuento Distinto Con Nulo {#distinct-count-with-null}

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

## Primer `n` en matriz {#first-n}

La función `topN` se usa para devolver los primeros `N` elementos de una matriz, cuando se ordenan en orden ascendente en función de la expresión numérica dada.

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


<!-- ## Intersection{#intersection}

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

## Últimos `n` en matriz{#last-n}

La función `bottomN` se usa para devolver los últimos `N` elementos de una matriz, cuando se ordenan en orden ascendente en función de la expresión numérica dada.

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
>La función `notIn`also *de* garantiza que ninguno de los valores es igual a nulo. Por lo tanto, los resultados no son una negación exacta de la función `in`.

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
