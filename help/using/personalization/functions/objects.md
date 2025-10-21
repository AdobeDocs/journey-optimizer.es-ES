---
title: Biblioteca de funciones de objetos
description: Biblioteca de funciones de objetos
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# Funciones de objeto {#objects}

## Es nulo{#isNull}

La función `isNull` determina si no existe una referencia de objeto.

**Sintaxis**

```sql
{%= isNull(object) %}
```

**Ejemplo**

La siguiente operación comprueba si la dirección postal de la persona no existe.

```sql
{%= isNull(person.homeAddress) %}
```

## No es nulo{#isNotNull}

La función `isNotNull` determina si existe una referencia a un objeto.

**Sintaxis**

```sql
{%= isNotNull(object) %}
```

**Ejemplo**

La siguiente operación comprueba si existe la dirección particular de la persona.

```sql
{%= isNotNull(person.homeAddress) %}
```
