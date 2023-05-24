---
product: journey optimizer
title: toDuration
description: Obtenga información acerca de la función toDuration
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDuration, function, expression, recorrido
exl-id: c78e30c5-99ee-4dc7-a03a-17f7ee65f83a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 3%

---

# toDuration {#toDuration}

Convierte un valor de argumento en una duración. Para obtener más información sobre los tipos de datos, consulte [esta página](../expression/data-types.md).

## Categoría

Conversión

## Sintaxis de función

`toDuration(<parameter>)`

## Parámetros

| Parámetro | Descripción |
|--- |--- |
| string | formatos basados en el formato de duración ISO-8601 PnDTnHnMn.nS con días considerados exactamente 24 horas |
| entero | número de milisegundos |

Expresión de cadena If: los formatos aceptados se basan en el formato de duración ISO-8601 PnDTnHnMn.nS con días considerados exactamente 24 horas.

La cadena comienza con un signo opcional, indicado por el símbolo ASCII negativo o positivo. Si es negativo, se anula todo el periodo. La letra ASCII &quot;P&quot; es la siguiente en mayúsculas o minúsculas. A continuación, hay cuatro secciones, cada una de las cuales consta de un número y un sufijo. Las secciones tienen sufijos en ASCII de &quot;D&quot;, &quot;H&quot;, &quot;M&quot; y &quot;S&quot; para días, horas, minutos y segundos, aceptados en mayúsculas o minúsculas. Los sufijos deben aparecer en orden. La letra ASCII &quot;T&quot; debe aparecer antes de la primera aparición, si la hay, de una sección de hora, minuto o segunda. Al menos una de las cuatro secciones debe estar presente, y si &quot;T&quot; está presente debe haber al menos una sección después de la &quot;T&quot;. La parte numérica de cada sección debe constar de uno o más dígitos ASCII. El número puede ir precedido del símbolo ASCII negativo o positivo. El número de días, horas y minutos que se deben analizar. El número de segundos debe analizarse en junto con una fracción opcional. El punto decimal puede ser un punto o una coma. La parte fraccionada puede tener de cero a 9 dígitos.

## Firmas y tipo devuelto

`toDuration(<string>)`

`toDuration(<integer>)`

Devuelve una duración.

## Ejemplos

`toDuration("PT10H")`

Devuelve una duración de 10 horas.

`toDuration("PT4S")`

Devuelve la duración de 4 segundos.

`toDuration(4000)`

Devuelve la duración de 4 segundos.
