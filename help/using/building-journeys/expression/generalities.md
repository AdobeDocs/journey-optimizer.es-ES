---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxis
description: Obtenga información acerca del editor de expresiones avanzadas
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sintaxis, editor, recorrido
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---

# Sintaxis avanzada del editor de expresiones {#syntax}

## Paréntesis y prioridad de expresión{#parentheses-and-expression-priority}

Los paréntesis se pueden utilizar para hacer que una expresión compleja sea más legible. _(&lt;expression>)_ es el equivalente de _&lt;expression>_. Los paréntesis también pueden utilizarse para definir el orden de evaluación y la asociatividad.

Las expresiones se evalúan de izquierda a derecha. Se debe aplicar la asociatividad en operadores aritméticos: las multiplicaciones y divisiones tienen prioridad sobre las sumas y las restas. Para imponer un orden específico, se deben añadir paréntesis para delimitar las operaciones. Por ejemplo:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Expresión | Evaluación |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39; tiene prioridad sobre &#39;+&#39;: 2 * 10 se evalúa → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Los paréntesis cambian la prioridad: (4 + 2) se evalúa → 6</li><li> 10 → 60</li></ul> |

## Distinción entre mayúsculas y minúsculas{#case-sensitivity}

Estas son las diferentes reglas de distinción de mayúsculas y minúsculas:

* Todos los operadores (y, o, etc.) debe escribirse en minúsculas. Por ejemplo, _`<expression1>`y`<expression2>`_ es una expresión válida, mientras que _`<expression1>`Y`<expression2>`_ no es.
* Todos los nombres de función distinguen entre mayúsculas y minúsculas. Por ejemplo, _inSegment()_ es válida, mientras que la función _INSEGMENT()_ no es.
* Las referencias de campo y los valores constantes distinguen entre mayúsculas y minúsculas: no son elementos integrados del lenguaje (a diferencia de operadores y funciones), son creados por el usuario final.

## Tipo de expresión devuelto{#returned-expression-type}

Según el contexto de uso, el editor de expresiones puede devolver valores diferentes.

| Uso del editor de expresiones avanzadas | Tipo de expresión devuelto esperado |
|--- |--- |
| Condición (condición de fuente de datos, condición de fecha) | Booleano |
| Temporizador personalizado | dateTimeOnly |
| Asignación de parámetros de acción | Cualquiera |
