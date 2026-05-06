---
solution: Journey Optimizer
product: journey optimizer
title: Personalización de direcciones URL en correos electrónicos
description: Conozca las prácticas recomendadas y las limitaciones para generar direcciones URL de forma dinámica a la vez que mantiene el seguimiento fiable
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: url, vínculo, personalización, seguimiento, codificación, llaves
source-git-commit: 36fad8d6c200118210794249fa12263ae70e5422
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 1%

---

# Personalización de direcciones URL en correos electrónicos {#url-personalization}

Las direcciones URL personalizadas le ayudan a entregar experiencias contextuales a través de sus mensajes de correo electrónico de [!DNL Journey Optimizer], como la generación de vínculos específicos del destinatario o la adición de parámetros dinámicos.

Llevan a los destinatarios a páginas específicas de un sitio web o a un micrositio personalizado, según los atributos del perfil.

## Personalización de una URL {#personalize-url}

Para personalizar una URL, siga los pasos a continuación.

1. En el Designer de correo electrónico, seleccione un elemento en el contenido e [inserte un vínculo](message-tracking.md#insert-links) mediante la barra de herramientas contextual.

   >[!IMPORTANT]
   >
   >Personalization solo está disponible para **[!UICONTROL vínculo externo]**, **[!UICONTROL vínculo de baja]** y **[!DNL Opt-Out]**. Asegúrese de seleccionar un tipo de vínculo adecuado.

1. Seleccione el icono de personalización.

   ![](assets/message-tracking-insert-link-perso.png)

1. Utilice el editor de personalización para añadir los atributos de perfil con los que desea personalizar la URL.

1. Guarde los cambios.

Estos son algunos ejemplos de direcciones URL personalizadas:

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!NOTE]
>
>Al editar una URL personalizada en el editor de personalización, las funciones de ayuda y la pertenencia a audiencias se desactivan por motivos de seguridad.
>
>No se admiten espacios en los tokens de personalización utilizados dentro de las direcciones URL.

Para un procesamiento y seguimiento confiables, siga las [prácticas recomendadas y protecciones](#best-practices) a continuación.

## Personalizar una dirección URL completa/base {#personalize-complete-base-url}

Journey Optimizer también admite la personalización de la dirección URL **entera** o del **dominio base** de una dirección URL, por ejemplo:

```html
<a href="{{profile.social.link}}" />
<a href="{{profile.social.baseUrl}}/profile" />
<a href="https://{{profile.social.baseUrl}}/profile" />
```

>[!IMPORTANT]
>
>Para habilitar la personalización completa o básica de la URL, póngase en contacto con Adobe y proporcione su lista de dominios aceptados. Esto es necesario para evitar redirecciones no seguras.

## Personalizar parámetros de seguimiento de URL {#personalize-url-tracking-parameters}

[El seguimiento de URL](url-tracking.md) se administra en el nivel de configuración de canal y se aplica a todas las URL incluidas en el contenido del mensaje. También puede personalizar los parámetros de seguimiento de URL para un vínculo individual en el Designer de correo electrónico. Esto permite anexar un parámetro específico del destinatario a un único vínculo (por ejemplo, para pasar un identificador a las herramientas de análisis web).

Para ello, [inserte un vínculo](message-tracking.md#insert-links), seleccione el icono de personalización, agregue el parámetro de seguimiento de URL y seleccione el atributo de perfil que desee en [editor de personalización](../personalization/personalization-build-expressions.md).

![](assets/message-tracking-perso-parameter.png)

Repita los pasos anteriores para cada vínculo al que desee agregar este parámetro de seguimiento.

Ahora, cuando se envía el correo electrónico, este parámetro se anexa automáticamente al final de la dirección URL. A continuación, puede capturar este parámetro en las herramientas de análisis web o en los informes de rendimiento.

>[!NOTE]
>
>Para comprobar la dirección URL final, puede [enviar una prueba](../content-management/proofs.md) y hacer clic en el vínculo del contenido del correo electrónico una vez que reciba la prueba. La dirección URL debe mostrar el parámetro de seguimiento. Por ejemplo: <https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>

## Prácticas recomendadas y protecciones {#best-practices}

Para mantener los vínculos válidos, en los que se puede hacer clic y rastreables, siga las prácticas recomendadas y las protecciones a continuación.

### Llaves para URL dinámicas {#use-braces}

Al insertar una dirección URL que contenga personalización, utilice tres llaves (`{{{ ... }}}`) para la parte dinámica de la dirección URL. Esto evita que el escape modifique los caracteres especiales (por ejemplo, `/` y `+`) y ayuda a evitar direcciones URL rotas, redirecciones incorrectas o problemas de seguimiento.

Vea el siguiente ejemplo:

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>El uso de la salida sin procesar (`{{{ ... }}}`) significa que el valor se inserta tal cual. Utilícelo únicamente con valores en los que confíe y que estén pensados para ser seguros para URL (por ejemplo, valores que genere o valide en sentido ascendente).

### Seguimiento de URL correcto {#enable-url-tracking}

* Cuando utilice la personalización para generar la dirección URL, asegúrese de que el valor resuelto comience por `http`/`https` para cada destinatario. De lo contrario, es posible que no se aplique el seguimiento y que el vínculo no se comporte como se espera.

* No utilice lógica dinámica como instrucciones `let`, `each` o `if` directamente en el campo URL del editor de personalización. Están desactivados por motivos de seguridad.

* Si su escenario implica una lógica compleja para generar direcciones URL personalizadas, evite colocar esa lógica directamente en el campo URL del editor de personalización. En su lugar:
   * Añada la lógica y las instrucciones necesarias en el contenido de HTML encima o cerca del campo URL.
   * Genere y almacene atributos personalizados por separado y, a continuación, haga referencia a ellos en el contenido del correo electrónico.

### Codificación y longitud de URL {#encoding}

* Las reglas de sintaxis de URI ([estándar RFC 3986](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}) se aplican a todas las direcciones URL del contenido del correo electrónico. Sin embargo, es más probable que las direcciones URL personalizadas aparezcan problemas de codificación, ya que los valores específicos del destinatario pueden introducir caracteres reservados (por ejemplo, en parámetros de consulta). Por lo tanto, asegúrese de que los valores dinámicos tengan codificación de dirección URL (especialmente espacios, `&`, `#`, `%` y `+`) y evite usar `+` para los valores de consulta.

* Los exploradores, los clientes de correo o los sistemas descendentes pueden truncar o rechazar las direcciones URL muy largas. Por ejemplo, las direcciones URL de páginas espejo pueden crecer significativamente cuando la personalización en tiempo de ejecución es intensiva. Mantenga las cargas personalizadas pequeñas y evite incrustar objetos grandes en las direcciones URL.

### Pasos de validación recomendados {#validation}

Antes de activar un recorrido o una campaña, siga las recomendaciones siguientes:

* Envíe una [revisión](../content-management/proofs.md) y haga clic en los vínculos para confirmar que la dirección URL resuelta comienza por `http`/`https` y mantiene la estructura esperada.
* Si se adjuntan parámetros de seguimiento, confirme que la dirección URL final los incluye (ya sea mediante el seguimiento de URL en el nivel de configuración o mediante parámetros de seguimiento por vínculo).

