---
title: Biblioteca de funciones de objetos
description: Biblioteca de funciones de objetos
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# Funciones de objeto {#objects}

## Is null{#isNull}

La variable `isNull` determina si no existe una referencia de objeto.

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

La variable `isNotNull` determina si existe una referencia de objeto.

**Formato**

```sql
{%= isNotNull(object) %}
```

**Ejemplo**

La siguiente operación comprueba si existe la dirección principal de la persona.

```sql
{%= isNotNull(person.homeAddress) %}
```
