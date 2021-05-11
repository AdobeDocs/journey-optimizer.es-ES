---
title: Biblioteca de funciones
description: Biblioteca de funciones
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 5%

---

# Matrices y funciones de lista {#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) ofrece funciones para facilitar la interacción con matrices, listas y cadenas.

## En

La función `in` se utiliza para determinar si un elemento es miembro de una matriz o lista.

**Formato**

```sql
in ({VALUE},{ARRAY})
```

**Ejemplo**

La siguiente consulta PQL define las personas con cumpleaños en marzo, junio o septiembre.

```sql
in (person.birthMonth, [3, 6, 9])
```

## Not in

La función `notIn` se utiliza para determinar si un elemento no es miembro de una matriz o lista.

>[!NOTE]
>
>La función `notIn` *también* garantiza que ninguno de los valores sea igual a nulo. Por lo tanto, los resultados no son una negación exacta de la función `in`.

**Formato**

```sql
notIn ({VALUE},{ARRAY})
```

**Ejemplo**

La siguiente consulta PQL define las personas con cumpleaños que no están en marzo, junio o septiembre.

```sql
notIn (person.birthMonth ,[3, 6, 9])
```

## Intersecciones

La función `intersects` se utiliza para determinar si dos matrices o listas tienen al menos un miembro común.

**Formato**

```sql
intersects({ARRAY},{ARRAY})
```

**Ejemplo**

La siguiente consulta PQL define las personas cuyos colores favoritos incluyen al menos uno de rojo, azul o verde.

```sql
intersects(person.favoriteColors,["red", "blue", "green"])
```

## Intersección

La función `intersection` se utiliza para determinar los miembros comunes de dos matrices o listas.

**Formato**

```sql
intersection({ARRAY},{ARRAY})
```

**Ejemplo**

La siguiente consulta PQL define si la persona 1 y la persona 2 tienen los colores favoritos de rojo, azul y verde.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```

## Subconjunto de

La función `subsetOf` se utiliza para determinar si una matriz específica (matriz A) es un subconjunto de otra matriz (matriz B). En otras palabras, que todos los elementos de la matriz A son elementos de la matriz B.

**Formato**

```sql
subsetOf({ARRAY},{ARRAY})
```

**Ejemplo**

La siguiente consulta PQL define las personas que han visitado todas sus ciudades favoritas.

```sql
subsetOf(person.favoriteCities,person.visitedCities)
```

## Superconjunto de

La función `supersetOf` se utiliza para determinar si una matriz específica (matriz A) es un superconjunto de otra matriz (matriz B). En otras palabras, la matriz A contiene todos los elementos de la matriz B.

**Formato**

```sql
supersetOf({ARRAY},{ARRAY})
```

**Ejemplo**

La siguiente consulta PQL define a las personas que han comido sushi y pizza al menos una vez.

```sql
supersetOf(person.eatenFoods,["sushi", "pizza"])
```

## Incluye

La función `includes` se utiliza para determinar si una matriz o lista contiene un elemento determinado.

**Formato**

```sql
includes({ARRAY},{ITEM})
```

**Ejemplo**

La siguiente consulta PQL define las personas cuyo color favorito incluye el rojo.

```sql
includes(person.favoriteColors,"red")
```

## Distinct

La función `distinct` se utiliza para eliminar valores duplicados de una matriz o lista.

**Formato**

```sql
distinct({ARRAY})
```

**Ejemplo**

La siguiente consulta PQL especifica las personas que han realizado pedidos en más de un almacén.

```sql
distinct(person.orders.storeId).count() > 1
```

## Primera `n` en la matriz {#first-n}

La función `topN` se utiliza para devolver los primeros `N` elementos de una matriz, cuando se ordenan en orden ascendente según la expresión numérica dada.

**Formato**

```sql
topN({ARRAY},{VALUE}, {AMOUNT})
```

| Argumento | Descripción |
| --------- | ----------- |
| `{ARRAY}` | Matriz o lista que se va a ordenar. |
| `{VALUE}` | La propiedad en la que se va a ordenar la matriz o la lista. |
| `{AMOUNT}` | Número de elementos que se van a devolver. |

**Ejemplo**

La siguiente consulta PQL devuelve los cinco pedidos principales con el precio más alto.

```sql
topN(orders,price, 5)
```

## Última `n` en la matriz

La función `bottomN` se utiliza para devolver los últimos `N` elementos de una matriz, cuando se ordenan en orden ascendente según la expresión numérica dada.

**Formato**

```sql
bottomN({ARRAY},{VALUE}, {AMOUNT})
```

| Argumento | Descripción |
| --------- | ----------- | 
| `{ARRAY}` | Matriz o lista que se va a ordenar. |
| `{VALUE}` | La propiedad en la que se va a ordenar la matriz o la lista. |
| `{AMOUNT}` | Número de elementos que se van a devolver. |

**Ejemplo**

La siguiente consulta PQL devuelve los cinco pedidos principales con el precio más bajo.

```sql
bottomN(orders,price, 5)
```

## Primer elemento

La función `head` se utiliza para devolver el primer elemento de la matriz o lista.

**Formato**

```sql
head({ARRAY})
```

**Ejemplo**

La siguiente consulta PQL devuelve el primero de los cinco pedidos principales con el precio más alto. Puede encontrar más información sobre la función `topN` en la sección [first `n` en array](#first-n).

```sql
head(topN(orders,price, 5))
```
