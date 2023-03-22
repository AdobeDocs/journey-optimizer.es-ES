---
title: Biblioteca de funciones de cadena
description: Biblioteca de funciones de cadena
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 9301d02be37c6aabad9c10a4cc43c20d3e3ee23e
workflow-type: tm+mt
source-wordcount: '1857'
ht-degree: 7%

---

# Funciones de cadena {#string}

Aprenda a utilizar funciones de cadena en el editor de expresiones.

## Camello {#camelCase}

La variable `camelCase` pone en mayúscula la primera letra de cada palabra de una cadena.

**Sintaxis**

```sql
{%= camelCase(string)%}
```

**Ejemplo**

La siguiente función pone en mayúscula la primera letra de la palabra en la dirección del perfil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Char código en {#char-code-at}

La variable `charCodeAt` devuelve el valor ASCII de un carácter, como la función charCodeAt en JavaScript. Toma una cadena y un entero (que define la posición del carácter) como argumentos de entrada y devuelve su valor ASCII correspondiente.

**Sintaxis**

```sql
{%= charCodeAt(string,int) %}: int
```

**Ejemplo**

La siguiente función devuelve el valor ASCII de o, es decir, 111.

```sql
{%= charCodeAt("some", 1)%}
```

## Concat {#concate}

La variable `concat` combina dos cadenas en una.

**Sintaxis**

```sql
{%= concat(string,string) %}
```

**Ejemplo**

La siguiente función combinará ciudad y país del perfil en una sola cadena.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contains {#contains}

La variable `contains` para determinar si una cadena contiene una subcadena especificada.

**Sintaxis**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `STRING_1` | La cadena en la que se va a realizar la comprobación. |
| `STRING_2` | La cadena que se va a buscar dentro de la primera cadena. |
| `CASE_SENSITIVE` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplos**

* La siguiente función comprobará si el nombre del perfil contiene la letra A (en mayúsculas o minúsculas). Si este es el caso, devolverá &#39;true&#39;, de lo contrario devolverá &#39;false&#39;.

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona contiene la cadena &quot;2010@gm&quot;.

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## No contiene{#doesNotContain}

La variable `doesNotContain` para determinar si una cadena no contiene una subcadena especificada.

**Sintaxis**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descripción |
| --------- | ----------- |
| `STRING_1` | La cadena en la que se va a realizar la comprobación. |
| `STRING_2` | La cadena que se va a buscar dentro de la primera cadena. |
| `CASE_SENSITIVE` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona no contiene la cadena &quot;2010@gm&quot;.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## No termina con{#doesNotEndWith}

La variable `doesNotEndWith` se utiliza para determinar si una cadena no termina con una subcadena especificada.

**Sintaxis**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona no termina con &quot;.com&quot;.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Does not start with{#doesNotStartWith}

La variable `doesNotStartWith` para determinar si una cadena no comienza con una subcadena especificada.

**Sintaxis**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si el nombre de la persona no comienza con &quot;Joe&quot;.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Codificar 64{#encode64}

La variable `encode64` se utiliza para codificar una cadena para conservar la información personal (PI) si se va a incluir, por ejemplo, en una dirección URL.

**Sintaxis**

```sql
{%= encode64(string) %}
```

## Finaliza con{#endsWith}

La variable `endsWith` para determinar si una cadena termina con una subcadena especificada.

**Sintaxis**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona termina en &quot;.com&quot;.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## Es igual a{#equals}

La variable `equals` se utiliza para determinar si una cadena es igual a la cadena especificada, con distinción entre mayúsculas y minúsculas.

**Sintaxis**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si el nombre de la persona es &quot;John&quot;.

```sql
{%=equals(profile.person.name,"John") %}
```

## Es igual a omitir mayúsculas y minúsculas{#equalsIgnoreCase}

La variable `equalsIgnoreCase` para determinar si una cadena es igual a la cadena especificada, sin distinción de mayúsculas y minúsculas.

**Sintaxis**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina, sin distinción de mayúsculas y minúsculas, si el nombre de la persona es &quot;John&quot;.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## Extraer dominio de correo electrónico {#extractEmailDomain}

La variable `extractEmailDomain` se utiliza para extraer el dominio de una dirección de correo electrónico.

**Sintaxis**

```sql
{%= extractEmailDomain(string) %}
```

**Ejemplo**

La siguiente consulta extrae el dominio de correo electrónico de la dirección de correo electrónico personal.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Formato de moneda {#format-currency}

La variable `formatCurrency` se utiliza para convertir cualquier número a su correspondiente representación de moneda que distinga entre idiomas, dependiendo de la configuración regional que se pase como cadena en el segundo argumento.

**Sintaxis**

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Ejemplo**

Esta consulta devuelve £56.00

```sql
{%= formatCurrency(56L,"en_GB") %}
```

## Obtener host de URL {#get-url-host}

La variable `getUrlHost` se utiliza para recuperar el nombre de host de una URL.

**Sintaxis**

```sql
{%= getUrlHost(string) %}: string
```

**Ejemplo**

```sql
{%= getUrlHost("http://www.myurl.com/contact") %}
```

Devuelve &quot;www.myurl.com&quot;

## Obtener ruta de URL {#get-url-path}

La variable `getUrlPath` se utiliza para recuperar la ruta después del nombre de dominio de una dirección URL.

**Sintaxis**

```sql
{%= getUrlPath(string) %}: string
```

**Ejemplo**

```sql
{%= getUrlPath("http://www.myurl.com/contact.html") %}
```

Devuelve &quot;/contact.html&quot;

## Obtener protocolo de url {#get-url-protocol}

La variable `getUrlProtocol` se utiliza para recuperar el protocolo de una URL.

**Sintaxis**

```sql
{%= getUrlProtocol(string) %}: string
```

**Ejemplo**

```sql
{%= getUrlProtocol("http://www.myurl.com/contact.html") %}
```

Devuelve &quot;http&quot;

## Índice de {#index-of}

La variable `indexOf` se utiliza para devolver la posición (en el primer argumento) de la primera incidencia del segundo parámetro. Devuelve -1 si no hay coincidencia.

**Sintaxis**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar en el primer parámetro |

**Ejemplo**

```sql
{%= indexOf("hello world","world" ) %}
```

Devuelve 6.

## Is empty {#isEmpty}

La variable `isEmpty` para determinar si una cadena está vacía.

**Sintaxis**

```sql
{%= isEmpty(string) %}
```

**Ejemplo**

La siguiente función devuelve &#39;true&#39; si el número de teléfono móvil del perfil está vacío. De lo contrario, devolverá &#39;false&#39;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Is Not Empty {#is-not-empty}

La variable `isNotEmpty` para determinar si una cadena no está vacía.

**Sintaxis**

```sql
{= isNotEmpty(string) %}: boolean
```

**Ejemplo**

La siguiente función devuelve &#39;true&#39; si el número de teléfono móvil del perfil no está vacío. De lo contrario, devolverá &#39;false&#39;.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## Último índice de {#last-index-of}

La variable `lastIndexOf` se utiliza para devolver la posición (en el primer argumento) de la última incidencia del segundo parámetro. Devuelve -1 si no hay coincidencia.

**Sintaxis**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar en el primer parámetro |

**Ejemplo**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Devuelve 7.

## Guarnecido izquierdo {#leftTrim}

La variable `leftTrim` se utiliza para eliminar los espacios en blanco del principio de una cadena.

**Sintaxis**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

La variable `length` se utiliza para obtener el número de caracteres de una cadena o una expresión.

**Sintaxis**

```sql
{%= length(string) %}
```

**Ejemplo**

La siguiente función devuelve la longitud del nombre de ciudad del perfil.

```sql
{%= length(profile.homeAddress.city) %}
```

## Like{#like}

La variable `like` para determinar si una cadena coincide con un patrón especificado.

**Sintaxis**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La expresión que debe coincidir con la primera cadena. Existen dos caracteres especiales admitidos para crear una expresión: `%` y `_`. <ul><li>`%` se utiliza para representar cero o más caracteres.</li><li>`_` se utiliza para representar exactamente un carácter.</li></ul> |

**Ejemplo**

La siguiente consulta recupera todas las ciudades donde viven los perfiles que contienen el patrón &quot;es&quot;.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Lower Case{#lower}

La variable `lowerCase` convierte una cadena en minúsculas.

**Sintaxis**

```sql
{%= lowerCase(string) %}
```

**Ejemplo**

Esta función convierte el nombre del perfil en letras minúsculas.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## Devuelve como resultado {#matches}

La variable `matches` para determinar si una cadena coincide con una expresión regular específica. Consulte [este documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) para obtener más información sobre patrones coincidentes en expresiones regulares.

**Sintaxis**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Ejemplo**

La siguiente consulta determina, sin distinción de mayúsculas y minúsculas, si el nombre de la persona empieza por &quot;John&quot;.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Máscara {#mask}

La variable `Mask` se utiliza para reemplazar una parte de una cadena con caracteres &quot;X&quot;.

**Sintaxis**

```sql
{%= mask(string,integer,integer) %}
```

**Ejemplo**

La siguiente consulta reemplaza la cadena &quot;123456789&quot; por caracteres &quot;X&quot;, excepto para los dos primeros y últimos caracteres.

```sql
{%= mask("123456789",1,2) %}
```

La consulta devuelve `1XXXXXX89`.

## MD5 {#md5}

La variable `md5` se utiliza para calcular y devolver el hash md5 de una cadena.

**Sintaxis**

```sql
{%= md5(string) %}: string
```

**Ejemplo**

```sql
{%= md5("hello world") %}
```

Devuelve &quot;5eb63bbbe01eed093cb22bb8f5acdc3&quot;

## Not equal to{#notEqualTo}

La variable `notEqualTo` para determinar si una cadena no es igual a la cadena especificada.

**Sintaxis**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si el nombre de la persona no es &quot;John&quot;.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Distinto de mayúsculas y minúsculas ignoradas {#not-equal-with-ignore-case}

La variable `notEqualWithIgnoreCase` se utiliza para comparar dos cadenas que ignoran mayúsculas y minúsculas.

**Sintaxis**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina si el nombre de la persona no es &quot;john&quot;, sin distinción de mayúsculas y minúsculas.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## Grupo de expresiones regulares{#regexGroup}

La variable `Group` se utiliza para extraer información específica, según la expresión regular proporcionada.

**Sintaxis**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING}` | La cadena en la que se va a realizar la comprobación. |
| `{EXPRESSION}` | La expresión regular que coincide con la primera cadena. |
| `{GROUP}` | Grupo de expresiones con el que hacer coincidir. |

**Ejemplo**

La siguiente consulta se utiliza para extraer el nombre de dominio de una dirección de correo electrónico.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## Reemplazar {#replace}

La variable `replace` se utiliza para reemplazar una subcadena determinada de una cadena por otra subcadena.

**Sintaxis**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena donde se debe reemplazar la subcadena. |
| `{STRING_2}` | La subcadena que se va a reemplazar. |
| `{STRING_3}` | La subcadena de reemplazo. |

**Ejemplo**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Devuelve &quot;Hello Mark, aquí tiene su boletín mensual&quot;.

## Reemplazar todo{#replaceAll}

La variable `replaceAll` se utiliza para reemplazar todas las subcadenas de un texto que coincida con la expresión &quot;regex&quot; con la cadena de literal &quot;replace&quot; especificada. Regex tiene un manejo especial de &quot;\&quot; y &quot;+&quot; y todas las expresiones regex siguen la estrategia de escape de PQL. La sustitución procede desde el principio de la cadena hasta el final, por ejemplo, reemplazar &quot;aa&quot; por &quot;b&quot; en la cadena &quot;aaa&quot; resultará en &quot;ba&quot; en lugar de &quot;ab&quot;.

**Sintaxis**

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Cuando la expresión tomada como segundo argumento sea un carácter regex especial, utilice una barra invertida doble (`//`).  Los caracteres especiales de regex son: [, +, *, ?, ^, $, (, ), [, ], {, }, |, \.]
> 
> Obtenga más información en [documentación de oracle](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.

## Guarnecido derecho {#rightTrim}

La variable `rightTrim` se utiliza para eliminar los espacios en blanco del final de una cadena.

**Sintaxis**

```sql
{%= rightTrim(string) %}
```

## Split {#split}

La variable `split` se utiliza para dividir una cadena por un carácter determinado.

**Sintaxis**

```sql
{%= split(string,string) %}
```

## Comienza con{#startsWith}

La variable `startsWith` se utiliza para determinar si una cadena comienza con una subcadena especificada.

**Sintaxis**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. De forma predeterminada, se establece en true. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si el nombre de la persona empieza por &quot;Joe&quot;.

```sql
{%= startsWith(person.name,"Joe") %}
```

## Cadena hasta la fecha {#string-to-date}

La variable `stringToDate` convierte un valor de cadena en un valor de fecha-hora. Toma dos argumentos: representación de cadena de una representación de fecha-hora y de cadena del formateador.

**Sintaxis**

```sql
{= stringToDate("date-time value","formatter" %}
```

**Ejemplo**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## Cadena a entero {#string-to-integer}

La variable `string_to_integer` se utiliza para convertir un valor de cadena en un valor entero.

**Sintaxis**

```sql
{= string_to_integer(string) %}: int
```

## Cadena para número {#string-to-number}

La variable `stringToNumber` se utiliza para convertir una cadena en número. Devuelve la misma cadena que el resultado de una entrada no válida.

**Sintaxis**

```sql
{%= stringToNumber(string) %}: double
```

## Subcadena {#sub-string}

La variable `Count string` se utiliza para devolver la subcadena de la expresión de cadena entre el índice begin y el índice end.
**Sintaxis**

```sql
{= substr(string, integer, integer) %}: string
```

## Caso de título{#titleCase}

La variable **titleCase** se utiliza para poner en mayúsculas las primeras letras de cada palabra de una cadena.

**Sintaxis**

```sql
{%= titleCase(string) %}
```

**Ejemplo**

Si la persona vive en Washington High Street, esta función regresará a Washington High Street.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## A Bool {#to-bool}

La variable `toBool` se utiliza para convertir un valor de argumento en un valor booleano, según su tipo.

**Sintaxis**

```sql
{= toBool(string) %}: boolean
```

## Hasta la fecha {#to-date-time}

La variable `toDateTime` se utiliza para convertir cadena a fecha. Devuelve la fecha de epoch como salida para una entrada no válida.

**Sintaxis**

```sql
{%= toDateTime(string, string) %}: date-time
```

## Hasta fecha solamente {#to-date-time-only}

La variable `toDateTimeOnly` se utiliza para convertir un valor de argumento en un valor de solo fecha. Devuelve la fecha de epoch como salida para una entrada no válida. Esta función acepta tipos de campo de cadena, fecha, larga e int.

**Sintaxis**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## Recortar {#trim}

La variable **trim** elimina todos los espacios en blanco del principio y del final de una cadena.

**Sintaxis**

```sql
{%= trim(string) %}
```

## Mayúsculas{#upper}

La variable **upperCase** convierte una cadena en mayúsculas.

**Sintaxis**

```sql
{%= upperCase(string) %}
```

**Ejemplo**

Esta función convierte los apellidos del perfil en mayúsculas.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## Descodificación de URL {#url-decode}

La variable `urlDecode` se utiliza para decodificar una cadena con codificación url.

**Sintaxis**

```sql
{%= urlDecode(string) %}: string
```

## Codificación de URL {#url-encode}

La variable `Count only null` para codificar una cadena.

**Sintaxis**

```sql
{%= urlEncode(string) %}: string
```
