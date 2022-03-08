---
title: Biblioteca de funciones Date Time
description: Biblioteca de funciones Date Time
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 6%

---

# Funciones de fecha y hora{#date-time}

Las funciones de fecha y hora se utilizan para realizar operaciones de fecha y hora en valores dentro de Journey Optimizer.

## Edad{#age}

La variable `age` se utiliza para recuperar la edad de una fecha determinada.

**Formato**

```sql
 {%= age(date) %}
```

<!--
**Example**

The following operation gets the value of the identity map for the key `example@example.com`.

```sql
 {%= age(date) %}
```
-->

## Tiempo actual en milisegundos{#current-time}

La variable `currentTimeInMillis` se utiliza para recuperar la hora actual en milisegundos de epoch.

**Formato**

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

**Formato**

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

**Formato**

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

**Formato**

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

**Formato**

```sql
{%= formatDate(date, format) %}
```

Donde la primera cadena es el atributo date y el segundo valor es cómo desea que se convierta y muestre la fecha.

>[!NOTE]
>
> Si un patrón de fecha no es válido, la fecha se volverá al formato estándar ISO.
>
> Puede utilizar las funciones de formato de fecha Java como se resume [en la documentación de Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Ejemplo**

La siguiente operación devolverá la fecha con el formato siguiente: MM/DD/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY") %}
```

## Días establecidos{#set-days}

La variable `setDays` se utiliza para establecer el día del mes para una fecha y hora determinadas.

**Formato**

```sql
{%= setDays(date, day) %}
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

**Formato**

```sql
{%= setHours(date, hour) %}
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


**Formato**

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

**Formato**

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
