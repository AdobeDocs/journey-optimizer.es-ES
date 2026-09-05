---
product: journey optimizer
title: Funciones de fecha
description: Obtenga información acerca de las funciones de fecha
feature: Journeys
role: Developer
level: Experienced
keywords: fecha, funciones, expresión, recorrido, hora
version: Journey Orchestration
exl-id: 68c102c1-f1c7-44b7-893f-9a3b7e0854b6
TQID: https://experienceleague.adobe.com/C2Z5SufckUxCNf9TsloziZS-Q3KPzmgMVNGJGiwDQ08
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: []
source-git-commit: 52f7da843df1b3165aa6064efe893328413a7ad3
workflow-type: tm+mt
source-wordcount: 1135
ht-degree: 9%

---

# Funciones de fecha {#date-functions}

Las funciones de fecha permiten manipular y trabajar con valores de fecha y hora dentro de las expresiones de recorrido. Estas funciones son esenciales para las condiciones basadas en el tiempo, la programación y los cálculos temporales de los recorridos del cliente.

Utilice las funciones de fecha cuando necesite:

* Obtener la hora o fecha actual con el control específico de zona horaria ([ahora](#now), [nowWithDelta](#nowWithDelta), [currentTimeInMillis](#currentTimeInMillis))
* Calcule la diferencia entre dos fechas u horas, en días o milisegundos, según el tipo de parámetro ([dateDiff](#dateDiff))
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

## dateDiff {#dateDiff}

Devuelve la diferencia entre dos fechas u horas del mismo tipo. La unidad del resultado depende del tipo de parámetro: `dateOnly` parámetros devuelven la diferencia en **días**, mientras que `dateTimeOnly` y `dateTime` parámetros devuelven la diferencia en **milisegundos**. Devuelve `null` si alguno de los parámetros es `null`.

>[!NOTE]
>
>Esta función es diferente de `dateDiff`, disponible en el [editor de personalización](../../personalization/functions/dates.md#date-diff). La versión del editor de personalización solo acepta `dateTime` parámetros y siempre devuelve la diferencia en días.

+++Sintaxis

`dateDiff(<date1>,<date2>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|--------------------------------------|
| fecha 1 | dateOnly, dateTimeOnly o dateTime |
| fecha 2 | dateOnly, dateTimeOnly o dateTime |

Ambos parámetros deben utilizar el mismo tipo de datos; no se admiten los tipos de mezcla (por ejemplo, `dateOnly` con `dateTime`). Los parámetros pueden ser valores de fecha literales, otras funciones como `now()` o atributos contextuales (campos de carga útil de evento, campos de respuesta de acción personalizada, campos de entidad o perfil y variables) siempre y cuando se escriban como `dateOnly`, `dateTimeOnly` o `dateTime`.

+++

+++Firmas y tipo devuelto

`dateDiff(<dateOnly>,<dateOnly>)`

Devuelve un entero que representa el número de días entre las dos fechas.

`dateDiff(<dateTimeOnly>,<dateTimeOnly>)`

Devuelve un entero que representa el número de milisegundos entre las dos fechas y horas.

`dateDiff(<dateTime>,<dateTime>)`

Devuelve un entero que representa el número de milisegundos entre las dos fechas y horas.

+++

+++Ejemplos

`dateDiff(toDateOnly('2023-12-15'), toDateOnly('2023-12-12'))`

Devuelve 3 (días).

`dateDiff(toDateTimeOnly('2023-12-15T00:00:00'), toDateTimeOnly('2023-12-12T00:00:00'))`

Devuelve 259200000 (milisegundos, equivalente a 3 días).

`dateDiff(now(), toDateTime('2024-12-25T00:00:00Z'))`

Devuelve el número de milisegundos entre hoy y el 25 de diciembre de 2024.

`dateDiff(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate}, toDateOnly('2023-01-01'))`

Devuelve el número de días entre el campo `birthDate` del perfil y el 1 de enero de 2023, suponiendo que `birthDate` tiene el tipo `dateOnly`.

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

`nowWithDelta(1, "months", "Asia/Tokyo")`

Cuando se evalúa el 31-01-2026, devuelve 2026-02-28T...; cuando se evalúa el 31-05-2026, devuelve 30-06-2026...

`nowWithDelta()` utiliza aritmética de mes calendario. Si el mes de destino tiene menos días que el día del mes actual, el resultado se normaliza al último día válido de ese mes. La función no se traslada al mes siguiente.

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

Regresa mañana a las 8:XY p.m., siendo XY los minutos en el momento de la evaluación de la hora actual. Si la evaluación se realiza a las 2:45, la hora de retorno será las 8:45 p.m.

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

{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-functions-date-functions.md}}
