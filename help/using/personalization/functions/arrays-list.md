---
title: Biblioteca de funciones de matrices
description: Biblioteca de funciones de matrices
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 6%

---

# Funciones de matrices y listas {#arrays}

Utilice estas funciones para facilitar la interacción con matrices, listas y cadenas.

## Contar solo nulo {#count-only-null}

El `countOnlyNull` se utiliza para contar el número de valores nulos de una lista.

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

El `countWithNull` se utiliza para contar todos los elementos de una lista, incluidos los valores nulos.

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

El `distinct` se utiliza para obtener valores de una matriz o lista con valores duplicados eliminados.

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

El `distinctCountWithNull` se utiliza para contar el número de valores diferentes en una lista, incluidos los valores nulos.

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

El `head` se utiliza para devolver el primer elemento de una matriz o lista.

**Sintaxis**

```sql
{%= head(array) %}
```

**Ejemplo**

La siguiente operación devuelve el primero de los cinco pedidos principales con el precio más alto. Más información sobre la `topN` se puede encontrar en la [primero `n` en matriz](#first-n) sección.

```sql
{%= head(topN(orders,price, 5)) %}
```

## Primero `n` en matriz {#first-n}

El `topN` se utiliza para devolver la primera función `N` elementos de una matriz, cuando se ordenan en orden ascendente según la expresión numérica dada.

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

El `in` se utiliza para determinar si un elemento es miembro de una matriz o lista.

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

El `includes` se utiliza para determinar si una matriz o lista contiene un elemento determinado.

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

El `intersects` se utiliza para determinar si dos matrices o listas tienen al menos un miembro común.

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

## Último `n` en matriz{#last-n}

El `bottomN` se utiliza para devolver el último `N` elementos de una matriz, cuando se ordenan en orden ascendente según la expresión numérica dada.

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

El `notIn` se utiliza para determinar si un elemento no es miembro de una matriz o lista.

>[!NOTE]
>
>El `notIn` función *también* garantiza que ninguno de los valores sea igual a nulo. Por lo tanto, los resultados no son una negación exacta de la `in` función.

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

El `subsetOf` se utiliza para determinar si una matriz específica (matriz A) es un subconjunto de otra matriz (matriz B). En otras palabras, que todos los elementos de la matriz A son elementos de la matriz B.

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

El `supersetOf` se utiliza para determinar si una matriz específica (matriz A) es un superconjunto de otra matriz (matriz B). En otras palabras, esa matriz A contiene todos los elementos de la matriz B.

**Sintaxis**

```sql
{%= supersetOf(array1, array2) %}
```

**Ejemplo**

La siguiente operación define a las personas que han comido sushi y pizza al menos una vez.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
