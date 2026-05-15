---
title: Biblioteca de funciones de mapas
description: Biblioteca de funciones de mapas
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
TQID: https://experienceleague.adobe.com/KeitEe0NQxxc-snCyWSGlov-OyUgiva6ddzrCTxEKSs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 6%

---

# Funciones de mapas{#maps}

Utilice las funciones de mapa en la personalización para facilitar la interacción con los mapas.

## Obtener{#get}

La función `get` se usa para recuperar el valor de un mapa para una clave determinada.

**Sintaxis**

```sql
{%= get(map, string) %}
```

**Ejemplo**

La siguiente operación obtiene el valor del mapa de identidad para la clave `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## Claves{#keys}

La función `keys` se usa para recuperar todas las claves de un mapa determinado.

**Sintaxis**

```sql
{%= keys(map) %}
```

**Ejemplo**

La siguiente operación obtiene todas las claves del mapa `identityMap`.

```sql
{%= keys(identityMap) %}
```

## Valores{#values}

La función `values` se usa para recuperar todos los valores de un mapa determinado.

**Sintaxis**

```sql
{%= values(map) %}
```

**Ejemplo**

La siguiente operación obtiene todos los valores del mapa `identityMap`.

```sql
{%= values(identityMap) %}
```
