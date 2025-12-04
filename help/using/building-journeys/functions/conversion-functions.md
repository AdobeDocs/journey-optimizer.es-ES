---
product: journey optimizer
title: Funciones de conversión
description: Obtenga información acerca de las funciones de conversión
feature: Journeys
role: Developer
level: Experienced
keywords: conversión, funciones, expresión, recorrido, tipo, conversión
version: Journey Orchestration
source-git-commit: 451a9e1e5d5e6e1408849e8d1c5c9644a95359da
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 6%

---

# Funciones de conversión {#conversion-functions}

Las funciones de conversión permiten transformar datos de un tipo a otro dentro de las expresiones de recorrido. Estas funciones son esenciales para garantizar la compatibilidad de los datos y la administración adecuada de tipos al trabajar con diferentes fuentes de datos y operaciones.

Utilice las funciones de conversión cuando necesite:

* Convertir valores de cadena a tipos numéricos, booleanos o de fecha ([toInteger](#toInteger), [toDecimal](#toDecimal), [toBool](#toBool))
* Transformar fechas y horas entre diferentes formatos y representaciones ([toDateTime](#toDateTime), [toDateTimeOnly](#toDateTimeOnly), [toDateOnly](#toDateOnly))
* Convierta valores numéricos entre tipos enteros y decimales ([toInteger](#toInteger), [toDecimal](#toDecimal))
* Convertir valores al formato de cadena ([toString](#toString)) o duración ([toDuration](#toDuration))
* Garantizar la compatibilidad de tipos para comparaciones y operaciones
* Procesar datos de fuentes externas que pueden tener diferentes formatos de tipo

Cada función de conversión gestiona automáticamente las reglas específicas del tipo y los casos extremos, lo que hace que la transformación de datos sea más fiable y predecible en las expresiones de recorrido.

## toBool {#toBool}

Convierte un valor de argumento en un valor booleano, según su tipo.

* Desde cadena: intente convertir el valor de cadena como booleano, de &quot;true&quot; si el valor de cadena es &quot;true&quot; y de &quot;false&quot; en caso contrario
* Desde numérico: true si el valor numérico no es igual a 0, false en caso contrario

+++Sintaxis

`toBool(<parameter>)`

+++

+++Parámetros

* decimal
* Booleano
* cadena
* entero

+++

+++Firmas y tipos devueltos

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`toBool("true")`

`toBool(1)`

Devuelve verdadero.

`toBool("this is not a boolean")`

Devuelve falso.

+++

## toDateOnly {#toDateOnly}

Convierte un argumento en un valor de tipo dateOnly. Para obtener más información sobre los tipos de datos, consulte esta [sección](../expression/data-types.md).

+++Sintaxis

`toDateOnly(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| Representación de cadena de una fecha como &quot;AAAA-MM-DD&quot; (formato XDM). También admite el formato ISO-8601: solo se tiene en cuenta la parte **full-date** (consulte [RFC 3339, sección 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | cadena |
| fecha y hora | dateTime |
| fecha y hora sin zona horaria | dateTimeOnly |
| valor entero de una época en milisegundos | entero |

+++

+++Firmas y tipos devueltos

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

Devuelve un valor de tipo dateOnly.

+++

+++Ejemplos

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

todos devuelven un objeto dateOnly que representa el 18-08-2023.

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

Devuelve dateOnly.

+++

## toDateTime {#toDateTime}

Convierte los parámetros en un valor de fecha y hora, según sus tipos.

+++Sintaxis

`toDateTime(<parameters>)`

+++

+++Parámetros

| Parámetro | Descripción |
|--- |--- |
| cadena | fecha y hora en formato ISO-8601. Una representación de cadena de una fecha y hora con información de zona horaria |
| cadena | id de zona horaria. Un identificador de zona horaria (por ejemplo, &quot;UTC&quot;, &quot;Europe/Paris&quot;) |
| dateOnly | representa una fecha sin zona horaria, vista como año-mes-día |
| dateTimeOnly | representa una fecha y hora sin una zona horaria, vista como año-mes-día-hora-minuto-segundo-milisegundo |
| entero | valor entero de una época en milisegundos |

+++

+++Firmas y tipos devueltos

`toDateTime(<string>)`

`toDateTime(<string>, <dateOnly>)`

`toDateTime(<string>, <dateTimeOnly>)`

`toDateTime(<integer>)`

Devolver **dateTime**.

+++

+++Ejemplos

`toDateTime("2023-08-18T23:17:59.123Z")`

Devuelve 2023-08-18T23:17:59.123Z

La cadena ISO-8601 ya incluye información de zona horaria.

`toDateTime("Europe/Paris", toDateOnly("2023-08-18"))`

Devuelve 2023-08-18T00:00:00.000+02:00

Esto crea un dateTime combinando una zona horaria con un valor de solo fecha. La hora se establece en medianoche (00:00:00) en la zona horaria especificada.

`toDateTime("UTC", toDateTimeOnly("2023-08-18T23:17:59.123"))`

Devuelve 2023-08-18T23:17:59.123Z

Esto crea un dateTime al aplicar una zona horaria a un valor dateTimeOnly (que no tiene información de zona horaria).

`toDateTime(1560762190189)`

Devuelve 2019-06-17T09:03:10.189Z

Convierte una marca de tiempo Unix en milisegundos en un valor dateTime.

+++

>[!NOTE]
>
>El ID de zona horaria debe ser una constante de cadena. No puede ser una referencia de campo ni una expresión. Para obtener más información sobre los tipos de datos, consulte [esta página](../expression/data-types.md).

## toDateTimeOnly {#toDateTimeOnly}

Convierte un valor de argumento en un valor de solo fecha y hora.

+++Sintaxis

`toDateTimeOnly(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| fecha y hora en formato ISO-8601 o &quot;AAAA-MM-DD&quot; (formato de fecha XDM) | cadena |
| fecha y hora | dateTime |

+++

+++Firmas y tipos devueltos

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`

Devuelve una fecha y hora sin tener en cuenta la zona horaria.

+++

+++Ejemplos

`toDateTimeOnly ("2023-08-18")`

devuelve un valor dateTime que representa el valor 2023-08-18T00:00:00.000

`toDateTimeOnly(now())`

+++

## toDecimal {#toDecimal}

Convierte un valor de argumento en un valor decimal, según su tipo.

+++Sintaxis

`toDecimal(<parameter>)`

+++

+++Parámetros

| Parámetro | Descripción |
|--- |--- |
| cadena | convierte el valor de cadena como decimal |
| dateTime | convierte la fecha como el número de milisegundos (epoch milisegundos) |
| Booleano | convierte el valor booleano como 1 si es verdadero, 0 si es falso |
| entero | convierte a decimal (ejemplo).: 1 se convierte en 1,0) |

+++

+++Firmas y tipos devueltos

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

Devuelve un decimal.

+++

+++Ejemplos

`toDecimal("4.0")`

Devuelve 4.0.

+++

## toDuration {#toDuration}

Convierte un valor de argumento en una duración. Para obtener más información sobre los tipos de datos, consulte [esta página](../expression/data-types.md).

+++Sintaxis

`toDuration(<parameter>)`

+++

+++Parámetros

| Parámetro | Descripción |
|--- |--- |
| cadena | formatos basados en el formato de duración ISO-8601 PnDTnHnMn.nS con días considerados exactamente 24 horas |
| entero | número de milisegundos |

Expresión de cadena If: los formatos aceptados se basan en el formato de duración ISO-8601 PnDTnHnMn.nS con días considerados exactamente 24 horas.

La cadena comienza con un signo opcional, indicado por el símbolo ASCII negativo o positivo. Si es negativo, se anula todo el periodo. La letra ASCII &quot;P&quot; es la siguiente en mayúsculas o minúsculas. A continuación, hay cuatro secciones, cada una de las cuales consta de un número y un sufijo. Las secciones tienen sufijos en ASCII de &quot;D&quot;, &quot;H&quot;, &quot;M&quot; y &quot;S&quot; para días, horas, minutos y segundos, aceptados en mayúsculas o minúsculas. Los sufijos deben aparecer en orden. La letra ASCII &quot;T&quot; debe aparecer antes de la primera aparición, si la hay, de una sección de hora, minuto o segunda. Al menos una de las cuatro secciones debe estar presente, y si &quot;T&quot; está presente debe haber al menos una sección después de la &quot;T&quot;. La parte numérica de cada sección debe constar de uno o más dígitos ASCII. El número puede ir precedido del símbolo ASCII negativo o positivo. El número de días, horas y minutos que se deben analizar. El número de segundos debe analizarse en junto con una fracción opcional. El punto decimal puede ser un punto o una coma. La parte fraccionada puede tener de cero a 9 dígitos.

+++

+++Firmas y tipo devuelto

`toDuration(<string>)`

`toDuration(<integer>)`

Devuelve una duración.

+++

+++Ejemplos

`toDuration("PT10H")`

Devuelve una duración de 10 horas.

`toDuration("PT4S")`

Devuelve la duración de 4 segundos.

`toDuration(4000)`

Devuelve la duración de 4 segundos.

+++

## toInteger {#toInteger}

Convierte un valor de argumento en un entero.

+++Sintaxis

`toInteger(<parameter>)`

+++

+++Parámetros

| Parámetro | Descripción |
|--- |--- |
| cadena | convierte el valor de cadena como un entero |
| dateTime | convierte la fecha como el número de milisegundos (epoch milisegundos) |
| decimal | convierte en entero eliminando la parte decimal (ejemplo: 1,5 se convierte en 1) |
| Booleano | convierte el valor booleano como 1 si es verdadero, 0 si es falso |

+++

+++Firmas y tipo devuelto

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

Devuelve un entero.

+++

+++Ejemplos

`toInteger("4")`

Devuelve 4.

+++

## toString {#toString}

Convierte un valor de argumento en un valor de cadena, según su tipo. Para obtener más información sobre los tipos de datos, consulte [esta página](../expression/data-types.md).

+++Sintaxis

`toString(<parameter>)`

+++

+++Parámetros

| Parámetro | Descripción |
|--- |--- |
| dateTime | convierte la fecha en formato UTC |
| dateTimeOnly | convierte la fecha en formato UTC |
| duration | convertir en el número correspondiente de milisegundos como cadena |
| entero | convierte en una representación de cadena del valor (1 se convierte en &quot;1&quot;) |
| decimal | convierte en una representación de cadena del valor (1,5 se convierte en &quot;1,5&quot;) |
| Booleano | convertir el valor booleano como &quot;true&quot; si es verdadero, como &quot;false&quot; si es falso |

+++

+++Firmas y tipo devuelto

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Devolver una cadena.

+++

+++Ejemplos

`toString(4)`

Devuelve &quot;4&quot;.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Devuelve la representación de cadena del campo dateOnly dado (campo de fecha XDM), por ejemplo &quot;2023-08-18&quot;.

`toString(toDuration(1520))`

Devuelve &quot;PT1.52S&quot;.

+++

