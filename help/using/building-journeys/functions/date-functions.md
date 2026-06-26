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
source-git-commit: 15cd7992e3263d7d2b94cf2efe50850d16e04a5d
workflow-type: tm+mt
source-wordcount: 1384
ht-degree: 7%

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

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página documenta todas las funciones de fecha y hora disponibles en las expresiones de recorrido de AJO, e incluye información sobre cómo obtener la hora actual, comprobar si una fecha se encuentra dentro de una ventana de hora relativa y modificar los componentes de fecha y hora.

**Intenciones:**
* Obtener la fecha y hora actual (con zona horaria opcional) utilizando `now` o `nowWithDelta`
* Recuperar la hora actual como un entero epoch usando `currentTimeInMillis`
* Compruebe si una fecha y hora se encuentra dentro de los últimos N días, horas, meses o años con `inLastDays`, `inLastHours`, `inLastMonths`, `inLastYears`
* Compruebe si una fecha y hora se encuentra dentro de los N días, horas, meses o años siguientes usando `inNextDays`, `inNextHours`, `inNextMonths`, `inNextYears`
* Forzar una hora o día específico del mes en un valor datetime utilizando `setHours` o `setDays`
* Convertir una fecha y hora en una zona horaria diferente preservando al mismo tiempo el mismo instante mediante `updateTimeZone`

**Glosario:**
* **dateTime**: un valor de fecha y hora que incluye información de desplazamiento de zona horaria *(específico del producto)*
* **dateTimeOnly**: un valor de fecha y hora sin información de zona horaria *(específico del producto)*
* **epoch milisegundos**: Un entero que representa el número de milisegundos transcurridos desde 1970-01-01T00:00:00Z
* **delta**: Un desplazamiento entero (positivo o negativo) utilizado con `nowWithDelta` para cambiar el tiempo actual en un número de años, meses, días, horas, minutos o segundos

**Protecciones:**
* `now()` solo está disponible en expresiones de recorrido; en su lugar, utilice `getCurrentZonedDateTime()` para la personalización del correo electrónico
* El identificador de zona horaria de `nowWithDelta` debe ser una constante de cadena; no se admiten referencias de campo ni expresiones dinámicas
* El identificador de zona horaria de `updateTimeZone` debe ser una constante de cadena

**Terminología:**
* Nombre canónico: Funciones de fecha — Acrónimo: none — variantes: funciones de fecha y hora, funciones temporales
* Sinónimos: &quot;now()&quot; = &quot;current datetime&quot;; &quot;currentTimeInMillis()&quot; = &quot;current epoch miliseconds&quot;
* No confunda: &quot;inLastDays&quot; (retrocede en el tiempo) ≠ &quot;inNextDays&quot; (retrocede en el tiempo)
* No confunda: &quot;setHours&quot; (reemplaza el componente de hora) ≠ &quot;nowWithDelta&quot; (desplaza la hora actual)
* No confunda: &quot;updateTimeZone&quot; (mismo instante, diferente representación de zona horaria) ≠ &quot;setHours&quot; (cambia el valor de hora en sí)

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Puedo usar `now()` en el contenido de personalización de correo electrónico?** — No, `now()` solo está disponible en expresiones de recorrido. Usar `getCurrentZonedDateTime()` para la personalización del correo electrónico.
* **Q: ¿Cómo puedo comprobar si se ha producido un evento en las últimas 24 horas?** — Usar `inLastHours(@event{MyEvent.timestamp}, 24)`.
* **Q: ¿Cómo puedo obtener el desfase de tiempo actual de 2 horas en el pasado?** — Usar `nowWithDelta(-2, "hours")`.
* **Q: ¿Qué hace `updateTimeZone` de manera diferente a `setHours`?** — `updateTimeZone` mantiene el mismo instante en el tiempo pero lo expresa en una zona horaria diferente, mientras que `setHours` cambia realmente el componente de hora del valor datetime.
* **Q: ¿Puede el parámetro de zona horaria de `nowWithDelta` ser un campo de perfil?** — No, el ID de zona horaria debe ser una constante de cadena; no se admiten referencias de campo.
* **Q: ¿Qué sucede cuando `nowWithDelta()` se usa con meses y la fecha actual es una fecha de fin de mes?** — La función utiliza aritmética de mes-calendario y normaliza el resultado hasta el último día válido del mes de destino. Por ejemplo, si agrega 1 mes al 31 de enero, se devuelve el 28 de febrero (no el 3 de marzo).

+++
