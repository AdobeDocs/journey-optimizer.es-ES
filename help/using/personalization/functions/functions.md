---
title: Introducción a las funciones de ayuda
description: Biblioteca de funciones de Journey Optimizer Helper
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: e255751e411d8b623a12780a52a54551b5d65182
workflow-type: tm+mt
source-wordcount: '2399'
ht-degree: 27%

---

# Introducción a las funciones de ayuda{#functions}

Utilice el lenguaje de plantilla [!DNL Journey Optimizer] para realizar operaciones con los datos, como cálculos, conversiones o formato de datos, condiciones y manipularlos en el contexto de la personalización. Conozca las directrices de sintaxis de personalización en [esta página](../personalization-syntax.md).

➡️ [Aprenda a utilizar las funciones de ayuda en este vídeo](#video)

El lenguaje de plantilla se aprovecha de las funciones de ayuda disponibles en la lista desplegable de personalización del editor de personalización, como se muestra a continuación:

![](../assets/access-helper-functions.png)

>[!NOTE]
>
>Las funciones y capacidades disponibles en el editor de personalización difieren de las disponibles en el [editor de expresiones avanzadas de Recorrido](../../building-journeys/expression/expressionadvanced.md).

En el editor de personalización [!DNL Journey Optimizer], las funciones de ayuda se agrupan en tres categorías: [Funciones](#functions-helper), [Ayudantes](#helper-helper) y [Operadores](#operators-helper).

Seleccione una categoría para acceder a subcategorías y funciones.

Acceda a subcategorías haciendo clic en el icono `>`. Seleccione una función haciendo clic en el icono `+`: la función se agrega automáticamente a la pantalla de personalización.

Haga clic en el icono `...` para ver la descripción de la función y agregarla a sus favoritos. [Más información](../personalize.md#fav)

## Funciones{#functions-helper}

### Funciones de agregación y matriz

<table>
    <tr>
        <td><a href="aggregation.md#average">Promedio</a></td><td>Esta función devuelve la media aritmética de todos los valores seleccionados dentro de la matriz</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Recuento</a></td><td>Esta función devuelve el número de elementos dentro de la matriz determinada</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Contar Solo Nulo</a></td><td>Esta función cuenta el número de valores nulos de la lista.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Contar Con Nulo</a></td><td>Esta función cuenta todos los elementos de la lista, incluidos los valores nulos</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinto</a></td><td>Esta función obtiene valores de una matriz o una lista con valores duplicados eliminados</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Contar Distinto Con Nulo</a></td><td>Esta función cuenta el número de valores diferentes, incluidos los valores nulos</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Primer elemento</a></td><td>Esta función devuelve el primer elemento de una matriz o lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Primer n en matriz</a></td><td>Esta función devuelve los primeros elementos "N" de una matriz, cuando se ordenan en orden ascendente en función de la expresión numérica dada</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">En</a></td><td>Esta función se utiliza para determinar si un elemento es miembro de una matriz o lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Incluye</a></td><td>Esta función determina si una matriz o lista contiene un elemento determinado</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Interseca</a></td><td>Esta función determina si dos matrices o listas tienen al menos un miembro común</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Último n en matriz</a></td><td>Esta función devuelve los últimos elementos "N" de una matriz, cuando se ordenan en orden ascendente en función de la expresión numérica dada</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Máximo</a></td><td>Esta función devuelve el mayor de todos los valores seleccionados dentro de una matriz</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Mínimo</a></td><td>Esta función devuelve el menor de todos los valores seleccionados dentro de la matriz</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">No en</a></td><td>Esta función determina si un elemento no es miembro de una matriz o lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subconjunto de</a></td><td>Esta función determina si una matriz específica (matriz A) es un subconjunto de otra matriz (matriz B), es decir, si todos los elementos de la matriz A son elementos de la matriz B</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Sum</a></td><td>Esta función devuelve la suma de todos los valores seleccionados dentro de la matriz</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superconjunto de</a></td><td>Esta función determina si una matriz específica (matriz A) es un superconjunto de otra matriz (matriz B), es decir, si esa matriz A contiene todos los elementos de la matriz B</td>
    </tr>
</table>

### Funciones de fecha y hora{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#add-days">Añadir días</a></td><td>Esta función ajusta una fecha determinada en un número determinado de días, utilizando valores positivos para aumentar y valores negativos para disminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-hours">Añadir horas</a></td><td>Esta función ajusta una fecha determinada en un número determinado de horas, utilizando valores positivos para aumentar y valores negativos para disminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-minutes">Añadir minutos</a></td><td>Esta función ajusta una fecha determinada en un número determinado de minutos, utilizando valores positivos para aumentar y valores negativos para disminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-months">Añadir meses</a></td><td>Esta función ajusta una fecha determinada en un número determinado de meses, utilizando valores positivos para aumentar y valores negativos para disminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-seconds">Añadir segundos</a></td><td>Esta función ajusta una fecha determinada en un número determinado de segundos, utilizando valores positivos para aumentar y negativos para disminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#add-years">Añadir años</a></td><td>Esta función ajusta una fecha determinada en un número determinado de años, utilizando valores positivos para aumentar y valores negativos para disminuir.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age">Edad</a></td><td>Esta función recupera la edad de una fecha determinada.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-days">Antigüedad en días</a></td><td>Esta función calcula la antigüedad de una fecha determinada en días, es decir, el número de días transcurridos entre la fecha determinada y la fecha actual, negativos para fechas futuras y positivos para fechas pasadas.</td>
    </tr>
    <tr>
        <td><a href="dates.md#age-months">Antigüedad en meses</a></td><td>Esta función calcula la edad de una fecha determinada en meses, es decir, el número de meses transcurridos entre la fecha determinada y la fecha actual, negativos para fechas futuras y positivos para fechas pasadas.</td>
    </tr>
    <tr>
        <td><a href="dates.md#compare-dates">Comparar fechas</a></td><td>Esta función compara la primera fecha de entrada con la otra. Devuelve 0 si fecha1 es igual a fecha2, -1 si fecha1 es anterior a fecha2, y 1 si fecha1 es posterior a fecha2.</td>
    </tr>
    <tr>
        <td><a href="dates.md#convert-zoned-date-time">Convertir ZonedDateTime</a></td><td>Esta función convierte una fecha y hora en una zona horaria determinada.</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Hora actual en milisegundos</a></td><td>Esta función recupera el tiempo actual en milisegundos epoch.</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Diferencia de fechas</a></td><td>Esta función recupera la diferencia entre dos fechas en número de días.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-month">Día del mes</a></td><td>Esta función devuelve el número que representa el día del mes.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Día de la semana</a></td><td>Esta función recupera el día de la semana.</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Día del año</a></td><td>Esta función recupera el día del año.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-seconds">Diferencia en segundos</a></td><td>Esta función devuelve la diferencia entre dos fechas en valor de segundos.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-hours">Extraer horas</a></td><td>Esta función extrae el componente de hora de una marca de tiempo determinada.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-minutes">Extraer minutos</a></td><td>Esta función extrae el componente de minutos de una marca de tiempo determinada.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-months">Extraer meses</a></td><td>Esta función extrae el componente de meses de una marca de tiempo determinada.</td>
    </tr>
    <tr>
        <td><a href="dates.md#extract-seconds">Extraer segundos</a></td><td>Esta función extrae el componente de segundos de una marca de tiempo determinada.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Dar formato a fecha</a></td><td>Esta función da formato a un valor de fecha y hora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date-locale">Formato de fecha con compatibilidad con configuración regional</a></td><td>Esta función da formato a un valor de fecha y hora en su representación sensible al idioma correspondiente, es decir, en una configuración regional deseada.</td>
    </tr>
    <tr>
        <td><a href="dates.md#get-current-zoned-date-time">Obtener CurrentZonedDateTime</a></td><td>Esta función devuelve la fecha y la hora actuales con información de zona horaria.</td>
    </tr>
    <tr>
        <td><a href="dates.md#hours-difference">Diferencia de horas</a></td><td>Esta función devuelve la diferencia entre dos fechas en términos de horas.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-minutes">Diferencia de minutos</a></td><td>Esta función devuelve la diferencia entre dos fechas en términos de minutos.</td>
    </tr>
    <tr>
        <td><a href="dates.md#months-difference">Diferencia de meses</a></td><td>Esta función devuelve la diferencia entre dos fechas en términos de meses.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Configurar Días</a></td><td>Esta función establece el día del mes para la fecha y hora determinadas.</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Establecer Horas</a></td><td>Esta función establece la hora de la fecha y hora.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-date-time">A Fecha Hora</a></td><td>Esta función convierte la cadena en fecha. Devuelve la fecha epoch como salida para una entrada no válida.</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">A UTC</a></td><td>Esta función convierte una fecha y hora en UTC.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-day">Truncar al inicio del día</a></td><td>Esta función modifica una fecha y hora determinadas configurándolas en el inicio del día con la hora establecida en 00:00.</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-quarter">truncateToStartOfQuarter</a></td><td>Esta función trunca una fecha y hora al primer día de su trimestre (por ejemplo, 1 de enero, 1 de abril, 1 de julio, 1 de octubre) a las 00:00.
</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-week">truncateToStartOfWeek</a></td><td>Esta función modifica una fecha y hora determinadas configurándolas en el inicio de la semana (lunes a las 00:00).</td>
    </tr>
    <tr>
        <td><a href="dates.md#truncate-year">truncateToStartOfYear</a></td><td>Esta función modifica una fecha y hora determinadas truncándolas al primer día del año (1 de enero) a las 00:00.</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Semana del año</a></td><td>Esta función devuelve la semana del año.</td>
    </tr>
    <tr>
        <td><a href="dates.md#diff-years">Diferencia de años</a></td><td>Esta función devuelve la diferencia entre dos fechas en términos de años.</td>
    </tr>
</table>
</table>

### Funciones de mapa {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Obtener</a></td><td>Esta función se utiliza para recuperar el valor de un mapa para una clave determinada</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Claves</a></td><td>Esta función se utiliza para recuperar todas las claves de un mapa determinado</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Valores</a></td><td>Esta función recupera todos los valores de un mapa determinado</td>
    </tr>
</table>

### Funciones matemáticas {#math-functions}

<table>
    <tr>
        <td><a href="math.md#absolute">Absoluto</a></td><td>Esta función da formato a cualquier número en su representación sensible al idioma.</td>
    </tr>
    <tr>
        <td><a href="math.md#format-number">Número de formato</a></td><td>Esta función da formato a cualquier número en su representación sensible al idioma.</td>
    </tr>
    <tr>
        <td><a href="math.md#random">Aleatorio</a></td><td>Esta función devuelve un valor aleatorio entre 0 y 1.</td>
    </tr>
    <tr>
        <td><a href="math.md#round-down">Redondear a la baja</a></td><td>Esta función redondea un número.</td>
    </tr>
    <tr>
        <td><a href="math.md#round-up">Redondear al alza</a></td><td>Esta función redondea un número al alza</td>
    </tr>
    <tr>
    <td><a href="math.md#to-hex-string">A la cadena hexadecimal</a></td><td>convierte cualquier número en su cadena hexadecimal.</td>
    </tr>
    <tr>
    <td><a href="math.md#to-int">ToInt</a></td><td>Convierte cualquiera de estos tipos (número, doble, entero, largo, flotante, corto, byte, booleano, cadena) en un entero.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-percentage">A porcentaje</a></td><td>Esta función convierte un número en porcentaje.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-precision">A precisión</a></td><td>Esta función convierte un número en una precisión requerida.</td>
    </tr>
    <tr>
        <td><a href="math.md#to-string">Para crear una cadena</a></td><td>Esta función convierte cualquier número en su representación de cadena. </td>
    </tr>
</table>

### Funciones de objeto {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">No es nulo</a></td><td>Esta función se utiliza para determinar si existe una referencia de objeto</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Es nulo</a></td><td>Esta función se utiliza para determinar si no existe una referencia de objeto</td>
    </tr>
</table>

### Funciones de cadena {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a></td><td>Esta función se utiliza para poner en mayúscula la primera letra de cada palabra de una cadena</td>
    </tr>
    <tr>
        <td><a href="string.md#char-code-at">Código Char en</a></td><td>Esta función devuelve el valor ASCII de un carácter, como la función charCodeAt de JavaScript</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>Esta función se utiliza para combinar dos cadenas en una</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contiene</a></td><td>Esta función se utiliza para determinar si una cadena contiene una subcadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">No contiene</a></td><td>Esta función se utiliza para determinar si una cadena no contiene una subcadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">No termina por</a></td><td>Esta función se utiliza para determinar si una cadena no termina con una subcadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">No empieza por</a></td><td>Esta función se utiliza para determinar si una cadena no comienza con una subcadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Codificar 64</a></td><td>Esta función se utiliza para codificar una cadena.</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Termina por</a></td><td>Esta función se utiliza para determinar si una cadena termina con una subcadena especificada</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Es igual a</a></td><td>Esta función se utiliza para determinar si una cadena no comienza con una subcadena especificada, con distinción de mayúsculas y minúsculas</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Igual a Ignorar Mayúsculas y Minúsculas</a></td><td>Esta función se utiliza para determinar si una cadena no comienza con una subcadena especificada, sin distinción de mayúsculas y minúsculas</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">Extraer dominio de correo electrónico</a></td><td>Esta función se utiliza para extraer el dominio de una dirección de correo electrónico</td>
    </tr>
    <tr>
        <td><a href="string.md#format-currency">Formato de moneda</a></td><td>Esta función convierte cualquier número en su correspondiente representación de moneda sensible al idioma según la configuración regional pasada como cadena en el segundo argumento</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">Obtener host de URL</a></td><td>Esta función se utiliza para obtener el host de URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">Obtener ruta de URL</a></td><td>Esta función se utiliza para obtener la ruta de la URL</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">Obtener protocolo de URL</a></td><td>Esta función se utiliza para obtener el protocolo de la URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">Índice De</a></td><td>Esta función devuelve la posición (en el primer argumento) de la primera aparición del segundo parámetro. Devuelve -1 si no hay ninguna coincidencia</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Esta función se utiliza para comprobar si una cadena o expresión está vacía.</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">No está vacío</a></td><td>Esta función devuelve true si la cadena del parámetro no está vacía.</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">Último Índice De</a></td><td>Esta función devuelve la posición (en el primer argumento) de la última aparición del segundo parámetro. Devuelve -1 si no hay ninguna coincidencia.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Guarnecido izquierdo</a></td><td>Esta función elimina los espacios en blanco del principio de una cadena.</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Longitud</a></td><td>Esta función se utiliza para obtener el número de caracteres de una cadena o expresión</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Como</a></td><td>Esta función se utiliza para determinar si una cadena coincide con un patrón especificado</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Minúsculas</a></td><td>Esta función convierte una cadena en letras minúsculas.</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">Máscara</a></td><td>Esta función se utiliza para reemplazar una parte de una cadena con caracteres "X".</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Iguala</a></td><td>Esta función se utiliza para determinar si una cadena coincide con una expresión regular específica.</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>Esta función devuelve el hash md5 de la cadena de entrada.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">No igual a</a></td><td>Esta función se utiliza para determinar si una cadena no es igual a la cadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">No Igual Con Ignorar Mayúsculas y Minúsculas</a></td><td>Esta función compara dos cadenas ignorando mayúsculas y minúsculas.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Grupo de expresiones regulares</a></td><td>Esta función se utiliza para extraer información específica, basada en la expresión regular proporcionada</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Reemplazar</a></td><td>Esta función reemplaza una subcadena determinada de una cadena con otra subcadena</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Reemplazar todo</a></td><td>Esta función reemplaza todas las subcadenas de un texto que coincide con el "destino" por la cadena literal de "reemplazo" especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Guarnecido derecho</a></td><td>Esta función elimina los espacios en blanco del final de una cadena. </td>
    </tr>
    <tr>
        <td><a href="string.md#sha256">SHA256</a></td><td>Esta función calcula y devuelve el hash sha256 de una cadena.</td>
    </tr>
    <tr>
        <td><a href="string.md#split">División</a></td><td>Esta función se utiliza para dividir una cadena por un carácter determinado</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Comienza por</a></td><td>Esta función se utiliza para determinar si una cadena empieza con una subcadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">Cadena a fecha</a></td><td>Esta función convierte un valor de cadena en un valor de fecha y hora.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">Cadena a entero</a></td><td>Esta función convierte un valor de cadena en un valor entero.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">Cadena a número</a></td><td>Esta función se utiliza para convertir una cadena en número. Devuelve la misma cadena como salida para la entrada no válida.</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">Subcadena</a></td><td>Esta función devuelve la subcadena de la expresión de cadena entre el índice inicial y el índice final.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Caso de título</a></td><td>Esta función se utiliza para poner en mayúsculas las primeras letras de cada palabra de una cadena</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">A Bool</a></td><td>Esta función convierte un valor de argumento en un valor booleano, según su tipo.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">A Fecha Hora</a></td><td>Esta función se utiliza para convertir la cadena a fecha. Devuelve la fecha epoch como salida para una entrada no válida.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">A Fecha Hora solamente</a></td><td>Esta función convierte un valor de argumento en un valor de solo fecha y hora. Devuelve la fecha epoch como salida para una entrada no válida.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Recortar</a></td><td>Esta función elimina los espacios en blanco del principio y del final de una cadena.</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Mayúsculas</a></td><td>Esta función convierte una cadena en letras mayúsculas.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">Descifrar URL</a></td><td>Esta función se utiliza para descodificar una cadena con codificación URL.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Cifrar URL</a></td><td>Esta función se utiliza para codificar una cadena mediante URL.</td>
    </tr>
</table>


## Ayudantes{#helper-helper}

Los ayudantes se encuentran detallados en [esta página](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">Valor de reserva predeterminado</a></td><td>Esta función se utiliza para procesar una variable de forma predeterminada</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Each</a></td><td>Esta función se utiliza para repetir una matriz</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">Si</a></td><td>Esta función se utiliza para definir un bloque condicional: si la evaluación de la expresión devuelve true, se procesa el bloque</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>Esta función permite almacenar una expresión como variable para utilizarla posteriormente en una consulta</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Unless</a></td><td>Esta función se utiliza para definir un bloque condicional: si la evaluación de la expresión devuelve false, se procesa el bloque</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">With</a></td><td>Esta función se utiliza para cambiar el token de evaluación de la plantilla-parte</td>
    </tr>
</table>

## Operadores{#operators-helper}

### Funciones aritméticas {#arithmetic-helper}

Las funciones aritméticas se utilizan para realizar cálculos básicos sobre los valores.

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Suma</a></td><td>Este operador se utiliza para encontrar la suma de dos expresiones de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Dividir</a></td><td>Este operador se utiliza para encontrar el cociente de dos expresiones de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Multiplicación</a></td><td>Este operador se utiliza para encontrar el producto de dos expresiones de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Restante</a> </td><td>Este operador se utiliza para encontrar el resto después de dividir las dos expresiones de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">Resta</a> </td><td>Este operador encuentra la diferencia entre dos expresiones</td>
    </tr>
</table>


### Funciones booleanas {#boolean-functions}

Las funciones booleanas se utilizan para realizar lógica booleana en diferentes elementos.

<table>
    <tr>
        <td><a href="operators.md#and">Y</a></td><td>Este operador crea una conjunción lógica</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">O</a></td><td>Este operador crea una disyunción lógica</td>
    </tr>
</table>


### Funciones de comparación {#comparison-functions}

Las funciones de comparación se utilizan para comparar entre diferentes expresiones y valores, lo que devuelve true o false en consecuencia.

<table>
    <tr>
        <td><a href="operators.md#equals">Es igual a</a></td><td>Esta operación comprueba si los valores son iguales</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Mayor que</a></td><td>Este operador comprueba si el primer valor es mayor que el segundo</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Mayor o igual que</a></td><td>Este operador comprueba si el primer valor es mayor o igual que el segundo</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Menor o igual que</a> </td><td>Este operador comprueba si el primer valor es menor o igual que el segundo valor</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">No es igual a</a></td><td>Este operador comprueba si una expresión dada no es igual a dar valor</td>
    </tr>
</table>

## Vídeo práctico{#video}

Aprenda a transformar los valores de personalización mediante las funciones de ayuda de personalización y comprenda diferentes casos de uso de las funciones de ayuda.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
