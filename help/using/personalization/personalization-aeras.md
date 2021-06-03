---
title: Contextos de personalización en Journey Optimizer
description: Descubra en qué contextos puede añadir personalización
source-git-commit: 741fe2b614e3ded57c4a7ecd9b7333bdd99ab359
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 3%

---

# Herramienta y contexto de personalización {#personalization-areas}

![](../assets/do-not-localize/badge.png)

El contenido y la visualización de los mensajes que entrega Journey Optimizer se pueden personalizar de varias formas diferentes.

Todos los campos asociados con el icono del editor pueden abrir el editor de personalización y recibir contenido de personalización.

![](assets/perso_icon.png)

## Personalización de los correos electrónicos

Al crear un correo electrónico, puede añadir una personalización en el campo **Email subject** del mensaje.

![](assets/perso_subject.png)

En el Diseñador de correo electrónico, puede personalizar el contenido:

* En el **mensaje**: haga clic dentro de un bloque de texto, haga clic en el icono **Personalizar** de la barra de herramientas contextual y seleccione el campo **Insertar personalización**. Para obtener más información sobre la interfaz del Diseñador de correo electrónico, consulte esta [sección](../design-emails.md).

   ![](assets/perso_insert.png)

* Para un **enlace**: seleccione texto o imagen dentro de un bloque de texto, haga clic en el icono **Insert link** de la barra de herramientas contextual. En la ventana , puede añadir un bloque personalizado haciendo clic en el icono **Add personalization**.

   ![](assets/perso_link.png)

## Personalización de notificaciones push

También puede personalizar sus **Push notifications** en los campos siguientes:

* **Título**
* **Cuerpo**
* **Sonido personalizado**
* **Distintivos**
* **Datos personalizados**

![](assets/perso_push.png)

Obtenga más información sobre la configuración de notificaciones push en [esta sección](../create-push.md).

## Uso del editor de expresiones

El editor de expresiones es la parte central de la personalización en Journey Optimizer.

Está disponible en todos los contextos en los que es necesario definir la personalización como correos electrónicos, mensajes push y ofertas.

En la interfaz del editor de expresiones, se seleccionan, organizan, personalizan y validan todos los datos para crear una personalización personalizada para el contenido.

![](assets/perso_ee1.png)

La parte izquierda de la pantalla muestra un selector de dominio que le permite seleccionar el origen de la personalización.

* **Perfil** : enumera todas las referencias asociadas al esquema de perfil que se describen en la documentación [ del Modelo de datos de ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es)Adobe Experience Platform (XDM).
* **Pertenencia a segmentos** : enumera todos los segmentos creados en el servicio de segmentación de Adobe Experience Platform. Más información sobre la segmentación disponible [aquí](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)
* **Ofertas** : enumera todas las ofertas asociadas a una ubicación específica. Seleccione la ubicación e inserte las ofertas en el contenido. Para obtener una documentación completa sobre cómo administrar ofertas, consulte [esta sección](../deliver-personalized-offers.md)
* **Contexto** : cuando la  **** actividad Mensajería se utiliza en un recorrido, los campos de recorrido contextual están disponibles en este menú. Consulte [esta sección](personalization-use-case.md)
* **Funciones**  de ayuda: enumera todas las funciones de ayuda disponibles para realizar operaciones con datos, como cálculos, formato de datos o conversiones, condiciones y manipularlas en el contexto de la personalización. [Más información](functions/functions.md)



Al seleccionarla, la referencia se añade en el editor.

>[!NOTE]
>
>El icono de información situado junto al icono &quot;+&quot; abre una información sobre herramientas que proporciona más detalles para cada variable.

En el siguiente ejemplo, el editor de expresiones permite seleccionar los perfiles que tienen su cumpleaños hoy y luego completar la personalización insertando una oferta específica correspondiente a este día.

![](assets/perso_ee2.png)




