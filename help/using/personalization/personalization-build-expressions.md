---
solution: Journey Optimizer
product: journey optimizer
title: Acerca del Editor de expresiones
description: Aprenda a trabajar con el editor de expresiones.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expresión, editor, acerca de, iniciar
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 93e3ed9e1a9a437353b800aee58952b86eab9370
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 12%

---

# Introducción al editor de expresiones {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Acerca del Editor de expresiones"
>abstract="El editor de expresiones permite seleccionar, organizar, personalizar y validar todos los datos para crear una personalización ajustada del contenido."

El editor de expresiones es la parte central de la personalización en [!DNL Journey Optimizer]. Está disponible en todos los contextos en los que es necesario definir la personalización como correos electrónicos, mensajes push y ofertas.

En la interfaz del editor de expresiones, se seleccionan, organizan, personalizan y validan todos los datos para crear una personalización personalizada para el contenido.

![](assets/perso_ee1.png)

## Fuentes de personalización disponibles {#sources}

La parte izquierda de la pantalla muestra un selector de dominio que le permite seleccionar el origen de la personalización. Las fuentes disponibles son:

* **[!UICONTROL Atributos de perfil]** : enumera todas las referencias asociadas al esquema de perfil descrito en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.
* **[!UICONTROL Pertenencia a segmentos]** : enumera todos los segmentos creados en el servicio de segmentación de Adobe Experience Platform. Más información sobre segmentación disponible [here](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"}.
* **[!UICONTROL Decisiones de oferta]** : enumera todas las ofertas asociadas a una ubicación específica. Seleccione la ubicación e inserte las ofertas en el contenido. Para obtener una documentación completa sobre cómo administrar ofertas, consulte [esta sección](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL Atributos contextuales]** : cuando se utiliza una actividad de acción de canal (correo electrónico, push, SMS) en un recorrido, los campos de recorrido contextual están disponibles a través de este menú. Obtenga más información en [esta sección](personalization-use-case.md).
* **[!UICONTROL Funciones de ayuda]** : enumera todas las funciones de ayuda disponibles para realizar operaciones con datos, como cálculos, formato de datos o conversiones, condiciones y manipularlas en el contexto de la personalización. Obtenga más información en [esta sección](functions/functions.md).

## Añadir atributos de personalización {#add}

Haga clic en el botón + para añadir un atributo a la expresión de personalización.

El menú de elipsis junto al icono &quot;+&quot; le permite obtener más detalles para cada variable y agregar los atributos usados con más frecuencia a los favoritos. [Aprenda a añadir atributos a favoritos](personalization-favorites.md)

Además, puede definir el texto de reserva predeterminado que se mostrará si un atributo de perfil de tipo cadena está vacío. Para ello, haga clic en el botón de puntos suspensivos situado junto al atributo y seleccione **[!UICONTROL Insertar con texto alternativo]**. Escriba el texto que debería mostrarse de forma predeterminada si el valor del atributo está vacío para un perfil y haga clic en **[!UICONTROL Agregar]**.

![](assets/attribute-details.png)

En el siguiente ejemplo, el editor de expresiones permite seleccionar los perfiles que tienen su cumpleaños hoy y luego completar la personalización insertando una oferta específica correspondiente a este día.

![](assets/perso_ee2.png)

Una vez que la expresión de personalización esté lista, debe tener el editor de expresiones validado. Obtenga más información en [esta sección](personalization-validation.md).
