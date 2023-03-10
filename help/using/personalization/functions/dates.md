---
title: Biblioteca de funciones de fecha y hora
description: Biblioteca de funciones de fecha y hora
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 2444d8fbe3a86feb0497d754b4f57f234fa29e49
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 4%

---

# Funciones de fecha y hora{#date-time}

Las funciones de fecha y hora se utilizan para realizar operaciones de fecha y hora en valores dentro de Journey Optimizer.

## Edad{#age}

El `age` se utiliza para recuperar la edad de una fecha determinada.

**Sintaxis**

```sql
 {%= age(datetime) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(datetime) %}
```
-->

## Hora actual en milisegundos{#current-time}

El `currentTimeInMillis` se utiliza para recuperar el tiempo actual en milisegundos epoch.

**Sintaxis**

```sql
{%= currentTimeInMillis() %}
```

<!--
**Example**

The following operation gets all the keys for the map `identityMap`.

```sql
{%= keys(identityMap) %}
```
-->

## Diferencia de fechas{#date-diff}

El `dateDiff` se utiliza para recuperar la diferencia entre dos fechas en número de días.

**Sintaxis**

```sql
{%= dateDiff(datetime,datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## Día de la semana{#day-week}

El `dayOfWeek` se utiliza para recuperar el día de la semana.

**Sintaxis**

```sql
{%= dayOfWeek(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Día del año{#day-year}

El `dayOfYear` se utiliza para recuperar el día del año.

**Sintaxis**

```sql
{%= dayOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Formato de fecha{#format-date}

El `formatDate` se utiliza para dar formato a un valor de fecha y hora. El formato debe ser un patrón DateTimeFormat de Java válido.

**Sintaxis**

```sql
{%= formatDate(datetime, format) %}
```

Donde la primera cadena es el atributo de fecha y el segundo valor es cómo desea que se convierta y muestre la fecha.

>[!NOTE]
>
> Si un patrón de fecha no es válido, la fecha volverá a estar en el formato estándar ISO.
>
> Puede utilizar funciones de formato de fecha de Java como se resume en [documentación del oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Ejemplo**

La siguiente operación devuelve la fecha con el siguiente formato: MM/DD/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## Formato de fecha con compatibilidad con configuración regional{#format-date-locale}

El `formatDate` se utiliza para dar formato a un valor de fecha y hora en su representación sensible al idioma correspondiente, es decir, en una configuración regional deseada. El formato debe ser un patrón DateTimeFormat de Java válido.

**Sintaxis**

```sql
{%= formatDate(datetime, format, locale) %}
```

Cuando la primera cadena es el atributo de fecha, el segundo valor es cómo desea que se convierta y muestre la fecha y el tercer valor representa la configuración regional en formato de cadena.

>[!NOTE]
>
> Si un patrón de fecha no es válido, la fecha volverá a estar en el formato estándar ISO.
>
> Puede utilizar funciones de formato de fecha de Java como se resume en [documentación del oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Puede utilizar formatos y configuraciones regionales válidas, tal como se resume en [documentación del oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) y [Configuraciones regionales compatibles](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).


**Ejemplo**

La siguiente operación devuelve la fecha con el siguiente formato: MM/DD/AA y configuración regional FRANCIA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## Establecer días{#set-days}

El `setDays` se utiliza para establecer el día del mes para la fecha y hora determinadas.

**Sintaxis**

```sql
{%= setDays(datetime, day) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->

## Establecer horas{#set-hours}

El `setHours` se utiliza para establecer la hora de la fecha y hora.

**Sintaxis**

```sql
{%= setHours(datetime, hour) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## A UTC{#to-utc}

El `toUTC` se utiliza para convertir una fecha y hora en UTC.


**Sintaxis**

```sql
{%= toUTC(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->


## Semana del año UTC{#week-of-year}

El `weekOfYear` se utiliza para recuperar la semana del año.

**Sintaxis**

```sql
{%= weekOfYear(datetime) %}
```

<!--
**Example**

The following operation gets all the values for the map `identityMap`.

```sql
{%= values(identityMap) %}
```
-->