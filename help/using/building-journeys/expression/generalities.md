---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxis avanzada del editor de expresiones
description: Obtenga información acerca de la sintaxis utilizada en el editor de expresiones avanzadas
feature: Journeys
role: Developer
level: Experienced
keywords: sintaxis, editor, recorrido
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-PTYUf-njT3-LsI-A5IKEMDGOl4JecZ-ayM0rU4f2HI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 620
ht-degree: 2%

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

* Todos los operadores (y, o, etc.) debe escribirse en minúsculas. Por ejemplo, _`<expression1>`y`<expression2>`_ son una expresión válida, mientras que la expresión _`<expression1>`Y`<expression2>`_ no lo son.
* Todos los nombres de función distinguen entre mayúsculas y minúsculas. Por ejemplo, _inAudience()_ es válida, mientras que la función _INAUDIENCE()_ no lo es.
* Las referencias de campo y los valores constantes distinguen entre mayúsculas y minúsculas: no son elementos integrados del lenguaje (a diferencia de operadores y funciones), son creados por el usuario final.

## Tipo de expresión devuelto {#returned-expression-type}

Según el contexto de uso, el editor de expresiones puede devolver valores diferentes.

| Uso del editor de expresiones avanzadas | Tipo de expresión devuelto esperado |
|--- |--- |
| Condición (condición de fuente de datos, condición de fecha) | Booleano |
| Temporizador personalizado | dateTimeOnly |
| Asignación de parámetros de acción | Cualquiera |

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página describe las reglas de sintaxis principales del editor de expresiones avanzadas de Recorrido: la prioridad de los operadores entre paréntesis, la distinción entre mayúsculas y minúsculas para los operadores y las funciones y el tipo de valor devuelto esperado para cada contexto de editor.

**Intenciones:**

* Controle el orden de evaluación de expresiones ajustando las subexpresiones entre paréntesis
* Operadores de escritura (`and`, `or`, `not`) en minúsculas para evitar errores de sintaxis
* Use nombres de funciones con mayúsculas y minúsculas correctamente (p. ej. `inAudience()` no `INAUDIENCE()`)
* Comprenda que las condiciones deben devolver un booleano, los temporizadores personalizados deben devolver `dateTimeOnly` y las asignaciones de parámetros de acción pueden devolver cualquier tipo

**Glosario:**

* **Prioridad de expresión**: El orden en que se evalúan los operadores; las multiplicaciones y divisiones tienen prioridad sobre las adiciones y las sustracciones *(específicas del producto)*
* **Distinción entre mayúsculas y minúsculas**: en el editor avanzado, los operadores deben estar en minúsculas, los nombres de función distinguen entre mayúsculas y minúsculas y las referencias de campo distinguen entre mayúsculas y minúsculas según el usuario *(específico del producto)*
* **dateTimeOnly**: El tipo de valor devuelto requerido para las expresiones de temporizador personalizadas (actividad de espera); representa una fecha y hora sin una zona horaria *(específica del producto)*

**Protecciones:**

* Operadores (`and`, `or`, `not`, etc.) debe escribirse en minúsculas; las variantes en mayúsculas no son válidas
* Todos los nombres de función distinguen entre mayúsculas y minúsculas: `inAudience()` es válido pero `INAUDIENCE()` no lo es
* La aritmética sigue la prioridad estándar: `*` y `/` se evalúan antes que `+` y `-`; use paréntesis para anular la prioridad
* Las condiciones siempre devuelven un valor booleano; los temporizadores personalizados siempre devuelven `dateTimeOnly`

**Terminología:**

* Nombre canónico: Sintaxis del editor de expresiones avanzadas — Acrónimo: none — variants: sintaxis de expresión, sintaxis de editor
* Sinónimos: &quot;prioridad de expresión&quot; = &quot;prioridad de operador&quot;; &quot;paréntesis&quot; = &quot;corchetes&quot; (en contexto de expresión)
* No confundir: distingue entre mayúsculas y minúsculas en el operador (los operadores deben estar en minúsculas) ≠ la distinción entre mayúsculas y minúsculas en las referencias de campo (los nombres de campo son creados por el usuario y distinguen entre mayúsculas y minúsculas cuando se escriben).

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Se evalúa `4 + 2 * 10` en 60 o 24?** — Se evalúa como 24 porque `*` tiene prioridad sobre `+`; use `(4 + 2) * 10` para obtener 60.
* **Q: ¿Puedo escribir `AND` en mayúsculas en una expresión?** — No; todos los operadores deben estar en minúsculas (`and`, `or`, `not`).
* **Q: ¿Los nombres de función distinguen entre mayúsculas y minúsculas?** — Sí; `inAudience()` es válido pero `INAUDIENCE()` no.
* **Q: ¿Qué tipo debe devolver una expresión de condición?** — Un booleano.
* **Q: ¿Qué tipo de valor devuelto se requiere para una expresión de temporizador de actividad de espera personalizada?** — `dateTimeOnly`.

+++
