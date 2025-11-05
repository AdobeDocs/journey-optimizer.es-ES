---
solution: Journey Optimizer
product: journey optimizer
title: Funciones
description: Obtenga información sobre las funciones en expresiones de recorrido
feature: Journeys
role: Developer
level: Experienced
keywords: función, expresiones, editor, recorrido, datos, manipulación
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 99053c6c1327818645adc4ab9a5d3dd30eb96b87
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 9%

---

# Funciones {#functions}

Las funciones son los componentes básicos de las expresiones de recorrido dinámico en Adobe Journey Optimizer. Permiten transformar, calcular, validar y manipular datos en tiempo real para crear experiencias del cliente personalizadas. Con más de 60 funciones organizadas en categorías intuitivas, puede crear condiciones sofisticadas, realizar cálculos complejos y tomar decisiones basadas en datos en cada paso del recorrido del cliente.

## Explicación de las funciones

Las funciones de las expresiones de recorrido siguen un patrón de sintaxis coherente:

`<function name>`(`<expression as param 1>`, `<expression as param 2>`, ... ,`<expression as param N>`)

**Características clave:**

* **Varias firmas**: una función puede tener diferentes firmas (diferentes conjuntos de parámetros ordenados) para dar cabida a varios casos de uso
* **Devoluciones específicas del tipo**: Cada función tiene un tipo devuelto específico (cadena, entero, booleano, fecha, lista, etc.)
* **Parámetros cero a N**: las funciones pueden aceptar expresiones 0-N como parámetros ordenados, lo que proporciona flexibilidad en el uso

## ¿Por qué utilizar funciones?

Las funciones le permiten lo siguiente:

* **Crear condiciones dinámicas**: rutas de recorrido de ramas basadas en la evaluación de datos en tiempo real
* **Personalizar a escala**: adapte el contenido y las experiencias con datos de clientes y perspectivas de comportamiento
* **Automatizar decisiones**: cree una lógica inteligente sin intervención manual
* **Transformar datos**: convierta, aplique formato y manipule tipos de datos para garantizar la compatibilidad
* **Realizar cálculos**: ejecutar operaciones matemáticas y análisis estadístico
* **Validar entradas**: compruebe la calidad y la integridad de los datos antes de realizar acciones

## Funciones por categoría

Examine las funciones organizadas según su propósito principal para encontrar rápidamente la herramienta adecuada para sus necesidades.

### Adobe Experience Platform {#aep-functions}

**Segmentación y direccionamiento de audiencias**

Evalúe la pertenencia a audiencias para crear rutas de recorrido personalizadas basadas en segmentos de clientes definidos en Adobe Experience Platform.

| Función | Descripción |
|----------|-------------|
| [inAudience](../functions/functioninaudience.md) | Comprobar si un individuo pertenece a una audiencia específica |

[Ver → de detalles de función de Adobe Experience Platform](../functions/functioninaudience.md)

### Funciones de agregación {#aggregation-functions}

**Cálculos estadísticos y Resumen de Datos**

Realice cálculos en conjuntos de valores para obtener perspectivas como promedios, recuentos, sumas y valores mínimo/máximo. Esencial para la toma de decisiones basada en datos.

| Función | Descripción |
|----------|-------------|
| [avg](../functions/aggregation-functions.md#avg) | Calcular valor promedio |
| [count](../functions/aggregation-functions.md#count) | Recuento de elementos no nulos |
| [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) | Contar solo valores nulos |
| [countWithNull](../functions/aggregation-functions.md#countWithNull) | Contar todos los elementos, incluidos los valores nulos |
| [distinctCount](../functions/aggregation-functions.md#distinctCount) | Contar valores únicos no nulos |
| [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) | Contar valores únicos, incluidos valores nulos |
| [max](../functions/aggregation-functions.md#max) | Buscar valor máximo |
| [min](../functions/aggregation-functions.md#min) | Buscar valor mínimo |
| [sum](../functions/aggregation-functions.md#sum) | Calcular suma total |

[Ver todas las funciones de agregación →](../functions/aggregation-functions.md)

### Funciones de conversión {#conversion-functions}

**Transformación de tipo de datos**

Convierta datos entre diferentes tipos (cadena, entero, decimal, booleano, fecha, duración) para garantizar la compatibilidad entre operaciones y fuentes de datos.

| Función | Descripción |
|----------|-------------|
| [toBool](../functions/conversion-functions.md#toBool) | Convertir en booleano |
| [toDateOnly](../functions/conversion-functions.md#toDateOnly) | Convertir solo a fecha (sin hora) |
| [toDateTime](../functions/conversion-functions.md#toDateTime) | Convertir a fecha con hora |
| [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) | Convertir a fecha y hora sin zona horaria |
| [toDecimal](../functions/conversion-functions.md#toDecimal) | Convertir en número decimal |
| [toDuration](../functions/conversion-functions.md#toDuration) | Convertir a duración |
| [toInteger](../functions/conversion-functions.md#toInteger) | Convertir en entero |
| [toString](../functions/conversion-functions.md#toString) | Convertir en cadena |

[Ver todas las funciones de conversión →](../functions/conversion-functions.md)

### Funciones de fecha {#date-functions}

**Manipulación de fecha y hora**

Trabaje con fechas, horas y zonas horarias para crear condiciones basadas en el tiempo, programar acciones y realizar cálculos temporales.

| Función | Descripción |
|----------|-------------|
| [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) | Obtener el tiempo actual en milisegundos |
| [inLastDays](../functions/date-functions.md#inLastDays) | Comprobar si la fecha está dentro de los últimos N días |
| [inLastHours](../functions/date-functions.md#inLastHours) | Comprobar si la fecha está dentro de las últimas N horas |
| [inLastMonths](../functions/date-functions.md#inLastMonths) | Comprobar si la fecha está dentro de los últimos N meses |
| [inLastYears](../functions/date-functions.md#inLastYears) | Comprobar si la fecha está dentro de los últimos N años |
| [inNextDays](../functions/date-functions.md#inNextDays) | Comprobar si la fecha está dentro de los próximos N días |
| [inNextHours](../functions/date-functions.md#inNextHours) | Comprobar si la fecha está dentro de las próximas N horas |
| [inNextMonths](../functions/date-functions.md#inNextMonths) | Comprobar si la fecha está dentro de los próximos N meses |
| [inNextYears](../functions/date-functions.md#inNextYears) | Comprobar si la fecha está dentro de los próximos N años |
| [now](../functions/date-functions.md#now) | Obtener fecha y hora actuales |
| [nowWithDelta](../functions/date-functions.md#nowWithDelta) | Obtener la hora actual con desplazamiento |
| [setHours](../functions/date-functions.md#setHours) | Establecer horas específicas en fecha-hora |
| [setDays](../functions/date-functions.md#setDays) | Establecer días específicos en fecha-hora |
| [updateTimeZone](../functions/date-functions.md#updateTimeZone) | Actualizar zona horaria de fecha y hora |

[Ver todas las funciones de fecha →](../functions/date-functions.md)

### Funciones de lista {#list-functions}

**Manipulación y análisis de colecciones**

Filtre, ordene, transforme y analice matrices y listas para trabajar con estructuras de datos complejas y realizar operaciones de conjunto.

| Función | Descripción |
|----------|-------------|
| [distinct](../functions/list-functions.md#distinct) | Obtener valores únicos (excluye valores nulos) |
| [distinctWithNull](../functions/list-functions.md#distinctWithNull) | Obtener valores únicos (incluye valores nulos) |
| [filtro](../functions/list-functions.md#filter) | Filtrar lista según ciertos criterios |
| [getListItem](../functions/list-functions.md#getListItem) | Obtener elemento en un índice específico |
| [in](../functions/list-functions.md#in) | Comprobar si el valor existe en la lista |
| [intersección](../functions/list-functions.md#intersect) | Búsqueda de elementos comunes entre listas |
| [límite](../functions/list-functions.md#limit) | Limitar el número de elementos devueltos |
| [listSize](../functions/list-functions.md#listSize) | Obtener el tamaño de la lista |
| [serializeList](../functions/list-functions.md#serializeList) | Convertir lista en cadena |
| [sort](../functions/list-functions.md#sort) | Ordenar elementos de lista |

[Ver todas las funciones de la lista →](../functions/list-functions.md)

### Funciones matemáticas {#math-functions}

**Operaciones matemáticas**

Realizar cálculos numéricos y transformaciones para el procesamiento de datos y la lógica empresarial.

| Función | Descripción |
|----------|-------------|
| [random](../functions/math-functions.md#random) | Generar número aleatorio (0-1) |
| [round](../functions/math-functions.md#round) | Redondear al entero más cercano |

[Ver todas las funciones matemáticas →](../functions/math-functions.md)

### Funciones de cadena {#string-functions}

**Manipulación y validación de texto**

Procese, transforme, busque y valide datos de texto para la creación de contenido dinámico y la lógica condicional.

| Función | Descripción |
|----------|-------------|
| [concat](../functions/string-functions.md#concat) | Concatenar cadenas |
| [contain](../functions/string-functions.md#contain) | Comprobar si la cadena contiene una subcadena |
| [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) | La comprobación contiene (sin distinción de mayúsculas) |
| [endWith](../functions/string-functions.md#endWith) | Comprobar si la cadena termina con el sufijo |
| [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) | La comprobación termina por (sin distinción de mayúsculas y minúsculas) |
| [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) | Comparar cadenas (sin distinción de mayúsculas y minúsculas) |
| [indexOf](../functions/string-functions.md#indexOf) | Buscar la primera posición de ocurrencia |
| [isEmpty](../functions/string-functions.md#isEmpty) | Comprobar si la cadena está vacía |
| [isNotEmpty](../functions/string-functions.md#isNotEmpty) | Comprobar si la cadena no está vacía |
| [lastIndexOf](../functions/string-functions.md#lastIndexOf) | Buscar la última posición de ocurrencia |
| [length](../functions/string-functions.md#length) | Obtener longitud de cadena |
| [lower](../functions/string-functions.md#lower) | Convertir a minúsculas |
| [matchRegExp](../functions/string-functions.md#matchRegExp) | Coincidir expresión regular |
| [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) | Comprobación no igual a (sin distinción de mayúsculas y minúsculas) |
| [replace](../functions/string-functions.md#replace) | Reemplazar la primera ocurrencia |
| [replaceAll](../functions/string-functions.md#replaceAll) | Reemplazar todas las ocurrencias |
| [split](../functions/string-functions.md#split) | Dividir cadena en matriz |
| [startWith](../functions/string-functions.md#startWith) | Comprobar si la cadena comienza con un prefijo |
| [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) | La comprobación empieza por (sin distinción de mayúsculas y minúsculas) |
| [substr](../functions/string-functions.md#substr) | Extraer subcadena |
| [trim](../functions/string-functions.md#trim) | Eliminar espacios iniciales y finales |
| [upper](../functions/string-functions.md#upper) | Convertir a mayúsculas |
| [uuid](../functions/string-functions.md#uuid) | Generar UUID |

[Ver todas las funciones de cadena →](../functions/string-functions.md)

## Próximos pasos

Ahora que comprende las funciones disponibles, explore:

* **[Editor de expresiones avanzadas](expressionadvanced.md)**: aprenda a crear expresiones complejas con el editor avanzado
* **[Sintaxis de expresión](generalities.md)**: domine las reglas de sintaxis para escribir expresiones de recorrido
* **[Operadores](operators.md)**: descubra los operadores que puede usar con funciones para generar lógica
* **[Referencias de campos](field-references.md)**: obtenga información sobre cómo hacer referencia a campos de datos en sus expresiones
