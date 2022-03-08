---
title: Sintaxis de personalización
description: Aprenda a utilizar la sintaxis de personalización.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 5%

---

# Sintaxis de personalización {#personalization-syntax}

Personalización en [!DNL Journey Optimizer] se basa en la sintaxis de plantilla denominada Handlebars.
Para obtener una descripción completa de la sintaxis de Handlebars, consulte [Documentación de HandlebarsJS](https://handlebarsjs.com/).

Utiliza una plantilla y un objeto de entrada para generar un HTML u otros formatos de texto. Las plantillas de Handlebars tienen el aspecto de texto normal con expresiones de Handlebars incrustadas.

Ejemplo de expresión simple:

`{{profile.person.name}}`

dónde:

* `profile` es un área de nombres.
* `person.name` es un token compuesto por atributos. La estructura de atributos se define en un esquema Adobe Experience Platform XDM. [Más información](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target=&quot;_blank&quot;}.

## Reglas generales de sintaxis {#general-rules}

Los identificadores pueden ser cualquier carácter Unicode excepto los siguientes:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

La sintaxis distingue entre mayúsculas y minúsculas.

Las palabras **true**, **false**, **null** y **undefined** solo se permiten en la primera parte de una expresión de ruta.

En Handlebars, los valores devueltos por {{expression}} son **HTML escapado**. Si la expresión contiene `&`, la salida de escape del HTML que se devuelve se genera como `&amp;`. Si no desea que Handlebars escape un valor, utilice el &quot;triple stash&quot;.

## Perfil

Este espacio de nombres le permite hacer referencia a todos los atributos definidos en el esquema de perfil descrito en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

Los atributos deben definirse en el esquema antes de hacer referencia a ellos en un [!DNL Journey Optimizer] bloque personalizado.

>[!NOTE]
>
>Aprenda a aprovechar los atributos de perfil en condiciones de [esta sección](functions/helpers.md#if-function).

**Referencias de muestra:**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## Segmentos{#perso-segments}

Aprenda a aprovechar los atributos de perfil en condiciones de [esta sección](functions/helpers.md#if-function).

>[!NOTE]
>Para obtener más información sobre segmentación y servicio de segmentación, consulte [esta sección](../segment/about-segments.md).

## Ofertas {#offers-syntax}

Este espacio de nombres le permite hacer referencia a las decisiones de ofertas existentes.
Para hacer referencia a una oferta, debe declarar una ruta con la información diferente que define una oferta.

Esta ruta tiene la siguiente estructura:

`offers.Type.[Placement Id].[Activity Id].Attribute`

dónde:

* `offers` identifica la expresión de ruta que pertenece al espacio de nombres de la oferta
* `Type`  determina el tipo de representación de la oferta. Los valores posibles son: `image`, `html` y `text`
* `Placement Id` y `Activity Id` son identificadores de ubicación y actividad
* `Attributes` son atributos específicos de oferta que dependen del tipo de oferta. Ejemplo: `deliveryUrl` para imágenes

Para obtener más información sobre la API de decisiones y sobre la representación de ofertas, consulte [esta página](../../using/offers/api-reference/decisions-api/deliver-offers.md)

Todas las referencias se validan con el esquema de ofertas con un mecanismo de validación descrito en [esta página](personalization-validation.md)

**Referencias de muestra:**

* Ubicación en la que se aloja la imagen:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* Dirección URL de destino cuando haga clic en la imagen:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Contenido de texto de la oferta procedente del motor de toma de decisiones:

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* contenido del HTML de la oferta procedente del motor de toma de decisiones:

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Ayudantes{#helpers-all}

Un asistente de Handlebars es un identificador simple que puede ir seguido de parámetros.
Cada parámetro es una expresión Handlebars. Se puede acceder a estos asistentes desde cualquier contexto en una plantilla.

Estos ayudantes de bloque se identifican con un # que precede al nombre del ayudante y requieren un / de cierre coincidente, del mismo nombre.
Los bloques son expresiones que tienen una apertura de bloque ({{# }}) y cierre ({/}}).


>[!NOTE]
>
>Las funciones de ayuda se detallan en [esta sección](functions/helpers.md).

## Tipos literales {#literal-types}

[!DNL Adobe Journey Optimizer] admite los siguientes tipos de literales:

| Literal | Definición |
| ------- | ---------- |
| Cadena | Tipo de datos compuesto por caracteres entre comillas dobles. <br>Ejemplos: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Tipo de datos verdadero o falso. |
| Número entero | Un tipo de datos que representa un número entero. Puede ser positivo, negativo o cero. <br>Ejemplos: `-201`, `0`, `412` |
| Matriz | Tipo de datos que se compone como grupo de otros valores literales. Utiliza corchetes para agrupar y comas para delimitar entre valores diferentes. <br> **Nota:** No se puede acceder directamente a las propiedades de los elementos de una matriz. <br> Ejemplos: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>El uso de **xEvent** no está disponible en expresiones de personalización. Cualquier referencia a xEvent producirá errores de validación.

## Personalización de URL{#perso-urls}

Journey Optimizer le permite personalizar una o varias direcciones URL en el mensaje al agregarles campos de personalización. Para ello:

* Cree un vínculo en el contenido de correo electrónico o push. Para obtener más información sobre la creación de vínculos, consulte [esta página](../messages/message-tracking.md#insert-links).
* Haga clic en el icono de personalización. Este icono está disponible para estos tipos específicos de vínculos: **Vínculo externo**, **Vínculo de baja** y **Exclusión**.

![](assets/perso-url.png)

>[!NOTE]
>
>En el editor de expresiones, al editar una URL personalizada, las funciones de ayuda y la pertenencia a segmentos se desactivan por motivos de seguridad.

**URL personalizadas de ejemplo**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>Los espacios no se admiten en los tokens de personalización utilizados dentro de las direcciones url.
