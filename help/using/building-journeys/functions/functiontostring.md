---
product: adobe campaign
title: toString
description: Obtenga información sobre la función toString
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 7%

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
| dateTime | convierte la fecha en formato de fecha UTC |
| dateTimeOnly | convierte la fecha en formato de fecha UTC |
| duration | convertir en el número correspondiente de milisegundos como una cadena |
| zona horaria | convertir en la representación de cadena de id de zona horaria (JOD id) |
| integer | se convierte en una representación de cadena del valor (1 se convierte en &quot;1&quot;) |
| decimal | se convierte en una representación de cadena del valor (1,5 se convierte en &quot;1,5&quot;) |
| Booleano | convierta el valor booleano en &#39;true&#39; si es &quot;true&quot;, &#39;false&#39; si es &quot;false&quot; |

## Firmas y tipo devuelto

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<timeZone>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

Devuelve una cadena.

## Ejemplo

`toString(4)`

Devuelve &quot;4&quot;.
