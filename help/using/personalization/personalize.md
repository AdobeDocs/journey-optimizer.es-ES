---
title: Personalización del contenido en Journey Optimizer
description: Introducción a la personalización
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 7be83409f7a594747963c5b125f3bf96c0b4f8b6
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 18%

---

# Introducción a la personalización{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] funcionalidades de personalización para adaptar los mensajes a cada destinatario específico aprovechando los datos y la información que tiene sobre ellos. Puede ser su nombre, intereses, dónde viven, qué compraron, etc.

➡️ [Aprenda a personalizar un mensaje en estos vídeos](#video-perso)

[!DNL Journey Optimizer] utiliza una sintaxis de personalización **en línea** sencilla basada en Handlebars, que le permite crear expresiones con contenido entre llaves dobles **{{}}**. Puede añadir varias expresiones en el mismo contenido o campo sin restricciones. Obtenga más información en [Sintaxis de personalización](personalization-syntax.md).

La personalización se basa en los datos de perfil que administra el esquema **Perfil individual de XDM** definido en Adobe Experience Platform. Obtenga más información en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target=&quot;_blank&quot;}.

>[!CAUTION]
>La variable **Perfil individual XDM** schema es el único esquema que puede utilizar para personalizar el contenido en [!DNL Journey Optimizer].

**Ejemplos:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Al procesar el mensaje (correo electrónico y push), Journey Optimizer reemplaza la expresión por los datos contenidos en la base de datos de Experience Cloud Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` se convierte en &quot;Hello John Doe&quot;.


## Contextos de personalización{#personalization-areas}

El contenido y la visualización de los mensajes enviados por [!DNL Journey Optimizer] se puede personalizar de varias formas.

En todos los campos con el icono del editor, puede abrir el editor de personalización (también conocido como Editor de expresiones) y definir la personalización.

![](assets/perso_icon.png)

### Personalización de los correos electrónicos

Al crear un correo electrónico, puede añadir personalización en la variable **[!UICONTROL Subject line]** del mensaje.

![](assets/perso_subject.png)

En el Diseñador de correo electrónico, puede personalizar el contenido:

* En el **message**: haga clic dentro de un bloque de texto y haga clic en el botón **Personalizar** en la barra de herramientas contextual y seleccione **Insertar personalización** campo . Para obtener más información sobre la interfaz del Diseñador de correo electrónico, consulte esta [sección](../design-emails.md).

   ![](assets/perso_insert.png)

* Para un **vínculo**: seleccione texto o imagen dentro de un bloque de texto, haga clic en el botón **Insertar vínculo** de la barra de herramientas contextual. En la ventana , puede añadir un bloque personalizado haciendo clic en el botón **Añadir personalización** icono.

   ![](assets/perso_link.png)

En ambos casos, se accede al editor de personalización.

![](assets/perso_ee.png)

### Personalización de las notificaciones push

También puede personalizar su **Notificaciones push** en los campos siguientes:

* **Título**
* **Cuerpo**
* **Sonido personalizado**
* **Distintivos**
* **Datos personalizados**

![](assets/perso_push.png)

Obtenga más información sobre la configuración de notificaciones push en [esta sección](../push-gs.md).

### Personalización de las ofertas {#personalize-offers}

También puede acceder al editor de personalización cuando añada contenido de tipo texto a las representaciones de sus ofertas.

Obtenga más información sobre la administración de contenido con la gestión de decisiones en [esta sección](../offers/offer-library/creating-personalized-offers.md#custom-text).

## Uso del Editor de expresiones {#use-expression-editor}

El editor de expresiones es la parte central de la personalización en [!DNL Journey Optimizer].

Está disponible en todos los contextos en los que es necesario definir la personalización como correos electrónicos, mensajes push y ofertas.

En la interfaz del editor de expresiones, se seleccionan, organizan, personalizan y validan todos los datos para crear una personalización personalizada para el contenido.

![](assets/perso_ee1.png)

La parte izquierda de la pantalla muestra un selector de dominio que le permite seleccionar el origen de la personalización.

![](assets/perso_ee3.png)

Las fuentes disponibles son:

* **[!UICONTROL Profile attributes]** : enumera todas las referencias asociadas al esquema de perfil descrito en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Segment memberships]** : enumera todos los segmentos creados en el servicio de segmentación de Adobe Experience Platform. Más información sobre segmentación disponible [here](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Offer decisions]** : enumera todas las ofertas asociadas a una ubicación específica. Seleccione la ubicación e inserte las ofertas en el contenido. Para obtener una documentación completa sobre cómo administrar ofertas, consulte [esta sección](../deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** : cuando la variable **Mensaje** se utiliza en un recorrido, los campos de recorrido contextual están disponibles a través de este menú. Obtenga más información en [esta sección](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : enumera todas las funciones de ayuda disponibles para realizar operaciones con datos, como cálculos, formato de datos o conversiones, condiciones y manipularlas en el contexto de la personalización. Obtenga más información en [esta sección](functions/functions.md).

Al seleccionarla, la referencia se añade en el editor.

>[!NOTE]
>
>El icono de información situado junto al icono &quot;+&quot; abre una información sobre herramientas que proporciona más detalles para cada variable.

En el siguiente ejemplo, el editor de expresiones permite seleccionar los perfiles que tienen su cumpleaños hoy y luego completar la personalización insertando una oferta específica correspondiente a este día.

![](assets/perso_ee2.png)

## Vídeotutoriales{#video-perso}

Aprenda a utilizar la información de evento contextual de un recorrido para personalizar un mensaje.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Aprenda a utilizar la información de evento contextual de un recorrido para personalizar un mensaje.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
