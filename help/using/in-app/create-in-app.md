---
title: Creación de una notificación en la aplicación
description: Obtenga información sobre cómo crear un mensaje en la aplicación en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: en la aplicación, mensaje, creación, inicio
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 64be9c41085dead10ff08711be1f39760a81ff95
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 6%

---

# Creación de un mensaje en la aplicación  {#create-in-app}

<!--
>[!BEGINTABS]

>[!TAB Add an In-app message to a journey]

>[!AVAILABILITY]
>
>The In-app activity is currently available as a beta to select users only. To join the beta program, contact Adobe Customer Care.

1. Open your journey, then drag and drop an **[!UICONTROL In-app]** activity from the **[!UICONTROL Actions]** section of the palette.

    When a profile reaches the end of their journey, any in-app messages displayed to them will automatically expire. For that reason, a Wait activity is automatically added after your In-app activity to ensure proper timing.

    ![](assets/in_app_journey_1.png)

1. Enter a **[!UICONTROL Label]** and **[!UICONTROL Description]** for your message.

1. Choose the [In-app surface](inapp-configuration.md) to use.

    ![](assets/in_app_journey_2.png)

1. You can now start designing your content with the **[!UICONTROL Edit content]** button. [Learn more](design-in-app.md)

1. Click **[!UICONTROL Edit trigger]** to configure your Trigger. 

    ![](assets/in_app_journey_4.png)

1. Choose the frequency of your trigger when your In-app message is active:

    * **[!UICONTROL Show every time]**: Always show the message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show once]**: Only show this message the first time the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show until click through]**: Show this message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur until an interact event is sent by the SDK with an action of "clicked".

1. From the **[!UICONTROL Mobile app trigger]** dropdown(s), choose the event(s) and criteria that will trigger your message:

    1. From the left drop-down, select the event required to trigger the message.
    1. From the right drop-down, select the validation required on the selected event.
    1. Click the **[!UICONTROL Add]** button if you want the trigger to consider multiple events or criteria. Then, repeat the steps above.
    1. Select how your events are linked, e.g. choose **[!UICONTROL And]** if you want **both** triggers to be true in order for a message to be shown or choose **[!UICONTROL Or]** if you want the message to be shown if **either** of the triggers are true.
    1. Click **[!UICONTROL Save]** when your Triggers have been configured.

    ![](assets/in_app_journey_3.png)
    
1. If necessary, complete your journey flow by dragging and dropping additional actions or events. [Learn more](../building-journeys/about-journey-activities.md)

1. Once your In-app message is ready, finalize the configuration and publish your journey to activate it.

For more information on how to configure a journey, refer to [this page](../building-journeys/journey-gs.md).

>[!TAB Add an In-app message to a campaign]
-->

1. Acceda a la **[!UICONTROL Campañas]** y haga clic en **[!UICONTROL Crear campaña]**.

1. En el **[!UICONTROL Propiedades]** , seleccione cuando el tipo de ejecución de la campaña: Programada o activada por API. Obtenga más información acerca de los tipos de campañas en [esta página](../campaigns/create-campaign.md#campaigntype).

1. En el **[!UICONTROL Acciones]** , seleccione la **[!UICONTROL Mensaje en la aplicación]** y el **[!UICONTROL Superficie de aplicación]** previamente configurado para su mensaje en la aplicación. A continuación, haga clic en **[!UICONTROL Crear]**.

   Obtenga más información acerca de la configuración en la aplicación en [esta página](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Desde el **[!UICONTROL Propiedades]** , introduzca la **[!UICONTROL Título]** y el **[!UICONTROL Descripción]** descripción.

1. Para asignar etiquetas de uso de datos personalizadas o principales al mensaje en la aplicación, seleccione **[!UICONTROL Administrar acceso]**. [Más información](../administration/object-based-access.md).

1. Haga clic en **[!UICONTROL Seleccionar audiencia]** para definir la audiencia de destino a partir de la lista de segmentos de Adobe Experience Platform disponibles. [Más información](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a los individuos del segmento seleccionado. [Más información](../event/about-creating.md#select-the-namespace).

1. Clic **[!UICONTROL Crear experimento]** para comenzar a configurar el experimento de contenido y crear tratamientos para medir su rendimiento e identificar la mejor opción para la audiencia de destino. [Más información](../campaigns/content-experiment.md)

1. Clic **[!UICONTROL Editar déclencheur]** para elegir los eventos y los criterios que almacenarán en déclencheur el mensaje:

   1. Clic **Añadir condición** si desea que el déclencheur considere varios eventos o criterios.
   1. Seleccione cómo están vinculados los eventos, p. ej. elija **[!UICONTROL Y]** si lo desea **ambos** Los déclencheur deben ser verdaderos para que se muestre o se elija un mensaje **[!UICONTROL O]** si desea que se muestre el mensaje si **o bien** Todos los déclencheur son verdaderos.
   1. Clic **[!UICONTROL Crear grupo]** para agrupar déclencheur.

   ![](assets/in_app_create_3.png)

1. Elija la frecuencia del déclencheur cuando su mensaje en la aplicación esté activo. Las opciones disponibles son las siguientes:

   * **[!UICONTROL Siempre]**: Mostrar siempre el mensaje cuando los eventos seleccionados en la **[!UICONTROL Déclencheur de aplicación móvil]** se produce la lista desplegable.
   * **[!UICONTROL Una]**: Mostrar solo este mensaje la primera vez que se seleccionen los eventos en la **[!UICONTROL Déclencheur de aplicación móvil]** se produce la lista desplegable.
   * **[!UICONTROL Hasta el clic]**: Muestra este mensaje cuando los eventos seleccionados en la **[!UICONTROL Déclencheur de aplicación móvil]** se producen hasta que el SDK envía un evento de interacción con una acción de &quot;clic&quot;.
   * **[!UICONTROL X número de veces]**: muestra este mensaje X vez.

1. Si es necesario, elija cuál **[!UICONTROL Día de la semana]** o **[!UICONTROL Hora del día]** se muestra el mensaje en la aplicación.

1. Las campañas están diseñadas para ejecutarse en una fecha específica o en una frecuencia recurrente. Obtenga información sobre cómo configurar el **[!UICONTROL Programación]** de la campaña en [esta sección](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Ahora puede empezar a diseñar el contenido con **[!UICONTROL Editar contenido]** botón. [Más información](design-in-app.md)

   ![](assets/in_app_create_4.png)

<!--
>[!ENDTABS]
-->

## Vídeo explicativo{#video}

El siguiente vídeo muestra cómo crear, configurar y publicar mensajes en la aplicación en sus campañas.

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**Temas relacionados:**

* [Diseño de un mensaje en la aplicación](design-in-app.md)
* [Prueba y envío de un mensaje en la aplicación](send-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report.md#inapp-report)
* [Configuración en la aplicación](inapp-configuration.md)