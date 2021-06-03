---
title: Biblioteca de funciones
description: Biblioteca de funciones
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 8%

---

# Funciones de asignación{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) ofrece funciones para facilitar la interacción con los mapas.

## Obtenga{#get}

La función `get` se utiliza para recuperar el valor de un mapa para una clave determinada.

**Formato**

```sql
{%= get(map, string) %}
```

**Ejemplo**

La siguiente operación obtiene el valor del mapa de identidad para la clave `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Claves{#keys}

La función `keys` se utiliza para recuperar todas las claves de un mapa determinado.

**Formato**

```sql
{%= keys(map) %}
```

**Ejemplo**

La siguiente operación obtiene todas las claves del mapa `identityMap`.

```sql
{%= keys(identityMap) %}
```

## Valores{#values}

La función `values` se utiliza para recuperar todos los valores de un mapa determinado.

**Formato**

```sql
{%= values(map) %}
```

**Ejemplo**

La siguiente operación obtiene todos los valores del mapa `identityMap`.

```sql
{%= values(identityMap) %}
```
