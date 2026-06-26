---
product: journey optimizer
title: Funciones de cadena
description: Obtenga información sobre las funciones de cadena
feature: Journeys
role: Developer
level: Experienced
keywords: cadena, funciones, expresión, recorrido, texto, manipulación
version: Journey Orchestration
exl-id: 8186c564-56fa-417a-afd3-8e479e5b23b9
TQID: https://experienceleague.adobe.com/wrP3c7l3uHzN6w3l-fXBQOSb5Tx2NuW-6iyogKpDPc8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1668
ht-degree: 10%

---

# Funciones de cadena {#string-functions}

Las funciones de cadena permiten manipular y trabajar con valores de texto dentro de las expresiones de recorrido. Estas funciones son esenciales para el procesamiento de texto, la validación, la transformación y el análisis en los recorridos del cliente.

Utilice funciones de cadena cuando necesite:

* Concatenar y combinar varios valores de texto ([concat](#concat))
* Busque patrones de texto o subcadenas específicos ([contain](#contain), [containIgnoreCase](#containIgnoreCase), [indexOf](#indexOf), [lastIndexOf](#lastIndexOf), [matchRegExp](#matchRegExp))
* Comparar cadenas con coincidencia que distingue entre mayúsculas y minúsculas ([equalIgnoreCase](#equalIgnoreCase), [notEqualIgnoreCase](#notEqualIgnoreCase))
* La cadena de comprobación comienza y finaliza ([startWith](#startWith), [startWithIgnoreCase](#startWithIgnoreCase), [endWith](#endWith), [endWithIgnoreCase](#endWithIgnoreCase))
* Extraer partes de texto mediante operaciones de subcadena ([substr](#substr))
* Transformar texto a mayúsculas o minúsculas ([mayúsculas](#upper), [minúsculas](#lower), [recortar](#trim))
* Compruebe si las cadenas están vacías o contienen valores específicos ([isEmpty](#isEmpty), [isNotEmpty](#isNotEmpty))
* Reemplazar patrones de texto con nuevos valores ([replace](#replace), [replaceAll](#replaceAll))
* Dividir cadenas en matrices para un procesamiento posterior ([split](#split))
* Obtener longitud de cadena ([length](#length)) o generar identificadores únicos ([uuid](#uuid))

Las funciones de cadena proporcionan funcionalidades completas de manipulación de texto, lo que permite un procesamiento de datos sofisticado y una lógica condicional basada en el contenido de texto de las expresiones de recorrido.

## concatena {#concat}

Concatena dos parámetros de cadena o una lista de cadenas.

+++Sintaxis

`concat(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| Lista | listString |
| cadena | cadena |

+++

+++Firma y tipo devuelto

`concat(<string>,<string>)`

`concat(<listString>)`

Devuelve una cadena.

+++

+++Ejemplos

`concat("Hello","World")`

Devuelve &quot;HelloWorld&quot;.

`concat(["Hello"," ","World"])`

Devuelve &quot;Hello World&quot;.

+++

## contain {#contain}

Comprueba si la cadena del segundo argumento está contenida en la primera.

+++Sintaxis

`contain(<parameters>)`

+++

+++Parámetros

* cadena

+++

+++Firma y tipo devuelto

`contain(<string>,<string>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`contain("rowing is great", "great")`

Devuelve verdadero.

+++

## containIgnoreCase {#containIgnoreCase}

Comprueba si la cadena del segundo argumento está contenida en la cadena del primer argumento, sin tener en cuenta el caso.

+++Sintaxis

`containIgnoreCase(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| cadena | cadena |
| cadena buscada | cadena |

+++

+++Firma y tipo devuelto

`containIgnoreCase(<string>,<string>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`containIgnoreCase("rowing is great", "GREAT")`

Devuelve verdadero.

+++

## endWith {#endWith}

Devuelve true si el segundo parámetro es un sufijo del primero.

+++Sintaxis

`endWith(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| cadena | cadena |
| sufijo | cadena |

+++

+++Firma y tipo devuelto

`endWith(<string>,<string>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`endWith("Hello World", "World")`

Devuelve verdadero.

`endWith("Hello World", "Hello")`

Devuelve falso.

+++

## endWithIgnoreCase {#endWithIgnoreCase}

Comprueba si la cadena del primer argumento termina con una cadena específica (cadena del segundo argumento), sin tener en cuenta el caso.

+++Sintaxis

`endWithIgnoreCase(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| cadena | cadena |
| sufijo | cadena |

+++

+++Firma y tipo devuelto

`endWithIgnoreCase(<string>,<string>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`endWithIgnoreCase("rowing is great", "AT")`

Devuelve verdadero.

+++

## equalIgnoreCase {#equalIgnoreCase}

Compara la cadena del primer argumento con la cadena del segundo, ignorando las consideraciones de mayúsculas y minúsculas.

+++Sintaxis

`equalIgnoreCase(<parameters>)`

+++

+++Parámetros

* cadena

+++

+++Firma y tipo devuelto

`equalIgnoreCase(<string>,<string>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`equalIgnoreCase("rowing is great", "rowing is GREAT")`

Devuelve verdadero.

+++

## indexOf {#indexOf}

Devuelve la posición (en el primer argumento) de la primera aparición del segundo parámetro. Devuelve -1 si no hay ninguna coincidencia.

+++Sintaxis

`indexOf(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| cadena | Cadena |
| valor especificado | Cadena |

+++

+++Firma y tipo devuelto

`indexOf(<string>,<string>)`

Devuelve un entero.

+++

+++Ejemplos

`indexOf("Hello", "l")`

Devuelve 2.

Explicación:

En &quot;Hello&quot;, la primera aparición de &quot;l&quot; es en la posición 2.

+++

## isEmpty {#isEmpty}

Devuelve true si la cadena del parámetro no tiene carácter.

+++Sintaxis

`isEmpty(<parameters>)`

+++

+++Parámetros

* cadena

+++

+++Firma y tipo devuelto

`isEmpty(<string>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`isEmpty("")`

Devuelve verdadero.

`isEmpty("Hello World")`

Devuelve falso.

`isEmpty(<null>)`

Devuelve falso.

+++

## isNotEmpty {#isNotEmpty}

Devuelve true si la cadena del parámetro no está vacía.

+++Sintaxis

`isNotEmpty(<parameters>)`

+++

+++Parámetros

* cadena

+++

+++Firma y tipo devuelto

`isNotEmpty(<string>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`isNotEmpty("")`

Devuelve falso.

`isNotEmpty("hello")`

Devuelve verdadero.

+++

## lastIndexOf {#lastIndexOf}

Devuelve la posición (en el primer argumento) de la última aparición del segundo parámetro. Devuelve -1 si no hay ninguna coincidencia.

+++Sintaxis

`lastIndexOf(<parameters>)`

+++

+++Parámetro

| Parámetro | Tipo |
|-----------|------------------|
| cadena | Cadena |
| valor especificado | Cadena |

+++

+++Firma y tipo devuelto

`lastIndexOf(<string>,<string>)`

Devuelve un entero.

+++

+++Ejemplos

`lastIndexOf("Hello", "l")`

Devuelve 3.

Explicación:

En &quot;Hello&quot;, la última ocurrencia de &quot;l&quot; está en la posición 3.

+++

## length {#length}

Devuelve el número de caracteres de la expresión de cadena en el parámetro.

+++Sintaxis

`length(<parameters>)`

+++

+++Parámetro

* cadena

+++

+++Firma y tipo devuelto

`length(<string>)`

Devuelve un entero.

+++

+++Ejemplos

`length("Hello World")`

Devuelve 11.

+++

## lower {#lower}

Devuelve una versión en minúsculas del parámetro.

+++Sintaxis

`lower(<parameter>)`

+++

+++Parámetro

* cadena

+++

+++Firma y tipo devuelto

`lower(<string>)`

Devuelve una cadena.

+++

+++Ejemplos

`lower("A")`

Devuelve &quot;a&quot;.

+++

## matchRegExp {#matchRegExp}

Devuelve true si la cadena del primer parámetro coincide con la expresión regular del segundo parámetro. Para obtener más información, vea [esta página](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

+++Sintaxis

`matchRegExp(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|--- |--- |
| cadena | cadena |
| regexp | cadena |

+++

+++Firma y tipo devuelto

`matchRegExp(<string>,<string>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`matchRegExp("12345", "\\d+")`

Devuelve verdadero.

+++

## notEqualIgnoreCase {#notEqualIgnoreCase}

Compruebe si la cadena del primer argumento con la cadena del segundo argumento es diferente, ignorando las consideraciones de mayúsculas y minúsculas.

+++Sintaxis

`notEqualIgnoreCase(<parameters>)`

+++

+++Parámetros

* cadena

+++

+++Firma y tipo devuelto

`notEqualIgnoreCase(<string>,<string>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`

+++

## replace {#replace}

Reemplaza la primera incidencia que coincida con la cadena de destino por la cadena de reemplazo de la cadena base.

La sustitución se realiza desde el principio de la cadena hasta el final, por ejemplo, si se sustituye &quot;a&quot; por &quot;b&quot; en la cadena &quot;aaa&quot;, el resultado será &quot;ba&quot; en lugar de &quot;ab&quot;.

+++Sintaxis

`replace(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|--------------|
| basar | cadena |
| Target | cadena (RegExp) |
| reemplazo | cadena |

+++

+++Firma y tipo devuelto

`replace(<base>,<target>,<replacement>)`

Devolver una cadena.

+++

+++Ejemplos

`replace("Hello World", "l", "x")`

Devuelve &quot;Mundo Hexlo&quot;.

**Ejemplo con RegExp:**

Dado que el parámetro de destino es RegExp, en función de la cadena que desee reemplazar, es posible que tenga que omitir algunos caracteres. Vea el siguiente ejemplo:

* cadena que evaluar: `|OFFER_A|OFFER_B`
* proporcionado por un atributo de perfil `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Cadena que reemplazar: `|OFFER_A`
* Cadena reemplazada por: `''`
* Debe agregar `\\` antes del carácter `|`.

La expresión es:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

La cadena devuelta es: `|OFFER_B`

También puede generar la cadena que desea reemplazar desde un atributo determinado:

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`

+++

## replaceAll {#replaceAll}

Reemplaza todas las ocurrencias que coincidan con la cadena de destino por la cadena de reemplazo de la cadena base.

La sustitución se realiza desde el principio de la cadena hasta el final, por ejemplo, si se sustituye &quot;a&quot; por &quot;b&quot; en la cadena &quot;aaa&quot;, el resultado será &quot;ba&quot; en lugar de &quot;ab&quot;.

+++Sintaxis

`replaceAll(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|--------------|
| basar | cadena |
| Target | cadena (RegExp) |
| reemplazo | cadena |

+++

+++Firma y tipo devuelto

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

Devuelve una cadena.

+++

+++Ejemplos

`replaceAll("Hello World", "l", "x")`

Devuelve &quot;Hexxo Worxd&quot;.

Dado que el parámetro de destino es RegExp, en función de la cadena que desee reemplazar, es posible que tenga que omitir algunos caracteres. Consulte el ejemplo en la función [replace](#replace).

+++

## split {#split}

Divide la cadena del primer argumento con una cadena de separador (cadena del segundo argumento, que puede ser una expresión regular) para producir una lista de cadenas (tokens).

+++Sintaxis

`split(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-----------|------------------|
| cadena de entrada | cadena |
| cadena de separación | cadena |

+++

+++Firmas y tipo devuelto

`split(<input string>, <separator string>)`

Devuelve un valor listString.

+++

+++Ejemplos

`split("A_B_C", "_")`

Devuelve `["A","B","C"]`

Ejemplo con un campo de evento &quot;event.appVersion&quot; con el valor: &quot;20.45.2.3434&quot;

`split(@event{event.appVersion}, "\\.")`

Devuelve `["20", "45", "2", "3434"]`

+++

## startWith {#startWith}

Devuelve true si el segundo parámetro es un prefijo del primero.

+++Sintaxis

`startWith(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-------------|--------|
| cadena | cadena |
| prefijo | cadena |

+++

+++Firma y tipo devuelto

`startWith(<string>,<string>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`startWith("Hello World", "Hello")`

Devuelve verdadero.

`startWith("Hello World", "World")`

Devuelve falso.

+++

## startWithIgnoreCase {#startWithIgnoreCase}

Devuelve true si el segundo parámetro es un prefijo del primero sin tener en cuenta las mayúsculas y minúsculas.

+++Sintaxis

`startWithIgnoreCase(<parameters>)`

+++

+++Parámetros

| Parámetro | Tipo |
|-------------|--------|
| cadena | cadena |
| prefijo | cadena |

+++

+++Firma y tipo devuelto

`startWithIgnoreCase(<string>,<string>)`

Devuelve un valor booleano.

+++

+++Ejemplos

`startWithIgnoreCase("rowing is great", "RO")`

Devuelve verdadero.

+++

## substr {#substr}

Devuelve la subcadena de la expresión de cadena entre el índice inicial y el índice final. Si no se define el índice final, se encuentra entre el índice inicial y el final.

+++Sintaxis

`substr(<parameters>)`

+++

+++Parámetros

| Parámetro | tipo |
|-------------|----------|
| cadena | cadena |
| beginIndex | entero |
| endIndex | entero |

+++

+++Firma y tipo devuelto

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

Devolver una cadena.

+++

+++Ejemplos

`substr("Hello World",6)`

Devuelve &quot;World&quot;.

`substr("Hello World", 0, 5)`

Devuelve &quot;Hello&quot;.

+++

## trim {#trim}

Elimina los espacios iniciales y finales.

+++Sintaxis

`trim(<parameters>)`

+++

+++Parámetro

| Parámetro | Tipo |
|-----------|------------------|
| cadena | cadena |

+++

+++Firma y tipo devuelto

`trim(<string>)`

Devolver una cadena.

+++

+++Ejemplos

`trim(" Hello ")`

Devuelve &quot;Hello&quot;.

+++

## upper {#upper}

Devuelve una versión en mayúsculas del parámetro.

+++Sintaxis

`upper(<parameters>)`

+++

+++Firma y tipo devuelto

`upper(<string>)`

Devolver una cadena.

+++

+++Ejemplos

`upper("b")`

Devuelve &quot;B&quot;.

+++

## UUID {#uuid}

Genera un UUID aleatorio (identificador único universal).

+++Sintaxis

`uuid()`

+++

+++Parámetros 

Esta función no requiere parámetros.

+++

+++Firma y tipo devuelto

`uuid()`

Devuelve una cadena.

+++

+++Ejemplos

`uuid()`

Devuelve &quot;79e70b7f-8a85-400b-97a1-9f9826121553&quot;.

+++

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página documenta todas las funciones de cadena disponibles en las expresiones de recorrido de AJO, que abarcan la búsqueda de texto, la comparación, la transformación, la extracción, la validación, el reemplazo, la división y la generación de identificadores únicos.

**Intenciones:**
* Concatenar dos o más cadenas utilizando `concat`
* Busque una subcadena dentro de una cadena (con distinción entre mayúsculas y minúsculas o sin distinción entre mayúsculas y minúsculas) usando `contain` o `containIgnoreCase`
* Comparar dos cadenas mientras se omiten las mayúsculas y minúsculas usando `equalIgnoreCase` o `notEqualIgnoreCase`
* Compruebe si una cadena comienza o termina con un prefijo o sufijo específico utilizando `startWith`, `endWith` y sus variantes que no distinguen entre mayúsculas y minúsculas
* Extraer una subcadena por posiciones de índice utilizando `substr`
* Reemplazar la primera o todas las ocurrencias de un patrón en una cadena usando `replace` o `replaceAll`
* Dividir una cadena en una lista de tokens mediante un separador con `split`
* Genere un UUID aleatorio para las necesidades de identificador único usando `uuid`
* Compruebe si una cadena está vacía o no está vacía usando `isEmpty` o `isNotEmpty`

**Glosario:**
* **RegExp**: un patrón de expresión regular utilizado como parámetro de destino en `replace`, `replaceAll` y `matchRegExp`; los caracteres especiales deben tener un carácter de escape de `\\`
* **UUID**: identificador único universal: identificador de cadena generado aleatoriamente devuelto por `uuid()`
* **substr**: extrae una parte de una cadena especificando un índice inicial y un índice final opcional (basado en cero)

**Protecciones:**
* El parámetro `target` en `replace` y `replaceAll` se trata como RegExp; los caracteres especiales (por ejemplo, `|`, `.`) deben tener un carácter de escape con `\\`
* `replace` reemplaza solamente la primera incidencia que coincida; use `replaceAll` para reemplazar todas las incidencias
* `isEmpty` devuelve falso para valores nulos (no verdadero); nulo no se considera una cadena vacía
* `indexOf` y `lastIndexOf` devuelven -1 cuando no se encuentra ninguna coincidencia
* Las posiciones de índice de la cadena están basadas en cero (el primer carácter se encuentra en la posición 0)

**Terminología:**
* Nombre canónico: Funciones de cadena — Acrónimo: none — variantes: funciones de texto, funciones de manipulación de cadenas
* Sinónimos: &quot;contain&quot; = &quot;substring check&quot;; &quot;split&quot; = &quot;tokenize string&quot;; &quot;trim&quot; = &quot;strip whitespace&quot;
* No confunda: &quot;replace&quot; (solo primera incidencia) ≠ &quot;replaceAll&quot; (todas las incidencias)
* No confunda: &quot;indexOf&quot; (posición de la primera incidencia) ≠ &quot;lastIndexOf&quot; (posición de la última incidencia)
* No confunda: &quot;isEmpty&quot; (verdadero solo para la cadena de longitud cero) ≠ comprobación nula (isEmpty devuelve falso para nulo)
* No confunda: &quot;equalIgnoreCase&quot; (devuelve true cuando el caso de omisión es igual) ≠ &quot;notEqualIgnoreCase&quot; (devuelve true cuando el caso de omisión es diferente)

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Cómo puedo comprobar si una cadena contiene una subcadena independientemente de las mayúsculas y minúsculas?** — Use `containIgnoreCase("myString", "searchTerm")`, que devuelve true si el término de búsqueda se encuentra en cualquier caso.
* **Q: ¿Cuál es la diferencia entre `replace` y `replaceAll`?** — `replace` sustituye solamente la primera aparición que coincida; `replaceAll` sustituye todas las apariciones de la cadena.
* **Q: ¿Por qué necesito omitir el carácter `|` en `replace`?** — El parámetro de destino se trata como una expresión regular; `|` es un carácter RegExp especial y debe omitirse como `\\|` para tratarse como una barra vertical literal.
* **Q: ¿Devuelve `isEmpty` true para null?** — No, `isEmpty` devuelve false para null; solo devuelve true para una cadena de longitud cero `""`.
* **Q: ¿Cómo extraigo el número de versión principal de una cadena de versión como &quot;20.45.2.3434&quot;?** — Utilice `getListItem(split(@event{event.appVersion}, "\\."), 0)` para dividir por puntos y recuperar el primer elemento.
* **Q: ¿Cómo se genera un identificador único en una expresión de recorrido?** — Use `uuid()`, que devuelve una cadena UUID generada aleatoriamente sin parámetros requeridos.

+++
