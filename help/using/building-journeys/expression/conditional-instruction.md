---
solution: Journey Optimizer
product: journey optimizer
title: Instrucción condicional (si, entonces, de lo contrario)
description: Obtenga información acerca de la instrucción condicional
feature: Journeys
role: Engineer
level: Experienced
keywords: avanzado, condición, acción, recorrido
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Instrucción condicional (si, entonces, de lo contrario) {#conditional-instruction}

La instrucción condicional (if, then, else) se admite en el editor avanzado. Permite definir expresiones más complejas. Se compone de los siguientes elementos:

* **[!UICONTROL if]**: la condición que se va a evaluar primero.
* **[!UICONTROL then]**: la expresión que se va a evaluar en caso de que el resultado de la evaluación de la condición sea true.
* **[!UICONTROL else]**: la expresión que se va a evaluar en caso de que el resultado de la evaluación de la condición sea false.

>[!NOTE]
>
>Se requieren paréntesis alrededor de todas las expresiones.

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` debe devolver un **booleano**.

`<expression2>` y `<expression3>` deben tener el mismo tipo o tipos compatibles. Las firmas admitidas y los tipos devueltos son:

```json
boolean,boolean : boolean
dateTime,dateTime : dateTime
dateTimeOnly,dateTimeOnly : dateTimeOnly
decimal,integer : decimal
integer,decimal : integer
integer,decimal : decimal
duration,duration : duration
string,string : string
listBoolean,listBoolean : listBoolean
listDateTime,listDateTime : listDateTime
listDateTimeOnly,listDateTimeOnly : listDateTimeOnly
listDateOnly,listDateOnly : listDateOnly
listDecimal,listDecimal : listDecimal
listInteger,listInteger : listInteger
listString,listString : listString
```

**Uso**

La instrucción condicional permite optimizar el flujo de trabajo de recorrido al reducir el número de actividades de condición. Por ejemplo, dentro de la misma actividad de acción, puede especificar dos alternativas para una definición de campo utilizando solo una expresión de condición.

Ejemplo de una actividad de acción (para un campo que espera una cadena como resultado de la instrucción condicional):

```json
if (startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```
