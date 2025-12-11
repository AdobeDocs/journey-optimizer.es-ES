---
product: journey optimizer
title: Funciones de fecha
description: Obtenga información acerca de las funciones de fecha
feature: Journeys
role: Developer
level: Experienced
keywords: fecha, funciones, expresión, recorrido, hora
version: Journey Orchestration
source-git-commit: 8ca1c995bc38b110fa07573f922906c775fd5e6f
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 11%

---

# Funciones de fecha {#date-functions}

Las funciones de fecha permiten manipular y trabajar con valores de fecha y hora dentro de las expresiones de recorrido. Estas funciones son esenciales para las condiciones basadas en el tiempo, la programación y los cálculos temporales de los recorridos del cliente.

Utilice las funciones de fecha cuando necesite:

* Obtener la hora o fecha actual con el control específico de zona horaria ([ahora](#now), [nowWithDelta](#nowWithDelta), [currentTimeInMillis](#currentTimeInMillis))
* Compruebe si una fecha está dentro de un intervalo de tiempo específico ([inLastDays](#inLastDays), [inLastHours](#inLastHours), [inLastMonths](#inLastMonths), [inLastYears](#inLastYears), [inNextDays](#inNextDays), [inNextHours](#inNextHours), [inNextMonths](#inNextMonths), [inNextYears](#inNextYears))
* Modificar componentes de fecha y hora ([setHours](#setHours), [setDays](#setDays), [updateTimeZone](#updateTimeZone))
* Realizar cálculos y comparaciones basados en el tiempo
* Convertir entre diferentes formatos de tiempo y representaciones

Las funciones de fecha proporcionan un control preciso sobre la lógica temporal, lo que le permite crear rutas y condiciones de recorrido con distinción de tiempo que responden a marcos de tiempo y programaciones específicos.

>[!NOTE]
>
>Las funciones de esta página están disponibles en expresiones de recorrido. Algunas funciones como `now()` no están disponibles en el editor de personalización para el contenido de correo electrónico. [Más información](../../personalization/functions/dates.md)

## currentTimeInMillis {#currentTimeInMillis}

Devuelve el tiempo actual en milisegundos epoch.

+++Sintaxis

`currentTimeInMillis()`

+++

+++Parámetros

Esta función no utiliza parámetros.

+++

+++Firmas y tipo devuelto

`currentTimeInMillis()`

Devuelve un entero.

+++

+++Ejemplos

`currentTimeInMillis()`

Devuelve &quot;1544712617131&quot;

+++

## inLastDays {#inLastDays}

Devuelve verdadero si un dateTime determinado está entre ahora y ahora (días delta).

+++Sintaxis

`inLastDays(<dateTime>,<delta>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

+++

+++Firmas y tipo devuelto

`inLastDays(<dateTime>,<integer>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.

+++

## inLastHours {#inLastHours}

Devuelve verdadero si la fecha y hora dadas son entre ahora y ahora (horas delta).

+++Sintaxis

`inLastHours(<dateTime>,<delta>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

+++

+++Firmas y tipo devuelto

`inLastHours(<dateTime>,<integer>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.

`inLastHours(@event{MyEvent.timestamp}, 4)`

Devuelve verdadero.

+++

## inLastMonths {#inLastMonths}

Devuelve true si una fecha o dateTime determinada está entre ahora y ahora (meses delta).

+++Sintaxis

`inLastMonths(<dateTime>,<delta>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

+++

+++Firmas y tipo devuelto

`inLastMonths(<dateTime>,<integer>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.

+++

## inLastYears {#inLastYears}

Devuelve true si una fecha o dateTime determinada está entre ahora y ahora (años delta).

+++Sintaxis

`inLastYears(<dateTime>,<delta>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

+++

+++Firmas y tipo devuelto

`inLastYears(<dateTime>,<integer>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.

+++

## inNextDays {#inNextDays}

Devuelve true si una fecha o dateTime determinados están entre ahora y ahora + días delta.

+++Sintaxis

`inNextDays(<dateTime>,<delta>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

+++

+++Firmas y tipo devuelto

`inNextDays(<dateTime>,<integer>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.

+++

## inNextHours {#inNextHours}

Devuelve true si una fecha o dateTime determinada está entre ahora y ahora + horas delta.

+++Sintaxis

`inNextHours(<dateTime>,<delta>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

+++

+++Firmas y tipo devuelto

`inNextHours(<dateTime>,<integer>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve verdadero.

+++

## inNextMonths {#inNextMonths}

Devuelve verdadero si una fecha o fechaHora determinada está entre ahora y ahora + meses delta.

+++Sintaxis

`inNextMonths(<dateTime>,<delta>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

+++

+++Firmas y tipo devuelto

`inNextMonths(<dateTime>,<integer>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

Devuelve verdadero.

+++

## inNextYears {#inNextYears}

Devuelve true si una fecha o dateTime determinada está entre ahora y ahora + años delta.

+++Sintaxis

`inNextYears(<dateTime>,<delta>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora | dateTime |
| delta | entero |

+++

+++Firmas y tipo devuelto

`inNextYears(<dateTime>,<integer>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

Devuelve verdadero.

+++

## now {#now}

Devuelve la fecha actual en formato de fecha y hora. Para obtener más información sobre los tipos de datos, consulte [esta página](../expression/data-types.md).

>[!NOTE]
>
>Esta función solo está disponible en expresiones de recorrido. Para la personalización de correo electrónico y otro contenido, use `getCurrentZonedDateTime()` en su lugar. [Más información](../../personalization/functions/dates.md#get-current-zoned-date-time)

+++Sintaxis

`now(<parameter>)`

+++

+++Parámetros

| Parámetro | Descripción |
|--- |--- |
| cadena | Identificador de zona horaria (opcional) |

+++

+++Firmas y tipo devuelto

`now()`

`now("<timeZone id>")`

Devuelve un valor dateTime.

+++

+++Ejemplos

`now()`

Devuelve 2023-06-03T06:30Z.

`toString(now())`

Devuelve &quot;2023-06-03T06:30Z&quot;

`now("Europe/Paris")`

Devuelve 2023-06-03T08:30+02:00.

+++

## nowWithDelta {#nowWithDelta}

Devuelve la fecha y hora actuales, incluido un desplazamiento. Si se especifica un ID de zona horaria, se aplica el desplazamiento de zona horaria. Para obtener más información sobre los tipos de datos, consulte [esta página](../expression/data-types.md).

+++Sintaxis

`nowWithDelta(<parameters>)`

+++

+++Parámetros

| Parámetro | Descripción |
|--- |--- |
| delta | valor entero positivo o negativo |
| parte de fecha | años, meses, días, horas, minutos o segundos como una cadena |
| id de zona horaria | representación de cadena del valor de zona horaria. Para obtener más información, consulte [Tipos de datos](../expression/data-types.md). El ID de zona horaria debe ser una constante de cadena. No puede ser una referencia de campo ni una expresión. |

+++

+++Firmas y tipo devuelto

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Devuelve un valor dateTime.

+++

+++Ejemplos

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Devuelve un valor dateTime de hace exactamente 2 horas.

+++

## setHours {#setHours}

Establece solo las horas de una fecha, hora u hora. Por ejemplo, si desea esperar hasta una hora determinada mañana, puede forzar la hora.

+++Sintaxis

`setHours(<parameter>)`

+++

+++Parámetros

| Parámetro | Tipo |
|--- |--- |
| fecha y hora | dateTime |
| fecha y hora sin considerar la zona horaria | dateTimeOnly |
| horas | entero |

+++

+++Firmas y tipo devuelto

`setHours(<dateTime>,<hours>)`

Devuelve una fecha y hora.

`setHours(<dateTimeOnly>,<hours>)`

Devuelve una fecha y hora sin considerar la zona horaria.

+++

+++Ejemplos

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

Devuelve 2023-12-12T04:11:00Z.

`setHours(nowWithDelta(1, "days"), 20)`

Regresa mañana a las 8:XY p.m., siendo XY los minutos en el momento de la evaluación de la hora actual. Si la evaluación se realiza a las 2:45 a. m., la hora devuelta será las 8:45 p. m.

+++

## setDays {#setDays}

Establece solo el día de una fecha y hora o la fecha y hora. Por ejemplo, si desea esperar hasta un día determinado del mes, puede forzar el día.

+++Sintaxis

`setDays(<parameter>)`

+++

+++Parámetros

| Parámetro | Tipo |
|--- |--- |
| fecha y hora | dateTime |
| fecha y hora sin considerar la zona horaria | dateTimeOnly |
| días | entero |

+++

+++Firmas y tipo devuelto

`setDays(<dateTime>,<days>)`

Devuelve una fecha y hora.

`setDays(<dateTimeOnly>,<days>)`

Devuelve una fecha y hora sin considerar la zona horaria.

+++

+++Ejemplos

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Devuelve 2023-12-25T01:11:00Z.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`

+++

## updateTimeZone {#updateTimeZone}

Devuelve una nueva fecha y hora, con una nueva zona horaria en el mismo instante.

+++Sintaxis

`updateTimeZone(<parameters>)`

+++

+++Parámetros

* id de zona horaria: cadena
* dateTime

+++

+++Firma y tipo devuelto

`updateTimeZone(<dateTime>,<timeZone id>)`

Devuelve una fecha y hora.

+++

+++Ejemplos

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

Devuelve 2023-08-28T17:15:30.123+02:00.

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

Si el valor del campo de marca de tiempo es `2021-11-16T16:55:12.939318+01:00`, la función devuelve `2021-11-17T02:55:12.942115+11:00`.

+++

