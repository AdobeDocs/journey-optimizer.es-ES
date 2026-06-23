---
solution: Journey Optimizer
product: journey optimizer
title: Instrucción condicional (si, entonces, de lo contrario)
description: Obtenga información acerca de la instrucción condicional
feature: Journeys
role: Developer
level: Experienced
keywords: avanzado, condición, acción, recorrido
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SObpEvgu0D-pcoLVaKM7iRffLTSP1stp1zcg4Ygs-vQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: cce82f05-fc3c-4af7-85ff-8bba603861a7id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 576
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

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica la instrucción condicional `if / then / else` disponible en el editor de expresiones avanzadas de Recorrido, incluidas las reglas de sintaxis, las combinaciones de tipos compatibles y un ejemplo práctico de uso.

**Intenciones:**

* Escriba una expresión condicional usando `if`, `then` y `else` para devolver valores diferentes basados en una condición booleana
* Reduzca el número de actividades de condición en un recorrido incrustando la lógica condicional en línea dentro de una sola actividad de acción
* Determine qué combinaciones de tipos de datos son válidas para las ramas `then` y `else`
* Aplique la instrucción condicional para enrutar los tokens de notificación push a APNS o FCM en función del modelo del dispositivo

**Glosario:**

* **Instrucción condicional**: Una construcción de expresión `if / then / else` en el editor avanzado que evalúa un valor booleano y devuelve una de las dos expresiones *(específicas del producto)*
* **Editor de expresiones avanzadas**: La interfaz de Journey Optimizer para escribir expresiones complejas usada en condiciones, actividades de espera y asignación de parámetros de acción *(específico del producto)*

**Protecciones:**

* Se requieren paréntesis en todas las expresiones de las cláusulas `if`, `then` y `else`
* La cláusula `if` (`<expression1>`) debe devolver un tipo booleano
* Las expresiones `then` y `else` (`<expression2>` y `<expression3>`) deben tener el mismo tipo o tipos compatibles (por ejemplo, `decimal` y `integer` son compatibles, `string` y `integer` no)
* No se admiten todas las combinaciones de tipos; sólo son válidos los pares enumerados en la tabla de firmas admitidas

**Terminología:**

* Nombre canónico: Instrucción condicional — Acrónimo: none — variantes: if/then/else, condición de estilo ternario
* Sinónimos: &quot;instrucción condicional&quot; = &quot;condición dentro de la línea&quot; = &quot;if-then-else expression&quot;
* No confunda: instrucción condicional (expresión en línea) ≠ actividad Condition (un nodo de lienzo de recorrido)

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Es necesario envolver la cláusula `if` entre paréntesis?** — Sí, se requieren paréntesis en todas las expresiones, incluida la condición de la cláusula `if`.
* **Q: ¿Puedo usar `if / then / else` para devolver un número de una rama y una cadena de otra?** — No; `<expression2>` y `<expression3>` deben tener tipos iguales o compatibles.
* **Q: ¿Cómo reduce la complejidad del recorrido la instrucción condicional?** — Permite especificar dos alternativas de valor de campo dentro de una sola actividad de acción mediante una expresión, evitando así un nodo de actividad Condición independiente en el lienzo.
* **Q: ¿Qué tipo devuelve la instrucción condicional si ambas ramas son cadenas?** — Devuelve un `string`.
* **Q: ¿Se puede usar `if / then / else` para seleccionar un canal de notificaciones push?** — Sí; por ejemplo, evaluando el modelo de dispositivo para devolver `'apns'` para los dispositivos Apple o `'fcm'` para otros.

+++
