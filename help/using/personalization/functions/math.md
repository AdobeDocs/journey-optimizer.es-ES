---
title: Biblioteca de funciones matemáticas
description: Biblioteca de funciones matemáticas
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 11%

---

# Funciones matemáticas {#math}

Aprenda a utilizar las funciones matemáticas en el editor de personalización.

## Absoluto {#absolute}

El `absolute` se utiliza para convertir un número en su valor absoluto.

**Sintaxis**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

El `formatNumber` se utiliza para dar formato a cualquier número en su representación sensible al idioma.

Acepta un número y una cadena que representa la configuración regional y devuelve una cadena con formato del número de la configuración regional deseada.

**Sintaxis**

```sql
{%= formatNumber(number/double,string) %}: string
```

Puede utilizar formatos y configuraciones regionales válidas, tal como se resume en [documentación del oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) y [Configuraciones regionales compatibles](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Ejemplo**

Esta consulta devuelve una cadena con formato en árabe correspondiente a 123456,789 como número de entrada.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Aleatorio {#random}

El `random` se utiliza para devolver un valor aleatorio entre 0 y 1.

**Sintaxis**

```sql
{%= random() %}: double
```

## Redondear a la baja {#round-down}

El `roundDown` se utiliza para redondear hacia abajo un número.

**Sintaxis**

```sql
{%= roundDown(double) %}: double
```

## Redondear al alza {#round-up}

El `Count only null` se utiliza para redondear un número.

**Sintaxis**

```sql
{%= roundUp(double) %}: double
```

## A la cadena hexadecimal {#to-hex-string}

El `toHexString` convierte cualquier número en su cadena hexadecimal.

**Sintaxis**

```sql
{%= toHexString(number) %}: string
```

**Ejemplo**

Esta consulta devuelve el valor hexadecimal de 158, es decir 9e.

```sql
{%= toHexString(158) %}
```

## A Int {#to-int}

El `toInt` se utiliza para convertir cualquiera de estos tipos (número, doble, int, largo, flotante, corto, byte, booleano, cadena) en un entero.

**Sintaxis**

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**Ejemplo**

Esta consulta devuelve el valor entero de 42,6, es decir, 42.

```sql
{%= toInt(42.6) %}: integer
```

## A Porcentaje {#to-percentage}

El `toPercentage` se utiliza para convertir un número en porcentaje.

**Sintaxis**

```sql
{%= toPercentage(double) %}: string
```

## A Precisión {#to-precision}

El `toPrecision` se utiliza para convertir un número en una precisión requerida.

**Sintaxis**

```sql
{%= toPrecision(double,int) %}: string
```

## Para crear una cadena {#to-string}

El **toString** convierte cualquier número en su representación de cadena.

**Sintaxis**

```sql
{%= toString(string) %}: string
```

**Ejemplo**

Esta consulta devuelve &quot;12&quot;.

```sql
{%= toString(12) %} 
```
