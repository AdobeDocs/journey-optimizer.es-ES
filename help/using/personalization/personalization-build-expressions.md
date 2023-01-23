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
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 9%

---

# Acerca del Editor de expresiones {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Acerca del Editor de expresiones"
>abstract="El editor de expresiones permite seleccionar, organizar, personalizar y validar todos los datos para crear una personalización personalizada del contenido."

El editor de expresiones es la parte central de la personalización en [!DNL Journey Optimizer]. Está disponible en todos los contextos en los que es necesario definir la personalización como correos electrónicos, mensajes push y ofertas.

En la interfaz del editor de expresiones, se seleccionan, organizan, personalizan y validan todos los datos para crear una personalización personalizada para el contenido.

![](assets/perso_ee1.png)

La parte izquierda de la pantalla muestra un selector de dominio que le permite seleccionar el origen de la personalización.

![](assets/perso_ee3.png)

Las fuentes disponibles son:

* **[!UICONTROL Atributos de perfil]** : enumera todas las referencias asociadas al esquema de perfil descrito en [Documentación del Modelo de datos de Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es){target="_blank"}.
* **[!UICONTROL Pertenencia a segmentos]** : enumera todos los segmentos creados en el servicio de segmentación de Adobe Experience Platform. Más información sobre segmentación disponible [here](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"}.
* **[!UICONTROL Decisiones de oferta]** : enumera todas las ofertas asociadas a una ubicación específica. Seleccione la ubicación e inserte las ofertas en el contenido. Para obtener una documentación completa sobre cómo administrar ofertas, consulte [esta sección](../email/add-offers-email.md).
* **[!UICONTROL Atributos contextuales]** : cuando se utiliza una actividad de acción de canal (correo electrónico, push, SMS) en un recorrido, los campos de recorrido contextual están disponibles a través de este menú. Obtenga más información en [esta sección](personalization-use-case.md).
* **[!UICONTROL Funciones de ayuda]** : enumera todas las funciones de ayuda disponibles para realizar operaciones con datos, como cálculos, formato de datos o conversiones, condiciones y manipularlas en el contexto de la personalización. Obtenga más información en [esta sección](functions/functions.md).

Haga clic en el botón + para añadir un atributo al editor.

>[!NOTE]
>
>El menú elipse junto al icono &quot;+&quot; le permite obtener más detalles para cada variable y agregar los atributos usados con más frecuencia a [favoritos](personalization-favorites.md).

![](assets/attribute-details.png)

En el siguiente ejemplo, el editor de expresiones permite seleccionar los perfiles que tienen su cumpleaños hoy y luego completar la personalización insertando una oferta específica correspondiente a este día.

![](assets/perso_ee2.png)

Una vez que la expresión de personalización esté lista, debe tener el editor de expresiones validado. Obtenga más información en [esta sección](personalization-validation.md).
