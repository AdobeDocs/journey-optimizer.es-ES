---
title: Biblioteca de funciones aritméticas
description: Biblioteca de funciones aritméticas
feature: Personalización
topic: Personalización
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---

# Funciones aritméticas {#maths}

![](../../assets/do-not-localize/badge.png)

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
