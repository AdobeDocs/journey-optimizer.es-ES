---
title: Biblioteca de funciones de cadena
description: Biblioteca de funciones de cadena
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 1f16b095b3b063f3fb881aee0b2a928644e19143
workflow-type: tm+mt
source-wordcount: '1859'
ht-degree: 9%

---

# Funciones de cadena {#string}

Aprenda a utilizar las funciones de cadena en el editor de personalización.

## Camel Case {#camelCase}

La función `camelCase` pone en mayúscula la primera letra de cada palabra de una cadena.

**Sintaxis**

```sql
{%= camelCase(string)%}
```

**Ejemplo**

La siguiente función pone en mayúscula la primera letra de la dirección del perfil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Código Char en {#char-code-at}

La función `charCodeAt` devuelve el valor ASCII de un carácter, como la función charCodeAt de JavaScript. Toma una cadena y un entero (que define la posición del carácter) como argumentos de entrada y devuelve su valor ASCII correspondiente.

**Sintaxis**

```sql
{%= charCodeAt(string,int) %}: int
```

**Ejemplo**

La siguiente función devuelve el valor ASCII o, es decir 111.

```sql
{%= charCodeAt("some", 1)%}
```

## Concat {#concate}

La función `concat` combina dos cadenas en una.

**Sintaxis**

```sql
{%= concat(string,string) %}
```

**Ejemplo**

La siguiente función combinará ciudad y país de perfil en una sola cadena.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contiene {#contains}

La función `contains` se usa para determinar si una cadena contiene una subcadena especificada.

**Sintaxis**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `STRING_1` | Cadena en la que se realizará la comprobación. |
| `STRING_2` | Cadena que se busca dentro de la primera cadena. |
| `CASE_SENSITIVE` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplos**

* La siguiente función comprobará si el nombre del perfil contiene la letra A (en mayúsculas o minúsculas). Si este es el caso, devuelve &quot;true&quot;; de lo contrario, devuelve &quot;false&quot;.

  ```sql
  {%= contains(profile.person.name.firstName, "A", false) %}
  ```

* La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona contiene la cadena &quot;2010@gm&quot;.

  ```sql
  {%= contains(profile.person.emailAddress,"2010@gm") %}
  ```

## No contiene{#doesNotContain}

La función `doesNotContain` se usa para determinar si una cadena no contiene una subcadena especificada.

**Sintaxis**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descripción |
| --------- | ----------- |
| `STRING_1` | Cadena en la que se realizará la comprobación. |
| `STRING_2` | Cadena que se busca dentro de la primera cadena. |
| `CASE_SENSITIVE` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona no contiene la cadena &quot;2010@gm&quot;.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## No termina por{#doesNotEndWith}

La función `doesNotEndWith` se usa para determinar si una cadena no termina con una subcadena especificada.

**Sintaxis**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se busca dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción entre mayúsculas y minúsculas, si la dirección de correo electrónico de la persona no termina con &quot;.com&quot;.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## No empieza por{#doesNotStartWith}

La función `doesNotStartWith` se usa para determinar si una cadena no comienza con una subcadena especificada.

**Sintaxis**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se busca dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción entre mayúsculas y minúsculas, si el nombre de la persona no comienza con &quot;Joe&quot;.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Codificar 64{#encode64}

La función `encode64` se usa para codificar una cadena para conservar la información personal (PI) si se va a incluir, por ejemplo, en una dirección URL.

**Sintaxis**

```sql
{%= encode64(string) %}
```

## Termina por{#endsWith}

La función `endsWith` se usa para determinar si una cadena termina con una subcadena especificada.

**Sintaxis**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se busca dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. Valores posibles: true (predeterminado) / false. |

**Ejemplo**

La siguiente consulta determina, con distinción entre mayúsculas y minúsculas, si la dirección de correo electrónico de la persona termina con &quot;.com&quot;.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## Es igual a{#equals}

La función `equals` se usa para determinar si una cadena es igual a la cadena especificada, con distinción entre mayúsculas y minúsculas.

**Sintaxis**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina, con distinción entre mayúsculas y minúsculas, si el nombre de la persona es &quot;John&quot;.

```sql
{%=equals(profile.person.name,"John") %}
```

## Igual a Ignorar Mayúsculas y Minúsculas{#equalsIgnoreCase}

La función `equalsIgnoreCase` se usa para determinar si una cadena es igual a la cadena especificada, sin distinción de mayúsculas y minúsculas.

**Sintaxis**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina, sin distinción entre mayúsculas y minúsculas, si el nombre de la persona es &quot;John&quot;.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## Extraer dominio de correo electrónico {#extractEmailDomain}

La función `extractEmailDomain` se usa para extraer el dominio de una dirección de correo electrónico.

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

La función `formatCurrency` se usa para convertir cualquier número en su correspondiente representación de moneda con distinción de idioma, en función de la configuración regional pasada como cadena en el segundo argumento.

**Sintaxis**

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Ejemplo**

Esta consulta devuelve 56 £

```sql
{%= formatCurrency(56L,"en_GB") %}
```

## Obtener host de URL {#get-url-host}

La función `getUrlHost` se usa para recuperar el nombre de host de una dirección URL.

**Sintaxis**

```sql
{%= getUrlHost(string) %}: string
```

**Ejemplo**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Devuelve &quot;www.myurl.com&quot;

## Obtener ruta de URL {#get-url-path}

La función `getUrlPath` se usa para recuperar la ruta de acceso después del nombre de dominio de una dirección URL.

**Sintaxis**

```sql
{%= getUrlPath(string) %}: string
```

**Ejemplo**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Devuelve &quot;/contact.html&quot;

## Obtener protocolo de URL {#get-url-protocol}

La función `getUrlProtocol` se usa para recuperar el protocolo de una dirección URL.

**Sintaxis**

```sql
{%= getUrlProtocol(string) %}: string
```

**Ejemplo**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Devuelve &quot;http&quot;

## Índice De {#index-of}

La función `indexOf` se usa para devolver la posición (en el primer argumento) de la primera aparición del segundo parámetro. Devuelve -1 si no hay ninguna coincidencia.

**Sintaxis**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | La cadena que se busca en el primer parámetro |

**Ejemplo**

```sql
{%= indexOf("hello world","world" ) %}
```

Devuelve 6.

## Está vacío {#isEmpty}

La función `isEmpty` se usa para determinar si una cadena está vacía.

**Sintaxis**

```sql
{%= isEmpty(string) %}
```

**Ejemplo**

La siguiente función devuelve &quot;true&quot; si el número de teléfono móvil del perfil está vacío. De lo contrario, devolverá &quot;false&quot;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## No está vacío {#is-not-empty}

La función `isNotEmpty` se usa para determinar si una cadena no está vacía.

**Sintaxis**

```sql
{= isNotEmpty(string) %}: boolean
```

**Ejemplo**

La siguiente función devuelve &quot;true&quot; si el número de teléfono móvil del perfil no está vacío. De lo contrario, devolverá &quot;false&quot;.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## Último Índice De {#last-index-of}

La función `lastIndexOf` se usa para devolver la posición (en el primer argumento) de la última aparición del segundo parámetro. Devuelve -1 si no hay ninguna coincidencia.

**Sintaxis**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | La cadena que se busca en el primer parámetro |

**Ejemplo**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Devuelve 7.

## Guarnecido izquierdo {#leftTrim}

La función `leftTrim` se usa para quitar espacios en blanco del principio de una cadena.

**Sintaxis**

```sql
{%= leftTrim(string) %}
```

## Longitud {#length}

La función `length` se usa para obtener el número de caracteres de una cadena o expresión.

**Sintaxis**

```sql
{%= length(string) %}
```

**Ejemplo**

La siguiente función devuelve la longitud del nombre de ciudad del perfil.

```sql
{%= length(profile.homeAddress.city) %}
```

## Como{#like}

La función `like` se usa para determinar si una cadena coincide con un patrón especificado.

**Sintaxis**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | La expresión que debe coincidir con la primera cadena. Existen dos caracteres especiales admitidos para crear una expresión: `%` y `_`. <ul><li>`%` se usa para representar cero o más caracteres.</li><li>`_` se usa para representar exactamente un carácter.</li></ul> |

**Ejemplo**

La siguiente consulta recupera todas las ciudades en las que residen los perfiles que contienen el patrón &quot;es&quot;.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Minúsculas{#lower}

La función `lowerCase` convierte una cadena en letras minúsculas.

**Sintaxis**

```sql
{%= lowerCase(string) %}
```

**Ejemplo**

Esta función convierte el nombre del perfil en letras minúsculas.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## Iguala{#matches}

La función `matches` se usa para determinar si una cadena coincide con una expresión regular específica. Consulte [este documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) para obtener más información sobre los patrones coincidentes en las expresiones regulares.

**Sintaxis**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Ejemplo**

La siguiente consulta determina, sin distinción entre mayúsculas y minúsculas, si el nombre de la persona comienza por &quot;John&quot;.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Máscara {#mask}

La función `Mask` se usa para reemplazar una parte de una cadena con caracteres &quot;X&quot;.

**Sintaxis**

```sql
{%= mask(string,integer,integer) %}
```

**Ejemplo**

La siguiente consulta reemplaza la cadena &quot;123456789&quot; por los caracteres &quot;X&quot;, excepto para los dos primeros y los últimos caracteres.

```sql
{%= mask("123456789",1,2) %}
```

La consulta devuelve `1XXXXXX89`.

## MD5 {#md5}

La función `md5` se usa para calcular y devolver el hash md5 de una cadena.

**Sintaxis**

```sql
{%= md5(string) %}: string
```

**Ejemplo**

```sql
{%= md5("hello world") %}
```

Devuelve &quot;5eb63bbbe01eeed093cb22bb8f5acdc3&quot;

## No igual a{#notEqualTo}

La función `notEqualTo` se usa para determinar si una cadena no es igual a la cadena especificada.

**Sintaxis**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina, con distinción entre mayúsculas y minúsculas, si el nombre de la persona no es &quot;John&quot;.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## No Igual Con Ignorar Mayúsculas y Minúsculas {#not-equal-with-ignore-case}

La función `notEqualWithIgnoreCase` se usa para comparar dos cadenas ignorando mayúsculas y minúsculas.

**Sintaxis**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina si el nombre de la persona no es &quot;john&quot;, sin distinción de mayúsculas y minúsculas.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## Grupo de expresiones regulares{#regexGroup}

La función `Group` se usa para extraer información específica, basada en la expresión regular proporcionada.

**Sintaxis**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING}` | Cadena en la que se realizará la comprobación. |
| `{EXPRESSION}` | La expresión regular que debe coincidir con la primera cadena. |
| `{GROUP}` | Grupo de expresiones con el que debe coincidir. |

**Ejemplo**

La siguiente consulta se utiliza para extraer el nombre de dominio de una dirección de correo electrónico.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## Reemplazar {#replace}

La función `replace` se usa para reemplazar una subcadena determinada de una cadena con otra subcadena.

**Sintaxis**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se debe reemplazar la subcadena. |
| `{STRING_2}` | La subcadena que se va a reemplazar. |
| `{STRING_3}` | La subcadena de reemplazo. |

**Ejemplo**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Devuelve &quot;Hola Mark, aquí tienes tu newsletter mensual&quot;.

## Reemplazar todo{#replaceAll}

La función `replaceAll` se usa para reemplazar todas las subcadenas de un texto que coincide con la expresión &quot;regex&quot; con la cadena &quot;replace&quot; literal especificada. Regex tiene un manejo especial de &quot;\&quot; y &quot;+&quot; y todas las expresiones regex siguen la estrategia de escape de PQL. La sustitución se realiza desde el principio de la cadena hasta el final, por ejemplo, si se sustituye &quot;a&quot; por &quot;b&quot; en la cadena &quot;aaa&quot;, el resultado será &quot;ba&quot; en lugar de &quot;ab&quot;.

**Sintaxis**

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Cuando la expresión tomada como segundo argumento sea un carácter regex especial, utilice una doble barra invertida (`//`).  Los caracteres regex especiales son: [., +, *, ?, ^, $, (, ), [,], {, }, |, \.]
> 
> Obtenga más información en [Documentación de Oracle](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

## Guarnecido derecho {#rightTrim}

La función `rightTrim` elimina los espacios en blanco del final de una cadena.

**Sintaxis**

```sql
{%= rightTrim(string) %}
```

## SHA256 {#sha256}

La función `SHA256` calcula y devuelve el hash sha256 de una cadena.

**Sintaxis**

```sql
{%= sha256(string) %} : string
```

**Ejemplo**

```sql
{%= sha256("Eliechxh")%}
```

devuelve: `0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d`

## División {#split}

La función `split` se usa para dividir una cadena entre un carácter determinado.

**Sintaxis**

```sql
{%= split(string,string) %}
```

## Comienza por{#startsWith}

La función `startsWith` se usa para determinar si una cadena empieza con una subcadena especificada.

**Sintaxis**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | Cadena en la que se realizará la comprobación. |
| `{STRING_2}` | Cadena que se busca dentro de la primera cadena. |
| `{CASE_SENSITIVE}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. De forma predeterminada, se establece en true. |

**Ejemplo**

La siguiente consulta determina, con distinción entre mayúsculas y minúsculas, si el nombre de la persona empieza por &quot;Joe&quot;.

```sql
{%= startsWith(person.name,"Joe") %}
```

## Cadena a fecha {#string-to-date}

La función `stringToDate` convierte un valor de cadena en un valor de fecha y hora. Se necesitan dos argumentos: la representación de cadena de una fecha y hora y la representación de cadena del formateador.

**Sintaxis**

```sql
{= stringToDate("date-time value","formatter" %}
```

**Ejemplo**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## Cadena a entero {#string-to-integer}

La función `string_to_integer` se usa para convertir un valor de cadena en un valor entero.

**Sintaxis**

```sql
{= string_to_integer(string) %}: int
```

## Cadena a número {#string-to-number}

La función `stringToNumber` se usa para convertir una cadena en número. Devuelve la misma cadena como salida para la entrada no válida.

**Sintaxis**

```sql
{%= stringToNumber(string) %}: double
```

## Subcadena {#sub-string}

La función `Count string` se usa para devolver la subcadena de la expresión de cadena entre el índice inicial y el índice final.
**Sintaxis**

```sql
{= substr(string, integer, integer) %}: string
```

## Caso de título{#titleCase}

La función **titleCase** se usa para poner en mayúsculas las primeras letras de cada palabra de una cadena.

**Sintaxis**

```sql
{%= titleCase(string) %}
```

**Ejemplo**

Si la persona vive en Washington High Street, esta función devolverá Washington High Street.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## A Bool {#to-bool}

La función `toBool` se usa para convertir un valor de argumento en un valor booleano, según su tipo.

**Sintaxis**

```sql
{= toBool(string) %}: boolean
```

## A Fecha Hora {#to-date-time}

La función `toDateTime` se usa para convertir la cadena a fecha. Devuelve la fecha epoch como salida para una entrada no válida.

**Sintaxis**

```sql
{%= toDateTime(string, string) %}: date-time
```

## A Fecha Hora Solo {#to-date-time-only}

La función `toDateTimeOnly` se usa para convertir un valor de argumento en un valor de solo fecha y hora. Devuelve la fecha epoch como salida para una entrada no válida. Esta función acepta tipos de campo string, date, long e int.

**Sintaxis**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## Recortar {#trim}

La función **trim** elimina todos los espacios en blanco del principio y del final de una cadena.

**Sintaxis**

```sql
{%= trim(string) %}
```

## Mayúsculas{#upper}

La función **upperCase** convierte una cadena en letras mayúsculas.

**Sintaxis**

```sql
{%= upperCase(string) %}
```

**Ejemplo**

Esta función convierte los apellidos del perfil en letras mayúsculas.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## Descifrar URL {#url-decode}

La función `urlDecode` se usa para descodificar una cadena con codificación URL.

**Sintaxis**

```sql
{%= urlDecode(string) %}: string
```

## Cifrar URL {#url-encode}

La función `Count only null` se usa para codificar una cadena mediante URL.

**Sintaxis**

```sql
{%= urlEncode(string) %}: string
```
