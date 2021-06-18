---
title: Biblioteca de funciones Mapas
description: Biblioteca de funciones Mapas
feature: Personalización
topic: Personalización
role: Data Engineer
level: Experienced
source-git-commit: e3b7e80b72e6be71d5b38cd5507d20ad2e8ca8d4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 9%

---

# Funciones de asignación{#maps}

Utilice las funciones de mapa en la personalización para facilitar la interacción con los mapas.

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
