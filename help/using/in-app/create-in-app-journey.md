---
title: Creación de una notificación en la aplicación en un Recorrido
description: Obtenga información sobre cómo crear un mensaje en la aplicación en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: en la aplicación, mensaje, creación, inicio
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
source-git-commit: 252011710574122c1f321a388b65bdafb7c666df
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 5%

---

# Creación de un mensaje en la aplicación en un recorrido {#create-in-app-journey}

>[!AVAILABILITY]
>
>La actividad en la aplicación está disponible actualmente como una versión beta para seleccionar solo usuarios. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.

1. Abra el recorrido y, a continuación, arrastre y suelte un **[!UICONTROL En la aplicación]** actividad desde el **[!UICONTROL Acciones]** de la paleta.

   Cuando un perfil llega al final de su recorrido, los mensajes en la aplicación que se les muestren caducarán automáticamente. Por este motivo, se añade automáticamente una actividad de Espera después de la actividad en la aplicación para garantizar un tiempo de espera adecuado.

   ![](assets/in_app_journey_1.png)

1. Introduzca una **[!UICONTROL Etiqueta]** y **[!UICONTROL Descripción]** para el mensaje.

1. Elija la [Superficie en la aplicación](inapp-configuration.md) para usar.

   ![](assets/in_app_journey_2.png)

1. Ahora puede empezar a diseñar el contenido con **[!UICONTROL Editar contenido]** botón. [Más información](design-in-app.md)

1. Clic **[!UICONTROL Editar déclencheur]** para configurar el Déclencheur.

   ![](assets/in_app_journey_4.png)

1. Elija la frecuencia del déclencheur cuando su mensaje en la aplicación esté activo:

   * **[!UICONTROL Mostrar cada vez]**: Mostrar siempre el mensaje cuando los eventos seleccionados en la **[!UICONTROL Déclencheur de aplicación móvil]** se produce la lista desplegable.
   * **[!UICONTROL Mostrar una vez]**: Mostrar solo este mensaje la primera vez que se seleccionen los eventos en la **[!UICONTROL Déclencheur de aplicación móvil]** se produce la lista desplegable.
   * **[!UICONTROL Mostrar hasta el clic]**: Muestra este mensaje cuando los eventos seleccionados en la **[!UICONTROL Déclencheur de aplicación móvil]** se producen hasta que el SDK envía un evento de interacción con una acción de &quot;clic&quot;.

1. Desde el **[!UICONTROL Déclencheur de aplicación móvil]** , elija los eventos y los criterios que van a almacenar el mensaje en déclencheur:

   1. En la lista desplegable izquierda, seleccione el evento necesario para almacenar el mensaje en déclencheur.
   1. En la lista desplegable de la derecha, seleccione la validación necesaria en el evento seleccionado.
   1. Haga clic en **[!UICONTROL Añadir]** si desea que el déclencheur tenga en cuenta varios eventos o criterios. A continuación, repita los pasos anteriores.
   1. Seleccione cómo están vinculados los eventos, p. ej. elija **[!UICONTROL Y]** si lo desea **ambos** Los déclencheur deben ser verdaderos para que se muestre o se elija un mensaje **[!UICONTROL O]** si desea que se muestre el mensaje si **o bien** Todos los déclencheur son verdaderos.
   1. Clic **[!UICONTROL Guardar]** cuando se hayan configurado los Déclencheur.

   ![](assets/in_app_journey_3.png)

1. Si es necesario, complete el flujo de recorrido arrastrando y soltando acciones o eventos adicionales. [Más información](../building-journeys/about-journey-activities.md)

1. Una vez que el mensaje en la aplicación esté listo, finalice la configuración y publique el recorrido para activarlo.

Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md).

## Limitaciones de actividad en la aplicación {#in-app-activity-limitations}

* Actualmente, esta función no está disponible para los clientes de atención sanitaria.

* La personalización solo puede contener atributos de perfil.

* La visualización en la aplicación está ligada a la duración del recorrido, lo que significa que cuando el recorrido termina para un perfil, todos los mensajes en la aplicación dentro de ese recorrido dejan de mostrarse para ese perfil.  Por lo tanto, no es posible detener un mensaje en la aplicación directamente desde una actividad de recorrido. En su lugar, deberá finalizar todo el recorrido para que los mensajes en la aplicación no se muestren en el perfil.

* En el modo de prueba, la visualización en la aplicación depende de la duración del recorrido. Para evitar que el recorrido termine demasiado pronto durante la prueba, ajuste el **[!UICONTROL Tiempo de espera]** valor para su **[!UICONTROL Esperar]** actividades.

* **[!UICONTROL Reacción]** Las actividades de no se pueden utilizar para reaccionar ante una apertura o un clic en la aplicación.

* Un retraso de activación se produce entre el momento en que un perfil de usuario alcanza una actividad en la aplicación en el lienzo y el momento en que comienza a ver ese mensaje en la aplicación. Este retraso puede oscilar entre 15 minutos y 1 hora.

**Temas relacionados:**

* [Diseño de un mensaje en la aplicación](design-in-app.md)
* [Prueba y envío de un mensaje en la aplicación](send-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report.md#inapp-report)
* [Configuración en la aplicación](inapp-configuration.md)
