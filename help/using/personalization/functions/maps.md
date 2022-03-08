---
title: Biblioteca de funciones Mapas
description: Biblioteca de funciones Mapas
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 7%

---

# Funciones de asignación{#maps}

Utilice las funciones de mapa en la personalización para facilitar la interacción con los mapas.

## Obtenga{#get}

La variable `get` se utiliza para recuperar el valor de un mapa para una clave determinada.

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

La variable `keys` se utiliza para recuperar todas las claves de un mapa determinado.

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

La variable `values` se utiliza para recuperar todos los valores de un mapa determinado.

**Formato**

```sql
{%= values(map) %}
```

**Ejemplo**

La siguiente operación obtiene todos los valores del mapa `identityMap`.

```sql
{%= values(identityMap) %}
```
