---
title: Acerca del Editor de expresiones
description: Aprenda a trabajar con el Editor de expresiones.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 50e12a28ed9f94133a9810a460172d34ad3a4593
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 8%

---

# Acerca del Editor de expresiones {#build-personalization-expressions}

El editor de expresiones es la parte central de la personalización en [!DNL Journey Optimizer]. Está disponible en todos los contextos en los que es necesario definir la personalización como correos electrónicos, mensajes push y ofertas.

En la interfaz del editor de expresiones, se seleccionan, organizan, personalizan y validan todos los datos para crear una personalización personalizada para el contenido.

![](assets/perso_ee1.png)

La parte izquierda de la pantalla muestra un selector de dominio que le permite seleccionar el origen de la personalización.

![](assets/perso_ee3.png)

Las fuentes disponibles son:

* **[!UICONTROL Profile attributes]** : enumera todas las referencias asociadas al esquema de perfil descrito en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target=&quot;_blank&quot;}.
* **[!UICONTROL Segment memberships]** : enumera todos los segmentos creados en el servicio de segmentación de Adobe Experience Platform. Más información sobre segmentación disponible [here](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Offer decisions]** : enumera todas las ofertas asociadas a una ubicación específica. Seleccione la ubicación e inserte las ofertas en el contenido. Para obtener una documentación completa sobre cómo administrar ofertas, consulte [esta sección](../deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** : cuando la variable **Mensaje** se utiliza en un recorrido, los campos de recorrido contextual están disponibles a través de este menú. Obtenga más información en [esta sección](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : enumera todas las funciones de ayuda disponibles para realizar operaciones con datos, como cálculos, formato de datos o conversiones, condiciones y manipularlas en el contexto de la personalización. Obtenga más información en [esta sección](functions/functions.md).

Al seleccionarla, la referencia se añade en el editor.

>[!NOTE]
>
>El icono de información situado junto al icono &quot;+&quot; abre una información sobre herramientas que proporciona más detalles para cada variable.
>
>Puede agregar los atributos usados con más frecuencia a los favoritos. Obtenga más información en [esta sección](personalization-favorites.md).

En el siguiente ejemplo, el editor de expresiones permite seleccionar los perfiles que tienen su cumpleaños hoy y luego completar la personalización insertando una oferta específica correspondiente a este día.

![](assets/perso_ee2.png)

Una vez que la expresión de personalización esté lista, el Editor de expresiones la debe validar. Obtenga más información en [esta sección](personalization-validation.md).