---
title: Biblioteca de funciones de fecha y hora
description: Biblioteca de funciones de fecha y hora
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: edc040de-dfb3-4ebc-91b4-239e10c2260b
TQID: https://experienceleague.adobe.com/J-aZtYitBu8T4oSwTwKNNDeA-7tA4l8Wi5YZ1WLcT3E
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1762
ht-degree: 5%

---

# Funciones de fecha y hora{#date-time}

Las funciones de fecha y hora se utilizan para realizar operaciones de fecha y hora en valores dentro de Journey Optimizer.

>[!NOTE]
>
>La función `now()` no está disponible en el editor de personalización. Use `getCurrentZonedDateTime()` o `currentTimeInMillis()` en su lugar para los valores de fecha y hora actuales. [Más información](../../email/code-content.md#date-time-limitations)

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

## Agregar horas {#add-hours}

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

La función `addMinutes` ajusta una fecha determinada en un número determinado de minutos, utilizando valores positivos para aumentar y valores negativos para disminuir.

**Sintaxis**

```sql
{%= addMinutes(date, number) %}
```

+++Ejemplo

* Entrada: `{%= addMinutes(stringToDate("2024-11-01T17:59:51Z"),10) %}`
* Salida: `2024-11-01T18:09:51Z`

+++

## Agregar meses {#add-months}

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

La función `addSeconds` ajusta una fecha determinada en un número determinado de segundos, utilizando valores positivos para aumentar y valores negativos para disminuir.

**Sintaxis**

```sql
{%= addSeconds(date, number) %}
```

+++Ejemplo

* Entrada: `{%= addSeconds(stringToDate("2024-11-01T17:19:51Z"),10) %}`
* Salida: `2024-11-01T17:20:01Z`

+++

## Añadir años {#add-years}

La función `addYears` ajusta una fecha determinada en un número determinado de años, utilizando valores positivos para aumentar y valores negativos para disminuir.

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

## Edad En Días {#age-days}

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

## Edad En Meses {#age-months}

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

## Convertir fechaZonaHora {#convert-zoned-date-time}

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

+++Ejemplo: Días restantes hasta un evento

La siguiente operación devuelve el número de días entre hoy y una fecha futura almacenada en el perfil (por ejemplo, una fecha de finalización de suscripción o una fecha de evento):

```sql
{%= dateDiff(getCurrentZonedDateTime(), stringToDate(profile.events.subscriptionEndDate)) %}
```

+++

+++Ejemplo real: Cuenta atrás en la línea de asunto

Use `dateDiff` para generar una cuenta atrás dinámica para las líneas de asunto o el contenido de correo electrónico:

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%} — use them before they're gone!
{%else%}
Your points have expired.
{%/if%}
```

Salida (ejemplo): `Your points expire in 7 days — use them before they're gone!`

+++

## Día del mes {#day-month}

`dayOfMonth` devuelve el número que representa el día del mes.

**Sintaxis**

```sql
{%= dayOfMonth(datetime) %}
```

+++Ejemplo

* Entrada: `{%= dayOfMonth(stringToDate("2024-11-05T17:19:51Z")) %}`
* Salida: `5`

+++


## Día de la semana {#day-week}

La función `dayOfWeek` se usa para recuperar el día de la semana. Devuelve un entero entre 1 (lunes) y 7 (domingo) según la norma ISO-8601.

**Sintaxis**

```sql
{%= dayOfWeek(datetime) %}
```

+++Ejemplo — Detectar fines de semana en contenido personalizado

Utilice esta función dentro del correo electrónico o el contenido para adaptar la mensajería en función del día. El operador de comparación en PQL es `=` (solo es igual a, no `==`):

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — your request will be processed on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

| Day | Valor devuelto |
|-----|----------------|
| Lunes | 1 |
| Martes | 2 |
| Miércoles | 3 |
| Jueves | 4 |
| Viernes | 5 |
| Sábado | 6 |
| Domingo | 7 |

+++

>[!NOTE]
>
>`dayOfWeek()` está diseñado para **personalizar el contenido** (por ejemplo, adaptar el texto del cuerpo del correo electrónico en función del día). Si necesita **enrutar perfiles de forma diferente en un recorrido** según el día de la semana (por ejemplo, omitir fines de semana para una actividad de espera), use la opción integrada **Condición de tiempo → día de la semana** disponible directamente en la actividad Condición de recorrido. [Más información](../../building-journeys/condition-activity.md#date_condition)

## Día del año{#day-year}

La función `dayOfYear` se usa para recuperar el día del año.

**Sintaxis**

```sql
{%= dayOfYear(datetime) %}
```

+++Ejemplo

* Entrada: `{%= dayOfYear(stringToDate("2024-03-15T00:00:00Z")) %}`
* Salida: `75`

+++

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

* Entrada: `{%= extractMinutes(stringToDate("2024-11-01T17:19:51Z"))%}`
* Salida: `19`

+++

+++Ejemplo real: mostrar el tiempo actual solo como HH:MM

Combine `extractHours` y `extractMinutes` para representar solamente la parte de tiempo sin ninguna fecha, día o año:

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is confirmed for {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

Salida (ejemplo): `Your appointment is confirmed for 14:05.`

El protector de cero a la izquierda (`{%#if m < 10%}0{%/if%}`) garantiza que los minutos por debajo de 10 se muestren como dos dígitos (p. ej. `09` en lugar de `9`).

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

## Formato de fecha{#format-date}

La función `formatDate` se usa para dar formato a un valor de fecha y hora. El formato debe ser un patrón DateTimeFormat de Java válido.

**Sintaxis**

```sql
{%= formatDate(datetime, format) %}
```

Donde el primer parámetro es el atributo de fecha y hora y el segundo valor es cómo desea que se convierta y muestre la fecha.

>[!NOTE]
>
> La función `formatDate` requiere un tipo de campo **fecha-hora** como entrada, no como cadena. Si el campo se almacena como un tipo de cadena en el esquema XDM, primero debe convertirlo a fecha-hora mediante una función de conversión como `stringToDate()` o `toDateTime()`. Consulte los ejemplos siguientes.
>
> Si un patrón de fecha no es válido, la fecha volverá a estar en el formato estándar ISO.
>
> Puede utilizar las funciones de formato de fecha de Java como se resume en [Documentación de Oracle](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html){_blank}

**Ejemplos**

+++Formato de un campo de fecha y hora

La siguiente operación aplica formato MM/DD/AA a un campo de fecha y hora.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}
```

+++

+++Convertir una cadena a fecha primero

Si el campo se almacena como una cadena, primero debe convertirlo a una fecha-hora con `stringToDate()` antes de aplicarle formato.

```sql
{%= formatDate(stringToDate(profile.person.birthDayAndMonth), "MM/DD/YY") %}
```

+++

+++Formato de fecha completo con nombre de día

La siguiente operación devuelve un formato de fecha completo con el nombre del día, el nombre del mes, el día y el año.

```sql
{%= formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy") %}
```

Salida: `Wednesday January 01 2020`

+++

+++Fecha dinámica basada en la hora del sistema

Puede dar formato a la hora del sistema actual para generar fechas dinámicas. La siguiente operación devuelve la fecha actual en formato MM/dd/AAAA.

```sql
{%= formatDate(getCurrentZonedDateTime(), "MM/dd/YYYY") %}
```

Salida (el 30 de enero de 2026): `01/30/2026`

+++

+++Formato de día de la semana

Puede extraer el día de la semana en forma corta.

```sql
{%= formatDate(getCurrentZonedDateTime(), "EEE") %}
```

Salida: `Sun` (para domingo), `Mon` (para lunes), `Tue` (para martes), etc.

Para salida en minúsculas, combine con la función `lowerCase`:

```sql
{%= lowerCase(formatDate(getCurrentZonedDateTime(), "EEE")) %}
```

Salida: `sun`, `mon`, `tue`, etc.

+++

+++Formato de una marca de tiempo desde un evento de contexto

Al utilizar una marca de tiempo de un atributo de contexto de evento de recorrido, se aplican dos requisitos:

* **Agrupe la marca de tiempo con`toDateTime()`**: `formatDate()` no reconoce automáticamente las marcas de tiempo de evento de contexto como valores de fecha y hora.
* **Agrupar identificadores de evento numéricos en comillas invertidas**: si el identificador de evento es un número (por ejemplo, `1697323153`), debe especificarse con comillas invertidas en la ruta de acceso de la expresión; de lo contrario, el editor genera un error de sintaxis de PQL.
* **Use la sintaxis `{% let %}` o `{%= %}`**: puede asignar el resultado a una variable con `{% let %}` y procesarla con `{{varName}}`, o usar directamente la sintaxis `{%= %}` en línea.

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
{{appointmentDate}}
```

Salida (ejemplo): `18/03/2026 14:30`

+++

>[!CAUTION]
>
>**Error común: &quot;entrada &#39;(&#39; no coincidente esperando \&lt;EOF\>&quot;**
>
>Este error de sintaxis de PQL se produce cuando se utiliza `formatDate()` con una marca de tiempo de evento de contexto en línea (`{%= formatDate(...) %}`). Las causas más comunes son un id. de evento numérico que no se ajusta entre comillas invertidas (`` ` ``) o un campo de marca de tiempo pasado directamente a `formatDate()` sin ajustarlo primero a `toDateTime()`. Para solucionar ambos problemas, utilice el patrón de asignación `{% let %}` que se muestra en el ejemplo anterior.

### Caracteres de patrón {#pattern-characters}

Algunas letras de patrón pueden tener un aspecto similar, pero representan conceptos diferentes.

| Patrón | Significado | Ejemplo (para `2023-12-31T10:15:30Z`) |
|---------|---------|--------------------------------------|
| `y` | Año natural (año estándar) | `2023` |
| `Y` | Año basado en la semana (ISO 8601). Puede diferir en los límites anuales. | `2024` (desde el 31 de diciembre de 2023 cae en la primera semana de 2024) |
| `M` | Mes del año (1-12 o texto como `Jan`, `January`) | `12` o `Dec` |
| `m` | Minuto de la hora (0-59) | `15` |
| `d` | Día del mes (1-31) | `31` |
| `D` | Día del año (1-366) | `365` |

### Formato de fecha con compatibilidad con configuración regional{#format-date-locale}

La función `formatDate` se puede usar para dar formato a un valor de fecha y hora en su representación correspondiente con distinción de idioma, es decir, en una configuración regional deseada. El formato debe ser un patrón DateTimeFormat de Java válido.

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

La siguiente operación devuelve la fecha con el siguiente formato: dd/MM/AA y configuración regional FRANCIA.

```sql
{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY", "fr_FR") %}
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

+++Ejemplo

Establezca el día del mes en el primero:

* Entrada: `{%= setDays(stringToDate("2024-11-15T17:19:51Z"), 1) %}`
* Salida: `2024-11-01T17:19:51Z`

+++

## Establecer horas{#set-hours}

La función `setHours` se usa para establecer la hora de la fecha y hora.

**Sintaxis**

```sql
{%= setHours(datetime, hour) %}
```

+++Ejemplo: Definir una fecha y hora en una hora específica

* Entrada: `{%= setHours(stringToDate("2024-11-01T17:19:51Z"), 0) %}`
* Salida: `2024-11-01T00:19:51Z`

+++

+++Ejemplo real: X días antes de una fecha de finalización dinámica

Para dirigirse a un perfil X días antes de una fecha almacenada en su perfil (por ejemplo, caducidad de suscripción), utilice `addDays` con un valor negativo:

```sql
{%= addDays(stringToDate(profile.subscription.endDate), -7) %}
```

Para normalizar también la hora a una hora fija (p. ej. 9 a. m.), combine con `setHours`:

```sql
{%= setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9) %}
```

+++

## Hasta la fecha y hora {#to-date-time}

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

* Entrada: `{%= truncateToStartOfWeek(stringToDate("2024-11-19T17:19:51Z"))%} // tuesday`
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

+++Ejemplo

* Entrada: `{%= weekOfYear(stringToDate("2024-11-01T17:19:51Z")) %}`
* Salida: `44`

+++

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
