---
title: Biblioteca de funciones aritméticas
description: Biblioteca de funciones aritméticas
feature: Personalización
topic: Personalización
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---

# Funciones aritméticas {#maths}

Las funciones aritméticas se utilizan para realizar cálculos básicos de los valores.

## Add{#add}

La función `+` (suma) se utiliza para encontrar la suma de dos expresiones de argumento.

**Formato**

```sql
{%= double + double %}
```

**Ejemplo**

La operación siguiente resume el precio de dos productos diferentes.

```sql
{%= product1.price + product2.price %}
```

## Multiplicar{#multiply}

La función `*` (multiplicación) se utiliza para encontrar el producto de dos expresiones de argumento.

**Formato**

```sql
{%= double * double %}
```

**Ejemplo**

La siguiente operación encuentra el producto del inventario y el precio de un producto para encontrar el valor bruto del producto.

```sql
{%= product.inventory * product.price %}
```

## Sustraer{#substract}

La función `-` (resta) se utiliza para encontrar la diferencia de dos expresiones de argumento.

**Formato**

```sql
{%= double - double %}
```

**Ejemplo**

La siguiente operación encuentra la diferencia de precio entre dos productos diferentes.

```sql
{%= product1.price - product2.price %}
```

## Dividir{#divide}

La función `/` (división) se utiliza para encontrar el cociente de dos expresiones de argumento.

**Formato**

```sql
{%= double / double %}
```

**Ejemplo**

La siguiente operación encuentra el cociente entre el total de productos vendidos y el total de dinero ganado para ver el costo promedio por artículo.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## Remainte{#remainder}

La función `%` (módulo/resto) se utiliza para encontrar el resto después de dividir las dos expresiones de argumento.

**Formato**

```sql
{%= double % double %}
```

**Ejemplo**

La siguiente operación comprueba si la edad de la persona es divisible entre cinco años.

```sql
{%= person.age % 5 = 0 %}
```
