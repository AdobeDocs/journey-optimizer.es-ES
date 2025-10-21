---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxis avanzada del editor de expresiones
description: Obtenga información acerca de la sintaxis utilizada en el editor de expresiones avanzadas
feature: Journeys
role: Engineer
level: Experienced
keywords: sintaxis, editor, recorrido
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 5%

---

# Sintaxis avanzada del editor de expresiones {#syntax}

A continuación se enumeran los conceptos básicos de sintaxis al usar el [Editor de expresiones avanzadas](expressionadvanced.md). <!-- Samples of use of the advanced expression editor are available on [this page](advanced-editor-use-cases.md).-->

## Paréntesis y prioridad de expresión {#parentheses-and-expression-priority}

Los paréntesis se pueden utilizar para hacer que una expresión compleja sea más legible. _(&lt;expression>)_ es el equivalente de _&lt;expression>_. Los paréntesis también pueden utilizarse para definir el orden de evaluación y la asociatividad.

Las expresiones se evalúan de izquierda a derecha. Se debe aplicar la asociatividad en operadores aritméticos: las multiplicaciones y divisiones tienen prioridad sobre las sumas y las restas. Para imponer un orden específico, se deben añadir paréntesis para delimitar las operaciones. Por ejemplo:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Expresión | Evaluación |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39; tiene prioridad sobre &#39;+&#39;: 2 \* 10 se evalúa → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Los paréntesis cambian la prioridad: (4 + 2) se evalúa → 6</li><li> 10 → 60</li></ul> |

## Distinción de mayúsculas y minúsculas {#case-sensitivity}

Estas son las diferentes reglas de distinción de mayúsculas y minúsculas:

* Todos los operadores (y, o, etc.) deben escribirse en minúsculas. Por ejemplo, _`<expression1>`y`<expression2>`_ son una expresión válida, mientras que la expresión _`<expression1>`Y`<expression2>`_ no lo son.
* Todos los nombres de función distinguen entre mayúsculas y minúsculas. Por ejemplo, _inAudience()_ es válida, mientras que la función _INAUDIENCE()_ no lo es.
* Las referencias de campo y los valores constantes distinguen entre mayúsculas y minúsculas: no son elementos integrados del lenguaje (a diferencia de operadores y funciones), son creados por el usuario final.

## Tipo de expresión devuelto {#returned-expression-type}

Según el contexto de uso, el editor de expresiones puede devolver valores diferentes.

| Uso del editor de expresiones avanzadas | Tipo de expresión devuelto esperado |
|--- |--- |
| Condición (condición de fuente de datos, condición de fecha) | Booleano |
| Temporizador personalizado | dateTimeOnly |
| Asignación de parámetros de acción | Cualquiera |
