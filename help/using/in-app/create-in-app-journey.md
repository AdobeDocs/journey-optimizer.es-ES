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
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 2%

---

# Creación de un mensaje en la aplicación en un Recorrido {#create-in-app-journey}

>[!AVAILABILITY]
>
>La actividad en la aplicación está disponible actualmente como una versión beta solo para usuarios seleccionados. Para unirse al programa beta, póngase en contacto con el Servicio de atención al cliente de Adobe.

1. Abra el recorrido y, a continuación, arrastre y suelte una **[!UICONTROL En la aplicación]** de **[!UICONTROL Acciones]** de la paleta.

   Cuando un perfil llega al final de su recorrido, cualquier mensaje en la aplicación que se le muestre caducará automáticamente. Por este motivo, se agrega automáticamente una actividad de Espera después de la actividad en la aplicación para garantizar el tiempo adecuado.

   ![](assets/in_app_journey_1.png)

1. Escriba un **[!UICONTROL Etiqueta]** y **[!UICONTROL Descripción]** para su mensaje.

1. Elija la [Superficie en la aplicación](inapp-configuration.md) para usar.

   ![](assets/in_app_journey_2.png)

1. Ahora puede empezar a diseñar el contenido con la variable **[!UICONTROL Editar contenido]** botón. [Más información](design-in-app.md)

1. Haga clic en **[!UICONTROL Editar déclencheur]** para configurar el Déclencheur.

   ![](assets/in_app_journey_4.png)

1. Elija la frecuencia de su déclencheur cuando el mensaje en la aplicación esté activo:

   * **[!UICONTROL Mostrar cada vez]**: Mostrar siempre el mensaje cuando los eventos seleccionados en la variable **[!UICONTROL Déclencheur de aplicación móvil]** se produce.
   * **[!UICONTROL Mostrar una vez]**: Mostrar este mensaje solo la primera vez que se seleccionan los eventos en la variable **[!UICONTROL Déclencheur de aplicación móvil]** se produce.
   * **[!UICONTROL Mostrar hasta pulsaciones]**: Mostrar este mensaje cuando los eventos seleccionados en la variable **[!UICONTROL Déclencheur de aplicación móvil]** se produce hasta que el SDK envía un evento de interacción con una acción de &quot;clic&quot;.

1. En el **[!UICONTROL Déclencheur de aplicación móvil]** , elija los eventos y criterios que almacenarán el déclencheur del mensaje:

   1. En el menú desplegable de la izquierda, seleccione el evento necesario para almacenar el mensaje en déclencheur.
   1. En la lista desplegable derecha, seleccione la validación requerida en el evento seleccionado.
   1. Haga clic en el **[!UICONTROL Agregar]** si desea que el déclencheur considere varios eventos o criterios. A continuación, repita los pasos anteriores.
   1. Seleccione cómo están vinculados los eventos, por ejemplo, elija **[!UICONTROL Y]** si desea **both** déclencheur que deben ser verdaderos para que un mensaje se muestre o elija **[!UICONTROL O]** si desea que se muestre el mensaje si **o** de los déclencheur son verdaderos.
   1. Haga clic en **[!UICONTROL Guardar]** cuando se hayan configurado los Déclencheur.

   ![](assets/in_app_journey_3.png)

1. Si es necesario, complete el flujo de recorrido arrastrando y soltando acciones o eventos adicionales. [Más información](../building-journeys/about-journey-activities.md)

1. Una vez que el mensaje en la aplicación esté listo, finalice la configuración y publique el recorrido para activarlo.

Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md).

## Limitaciones de las actividades en la aplicación {#in-app-activity-limitations}

* Actualmente, esta función no está disponible para los clientes sanitarios.

* La personalización solo puede contener atributos de perfil.

* La visualización en la aplicación está vinculada a la duración del recorrido, lo que significa que cuando el recorrido termina en un perfil, todos los mensajes en la aplicación de ese recorrido dejarán de mostrarse en ese perfil. Esto significa que no puede detener una aplicación directamente desde una actividad de recorrido. Tienes que terminar ese recorrido.
* La visualización en la aplicación está vinculada a la duración de un recorrido, lo que significa que una vez que se completa un recorrido para un perfil de usuario determinado, todos los mensajes en la aplicación de ese recorrido dejarán de mostrarse para ese perfil. Por lo tanto, no es posible detener un mensaje en la aplicación directamente desde una actividad de recorrido. En su lugar, tendrá que finalizar todo el recorrido para evitar que los mensajes en la aplicación se muestren en el perfil.

* Con esta función, aún no podrá usar **[!UICONTROL Reacción]** actividades para reaccionar ante una apertura o un clic en la aplicación.

* Se produce un retraso en la activación entre el momento en que un perfil de usuario alcanza una actividad en la aplicación en el lienzo y la hora en que comienza a ver ese mensaje en la aplicación. Este retraso puede variar de 15 minutos a 1 hora.

**Temas relacionados:**

* [Diseño de mensajes en la aplicación](design-in-app.md)
* [Pruebe y envíe su mensaje en la aplicación](send-in-app.md)
* [Informe en la aplicación](../reports/campaign-global-report.md#inapp-report)
* [Configuración en la aplicación](inapp-configuration.md)