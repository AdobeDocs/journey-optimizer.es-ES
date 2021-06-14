---
title: Biblioteca de funciones de objetos
description: Biblioteca de funciones de objetos
feature: Personalización
topic: Personalización
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 10%

---

# Funciones de objeto {#objects}

![](../../assets/do-not-localize/badge.png)

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
