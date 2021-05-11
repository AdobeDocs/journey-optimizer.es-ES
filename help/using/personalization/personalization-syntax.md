---
title: Sintaxis de personalización
description: Aprenda a utilizar la sintaxis de personalización
translation-type: tm+mt
source-git-commit: 568b37f0bbcb663cf7062f26b90d57d89452e862
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 3%

---

# Sintaxis de personalización {#personalization-syntax}

![](../assets/do-not-localize/badge.png)

## Introducción

La personalización en Journey Optimizer se basa en la sintaxis de plantilla denominada Handlebars.
Para obtener una descripción completa de la sintaxis de Handlebars, consulte [HandlebarsJS](https://handlebarsjs.com/).

Utiliza una plantilla y un objeto de entrada para generar HTML u otros formatos de texto. Las plantillas de Handlebars tienen el aspecto de texto normal con expresiones de Handlebars incrustadas.

Ejemplo de expresión simple:

```
{{profile.person.name}}
```

donde:

* **** es un área de nombres.
* **person.** name es un token compuesto por atributos. La estructura de atributos se define en un esquema Adobe Experience Platform XDM. [Más información](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es).

## Reglas generales de sintaxis

Los identificadores pueden ser cualquier carácter Unicode excepto los siguientes:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

La sintaxis distingue entre mayúsculas y minúsculas.

Las palabras **true**, **false**, **null** y **undefined** solo están permitidas en la primera parte de una expresión de ruta.

En Handlebars, los valores devueltos por {{expression}} son **HTML-escaped**. Si la expresión contiene &amp;, la salida de escape de HTML devuelta se genera como &amp;. Si no desea que Handlebars escape un valor, utilice el &quot;triple stash&quot;.

## Perfil

Este espacio de nombres le permite hacer referencia a todos los atributos definidos en el esquema de perfil descrito en la documentación del [Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

Los atributos deben definirse en el esquema antes de hacer referencia a ellos en un bloque personalizado de Journey Optimizer.

Todas las referencias se validan con el esquema de perfil con un mecanismo de validación descrito [aquí](personalization-validation.md).

**Referencias de muestra:**

* ```{{profile.person.name.fullName}}```
* ```{{profile.person.name.firstName}}```
* ```{{profile.person.gender}}```
* ```{{profile.personalEmail.address}}```
* ```{{profile.mobilePhone.number}}```
* ```{{profile.homeAddress.city}}```
* ```{{profile.faxPhone.number}}```

**Determine la extensión** de la dirección de correo electrónico:

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
{%else if contains(profile.personalEmail.address, ".org")%}
<a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
{%else%}
<a href="https://www.adobe.com/users">Checkout our page</a>
{%/if%}
```

## Segmentos

Para obtener más información sobre segmentación y servicio de segmentación, consulte esta [sección](../segment/about-segments.md).

**Representar contenido diferente en función de la pertenencia a segmentos**:

```
{%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
  Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
{%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
  Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
{%/if%}
```

**Determine si un perfil ya es miembro**:

```
{%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
    You're a member!
{%else%}
    You should be a member! Sign up now!
{%/if%}
```

## Ofertas

Este espacio de nombres le permite hacer referencia a las decisiones de ofertas existentes.
Para hacer referencia a una oferta, debe declarar una ruta con la información diferente que define una oferta.

Esta ruta tiene la siguiente estructura:
0 - &quot;ofertas&quot; : identifica la expresión de ruta que pertenece al espacio de nombres de la oferta
1 - Tipo : determina el tipo de representación de la oferta. Los valores válidos son &#39;image&#39;, &#39;html&#39; y &#39;text&#39;
2 - Id De Ubicación
3: ID de actividad
4 - Ofrezca atributos específicos. Se pueden utilizar los atributos compatibles en función del tipo de oferta. Por ejemplo, para imágenes `deliveryUrl`.

Para obtener más información sobre la API de Decisiones, consulte esta [página](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#deliver-offers-using-the-decisions-api)

Para obtener más información sobre la Representación de ofertas, consulte esta [página](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#accept-and-content-type-headers).

Todas las referencias se validan con el Esquema de ofertas con un mecanismo de validación descrito [aquí](personalization-validation.md).

**Referencias de muestra:**

* Ubicación en la que se aloja la imagen:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl```

* Dirección URL de destino cuando haga clic en la imagen:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl```

* Contenido de texto de la oferta procedente del motor de toma de decisiones:

```offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```

* Contenido HTML de la oferta procedente del motor de toma de decisiones:

```offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```


## Ayudantes

Un asistente de Handlebars es un identificador simple que puede ir seguido de parámetros.
Cada parámetro es una expresión Handlebars. Se puede acceder a estos asistentes desde cualquier contexto en una plantilla.

Estos ayudantes de bloque se identifican con un # antes del nombre del ayudante y requieren un / de cierre coincidente, del mismo nombre.
Los bloques son expresiones que tienen una apertura de bloque ({{# }}) y un cierre ({{/}}).

### Si

El asistente **if** se utiliza para definir un bloque condicional.
Si la evaluación de la expresión devuelve el valor &quot;True&quot;, el bloque se procesa; de lo contrario, se omite.

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Después del asistente **if**, puede introducir una instrucción **else** para especificar un bloque de código que se ejecutará, si la misma condición es falsa.
La sentencia **else if** especificará una nueva condición para comprobar si la primera sentencia devuelve el valor false.

**Representar diferentes vínculos de tienda basados en expresiones** condicionales:

```
{%#if profile.homeAddress.countryCode = "FR"%}
  <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
{%else%}
  <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
{%/if%}
```

### Except

**#** unlesshelper se utiliza para definir un bloque condicional. Por oposición al asistente **#if**, si la evaluación de la expresión devuelve false, se procesa el bloque.

**Representar contenido basado en la extensión** de dirección de correo electrónico:

```
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

### Cada

El asistente **each** se utiliza para iterar sobre una matriz.
La sintaxis del asistente es ```{{#each ArrayName}}``` YourContent {{/each}}
Podemos hacer referencia a los elementos individuales de la matriz utilizando la palabra clave **this** dentro del bloque . El índice del elemento de la matriz se puede representar utilizando {{@index}}.

Ejemplo:

```
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

```
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Representar una lista de productos que este usuario tiene en el carro de compras**:

```
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

### con

El asistente **#with** se utiliza para cambiar el token de evaluación de la parte de plantilla.

Ejemplo:

```
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

El asistente **#with** también es útil para definir una variable de acceso directo.

**Se utiliza con para alinear nombres de variables largos con nombres de variables más cortos**:

```
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```


## Limitaciones

* El uso de la variable **xEvent** no está disponible en las expresiones de personalización. Cualquier referencia a xEvent producirá errores de validación.
