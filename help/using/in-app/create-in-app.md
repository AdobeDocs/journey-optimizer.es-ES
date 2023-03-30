---
title: Creación de una notificación en la aplicación
description: Obtenga información sobre cómo crear un mensaje en la aplicación en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: en la aplicación, mensaje, creación, inicio
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 1af9a3adeb6727e965e61434b0ed2c41ff3d4911
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 4%

---

# Creación de un mensaje en la aplicación  {#create-in-app}

Los mensajes en la aplicación se crean en el contexto de una campaña.

Para crear un mensaje en la aplicación, siga los pasos a continuación:

1. Acceda a la **[!UICONTROL Campañas]** a continuación, haga clic en **[!UICONTROL Crear campaña]**.

1. En el **[!UICONTROL Propiedades]** , seleccione cuándo es el tipo de ejecución de la campaña: Programado o activado por API. Obtenga más información sobre los tipos de campaña en [esta página](../campaigns/create-campaign.md#campaigntype).

1. En el **[!UICONTROL Acciones]** , seleccione **[!UICONTROL Mensaje en la aplicación]** y **[!UICONTROL Superficie de la aplicación]** previamente configurado para el mensaje en la aplicación. A continuación, haga clic en **[!UICONTROL Crear]**.

   Obtenga más información sobre la configuración en la aplicación en [esta página](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. En el **[!UICONTROL Propiedades]** , introduzca el **[!UICONTROL Título]** y **[!UICONTROL Descripción]** descripción.

1. Para asignar etiquetas de uso de datos principales o personalizadas al mensaje en la aplicación, seleccione **[!UICONTROL Administrar acceso]**. [Más información](../administration/object-based-access.md).

1. Haga clic en el **[!UICONTROL Seleccionar la audiencia]** para definir la audiencia a la que se dirigirá desde la lista de segmentos de Adobe Experience Platform disponibles. [Más información](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado. [Más información](../event/about-creating.md#select-the-namespace).

1. Haga clic en **[!UICONTROL Editar déclencheur]** para elegir los eventos y criterios que almacenarán el déclencheur del mensaje:

   1. Haga clic en **Añadir condición** si desea que el déclencheur considere varios eventos o criterios.
   1. Seleccione cómo están vinculados los eventos, por ejemplo, elija **[!UICONTROL Y]** si desea **both** déclencheur que deben ser verdaderos para que un mensaje se muestre o elija **[!UICONTROL O]** si desea que se muestre el mensaje si **o** de los déclencheur son verdaderos.
   1. Haga clic en **[!UICONTROL Crear grupo]** para agrupar déclencheur.

   ![](assets/in_app_create_3.png)

1. Elija la frecuencia de su déclencheur cuando el mensaje en la aplicación esté activo. Las opciones disponibles son las siguientes:

   * **[!UICONTROL Cada vez]**: Mostrar siempre el mensaje cuando los eventos seleccionados en la variable **[!UICONTROL Déclencheur de aplicación móvil]** se produce.
   * **[!UICONTROL Una vez]**: Mostrar este mensaje solo la primera vez que se seleccionan los eventos en la variable **[!UICONTROL Déclencheur de aplicación móvil]** se produce.
   * **[!UICONTROL Hasta que haga clic]**: Mostrar este mensaje cuando los eventos seleccionados en la variable **[!UICONTROL Déclencheur de aplicación móvil]** se produce hasta que el SDK envía un evento de interacción con una acción de &quot;clic&quot;.
   * **[!UICONTROL X número de veces]**: Mostrar este mensaje X hora.

1. Si es necesario, elija cuál **[!UICONTROL Día de la semana]** o **[!UICONTROL Hora del día]** se mostrará el mensaje en la aplicación.

1. Las campañas están diseñadas para ejecutarse en una fecha específica o con una frecuencia recurrente. Obtenga información sobre cómo configurar la variable **[!UICONTROL Programación]** de su campaña en [esta sección](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Ahora puede empezar a diseñar el contenido con la variable **[!UICONTROL Editar contenido]** botón. [Más información](design-in-app.md)

   ![](assets/in_app_create_4.png)


## Vídeo explicativo{#video}

El siguiente vídeo muestra cómo crear, configurar y publicar mensajes en la aplicación en sus campañas.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**Temas relacionados:**

* [Diseño de mensajes en la aplicación](design-in-app.md)
* [Pruebe y envíe su mensaje en la aplicación](send-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report.md#inapp-report)
* [Configuración en la aplicación](inapp-configuration.md)