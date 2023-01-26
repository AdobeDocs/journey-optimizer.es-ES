---
title: Biblioteca de funciones matemáticas
description: Biblioteca de funciones matemáticas
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 6%

---

# Funciones matemáticas {#math}

Aprenda a utilizar funciones matemáticas en el editor de expresiones.

## Absoluta   {#absolute}

La variable `absolute` se utiliza para convertir un número que es un valor absoluto.

**Sintaxis**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

La variable `formatNumber` se utiliza para dar formato a cualquier número en su representación que distingue entre idiomas.

Acepta un número y una cadena que representan la configuración regional y devuelve una cadena formateada del número en la configuración regional deseada.

**Sintaxis**

```sql
{%= formatNumber(number/double,string) %}: string
```

Puede utilizar el formato y las configuraciones regionales válidas, como se resume en [documentación de oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) y [Localizaciones compatibles](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Ejemplo**

Esta consulta devuelve una cadena con formato en árabe que corresponde a 123456.789 como número de entrada.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Aleatorio {#random}

La variable `random` se utiliza para devolver un valor aleatorio entre 0 y 1.

**Sintaxis**

```sql
{%= random() %}: double
```

## Redondear hacia abajo {#round-down}

La variable `roundDown` para redondear hacia abajo un número.

**Sintaxis**

```sql
{%= roundDown(double) %}: double
```

## Redondear hacia arriba {#round-up}

La variable `Count only null` se utiliza redondeando un número.

**Sintaxis**

```sql
{%= roundUp(double) %}: double
```

## A cadena hexadecimal {#to-hex-string}

La variable `toHexString` convierte cualquier número en su cadena hexadecimal.

**Sintaxis**

```sql
{%= toHexString(number) %}: string
```

**Ejemplo**

Esta consulta devuelve el valor hexadecimal de 158, es decir, 9e.

```sql
{%= toHexString(158) %}
```

## A porcentaje {#to-percentage}

La variable `toPercentage` para convertir un número en porcentaje.

**Sintaxis**

```sql
{%= toPercentage(double) %}: string
```

## Para precisión {#to-precision}

La variable `toPrecision` para convertir un número a la precisión necesaria.

**Sintaxis**

```sql
{%= toPrecision(double,int) %}: string
```

## A cadena {#to-string}

La variable **toString** convierte cualquier número en su representación de cadena.

**Sintaxis**

```sql
{%= toString(string) %}: string
```

**Ejemplo**

Esta consulta devuelve &quot;12&quot;.

```sql
{%= toString(12) %} 
```
