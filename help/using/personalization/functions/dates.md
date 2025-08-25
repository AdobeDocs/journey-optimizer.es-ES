---
title: Biblioteca de funciones de fecha y hora
description: Biblioteca de funciones de fecha y hora
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
source-git-commit: 3eab04f28b1daab556c4b4395d67f28d292fc52b
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 13%

---

# Funciones de fecha y hora{#date-time}

Las funciones de fecha y hora se utilizan para realizar operaciones de fecha y hora en valores dentro de Journey Optimizer.

## Añadir días {#add-days}

La función `addDays` ajusta una fecha determinada en un número determinado de días, utilizando valores positivos para aumentar y valores negativos para disminuir.

**Sintaxis**

```sql
{%= addDays(date, number) %}
```

+++Ejemplo

* Entrada: `{%= addDays(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Salida: `2024-11-11T17:19:51Z`

+++

## Añadir horas {#add-hours}

La función `addHours` ajusta una fecha determinada en un número determinado de horas, utilizando valores positivos para aumentar y valores negativos para disminuir.

**Sintaxis**

```sql
{%= addHours(date, number) %}
```

+++Ejemplo

* Entrada: `{%= addHours(stringToDate("2024-11-01T17:19:51Z"),1) %}`
* Salida: `2024-11-01T18:19:51Z`

+++

## Añadir minutos {#add-minutes}

La función `addMinutes` ajusta una fecha determinada en un número determinado de minutos, utilizando valores positivos para aumentar y valores negativos para disminuir

**Sintaxis**

```sql
{%= addMinutes(date, number) %}
```

+++Ejemplo

* Entrada: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Salida: `2024-11-01T18:09:51Z`

+++

## Añadir meses {#add-months}

La función `addMonths` ajusta una fecha determinada en un número determinado de meses, utilizando valores positivos para aumentar y valores negativos para disminuir.

**Sintaxis**

```sql
{%= addMonths(date, number) %}
```

+++Ejemplo

* Entrada: `{%= addMonths(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Salida: `2025-01-01T17:19:51Z`

+++

## Añadir segundos {#add-seconds}

El `addSeconds` ajusta una fecha determinada en un número determinado de segundos, utilizando valores positivos para aumentar y valores negativos para disminuir.

**Sintaxis**

```sql
{%= addSeconds(date, number) %}
```

+++Ejemplo

* Entrada: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Salida: `2024-11-01T17:20:01Z`

+++

## Añadir años {#add-years}

El `addYears` ajusta una fecha determinada en un número determinado de años, utilizando valores positivos para aumentar y valores negativos para disminuir.

**Sintaxis**

```sql
{%= addYears(date, number) %}
```

+++Ejemplo

* Entrada: `{%= addYears(stringToDate("2024-11-01T17:19:51Z"),2) %}`
* Salida: `2026-11-01T17:19:51Z`

+++

## Edad{#age}

La función `age` se usa para recuperar la edad de una fecha determinada.

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

## Antigüedad en días {#age-days}

La función `ageInDays` calcula la antigüedad de una fecha determinada en días, es decir, el número de días transcurridos entre la fecha determinada y la fecha actual, negativos para fechas futuras y positivos para fechas pasadas.

**Sintaxis**

```sql
{%= ageInDays(date) %}
```

+++Ejemplo

currentDate = 2025-01-07T12:17:10.720122+05:30 (Asia/Calcuta)

* Entrada: `{%= ageInDays(stringToDate("2025-01-01T17:19:51Z"))%}`
* Salida: `5`

+++

## Antigüedad en meses {#age-months}

La función `ageInMonths` calcula la edad de una fecha determinada en meses, es decir, el número de meses transcurridos entre la fecha determinada y la fecha actual, negativos para fechas futuras y positivos para fechas pasadas.

**Sintaxis**

```sql
{%= ageInMonths(date) %}
```

+++Ejemplo

currentDate = 2025-01-07T12:22:46.993748+05:30(Asia/Calcuta)

* Entrada: `{%=ageInMonths(stringToDate("2024-01-01T00:00:00Z"))%}`
* Salida: `12`

+++

## Comparar fechas {#compare-dates}

La función `compareDates` compara la fecha de la primera entrada con la otra. Devuelve 0 si fecha1 es igual a fecha2, -1 si fecha1 es anterior a fecha2 y 1 si fecha1 es posterior a fecha2.

**Sintaxis**

```sql
{%= compareDates(date1, date2) %}
```

+++Ejemplo

* Entrada: `{%=compareDates(stringToDate("2024-12-02T00:00:00Z"), stringToDate("2024-12-03T00:00:00Z"))%}`
* Salida: `-1`

+++

## Convertir ZonedDateTime {#convert-zoned-date-time}

La función `convertZonedDateTime` convierte una fecha y hora en una zona horaria determinada.

**Sintaxis**

```sql
{%= convertZonedDateTime(dateTime, timezone) %}
```

+++Ejemplo

* Entrada: `{%=convertZonedDateTime(stringToDate("2019-02-19T08:09:00Z"), "Asia/Tehran")%}`
* Salida: `2019-02-19T11:39+03:30[Asia/Tehran]`

+++

## Hora actual en milisegundos{#current-time}

La función `currentTimeInMillis` se usa para recuperar el tiempo actual en milisegundos epoch.

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

La función `dateDiff` se usa para recuperar la diferencia entre dos fechas en número de días.

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

## Día del mes {#day-month}

`dayOfWeek` devuelve el número que representa el día del mes.

**Sintaxis**

```sql
{%= dayOfMonth(datetime) %}
```

+++Ejemplo

* Entrada: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Salida: `5`

+++


## Día de la semana {#day-week}

La función `dayOfWeek` se usa para recuperar el día de la semana.

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

La función `dayOfYear` se usa para recuperar el día del año.

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

## Diferencia en segundos {#diff-seconds}

La función `diffInSeconds` devuelve la diferencia entre dos fechas en términos de segundos.

**Sintaxis**

```sql
{%= diffInSeconds(endDate, startDate) %}
```

+++Ejemplo

* Entrada: `{%=diffInSeconds(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T17:19:01Z"))%}`
* Salida: `50`

+++

## Extraer horas {#extract-hours}

La función `extractHours` extrae el componente de hora de una marca de tiempo determinada.

**Sintaxis**

```sql
{%= extractHours(date) %}
```

+++Ejemplo

* Entrada: `{%= extractHours(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `17`

+++

## Extraer minutos {#extract-minutes}

La función `extractMinutes` extrae el componente de minuto de una marca de tiempo determinada.

**Sintaxis**

```sql
{%= extractMinutes(date) %}
```

+++Ejemplo

* Entrada: `{%= extractMinute(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `19`

+++

## Extraer meses {#extract-months}

La función `extractMonth` extrae el componente de mes de una marca de tiempo determinada.

**Sintaxis**

```sql
{%= extractMonths(date) %}
```

+++Ejemplo

* Entrada: `{%=extractMonth(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `11`

+++

## Extraer segundos {#extract-seconds}

La función `extractSeconds` extrae el segundo componente de una marca de tiempo determinada.

**Sintaxis**

```sql
{%= extractSeconds(date) %}
```

+++Ejemplo

* Entrada: `{%=extractSeconds(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `51`

+++

## Dar formato a fecha{#format-date}

La función `formatDate` se usa para dar formato a un valor de fecha y hora. El formato debe ser un patrón DateTimeFormat de Java válido.

**Sintaxis**

```sql
{%= formatDate(datetime, format) %}
```

Donde la primera cadena es el atributo de fecha y el segundo valor es cómo desea que se convierta y muestre la fecha.

>[!NOTE]
>
> Si un patrón de fecha no es válido, la fecha volverá a estar en el formato estándar ISO.
>
> Puede utilizar las funciones de formato de fecha de Java como se resume en [Documentación de Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Ejemplo**

La siguiente operación devuelve la fecha con el siguiente formato: MM/DD/AA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

## Formato de fecha con compatibilidad con configuración regional{#format-date-locale}

La función `formatDate` se usa para dar formato a un valor de fecha y hora en su representación correspondiente con distinción de idioma, es decir, en una configuración regional deseada. El formato debe ser un patrón DateTimeFormat de Java válido.

**Sintaxis**

```sql
{%= formatDate(datetime, format, locale) %}
```

Cuando la primera cadena es el atributo de fecha, el segundo valor es cómo desea que se convierta y muestre la fecha y el tercer valor representa la configuración regional en formato de cadena.

>[!NOTE]
>
> Si un patrón de fecha no es válido, la fecha volverá a estar en el formato estándar ISO.
>
> Puede usar funciones de formato de fecha Java como se resume en [Documentación de Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html).
>
> Puede usar formato y configuraciones regionales válidas, tal como se resume en [Documentación de Oracle](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) y [Configuraciones regionales compatibles](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html).

**Ejemplo**

La siguiente operación devuelve la fecha con el siguiente formato: MM/DD/AA y configuración regional FRANCIA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/DD/YY", "fr_FR") %}
```

## Obtener CurrentZonedDateTime {#get-current-zoned-date-time}

La función `getCurrentZonedDateTime` devuelve la fecha y la hora actuales con información de zona horaria.

**Sintaxis**

```sql
{%= getCurrentZonedDateTime() %}
```

+++Ejemplo

* Entrada: `{%= getCurrentZonedDateTime() %}`
* Salida: `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

+++

## Diferencia de horas {#hours-difference}

La función `diffInHours` devuelve la diferencia entre dos fechas en términos de horas.

**Sintaxis**

```sql
{%= diffInHours(endDate, startDate) %}
```

+++Ejemplo

* Entrada: `{%= diffInHours(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T07:19:51Z"))%}`
* Salida: `10`

+++

## Diferencia de minutos{#diff-minutes}

La función `diffInMinutes` se usa para devolver la diferencia entre dos fechas en términos de minutos.

**Sintaxis**

```sql
{%= diffInMinutes(endDate, startDate) %}
```

+++Ejemplo

* Entrada: `{%= diffInMinutes(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-11-01T16:19:51Z"))%}`
* Salida: `60`

+++

## Diferencia de meses {#months-difference}

La función `diffInMonths` devuelve la diferencia entre dos fechas en términos de meses.

**Sintaxis**

```sql
{%= diffInMonths(endDate, startDate) %}
```

+++Ejemplo

* Entrada: `{%=diffInMonths(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2024-08-01T17:19:51Z"))%}`
* Salida: `3`

+++

## Establecer días{#set-days}

La función `setDays` se usa para establecer el día del mes para la fecha y hora determinadas.

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

La función `setHours` se usa para establecer la hora de la fecha y hora.

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

## A Fecha Hora {#to-date-time}

La función `ToDateTime` convierte la cadena en fecha. Devuelve la fecha epoch como salida para una entrada no válida.

**Sintaxis**

```sql
{%= toDateTime(string, string) %}
```

+++Ejemplo

* Entrada: `{%=toDateTime("2024-11-01T17:19:51Z")%}`
* Salida: `2024-11-01T17:19:51Z`

+++

## A UTC{#to-utc}

La función `toUTC` se usa para convertir una fecha y hora en UTC.

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

## Truncar al inicio del día {#truncate-day}

La función `truncateToStartOfDay` se usa para modificar una fecha y hora determinadas al establecerla en el inicio del día con la hora establecida en 00:00.

**Sintaxis**

```sql
{%= truncateToStartOfDay(date) %}
```

+++Ejemplo

* Entrada: `{%= truncateToStartOfDay(stringToDate("2024-11-01T17:19:51Z")) %}`
* Salida: `2024-11-01T00:00Z`

+++

## truncateToStartOfQuarter {#truncate-quarter}

La función `truncateToStartOfQuarter` se usa para truncar una fecha y hora al primer día de su trimestre (por ejemplo, 1 de enero, 1 de abril, 1 de julio, 1 de octubre) a las 00:00.

**Sintaxis**

```sql
{%= truncateToStartOfQuarter(dateTime) %}
```

+++Ejemplo

* Entrada: `{%=truncateToStartOfQuarter(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `2024-10-01T00:00Z`

+++

## truncateToStartOfWeek {#truncate-week}

La función `truncateToStartOfWeek` modifica una fecha y hora determinada al establecerla en el inicio de la semana (lunes a las 00:00).

**Sintaxis**

```sql
{%= truncateToStartOfWeek(dateTime) %}
```

+++Ejemplo

* Entrada: `truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
* Salida: `2024-11-18T00:00Z // monday`

+++

## truncateToStartOfYear {#truncate-year}

La función `truncateToStartOfYear` se usa para modificar una fecha y hora determinadas truncándolas al primer día del año (1 de enero) a las 00:00.

**Sintaxis**

```sql
{%= truncateToStartOfYear(dateTime) %}
```

+++Ejemplo

* Entrada: `{%=truncateToStartOfYear(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `2024-01-01T00:00Z`

+++

## Semana del año {#week-of-year}

La función `weekOfYear` se usa para recuperar la semana del año.

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

## Diferencia de años {#diff-years}

La función `diffInYears` se usa para devolver la diferencia entre dos fechas en términos de años.

**Sintaxis**

```sql
{%= diffInYears(endDate, startDate) %}: int
```

+++Ejemplo

* Entrada: `{%=diffInYears(stringToDate("2024-11-01T17:19:51Z"), stringToDate("2019-10-01T17:19:51Z"))%}`
* Salida: `5`

+++
