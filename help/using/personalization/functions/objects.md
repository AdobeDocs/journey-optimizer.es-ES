---
title: Biblioteca de funciones de objetos
description: Biblioteca de funciones de objetos
feature: Personalización
topic: Personalización
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 10%

---

# Funciones de objeto {#objects}

## Is null{#isNull}

La función `isNull` determina si no existe una referencia de objeto.

**Formato**

```sql
{%= isNull(object) %}
```

**Ejemplo**

La siguiente operación comprueba si la dirección principal de la persona no existe.

```sql
{%= isNull(person.homeAddress) %}
```

## No es nulo{#isNotNull}

La función `isNotNull` determina si existe una referencia de objeto.

**Formato**

```sql
{%= isNotNull(object) %}
```

**Ejemplo**

La siguiente operación comprueba si existe la dirección principal de la persona.

```sql
{%= isNotNull(person.homeAddress) %}
```
