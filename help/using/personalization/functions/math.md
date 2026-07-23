---
title: Biblioteca de funciones matemáticas
description: Biblioteca de funciones matemáticas
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: c440ff464b2ea58519e6f1ba900728adfa718232
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 5%

---

# Funciones matemáticas {#math}

Aprenda a utilizar las funciones matemáticas en el editor de personalización.

## Absoluta {#absolute}

La función `absolute` se usa para convertir un número en su valor absoluto.

**Sintaxis**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

La función `formatNumber` se usa para dar formato a cualquier número en su representación con distinción de idioma.

Acepta un número y una cadena que representa la configuración regional y devuelve una cadena con formato del número de la configuración regional deseada.

**Sintaxis**

```sql
{%= formatNumber(number/double,string) %}: string
```

Puede usar formato y configuraciones regionales válidas, tal como se resume en [Documentación de Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) y [Configuraciones regionales compatibles](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**Ejemplo**

Esta consulta devuelve una cadena con formato en árabe correspondiente a 123456,789 como número de entrada.

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Aleatorio {#random}

La función `random` se usa para devolver un valor aleatorio entre 0 y 1.

**Sintaxis**

```sql
{%= random() %}: double
```

## Redondear hacia abajo {#round-down}

La función `roundDown` se usa para redondear hacia abajo un número.

**Sintaxis**

```sql
{%= roundDown(double) %}: double
```

## Redondear al alza {#round-up}

La función `roundUp` se usa para redondear un número.

**Sintaxis**

```sql
{%= roundUp(double) %}: double
```

## A la cadena hexadecimal {#to-hex-string}

La función `toHexString` convierte cualquier número en su cadena hexadecimal.

**Sintaxis**

```sql
{%= toHexString(number) %}: string
```

**Ejemplo**

Esta consulta devuelve el valor hexadecimal de 158, es decir, 9e.

```sql
{%= toHexString(158) %}
```

## A Int {#to-int}

La función `toInt` se usa para convertir cualquiera de estos tipos (número, doble, int, largo, flotante, corto, byte, booleano, cadena) en un entero.

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

La función `toPercentage` se usa para convertir un número en porcentaje.

**Sintaxis**

```sql
{%= toPercentage(double) %}: string
```

## A Precisión {#to-precision}

La función `toPrecision` convierte un número en un número fijo de decimales y devuelve una cadena con relleno cero.
Esta función equivale al comportamiento de JavaScript `toFixed()`.

**Sintaxis**

```sql
{%= toPrecision(double,int) %}: string
```

## Para crear una cadena {#to-string}

La función **toString** convierte cualquier número en su representación de cadena.

**Sintaxis**

```sql
{%= toString(string) %}: string
```

**Ejemplo**

Esta consulta devuelve &quot;12&quot;.

```sql
{%= toString(12) %} 
```

