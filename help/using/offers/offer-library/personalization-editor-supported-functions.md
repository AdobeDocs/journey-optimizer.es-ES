---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Funciones compatibles con el editor de personalización
description: Descubra qué funciones del editor de personalización se admiten al personalizar el contenido de la oferta en Gestión de decisiones (Offer Decisioning).
badge: label="Heredado" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
exl-id: c4df41a2-d740-437c-acc3-957508c4a1c0
source-git-commit: c15bae97ea52243d65aa59fdd4e924dc4e1852d8
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 15%

---

# Funciones compatibles con el editor de personalización {#personalization-editor-supported-functions}

En Administración de decisiones, usas el **editor de personalización** al [agregar representaciones](add-representations.md) y personalizar **contenido de ofertas** (imágenes, texto, vínculos en tus ofertas).

El servidor de Offer Decisioning solo admite un **subconjunto** de las funciones disponibles en el editor de personalización al personalizar ese contenido. Esta página enumera todas las funciones que puede utilizar de forma segura en el editor de contenido de ofertas. Expanda cada sección para ver los operadores, los ayudantes y las funciones compatibles.

>[!NOTE]
>
>Esta lista de funciones se aplica **solamente a la personalización del contenido de la oferta** (representaciones). Las reglas de decisión y las fórmulas de clasificación utilizan diferentes editores y no se limitan a este subconjunto.

## Lista de funciones compatibles {#supported-functions-list}

+++ Operadores

* Aritmética: `+` `-` `*` `/` `%`
* Lógico: `and` `or` `!`
* Comparación: `=` `!=` `>` `>=` `<` `<=`

+++

+++ Ayudantes

* Cada
* Con
* Si
* Unless
* Let
* Valor de reserva predeterminado
* fragmento
* datasetLookup
* externalDataLookup (Alpha)
* En línea
* Url
* Metadatos de ejecución
* valueAtPath

+++

+++ Funciones de cadena

| Nombre para mostrar | Nombre interno |
|--------------|---------------|
| Minúsculas | lowerCase |
| Mayúsculas | upperCase |
| Mayúsculas y minúsculas | camelCase |
| Caso de título | titleCase |
| Recortar | trim |
| Recorte izquierdo | leftTrim |
| Recorte derecho | rightTrim |
| Is Empty | isEmpty |
| Ignorar mayúsculas y minúsculas | igual a IgnoreCase |
| No Igual Con Ignorar Mayúsculas y Minúsculas | notEqualWithIgnoreCase |
| Reemplazar | replace |
| Reemplazar todo | replaceAll |
| Concat | concatena |
| División | split |
| Encode64 | encode64 |
| Longitud | length |
| MD5 | md5 |
| SHA256 | sha256 |
| Como | like |
| Comienza por | startsWith |
| No empieza por | doesNotStartWith |
| Termina por | endsWith |
| No termina por | doesNotEndWith |
| Contiene | contains |
| No contiene | doesNotContain |
| Es igual a | igual a |
| No igual a | notEqualTo |
| Coincide | matches |
| Grupo de expresiones regulares | regexGroup |
| Cadena a número | stringToNumber |
| Cadena a fecha | stringToDate |
| A Fecha Hora | toDateTime |
| A Fecha Hora Solamente | toDateTimeOnly |
| Extraer dominio de correo electrónico | extractEmailDomain |
| Extraer nombre de usuario de correo electrónico | extractEmailUsername |
| Is Not Empty | isNotEmpty |
| Índice De | indexOf |
| Último Índice De | lastIndexOf |
| Subcadena | substr |
| A Bool | toBool |
| Cadena a entero | cadena_a_entero |
| Máscara | enmascarar |
| Obtener moneda de formato | formatCurrency |
| Obtener el valor Unicode del carácter | charCodeAt |
| Obtener código Qr para cualquier texto | qrCode |

+++

+++ Funciones de matriz, lista y conjunto

| Nombre para mostrar | Nombre interno |
|--------------|---------------|
| Distinto | distinct |
| Entrada | en |
| No en | notIn |
| Intersecciones | intersecciones |
| Subconjunto de | subsetOf |
| Superconjunto de | supersetOf |
| Incluye | incluye |
| Ordenar y obtener el primer N en la matriz | topN |
| Ordenar y obtener el último N de la matriz | bottomN |
| Primer elemento | dirigir |
| Count | recuento |
| Sum | sum |
| Promedio | media |
| Mínimo | min |
| Máximo | max |

+++

+++ Funciones de asignación

| Nombre para mostrar | Nombre interno |
|--------------|---------------|
| Obtener | get |
| Claves | teclas |
| Valores | values |

+++

+++ Funciones de objeto

| Nombre para mostrar | Nombre interno |
|--------------|---------------|
| Es nulo | isNull |
| No es nulo | isNotNull |

+++

+++ Funciones matemáticas

| Nombre para mostrar | Nombre interno |
|--------------|---------------|
| A Porcentaje | toPercentage |
| Redondear al alza | roundUp |
| Redondear hacia abajo | roundDown |
| A Precisión | toPrecision |
| Absoluta   | absoluto |
| Aleatorio | random |
| A Hexadecimal | toHexString |
| Obtener número a configuración regional | formatNumber |
| A cadena | toString |
| A Int | toInt |
| Demasiado larga | toLong |

+++

+++ Funciones de fecha y hora

| Nombre para mostrar | Nombre interno |
|--------------|---------------|
| Ahora | now |
| Obtener CurrentZonedDateTime | getCurrentZonedDateTime |
| Hasta la fecha | toDate |
| Hasta hora | toTime |
| A Fecha Hora | toDateTime |
| A Fecha Hora Solamente | toDateTimeOnly |
| Solo hasta la fecha | toDateOnly |
| Hasta hora solamente | toTimeOnly |
| A Zona Horaria | toTimeZone |
| Formato de fecha | formatDate |
| Formato de fecha y hora | formatDateTime |
| Formato de hora | formatTime |
| Fecha de análisis | parseDate |
| Analizar fecha y hora | parseDateTime |
| Hora de análisis | parseTime |
| Añadir días | addDays |
| Agregar meses | addMonths |
| Añadir años | addYears |
| Agregar horas | addHours |
| Añadir minutos | addMinutes |
| Añadir segundos | addSeconds |
| Restar días | subtractDays |
| Restar meses | subtractMonths |
| Restar años | subtractYears |
| Restar horas | subtractHours |
| Restar minutos | subtractMinutes |
| Restar segundos | subtractSeconds |
| Diferencia en días | diffDays |
| Diferencia en meses | diffMonths |
| Diferencia en años | diffYears |
| Diferencia en horas | diffHours |
| Diferencia en minutos | diffMinutes |
| Diferencia en segundos | diffSeconds |
| Inicio del día | startOfDay |
| Fin del día | endOfDay |
| Es antes | isBefore |
| Después de | isAfter |

+++

+++ Funciones de URL

| Nombre para mostrar | Nombre interno |
|--------------|---------------|
| Codificar URL | encodeUrl |
| Descodificar URL | decodeUrl |
| Obtener parámetro de consulta de URL | getUrlQueryParam |
| Obtener protocolo de URL | getUrlProtocol |
| Obtener host de URL | getUrlHost |

+++

>[!NOTE]
>
>Si se utiliza una función que no está en la lista anterior al personalizar el contenido de la oferta, la expresión puede fallar durante la ejecución o producir resultados inesperados. Para ver el conjunto completo de funciones disponibles en la personalización de [!DNL Journey Optimizer], consulte [Lista de funciones de ayuda](../../personalization/functions/functions.md). Solo se admite el subconjunto documentado en esta página para personalizar el contenido en Offer Decisioning.
