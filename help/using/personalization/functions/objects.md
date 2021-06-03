---
title: Biblioteca de funciones
description: Biblioteca de funciones
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

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
