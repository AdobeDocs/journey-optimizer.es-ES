---
title: Biblioteca de funciones Date Time
description: Biblioteca de funciones Date Time
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

La variable `age` se utiliza para recuperar la edad de una fecha determinada.

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

## Tiempo actual en milisegundos{#current-time}

La variable `currentTimeInMillis` se utiliza para recuperar la hora actual en milisegundos de epoch.

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

La variable `dateDiff` se utiliza para recuperar la diferencia entre dos fechas en número de días.

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

La variable `dayOfWeek` se utiliza para recuperar el día de la semana.

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

La variable `dayOfYear` se utiliza para recuperar el día del año.

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

La variable `formatDate` se utiliza para dar formato a un valor de fecha y hora. El formato debe ser un patrón de Java DateTimeFormat válido.

**Sintaxis**

```sql
{%= formatDate(datetime, format) %}
```

Donde la primera cadena es el atributo date y el segundo valor es cómo desea que se convierta y muestre la fecha.

>[!NOTE]
>
> Si un patrón de fecha no es válido, la fecha se volverá al formato estándar ISO.
>
> Puede utilizar las funciones de formato de fecha de Java que se resumen en [documentación de oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Ejemplo**

La siguiente operación devolverá la fecha con el formato siguiente: MM/DD/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## Formato de fecha con compatibilidad con configuración regional{#format-date-locale}

La variable `formatDate` se utiliza para dar formato a un valor de fecha y hora en su representación correspondiente que diferencia el idioma, es decir, en una configuración regional deseada. El formato debe ser un patrón de Java DateTimeFormat válido.

**Sintaxis**

```sql
{%= formatDate(datetime, format, locale) %}
```

Cuando la primera cadena es el atributo date, el segundo valor es cómo desea que se convierta y muestre la fecha y el tercer valor representa la configuración regional en formato de cadena.

>[!NOTE]
>
> Si un patrón de fecha no es válido, la fecha se volverá al formato estándar ISO.
>
> Puede utilizar las funciones de formato de fecha de Java que se resumen en [documentación de oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Puede utilizar el formato y las configuraciones regionales válidas, como se resume en [documentación de oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) y [Localizaciones compatibles](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).


**Ejemplo**

La siguiente operación devolverá la fecha con el formato siguiente: MM/DD/AA y configuración regional FRANCIA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## Días establecidos{#set-days}

La variable `setDays` se utiliza para establecer el día del mes para una fecha y hora determinadas.

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

La variable `setHours` se utiliza para establecer la hora de la fecha y la hora.

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

La variable `toUTC` se utiliza para convertir una fecha y hora a UTC.


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

La variable `weekOfYear` se utiliza para recuperar la semana del año.

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