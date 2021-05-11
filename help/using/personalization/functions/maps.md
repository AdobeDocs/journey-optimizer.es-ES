---
title: Biblioteca de funciones
description: Biblioteca de funciones
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 7%

---

# Funciones de asignación {#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL) ofrece funciones para facilitar la interacción con los mapas.

## Obtenga

La función `get` se utiliza para recuperar el valor de un mapa para una clave determinada.

**Formato**

```sql
get({MAP},{STRING})
```

**Ejemplo**

La siguiente consulta PQL obtiene el valor del mapa de identidad para la clave `example@example.com`.

```sql
get(identityMap,"example@example.com")
```

## Claves

La función `keys` se utiliza para recuperar todas las claves de un mapa determinado.

**Formato**

```sql
keys({MAP})
```

**Ejemplo**

La siguiente consulta PQL obtiene todas las claves del mapa `identityMap`.

```sql
keys(identityMap)
```

## Valores

La función `values` se utiliza para recuperar todos los valores de un mapa determinado.

**Formato**

```sql
values({MAP})
```

**Ejemplo**

La siguiente consulta PQL obtiene todos los valores del mapa `identityMap`.

```sql
values(identityMap)
```
