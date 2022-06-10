---
title: Introducción a las funciones de ayuda
description: Biblioteca de funciones de Journey Optimizer Helper
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '1738'
ht-degree: 3%

---

# Introducción a las funciones de ayuda{#functions}

Uso [!DNL Journey Optimizer] crear plantillas de idioma para realizar operaciones con datos, como cálculos, formato de datos o conversiones, condiciones y manipularlas en el contexto de la personalización. Conozca las directrices de sintaxis de personalización en [esta página](../personalization-syntax.md).

➡️ [Aprenda a utilizar las funciones de ayuda en este vídeo](#video)

El lenguaje de plantilla se aprovecha en las funciones de ayuda disponibles en la lista desplegable de personalización del Editor de expresiones, como se muestra a continuación:

![](../assets/access-helper-functions.png)

En el [!DNL Journey Optimizer] El Editor de expresiones, las funciones de ayuda se agrupan en tres categorías: [Funciones](#functions-helper), [Ayudantes](#helper-helper) y [Operadores](#operators-helper).

Seleccione una categoría para acceder a las subcategorías y funciones.

Para acceder a las subcategorías, haga clic en el botón `>` icono. Para seleccionar una función, haga clic en el botón `+` icono: la función se añade automáticamente a la pantalla de personalización.

Haga clic en el `...` para ver la descripción de la función y agregarla a sus favoritos. [Más información](../personalize.md#fav)

## Funciones{#functions-helper}

### Funciones de agregación y matriz

<table>
    <tr>
        <td><a href="aggregation.md#average">Promedio</a></td><td>Esta función devuelve la media aritmética de todos los valores seleccionados dentro de la matriz</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Recuento</a></td><td>Esta función devuelve el número de elementos dentro de la matriz dada</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">Recuento solo nulo</a></td><td>Esta función cuenta el número de valores nulos en la lista.</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">Recuento con nulo</a></td><td>Esta función cuenta todos los elementos de la lista, incluidos los valores nulos</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a></td><td>Esta función obtiene valores de una matriz o una lista con valores duplicados eliminados</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">Recuento Distinto Con Nulo</a></td><td>Esta función cuenta el número de valores diferentes, incluidos los valores nulos</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">Primer elemento</a></td><td>Esta función devuelve el primer elemento de una matriz o una lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">Primeros n en la matriz</a></td><td>Esta función devuelve los primeros elementos "N" de una matriz, cuando se ordenan en orden ascendente según la expresión numérica dada</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">En</a></td><td>Esta función se utiliza para determinar si un elemento es miembro de una matriz o lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Incluye</a></td><td>Esta función determina si una matriz o lista contiene un elemento determinado</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersecciones</a></td><td>Esta función determina si dos matrices o listas tienen al menos un miembro común</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Última n en matriz</a></td><td>Esta función devuelve los últimos elementos "N" de una matriz, cuando se ordenan en orden ascendente según la expresión numérica dada</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Máximo</a></td><td>Esta función devuelve el mayor de todos los valores seleccionados dentro de una matriz</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Mínimo</a></td><td>Esta función devuelve el menor de todos los valores seleccionados dentro de la matriz</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Not in</a></td><td>Esta función determina si un elemento no es miembro de una matriz o lista</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subconjunto de</a></td><td>Esta función determina si una matriz específica (matriz A) es un subconjunto de otra matriz (matriz B), es decir, si todos los elementos de la matriz A son elementos de la matriz B</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">Sum</a></td><td>Esta función devuelve la suma de todos los valores seleccionados dentro de la matriz</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superconjunto de</a></td><td>Esta función determina si una matriz específica (matriz A) es un superconjunto de otra matriz (matriz B), es decir, si la matriz A contiene todos los elementos de la matriz B</td>
    </tr>
</table>

### Funciones de fecha y hora{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#age">Edad</a></td><td>Esta función recupera la edad de una fecha determinada</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">Tiempo actual en milisegundos</a></td><td>Esta función recupera la hora actual en milisegundos de epoch</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">Diferencia de fechas</a></td><td>Esta función recupera la diferencia entre dos fechas en número de días</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">Día de la semana</a></td><td>Esta función recupera el día de la semana</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">Día del año</a></td><td>Esta función recupera el día del año</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">Formato de fecha</a></td><td>Esta función da formato a un valor de fecha y hora</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">Definir días</a></td><td>Esta función establece el día del mes para la fecha y hora dadas</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">Establecer horas</a></td><td>Esta función establece la hora de la fecha y la hora</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">A UTC</a></td><td>Esta función convierte una fecha y hora a UTC</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">Semana del año</a></td><td>Esta función devuelve la semana del año</td>
    </tr>
</table>
</table>

### Funciones de mapa {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">Obtenga</a></td><td>Esta función se utiliza para recuperar el valor de un mapa para una clave determinada</td>
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
        <td><a href="objects.md#absolute">Absoluta  </a></td><td>Esta función convierte un número en su valor absoluto</td>
    </tr>
    <tr>
        <td><a href="objects.md#random">Aleatorio</a></td><td>Esta función devuelve un valor aleatorio entre 0 y 1</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-down">Redondear hacia abajo</a></td><td>Esta función redondea un número</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-up">Redondear</a></td><td>Esta función redondea un número</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-percentage">Hasta porcentaje</a></td><td>Esta función convierte un número en porcentaje</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-precision">Para precisión</a></td><td>Esta función convierte un número en la precisión necesaria</td>
    </tr>
</table>

### Funciones de objeto {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">No es nulo</a></td><td>Esta función se utiliza para determinar si existe una referencia de objeto</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Is null</a></td><td>Esta función se utiliza para determinar si no existe una referencia de objeto</td>
    </tr>
</table>

### Funciones de cadena {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">Camello</a></td><td>Esta función se utiliza para poner en mayúsculas la primera letra de cada palabra de una cadena</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>Esta función se utiliza para combinar dos cadenas en una</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contains</a></td><td>Esta función se utiliza para determinar si una cadena contiene una subcadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">No contiene</a></td><td>Esta función se utiliza para determinar si una cadena no contiene una subcadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">No termina con</a></td><td>Esta función se utiliza para determinar si una cadena no termina con una subcadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Does not start with</a></td><td>Esta función se utiliza para determinar si una cadena no comienza con una subcadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Codificar 64</a></td><td>Esta función se utiliza para codificar o descodificar una cadena</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Finaliza con</a></td><td>Esta función se utiliza para determinar si una cadena termina con una subcadena especificada</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Es igual a</a></td><td>Esta función se utiliza para determinar si una cadena no comienza con una subcadena especificada, con distinción de mayúsculas y minúsculas</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Es igual a omitir mayúsculas y minúsculas</a></td><td>Esta función se utiliza para determinar si una cadena no comienza con una subcadena especificada, sin distinción de mayúsculas y minúsculas</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">Extraer dominio de correo electrónico</a></td><td>Esta función se utiliza para extraer el dominio de una dirección de correo electrónico</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">Obtener host de URL</a></td><td>Esta función se utiliza para obtener el host de url.</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">Obtener ruta de URL</a></td><td>Esta función se utiliza para obtener la ruta de URL</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">Obtener protocolo de url</a></td><td>Esta función se utiliza para obtener el protocolo url</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">Índice de</a></td><td>Esta función devuelve la posición (en el primer argumento) de la primera incidencia del segundo parámetro. Devuelve -1 si no hay coincidencia</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>Esta función se utiliza para comprobar si una cadena o expresión está vacía.</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">No está vacío</a></td><td>Esta función devuelve el valor "True" si la cadena del parámetro no está vacía.</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">Último índice de</a></td><td>Esta función devuelve la posición (en el primer argumento) de la última incidencia del segundo parámetro. Devuelve -1 si no hay coincidencia.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Guarnecido izquierdo</a></td><td>Esta función elimina los espacios en blanco del principio de una cadena</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Length</a></td><td>Esta función se utiliza para obtener el número de caracteres de una cadena o una expresión</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Like</a></td><td>Esta función se utiliza para determinar si una cadena coincide con un patrón especificado</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Lower Case</a></td><td>Esta función convierte una cadena en minúsculas</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">Máscara</a></td><td>Esta función se utiliza para reemplazar una parte de una cadena por caracteres "X".</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Coincide</a></td><td>Esta función se utiliza para determinar si una cadena coincide con una expresión regular específica</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>Esta función devuelve el hash md5 de la cadena de entrada.</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Not equal to</a></td><td>Esta función se utiliza para determinar si una cadena no es igual a la cadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">Distinto de mayúsculas y minúsculas ignoradas</a></td><td>Esta función compara dos cadenas ignorando mayúsculas y minúsculas.</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Grupo de expresiones regulares</a></td><td>Esta función se utiliza para extraer información específica, en función de la expresión regular proporcionada</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Reemplazar</a></td><td>Esta función sustituye una subcadena determinada de una cadena por otra subcadena</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Reemplazar todo</a></td><td>Esta función reemplaza todas las subcadenas de un texto que coincida con el "destino" por la cadena de sustitución del literal especificado</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Guarnecido derecho</a></td><td>Esta función elimina los espacios en blanco del final de una cadena </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Split</a></td><td>Esta función se utiliza para dividir una cadena por un carácter determinado</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Comienza con</a></td><td>Esta función se utiliza para determinar si una cadena comienza con una subcadena especificada</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">Cadena hasta la fecha</a></td><td>Esta función se utiliza para convertir cadenas a la fecha. Devuelve la fecha de epoch como salida para una entrada no válida.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">Cadena a entero</a></td><td>Esta función convierte un valor de cadena en un valor entero.</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">Cadena para número</a></td><td>Esta función se utiliza para convertir una cadena en número. Devuelve la misma cadena que el resultado de una entrada no válida.</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">Subcadena</a></td><td>Esta función devuelve la subcadena de la expresión de cadena entre el índice de inicio y el índice final.</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Caso de título</a></td><td>Esta función se utiliza para poner en mayúsculas las primeras letras de cada palabra de una cadena</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">A Bool</a></td><td>Esta función convierte un valor de argumento en un valor booleano, según su tipo.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">Hasta la fecha</a></td><td>Esta función se utiliza para convertir cadenas a la fecha. Devuelve la fecha de epoch como salida para una entrada no válida.</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">Hasta la fecha solo</a></td><td>Esta función convierte un valor de argumento en un valor de solo fecha y hora. Devuelve la fecha de epoch como salida para una entrada no válida.</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Recortar</a></td><td>Esta función elimina los espacios en blanco del principio y del final de una cadena</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Mayúsculas</a></td><td>Esta función convierte una cadena en mayúsculas</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">Descodificación de URL</a></td><td>Esta función se utiliza para decodificar una cadena con codificación url.</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Encore de URL</a></td><td>Esta función se utiliza para codificar una cadena mediante url.</td>
    </tr>
</table>


## Ayudantes{#helper-helper}

Los ayudantes se detallan en [esta página](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">Valor predeterminado de reserva</a></td><td>Esta función permite procesar una variable con el valor predeterminado</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">Cada</a></td><td>Esta función se utiliza para iterar en una matriz</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">Si</a></td><td>Esta función se utiliza para definir un bloque condicional: si la evaluación de la expresión devuelve true, el bloque se procesa</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">Let</a></td><td>Esta función permite almacenar una expresión como variable para usarla más adelante en una consulta</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">Except</a></td><td>Esta función se utiliza para definir un bloque condicional: si la evaluación de la expresión devuelve false, el bloque se procesa</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">con</a></td><td>Esta función se utiliza para cambiar el token de evaluación de la parte de plantilla</td>
    </tr>
</table>

## Operadores{#operators-helper}

### Funciones aritméticas {#arithmetic-helper}

Las funciones aritméticas se utilizan para realizar cálculos básicos de los valores.

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">Adición</a></td><td>Este operador se utiliza para encontrar la suma de dos expresiones de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">Dividir</a></td><td>Este operador se utiliza para encontrar el cociente de dos expresiones de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">Multiplicación</a></td><td>Este operador se utiliza para encontrar el producto de dos expresiones de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">Remainte</a> </td><td>Este operador se utiliza para encontrar el resto después de dividir las dos expresiones de argumento</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">Sustracción</a> </td><td>Este operador encuentra la diferencia entre dos expresiones</td>
    </tr>
</table>


### Funciones booleanas {#boolean-functions}

Las funciones booleanas se utilizan para realizar lógicas booleanas en distintos elementos.

<table>
    <tr>
        <td><a href="operators.md#and">Y</a></td><td>Este operador crea una conjunción lógica</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">O</a></td><td>Este operador crea una disyunción lógica</td>
    </tr>
</table>


### Funciones de comparación {#comparison-functions}

Las funciones de comparación se utilizan para comparar diferentes expresiones y valores, devolviendo true o false en consecuencia.

<table>
    <tr>
        <td><a href="operators.md#equals">Es igual a</a></td><td>Esta operación comprueba si los valores son iguales</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Greater than</a></td><td>Este operador comprueba si el primer valor es bueno que el segundo valor</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Bueno o igual a</a></td><td>Este operador comprueba si el primer valor es bueno o igual al segundo valor</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">Less than or equals to</a> </td><td>Este operador comprueba si el primer valor es menor o igual que el segundo valor</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">No es igual a</a></td><td>Este operador comprueba si la expresión dada no es igual a dar valor</td>
    </tr>
</table>

## Vídeo explicativo{#video}

Aprenda a transformar los valores de personalización mediante las funciones de ayuda de personalización y comprenda diferentes casos de uso de las funciones de ayuda.

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
