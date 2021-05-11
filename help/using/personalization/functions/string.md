---
title: Biblioteca de funciones
description: Biblioteca de funciones
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 8%

---

# Funciones de cadena {#string}

![](../../assets/do-not-localize/badge.png)


Funciones de cadena CJM de TBC

## Like

La función `like` se utiliza para determinar si una cadena coincide con un patrón especificado.

**Formato**

```sql
like ({STRING_1},{STRING_2})
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La expresión que debe coincidir con la primera cadena. Existen dos caracteres especiales admitidos para crear una expresión: `%` y `_`. <ul><li>`%` se utiliza para representar cero o más caracteres.</li><li>`_` se utiliza para representar exactamente un carácter.</li></ul> |

**Ejemplo**

La siguiente consulta recupera todas las ciudades que contienen el patrón &quot;es&quot;.

```sql
like (city ,"%es%")
```

## Comienza con

La función `startsWith` se utiliza para determinar si una cadena comienza con una subcadena especificada.

**Formato**

```sql
startsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar dentro de la primera cadena. |
| `{BOOLEAN}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. De forma predeterminada, se establece en true. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si el nombre de la persona empieza por &quot;Joe&quot;.

```sql
startsWith(person.name,"Joe")
```

## Does not start with

La función `doesNotStartWith` se utiliza para determinar si una cadena no comienza con una subcadena especificada.

**Formato**

```sql
doesNotStartWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar dentro de la primera cadena. |
| `{BOOLEAN}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. De forma predeterminada, se establece en true. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si el nombre de la persona no comienza con &quot;Joe&quot;.

```sql
doesNotStartWith(person.name,"Joe")
```

## Finaliza con

La función `endsWith` se utiliza para determinar si una cadena termina con una subcadena especificada.

**Formato**

```sql
endsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar dentro de la primera cadena. |
| `{BOOLEAN}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. De forma predeterminada, se establece en true. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona termina en &quot;.com&quot;.

```sql
endsWith(person.emailAddress,".com")
```

## No termina con

La función `doesNotEndWith` se utiliza para determinar si una cadena no termina con una subcadena especificada.

**Formato**

```sql
doesNotEndWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar dentro de la primera cadena. |
| `{BOOLEAN}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. De forma predeterminada, se establece en true. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona no termina con &quot;.com&quot;.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Contains

La función `contains` se utiliza para determinar si una cadena contiene una subcadena especificada.

**Formato**

```sql
contains({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar dentro de la primera cadena. |
| `{BOOLEAN}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. De forma predeterminada, se establece en true. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona contiene la cadena &quot;2010@gm&quot;.

```sql
contains(person.emailAddress,"2010@gm")
```

## No contiene

La función `doesNotContain` se utiliza para determinar si una cadena no contiene una subcadena especificada.

**Formato**

```sql
doesNotContain({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a buscar dentro de la primera cadena. |
| `{BOOLEAN}` | Un parámetro opcional para determinar si la comprobación distingue entre mayúsculas y minúsculas. De forma predeterminada, se establece en true. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si la dirección de correo electrónico de la persona no contiene la cadena &quot;2010@gm&quot;.

```sql
doesNotContain(person.emailAddress,"2010@gm")
```

## Es igual a

La función `equals` se utiliza para determinar si una cadena es igual a la cadena especificada.

**Formato**

```sql
equals({STRING_1},{STRING_2})
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si el nombre de la persona es &quot;John&quot;.

```sql
equals(person.name,"John")
```

## Not equal to

La función `notEqualTo` se utiliza para determinar si una cadena no es igual a la cadena especificada.

**Formato**

```sql
notEqualTo({STRING_1},{STRING_2})
```

| Argumento | Descripción |
| --------- | ----------- |
| `{STRING_1}` | La cadena en la que se va a realizar la comprobación. |
| `{STRING_2}` | La cadena que se va a comparar con la primera cadena. |

**Ejemplo**

La siguiente consulta determina, con distinción de mayúsculas y minúsculas, si el nombre de la persona no es &quot;John&quot;.

```sql
notEqualTo(person.name,"John")
```

## Coincide

La función `matches` se utiliza para determinar si una cadena coincide con una expresión regular específica. Consulte [este documento](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) para obtener más información sobre los patrones coincidentes en las expresiones regulares.

**Formato**

```sql
matches({STRING_1},STRING_2})
```

**Ejemplo**

La siguiente consulta determina, sin distinguir entre mayúsculas y minúsculas, si el nombre de la persona empieza por &quot;John&quot;.

```sql
matches(person.name.,"(?i)^John")
```

## Grupo de expresiones regulares

La función `regexGroup` se utiliza para extraer información específica, según la expresión regular proporcionada.

**Formato**

```sql
regexGroup({STRING},{EXPRESSION})
```

**Ejemplo**

La siguiente consulta se utiliza para extraer el nombre de dominio de una dirección de correo electrónico.

```sql
regexGroup(emailAddress,"@(\w+)", 1)
```
