---
product: Journey Optimizer
title: Sintaxis
description: Obtenga información sobre el editor de expresiones avanzadas
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: 7588a675319324e43bbc61a71b1fdfaab9cce93a
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 5%

---

# Sintaxis del editor de expresiones avanzadas {#syntax}

## Paréntesis y prioridad de expresión{#parentheses-and-expression-priority}

Los paréntesis se pueden utilizar para que una expresión compleja sea más legible. _(&lt;expression>)_ es el equivalente de _&lt;expression>_. Los paréntesis también se pueden utilizar para definir el orden de evaluación y la asociatividad.

Las expresiones se evalúan de izquierda a derecha. Se debe aplicar la asociatividad en los operadores aritméticos: las multiplicaciones y las divisiones tienen prioridad sobre las adiciones y sustracciones. Para imponer un orden específico, se debe añadir un paréntesis para delimitar las operaciones. Por ejemplo:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Expresión | Evaluación |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39; tiene prioridad sobre &#39;+&#39;: 2 * 10 se evalúa → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Los paréntesis cambian la prioridad: (4 + 2) se evalúa → 6</li><li> 6 * 10 → 60</li></ul> |

## Distinción entre mayúsculas y minúsculas{#case-sensitivity}

Estas son las distintas reglas de distinción entre mayúsculas y minúsculas:

* Todos los operadores (y, o, etc.) debe escribirse en minúsculas. Por ejemplo, _`<expression1>`y`<expression2>`_ es una expresión válida, mientras que la expresión _`<expression1>`Y`<expression2>`_ no.
* Todos los nombres de funciones distinguen entre mayúsculas y minúsculas. Por ejemplo, _inSegment()_ es válido mientras que la función _INSEGMENT()_ no.
* Las referencias de campo y los valores constantes distinguen entre mayúsculas y minúsculas: no son elementos integrados del idioma (a diferencia de los operadores y funciones), los crea el usuario final.

## Tipo de expresión devuelto{#returned-expression-type}

Según el contexto de uso, el editor de expresiones puede devolver valores diferentes.

| Uso del editor de expresiones avanzadas | Tipo de expresión devuelto esperado |
|--- |--- |
| Condición (condición de fuente de datos, condición de fecha) | Booleano |
| Temporizador personalizado | dateTimeOnly |
| Asignación de parámetros de acción | Cualquiera |
