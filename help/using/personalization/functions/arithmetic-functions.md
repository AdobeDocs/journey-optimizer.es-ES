---
title: Biblioteca de funciones aritméticas
description: Biblioteca de funciones aritméticas
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# Funciones aritméticas {#maths}

Las funciones aritméticas se utilizan para realizar cálculos básicos sobre los valores.

## Add{#add}

El `+` (suma) se utiliza para encontrar la suma de dos expresiones de argumento.

**Sintaxis**

```sql
{%= double + double %}
```

**Ejemplo**

La siguiente operación suma el precio de dos productos diferentes.

```sql
{%= product1.price + product2.price %}
```

## Multiplicar{#multiply}

El `*` (multiplicación) se utiliza para encontrar el producto de dos expresiones de argumento.

**Sintaxis**

```sql
{%= double * double %}
```

**Ejemplo**

La siguiente operación encuentra el producto del inventario y el precio de un producto para encontrar el valor bruto del producto.

```sql
{%= product.inventory * product.price %}
```

## Restar{#substract}

El `-` (resta) se utiliza para encontrar la diferencia de dos expresiones de argumento.

**Sintaxis**

```sql
{%= double - double %}
```

**Ejemplo**

La siguiente operación encuentra la diferencia de precio entre dos productos diferentes.

```sql
{%= product1.price - product2.price %}
```

## Dividir{#divide}

El `/` (división) se utiliza para encontrar el cociente de dos expresiones de argumento.

**Sintaxis**

```sql
{%= double / double %}
```

**Ejemplo**

La siguiente operación encuentra el cociente entre el total de productos vendidos y el total de dinero ganado para ver el coste promedio por artículo.

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## Resto{#remainder}

El `%` (módulo/resto) se utiliza para encontrar el resto después de dividir las dos expresiones de argumento.

**Sintaxis**

```sql
{%= double % double %}
```

**Ejemplo**

La siguiente operación comprueba si la edad de la persona es divisible entre cinco.

```sql
{%= person.age % 5 = 0 %}
```
