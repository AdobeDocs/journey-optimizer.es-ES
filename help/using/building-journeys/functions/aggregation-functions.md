---
product: journey optimizer
title: Funciones de agregación
description: Obtenga información sobre las funciones de agregación
feature: Journeys
role: Developer
level: Experienced
keywords: agregación, funciones, expresión, recorrido, promedio, recuento, máximo, mínimo, suma
version: Journey Orchestration
exl-id: 871a5212-5b94-4a54-bf1d-276022be3c95
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1105
ht-degree: 5%

---

# Funciones de agregación {#aggregation-functions}

Las funciones de agregación realizan cálculos en un conjunto de valores y devuelven un único resultado resumido. Estas funciones permiten analizar los datos dentro de las expresiones de recorrido calculando promedios, buscando valores mínimos y máximos, contando elementos y sumando valores numéricos.

Utilice funciones de agregación cuando necesite:

* Calcular valores estadísticos de listas o matrices ([avg](#avg), [sum](#sum), [min](#min), [max](#max))
* Contar elementos en colecciones ([count](#count), [countOnlyNull](#countOnlyNull), [countWithNull](#countWithNull)), con opciones para incluir o excluir valores nulos
* Determinar valores únicos dentro de conjuntos de datos ([distinctCount](#distinctCount), [distinctCountWithNull](#distinctCountWithNull))
* Tome decisiones basadas en datos y en métricas calculadas

Las funciones de agregación administran automáticamente los valores nulos según su comportamiento específico, lo que facilita el trabajo con datos del mundo real que pueden contener valores que faltan o indefinidos.


## avg {#avg}

Devuelve el valor promedio entre un conjunto de expresiones, dado como una lista o dos expresiones. Los valores nulos se omiten.

+++Sintaxis

`avg(<parameter>)`

+++

+++Parámetros

Tipos admitidos:

* listInteger
* listDecimal
* decimal
* entero

+++

+++Firmas y tipo devuelto

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

Devuelve un valor decimal.

+++

+++Ejemplos

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

Devuelve 7.0.

`avg(10.2, 3)`

Devuelve 6.6.

+++

## recuento {#count}

Cuenta los elementos de la lista que no tienen en cuenta los valores nulos.

+++Sintaxis

`count(<listAny>)`

`count(<listObject>)`

+++

+++Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para procesar. Para listObject, debe ser una referencia de campo. Un listObject no puede contener un objeto nulo. |

+++

+++Firmas y tipo devuelto

`count(<listAny>)`

Devuelve un entero.

+++

+++Ejemplos

`count([10,2,10,null])`

Devuelve 3.

`count(@event{my_event.productListItems})`

Devuelve el número de objetos de una matriz determinada de objetos (tipo listObject). Nota: un listObject no puede contener un objeto nulo

+++

## countOnlyNull {#countOnlyNull}

Cuenta el número de valores nulos de la lista.

+++Sintaxis

`countOnlyNull(<listAny>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Firmas y tipo devuelto

`countOnlyNull(<listAny>)`

Devuelve un entero.

+++

+++Ejemplos

`countOnlyNull([10,2,10,null])`

Devuelve 1.

+++

**Nota:** El parámetro `<listObject>` no se admite en esta función.

## countWithNull {#countWithNull}

Cuenta todos los elementos de la lista, incluidos los valores nulos.

+++Sintaxis

`countWithNull(<listAny>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Firmas y tipo devuelto

`countWithNull(<listAny>)`

Devuelve un entero.

+++

+++Ejemplos

`countWithNull([10,2,10,null])`

Devuelve 4.

+++

**Nota:** El parámetro `<listObject>` no se admite en esta función.

## distinctCount {#distinctCount}

Cuenta el número de valores diferentes e ignora los valores nulos.

+++Sintaxis

`distinctCount(<listAny>)`

+++

+++Parámetros

| Parámetro | Tipo | Descripción |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly o listObject | Lista para procesar. Para listObject, debe ser una referencia de campo. |
| keyAttributeName | cadena | Este parámetro es opcional y solo para listObject. Si no se proporciona el parámetro, un objeto se considera duplicado si todos los atributos tienen los mismos valores. De lo contrario, un objeto se considera duplicado si el atributo dado tiene el mismo valor. |

+++

+++Firmas y tipo devuelto

`distinctCount(<listAny>)`

Devuelve un entero.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Devuelve una lista de objetos.

+++

+++Ejemplos

`distinctCount([10,2,10,null])`

Devuelve 2.

`distinctCount(@event{my_event.productListItems})`

Devuelve el número de objetos estrictamente distintos en la matriz de objetos determinada (tipo listObject).

`distinctCount(@event{my_event.productListItems}, "SKU")`

Devuelve el número de objetos que tienen un valor de atributo &quot;SKU&quot; distinto {}.

+++

## distinctCountWithNull {#distinctCountWithNull}

Cuenta el número de valores diferentes, incluidos los valores nulos.

+++Sintaxis

`distinctCountWithNull(<listAny>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

+++

+++Firmas y tipo devuelto

`distinctCountWithNull(<listAny>)`

Devuelve un entero.

+++

+++Ejemplos

`distinctCountWithNull([10,2,10,null])`

Devuelve 3.

+++

**Nota:** El parámetro `<listObject>` no se admite en esta función.

## max {#max}

Devuelve el valor máximo entre un conjunto de expresiones, dado como una lista o dos expresiones. Los valores nulos se omiten.

+++Sintaxis

`max(<parameter>)`

+++

+++Parámetros

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duration
* entero
* decimal
* dateTime
* dateTimeOnly

+++

+++Firmas y tipos devueltos

`max(<listDuration>)`

Devuelve una duración.

`max(<listInteger>)`

Devuelve una duración.

`max(<listDateTimeOnly>)`

Devuelve una fecha y hora sin considerar la zona horaria.

`max(<listDateTime>)`

Devuelve una fecha y hora.

`max(<listDateOnly>)`

Devuelve una fecha.

`max(<listDecimal>)`

Devuelve un valor decimal.

`max(<decimal>,<decimal>)`

Devuelve un valor decimal.

`max(<duration>,<duration>)`

Devuelve una duración.

`max(<dateTime>,<dateTime>)`

Devuelve una fecha y hora.

`max(<dateTimeOnly>,<dateTimeOnly>)`

Devuelve una fecha y hora sin considerar la zona horaria.

`max(<integer>,<integer>)`

Devuelve un entero.

+++

+++Ejemplos

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

Devuelve 10.

`max([10,null,8])`

Devuelve 10.

+++

## min {#min}

Devuelve el valor mínimo entre un conjunto de expresiones, dado como una lista o dos expresiones. Los valores nulos se omiten.

+++Sintaxis

`min(<parameters>)`

+++

+++Parámetros

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* duration
* entero
* decimal
* dateTime
* dateTimeOnly

+++

+++Firmas y tipos devueltos

`min(<listDuration>)`

Devuelve una duración.

`min(<listInteger>)`

Devuelve una duración.

`min(<listDateTimeOnly>)`

Devuelve una fecha y hora sin considerar la zona horaria.

`min(<listDateTime>)`

Devuelve una fecha y hora.

`min(<listDateOnly>)`

Devuelve una fecha.

`min(<listDecimal>)`

Devuelve un valor decimal.

`min(<decimal>,<decimal>)`

Devuelve un valor decimal.

`min(<duration>,<duration>)`

Devuelve una duración.

`min(<dateTime>,<dateTime>)`

Devuelve una fecha y hora.

`min(<dateTimeOnly>,<dateTimeOnly>)`

Devuelve una fecha y hora sin considerar la zona horaria.

`min(<integer>,<integer>)`

Devuelve un entero.

+++

+++Ejemplos

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

Devuelve 3.

`min([10,null,8])`

Devuelve 8.

+++

## sum {#sum}

Devuelve la suma de los valores de un conjunto de expresiones. Los valores nulos se omiten.

+++Sintaxis

`sum(<parameters>)`

+++

+++Parámetros

* listInteger
* listDecimal
* duration
* entero
* decimal

+++

+++Firmas y tipos devueltos

`sum(<listDecimal>)`

Devuelve un valor decimal.

`sum(<listInteger>)`

Devuelve un entero.

`sum(<integer>,<integer>)`

Devuelve un entero.

`sum(<decimal>,<decimal>)`

Devuelve un valor decimal.

+++

+++Ejemplos

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

Devuelve 21.

`sum([10.5,null,8.1])`

Devuelve 18.6.

+++

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página documenta todas las funciones de agregación disponibles en expresiones de recorrido de AJO, y cubre cómo calcular promedios, sumas, valores mínimo/máximo, recuentos y recuentos distintos en listas y matrices.

**Intenciones:**
* Calcular el promedio de una lista de valores numéricos mediante `avg`
* Suma de valores numéricos en una lista o de campos de eventos usando `sum`
* Buscar el valor mínimo o máximo en una lista usando `min` o `max`
* Contar elementos no nulos, nulos o todos los elementos de una lista usando `count`, `countOnlyNull` o `countWithNull`
* Contar valores distintos en una lista, con o sin valores nulos, utilizando `distinctCount` o `distinctCountWithNull`
* Filtrar objetos únicos en un listObject por un atributo clave específico utilizando `distinctCount` con un parámetro clave

**Glosario:**
* **listObject**: una lista de objetos complejos (referencias de campo); no puede contener objetos nulos *(específicos de producto)*
* **listAny**: Una lista de cualquier tipo escalar admitido (cadena, booleano, entero, decimal, duración, dateTime, dateTimeOnly, dateOnly) *(específico del producto)*
* **Valor nulo**: Un elemento ausente o indefinido en una lista; la mayoría de las funciones de agregación omiten los valores nulos a menos que la función los controle explícitamente (por ejemplo, `countOnlyNull`, `countWithNull`, `distinctCountWithNull`)

**Protecciones:**
* `countOnlyNull`, `countWithNull` y `distinctCountWithNull` no admiten el tipo de parámetro `<listObject>`
* `distinctCount` en `listObject` requiere que la lista sea una referencia de campo, no un literal en línea
* `count` en `listObject` requiere que la lista sea una referencia de campo; un listObject no puede contener objetos nulos

**Terminología:**
* Nombre canónico: Aggregation functions — Acrónimo: none — variants: aggregate functions, collection functions
* Sinónimos: &quot;count&quot; = &quot;count non-null elements&quot;; &quot;countWithNull&quot; = &quot;count all elements included nulls&quot;
* No confunda: &quot;distinctCount&quot; (ignora los valores nulos) ≠ &quot;distinctCountWithNull&quot; (incluye los valores nulos como un valor distinto)

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿`avg` incluye valores nulos en su cálculo?** — No, `avg` omite automáticamente los valores nulos.
* **Q: ¿Cuál es la diferencia entre `count` y `countWithNull`?** — `count` excluye del total los valores nulos, mientras que `countWithNull` cuenta todos los elementos, incluidos los valores nulos.
* **Q: ¿Puedo usar `countOnlyNull` en un listObject?** — No, `<listObject>` no es compatible con `countOnlyNull`, `countWithNull` o `distinctCountWithNull`.
* **Q: ¿Cómo se cuentan los objetos distintos de una matriz en función de un atributo específico?** — Use `distinctCount(@event{...}, "attributeName")` proporcionando el nombre de atributo clave como segundo parámetro.
* **Q: ¿Qué devuelve `max` cuando la lista contiene valores nulos?** — `max` ignora los valores nulos y devuelve el máximo entre los elementos no nulos.

+++
