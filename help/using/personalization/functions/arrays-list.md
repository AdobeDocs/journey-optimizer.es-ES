---
title: Biblioteca de funciones de matrices
description: Biblioteca de funciones de matrices
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 5%

---

# Funciones de matrices y listas {#arrays}

Utilice estas funciones para facilitar la interacción con matrices, listas y cadenas.

## Distinct{#distinct}

La variable `distinct` se utiliza para obtener valores de una matriz o lista con valores duplicados eliminados.

**Formato**

```sql
{%= distinct(array) %}
```

**Ejemplo**

La siguiente operación especifica las personas que han realizado pedidos en más de un almacén.

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Primer elemento{#head}

La variable `head` se utiliza para devolver el primer elemento de la matriz o lista.

**Formato**

```sql
{%= head({array}) %}
```

**Ejemplo**

La siguiente operación devuelve el primero de los cinco pedidos principales con el precio más alto. Más información sobre `topN` se puede encontrar en la variable [first `n` en matriz](#first-n) para obtener más información.

```sql
{%= head(topN(orders,price, 5)) %}
```

## First `n` en matriz {#first-n}

La variable `topN` se utiliza para devolver la primera función `N` elementos de una matriz, cuando se ordenan en orden ascendente según la expresión numérica dada.

**Formato**

```sql
{%= topN(array, value, amount) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{ARRAY}` | Matriz o lista que se va a ordenar. |
| `{VALUE}` | La propiedad en la que se va a ordenar la matriz o la lista. |
| `{AMOUNT}` | Número de elementos que se van a devolver. |

**Ejemplo**

La siguiente operación devuelve los cinco pedidos principales con el precio más alto.

```sql
{%= topN(orders,price, 5) %}
```

## En{#in}

La variable `in` para determinar si un elemento es miembro de una matriz o lista.

**Formato**

```sql
{%= in(value, array) %}
```

**Ejemplo**

La siguiente operación define las personas con cumpleaños en marzo, junio o septiembre.

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## Incluye{#includes}

La variable `includes` para determinar si una matriz o lista contiene un elemento determinado.

**Formato**

```sql
{%= includes(array,item) %}
```

**Ejemplo**

La siguiente operación define a las personas cuyo color favorito incluye el rojo.

```sql
{%= includes(person.favoriteColors,"red") %}
```

## Intersecciones{#intersects}

La variable `intersects` se utiliza para determinar si dos matrices o listas tienen al menos un miembro común.

**Formato**

```sql
{%= intersects(array1, array2) %}
```

**Ejemplo**

La siguiente operación define las personas cuyos colores favoritos incluyen al menos uno de rojo, azul o verde.

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## Última `n` en matriz{#last-n}

La variable `bottomN` se utiliza para devolver el último `N` elementos de una matriz, cuando se ordenan en orden ascendente según la expresión numérica dada.

**Formato**

```sql
{%= bottomN(array, value, amount) %}
```

| Argumento | Descripción |
| --------- | ----------- | 
| `{ARRAY}` | Matriz o lista que se va a ordenar. |
| `{VALUE}` | La propiedad en la que se va a ordenar la matriz o la lista. |
| `{AMOUNT}` | Número de elementos que se van a devolver. |

**Ejemplo**

La siguiente operación devuelve los cinco pedidos principales con el precio más bajo.

```sql
{%= bottomN(orders,price, 5) %}
```


## Not in{#notin}

La variable `notIn` para determinar si un elemento no es miembro de una matriz o lista.

>[!NOTE]
>
>La variable `notIn` function *also* garantiza que ninguno de los dos valores sea igual a nulo. Por lo tanto, los resultados no son una negación exacta del `in` función.

**Formato**

```sql
{%= notIn(value, array) %}
```

**Ejemplo**

La siguiente operación define las personas con cumpleaños que no están en marzo, junio o septiembre.

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## Subconjunto de{#subset}

La variable `subsetOf` para determinar si una matriz específica (matriz A) es un subconjunto de otra matriz (matriz B). En otras palabras, que todos los elementos de la matriz A son elementos de la matriz B.

**Formato**

```sql
{%= subsetOf(array1, array2) %}
```

**Ejemplo**

La siguiente operación define a las personas que han visitado todas sus ciudades favoritas.

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## Superconjunto de{#superset}

La variable `supersetOf` para determinar si una matriz específica (matriz A) es un superconjunto de otra matriz (matriz B). En otras palabras, la matriz A contiene todos los elementos de la matriz B.

**Formato**

```sql
{%= supersetOf(array1, array2) %}
```

**Ejemplo**

La siguiente operación define a las personas que han comido sushi y pizza al menos una vez.

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
