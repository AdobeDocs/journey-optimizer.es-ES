---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxis de personalización
description: Aprenda a utilizar la sintaxis de personalización.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: expresión, editor, sintaxis, personalización
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 50eff8b6c4aaa432595bf16ef1d567c272d6b084
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 3%

---

# Sintaxis de personalización {#personalization-syntax}

Personalization en [!DNL Journey Optimizer] se basa en la sintaxis de creación de plantillas denominada Handlebars. Para obtener una descripción completa de la sintaxis de Handlebars, consulte [Documentación de HandlebarsJS](https://handlebarsjs.com/).

Utiliza una plantilla y un objeto de entrada para generar HTML u otros formatos de texto. Las plantillas Handlebars se parecen al texto normal con expresiones Handlebars incrustadas.

Ejemplo de expresión simple:

`{{profile.person.name}}`

donde:

* `profile` es un área de nombres.
* `person.name` es un token compuesto por atributos. La estructura de atributos se define en un esquema XDM de Adobe Experience Platform. [Más información](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

## Sintaxis: reglas generales {#general-rules}

* Los identificadores pueden ser cualquier carácter Unicode excepto los siguientes:

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* La sintaxis distingue entre mayúsculas y minúsculas.

* Las palabras **true**, **false**, **null** y **undefined** solo se permiten en la primera parte de una expresión de ruta.

* En Handlebars, los valores devueltos por {{expression}} son **HTML-escaped**. Si la expresión contiene `&`, el resultado devuelto con escape de HTML se generará como `&amp;`. Si no desea que Handlebars escape un valor, utilice la &quot;pila triple&quot;.

  Supongamos que el valor del campo `profile.person.name` es &quot;Mark &amp; Mary&quot;. La sintaxis `{{profile.person.name}}` mostrará `Mark &amp; Mary`, mientras que `{{{profile.person.name}}}` mostrará `Mark & Mary`.

* En cuanto a los argumentos de funciones literales, el analizador de idioma de creación de plantillas no admite un único símbolo de barra invertida sin escape (`\`). Este carácter debe tener un carácter de escape con una barra invertida (`\`) adicional. Ejemplo :

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## Áreas de nombres disponibles {#namespaces}

* **Perfil**

  Este espacio de nombres le permite hacer referencia a todos los atributos definidos en el esquema de perfil descrito en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

  Es necesario definir los atributos en el esquema antes de hacer referencia a ellos en un bloque personalizado [!DNL Journey Optimizer].

  Para obtener más información sobre cómo aprovechar los atributos de perfil en condiciones, consulte [esta sección](functions/helpers.md#if-function).

  +++Referencias de muestra

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * `{{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

  +++

* **Audiencia**

  Para obtener más información sobre el servicio de segmentación, consulte [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=es){target="_blank"}.

* **Ofertas**

  Este área de nombres le permite hacer referencia a decisiones de ofertas existentes.

  Para hacer referencia a una oferta, debe declarar una ruta con la diferente información que define una oferta. Esta ruta tiene la siguiente estructura:

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  donde:

   * `offers` identifica la expresión de ruta que pertenece al área de nombres de la oferta
   * `Type` determina el tipo de representación de la oferta. Los valores posibles son: `image`, `html` y `text`
   * `Placement Id` y `Activity Id` son identificadores de ubicación y actividad
   * `Attributes` son atributos específicos de la oferta que dependen del tipo de oferta. Ejemplo: `deliveryUrl` para imágenes

  Para obtener más información sobre la API Decisions y las representaciones Offer, consulte [esta página](../offers/api-reference/offer-delivery-api/decisioning-api.md)

  Todas las referencias se validan con el esquema de ofertas con un mecanismo de validación descrito en [esta página](../personalization/personalization-build-expressions.md)

  +++Referencias de muestra

   * Ubicación donde se aloja la imagen:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * URL de destino al hacer clic en la imagen:

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * Contenido de texto de la oferta procedente del motor de decisión:

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * Contenido de HTML de la oferta proveniente del motor de decisión:

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

  +++

## Ayudantes{#helpers-all}

Un asistente de Handlebars es un identificador simple que puede ir seguido de parámetros. Cada parámetro es una expresión Handlebars. Se puede acceder a estos ayudantes desde cualquier contexto de una plantilla.

Estos ayudantes de bloque se identifican con un `#` antes del nombre del ayudante y requieren un `/` de cierre coincidente, del mismo nombre.

Los bloques son expresiones que tienen un bloque de apertura (`{{# }}`) y cierre (`{{/}}`).

Para obtener más información sobre las funciones de ayuda, consulte [esta sección](functions/helpers.md).

## Tipos literales {#literal-types}

[!DNL Adobe Journey Optimizer] admite los siguientes tipos literales:

| Literal | Definición |
| ------- | ---------- |
| Cadena | Un tipo de datos compuesto por caracteres entre comillas dobles. <br>Ejemplos: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Un tipo de datos que puede ser verdadero o falso. |
| Entero | Un tipo de datos que representa un número entero. Puede ser positivo, negativo o cero. <br>Ejemplos: `-201`, `0`, `412` |
| Matriz | Un tipo de datos que se comprende como un grupo de otros valores literales. Utiliza corchetes para agrupar y comas para delimitar entre distintos valores. <br> **Nota:** No puede tener acceso directo a las propiedades de los elementos de una matriz. <br> ejemplos: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>El uso de la variable **xEvent** no está disponible en expresiones de personalización. Cualquier referencia a xEvent producirá errores de validación.
