---
product: journey optimizer
title: Funciones de agregación
description: Obtenga información sobre las funciones de agregación
feature: Journeys
role: Developer
level: Experienced
keywords: agregación, funciones, expresión, recorrido, promedio, recuento, máximo, mínimo, suma
version: Journey Orchestration
source-git-commit: af1babe501a5b2c6a67730396a8f5e2c5d85e60a
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 8%

---

# Funciones de agregación {#aggregation-functions}

Las funciones de agregación se utilizan para realizar cálculos en un conjunto de valores y devolver un solo valor. Estas funciones son especialmente útiles cuando se trabaja con listas y matrices en expresiones de recorrido.

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

**Nota:** El parámetro `<listObject>` no se admite en esta función.

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

## countWithNull {#countWithNull}

Cuenta todos los elementos de la lista, incluidos los valores nulos.

**Nota:** El parámetro `<listObject>` no se admite en esta función.

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

Devuelve el número de objetos que tienen un valor de atributo SKU distinto {}.

+++

## distinctCountWithNull {#distinctCountWithNull}

Cuenta el número de valores diferentes, incluidos los valores nulos.

**Nota:** El parámetro `<listObject>` no se admite en esta función.

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
