---
title: Biblioteca de funciones
description: Biblioteca de funciones
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# Funciones de objeto {#objects}

![](../../assets/do-not-localize/badge.png)

## Is null

La función `isNull` determina si no existe una referencia de objeto.

**Formato**

```sql
isNull({OBJECT})
```

**Ejemplo**

La siguiente consulta PQL comprueba si la dirección principal de la persona no existe.

```sql
isNull(person.homeAddress)
```

## No es nulo

La función `isNotNull` determina si existe una referencia de objeto.

**Formato**

```sql
isNotNull({OBJECT})
```

**Ejemplo**

La siguiente consulta PQL comprueba si existe la dirección principal de la persona.

```sql
isNotNull(person.homeAddress)
```
