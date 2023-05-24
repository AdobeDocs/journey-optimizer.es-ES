---
product: journey optimizer
title: toString
description: Obtenga información acerca de la función toString
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toString, function, expression, recorrido
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 10%

---

# toString {#toString}

Convierte un valor de argumento en un valor de cadena, según su tipo. Para obtener más información sobre los tipos de datos, consulte [esta página](../expression/data-types.md).

## Categoría

Conversión

## Sintaxis de función

`toString(<parameter>)`

## Parámetros

| Parámetro | Descripción |
|--- |--- |
| dateTime | convierte la fecha en formato UTC |
| dateTimeOnly | convierte la fecha en formato UTC |
| duration | convertir en el número correspondiente de milisegundos como cadena |
| entero | convierte en una representación de cadena del valor (1 se convierte en &quot;1&quot;) |
| decimal | convierte en una representación de cadena del valor (1,5 se convierte en &quot;1,5&quot;) |
| Booleano | convertir el valor booleano como &quot;true&quot; si es verdadero, como &quot;false&quot; si es falso |

## Firmas y tipo devuelto

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Devolver una cadena.

## Ejemplo

`toString(4)`

Devuelve &quot;4&quot;.

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

Devuelve la representación de cadena del campo dateOnly dado (campo XDM Date), por ejemplo &quot;2016-08-18&quot;.
