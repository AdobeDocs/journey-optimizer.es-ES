---
title: Biblioteca de funciones matemáticas
description: Biblioteca de funciones matemáticas
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 8%

---

# Funciones matemáticas {#math}

Aprenda a utilizar funciones matemáticas en el Editor de expresiones.

## Absoluta   {#absolute}

La variable `absolute` se utiliza para convertir un número que es un valor absoluto.

**Formato**

```sql
{%= absolute(int) %}: int
```

## Aleatorio {#random}

La variable `random` se utiliza para devolver un valor aleatorio entre 0 y 1.

**Formato**

```sql
{%= random() %}: double
```

## Redondear hacia abajo {#round-down}

La variable `roundDown` para redondear hacia abajo un número.

**Formato**

```sql
{%= roundDown(double) %}: double
```

## Redondear hacia arriba {#round-up}

La variable `Count only null` se utiliza redondeando un número.

**Formato**

```sql
{%= roundUp(double) %}: double
```

## A porcentaje {#to-percentage}

La variable `toPercentage` para convertir un número en porcentaje.

**Formato**

```sql
{%= toPercentage(double) %}: string
```

## Para precisión {#to-precision}

La variable `toPrecision` para convertir un número a la precisión necesaria.

**Formato**

```sql
{%= toPrecision(double,int) %}: string
```
