---
solution: Journey Optimizer
product: journey optimizer
title: Sintaxis de personalización
description: Aprenda a utilizar la sintaxis de personalización.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor, sintaxis, personalización
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 10%

---

# Sintaxis de personalización {#personalization-syntax}

Personalización en [!DNL Journey Optimizer] se basa en la sintaxis de creación de plantillas denominada Handlebars.
Para obtener una descripción completa de la sintaxis de Handlebars, consulte [Documentación de HandlebarsJS](https://handlebarsjs.com/).

Utiliza una plantilla y un objeto de entrada para generar HTML u otros formatos de texto. Las plantillas Handlebars se parecen al texto normal con expresiones Handlebars incrustadas.

Ejemplo de expresión simple:

`{{profile.person.name}}`

donde:

* `profile` es un área de nombres.
* `person.name` es un token compuesto por atributos. La estructura de atributos se define en un esquema XDM de Adobe Experience Platform. [Más información](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

## Sintaxis: reglas generales {#general-rules}

Los identificadores pueden ser cualquier carácter Unicode excepto los siguientes:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

La sintaxis distingue entre mayúsculas y minúsculas.

Las palabras **true**, **false**, **null** y **indefinido** solo se permiten en la primera parte de una expresión de ruta.

En Handlebars, los valores devueltos por el {{expression}} son **escapado por el HTML**. Si la expresión contiene `&`, la salida devuelta con escape de HTML se genera como `&amp;`. Si no desea que Handlebars escape un valor, utilice la &quot;pila triple&quot;.

En cuanto a los argumentos de funciones literales, el analizador de lenguajes de plantilla no admite una sola barra invertida sin escape (`\`símbolo ). Este carácter debe tener una barra invertida adicional (`\`símbolo ). Por ejemplo :

`{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## Perfil

Este área de nombres le permite hacer referencia a todos los atributos definidos en el esquema de perfil descrito en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.

Los atributos deben definirse en el esquema antes de que se haga referencia a ellos en una [!DNL Journey Optimizer] bloque de personalización.

>[!NOTE]
>
>Aprenda a aprovechar los atributos de perfil en condiciones en [esta sección](functions/helpers.md#if-function).

**Referencias de muestra:**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## Audiencias{#perso-segments}

Aprenda a aprovechar los atributos de perfil en condiciones en [esta sección](functions/helpers.md#if-function).

>[!NOTE]
>Para obtener más información sobre el servicio de segmentación, consulte [esta documentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=es){target="_blank"}.

## Ofertas {#offers-syntax}

Este área de nombres le permite hacer referencia a decisiones de ofertas existentes.
Para hacer referencia a una oferta, debe declarar una ruta con la diferente información que define una oferta.

Esta ruta tiene la siguiente estructura:

`offers.Type.[Placement Id].[Activity Id].Attribute`

donde:

* `offers` identifica la expresión de ruta que pertenece al área de nombres de la oferta
* `Type`  determina el tipo de representación de la oferta. Los valores posibles son: `image`, `html` y `text`
* `Placement Id` y `Activity Id` son identificadores de ubicación y actividad
* `Attributes` son atributos específicos de la oferta que dependen del tipo de oferta. Ejemplo: `deliveryUrl` para imágenes

Para obtener más información sobre la API Decisions y la Representación de ofertas, consulte [esta página](../offers/api-reference/offer-delivery-api/decisioning-api.md)

Todas las referencias se validan con el esquema de ofertas con un mecanismo de validación descrito en [esta página](personalization-validation.md)

**Referencias de muestra:**

* Ubicación donde se aloja la imagen:

  `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* URL de destino al hacer clic en la imagen:

  `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Contenido de texto de la oferta procedente del motor de decisión:

  `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* Contenido del HTML de la oferta procedente del motor de decisión:

  `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Ayudantes{#helpers-all}

Un asistente de Handlebars es un identificador simple que puede ir seguido de parámetros.
Cada parámetro es una expresión Handlebars. Se puede acceder a estos ayudantes desde cualquier contexto de una plantilla.

Estos ayudantes de bloque se identifican con un número que precede al nombre del ayudante y requieren un / de cierre coincidente, del mismo nombre.
Los bloques son expresiones que tienen una apertura de bloque ({{# }}) and closing ({{/}}).


>[!NOTE]
>
>Las funciones de ayuda se detallan en [esta sección](functions/helpers.md).
>

## Tipos literales {#literal-types}

[!DNL Adobe Journey Optimizer] admite los siguientes tipos literales:

| Literal | Definición |
| ------- | ---------- |
| Cadena | Un tipo de datos compuesto por caracteres entre comillas dobles. <br>Ejemplos: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Un tipo de datos que puede ser verdadero o falso. |
| Número entero | Un tipo de datos que representa un número entero. Puede ser positivo, negativo o cero. <br>Ejemplos: `-201`, `0`, `412` |
| Matriz | Un tipo de datos que se comprende como un grupo de otros valores literales. Utiliza corchetes para agrupar y comas para delimitar entre distintos valores. <br> **Nota:** No puede acceder directamente a las propiedades de los elementos de una matriz. <br> Ejemplos: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>El uso de **xEvent** no está disponible en expresiones de personalización. Cualquier referencia a xEvent producirá errores de validación.

## Personalización de URL{#perso-urls}

Las direcciones URL personalizadas llevan a los destinatarios a páginas específicas de un sitio web o a un micrositio personalizado, según los atributos del perfil. En Adobe Journey Optimizer, puede añadir personalización a las direcciones URL en el contenido del mensaje. La personalización de URL se puede aplicar a texto e imágenes, y puede utilizar datos de perfil o datos contextuales.

Journey Optimizer le permite personalizar una o varias direcciones URL del mensaje añadiéndoles campos de personalización. Para personalizar una URL, siga los pasos a continuación:

1. Cree un vínculo en el contenido del mensaje. [Más información](../email/message-tracking.md#insert-links)
1. En el icono de personalización, seleccione los atributos. El icono de personalización solo está disponible para estos tipos de vínculos: **Vínculo externo**, **Vínculo de baja** y **Opción de exclusión**.

   ![](assets/perso-url.png)

>[!NOTE]
>
>En el editor de expresiones, cuando se edita una dirección URL personalizada, las funciones de ayuda y la pertenencia a audiencias se desactivan por motivos de seguridad.
>

**URL personalizadas de ejemplo**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>No se admiten espacios en los tokens de personalización utilizados dentro de las direcciones URL.
