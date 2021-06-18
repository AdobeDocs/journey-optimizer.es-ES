---
title: Biblioteca de funciones de cadena
description: Biblioteca de funciones de cadena
feature: Personalización
topic: Personalización
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 7%

---

# Funciones de cadena {#string}

Aprenda a utilizar funciones de cadena en el Editor de expresiones.

## Camello {#camelCase}

La función `camelCase` pone en mayúsculas la primera letra de cada palabra de una cadena.

**Formato**

```sql
{%= camelCase(string)%}
```

**Ejemplo**

La siguiente función pone en mayúscula la primera letra de la palabra en la dirección del perfil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Concat {#concate}

La función `concat` combina dos cadenas en una.

**Formato**

```sql
{%= concat(string,string) %}
```

**Ejemplo**

La siguiente función combinará ciudad y país del perfil en una sola cadena.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contains {#contains}

La función `contains` se utiliza para determinar si una cadena contiene una subcadena especificada.

**Formato**

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

La función `doesNotContain` se utiliza para determinar si una cadena no contiene una subcadena especificada.

**Formato**

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

La función `doesNotEndWith` se utiliza para determinar si una cadena no termina con una subcadena especificada.

**Formato**

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

La función `doesNotStartWith` se utiliza para determinar si una cadena no comienza con una subcadena especificada.

**Formato**

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

La función `encode64` se utiliza para codificar una cadena para conservar la información personal (PI) si se va a incluir, por ejemplo, en una dirección URL.

**Formato**

```sql
{%= encode64(string) %}
```

## Finaliza con{#endsWith}

La función `endsWith` se utiliza para determinar si una cadena termina con una subcadena especificada.

**Formato**

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

La función `equals` se utiliza para determinar si una cadena es igual a la cadena especificada, con distinción entre mayúsculas y minúsculas.

**Formato**

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

La función `equalsIgnoreCase` se utiliza para determinar si una cadena es igual a la cadena especificada, sin distinción de mayúsculas y minúsculas.

**Formato**

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

La función `extractEmailDomain` se utiliza para extraer el dominio de una dirección de correo electrónico.

**Formato**

```sql
{%= extractEmailDomain(string) %}
```

**Ejemplo**

La siguiente consulta extrae el dominio de correo electrónico de la dirección de correo electrónico personal.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Is empty {#isEmpty}

La función `isEmpty` se utiliza para determinar si una cadena está vacía.

**Formato**

```sql
{%= isEmpty(string) %}
```

**Ejemplo**

La siguiente función devuelve &#39;true&#39; si el número de teléfono móvil del perfil está vacío. De lo contrario, devolverá &#39;false&#39;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Guarnecido izquierdo {#leftTrim}

La función `leftTrim` se utiliza para eliminar los espacios en blanco del principio de una cadena.

**Formato**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

La función `length` se utiliza para obtener el número de caracteres de una cadena o una expresión.

**Formato**

```sql
{%= length(string) %}
```

**Ejemplo**

La siguiente función devuelve la longitud del nombre de ciudad del perfil.

```sql
{%= length(profile.homeAddress.city) %}
```

## Like{#like}

La función `like` se utiliza para determinar si una cadena coincide con un patrón especificado.

**Formato**

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

## Coincide{#matches}

La función `matches` se utiliza para determinar si una cadena coincide con una expresión regular específica. Consulte [este documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) para obtener más información sobre los patrones coincidentes en las expresiones regulares.

**Formato**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Ejemplo**

La siguiente consulta determina, sin distinción de mayúsculas y minúsculas, si el nombre de la persona empieza por &quot;John&quot;.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Not equal to{#notEqualTo}

La función `notEqualTo` se utiliza para determinar si una cadena no es igual a la cadena especificada.

**Formato**

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

## Grupo de expresiones regulares{#regexGroup}

La función `Group` se utiliza para extraer información específica, según la expresión regular proporcionada.

**Formato**

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
{%= regexGroup(emailAddress,"@(\w+)", 1) %}
```

## Replace {#replace}

La función `replace` se utiliza para reemplazar una subcadena determinada de una cadena por otra subcadena.

**Formato**

```sql
{%= replace(string,string,string) %}
```

**Ejemplo**

La siguiente función .

```sql

```


## Reemplazar todo{#replaceAll}

La función `replaceAll` se utiliza para reemplazar todas las subcadenas de un texto que coincida con el &quot;destino&quot; por la cadena de sustitución del literal especificada. La sustitución procede desde el principio de la cadena hasta el final, por ejemplo, reemplazar &quot;aa&quot; por &quot;b&quot; en la cadena &quot;aaa&quot; resultará en &quot;ba&quot; en lugar de &quot;ab&quot;.

**Formato**

```sql
{%= replaceAll(string,string,string) %}
```


## Guarnecido derecho {#rightTrim}

La función `rightTrim` se utiliza elimina los espacios en blanco del final de una cadena.


**Formato**

```sql
{%= rightTrim(string) %}
```

## Split {#split}

La función `split` se utiliza para dividir una cadena por un carácter determinado.

**Formato**

```sql
{%= split(string,string) %}
```

<!--
**Example**

The following function .

```sql

```

-->

## Comienza con{#startsWith}

La función `startsWith` se utiliza para determinar si una cadena comienza con una subcadena especificada.

**Formato**

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

## Caso de título{#titleCase}

La función **titleCase** se utiliza para poner en mayúsculas las primeras letras de cada palabra de una cadena.

**Sintaxis**

```sql
{%= titleCase(string) %}
```

**Ejemplo**

Si la persona vive en Washington High Street, esta función regresará a Washington High Street.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## Recortar{#trim}

La función **trim** elimina todos los espacios en blanco del principio y del final de una cadena.

**Sintaxis**

```sql
{%= trim(string) %}
```

## Mayúsculas{#upper}

La función **upperCase** convierte una cadena en mayúsculas.

**Sintaxis**

```sql
{%= upperCase(string) %}
```

**Ejemplo**

Esta función convierte los apellidos del perfil en mayúsculas.

```sql
{%= upperCase(profile.person.name.lastName) %}
```
