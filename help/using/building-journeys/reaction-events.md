---
solution: Journey Optimizer
product: journey optimizer
title: Eventos de reacciones
description: Obtenga información sobre cómo utilizar eventos de reacción para responder a los datos de seguimiento de mensajes, como aperturas y clics dentro de los recorridos, y configurar rutas de tiempo de espera para usuarios que no responden.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, eventos, reaction, seguimiento, platform
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
source-git-commit: dff732d14dd143f085b1287274f7571a900a0c87
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 17%

---

# Eventos de reacción {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Eventos de reacción"
>abstract="Esta actividad permite reaccionar ante los datos de seguimiento relacionados con un mensaje enviado dentro del mismo recorrido. Capturamos esta información en tiempo real en el momento en que se comparte con Adobe Experience Platform."

## Información general {#overview}

Entre las diferentes actividades de eventos disponibles en la paleta, se encuentra el evento **[!UICONTROL Reactions]** integrado. Esta actividad permite reaccionar ante los datos de seguimiento relacionados con un mensaje enviado dentro del mismo recorrido. Capturamos esta información en tiempo real en el momento en que se comparte con Adobe Experience Platform.

Puede reaccionar a los mensajes en los que se hace clic o que se abren.

Ver [actividades de acción](../building-journeys/about-journey-activities.md#action-activities).

Puede usar la actividad **[!UICONTROL Reacción]** para realizar una acción cuando no haya reacción a los mensajes. Para ello, cree una segunda ruta paralela a la actividad **[!UICONTROL Reaction]** y agregue una actividad **[!UICONTROL Wait]**. Si no hay ninguna reacción durante el período definido en la actividad **[!UICONTROL Wait]**, se elegirá la segunda ruta. Puede elegir enviar, por ejemplo, un mensaje de seguimiento.

## Configuración de eventos de reacción {#configure}

![Configuración de evento de reacción con selección de canal y opciones de tipo de evento](assets/journey45.png)

Siga estos pasos para configurar los eventos de reacción:

1. Coloque una actividad **[!UICONTROL Reaction]** **inmediatamente** después de una [actividad de acción del canal](journeys-message.md) en el lienzo del recorrido.
1. Agregue una **[!UICONTROL Etiqueta]** a la reacción. Este paso es opcional.
1. En la lista desplegable, seleccione la actividad de acción a la que desee reaccionar. Puede seleccionar cualquier actividad de acción colocada en los pasos anteriores de la ruta.
1. En función de la acción seleccionada, elija a qué desea reaccionar.
1. Puede definir un tiempo de espera de evento (entre 40 y 90 días) y una ruta de tiempo de espera. Esto crea una segunda ruta para las personas que no reaccionaron dentro de la duración definida. Al probar un recorrido que usa un evento de reacción, el modo de prueba **[!UICONTROL Tiempo de espera]** es el valor predeterminado y mínimo de 40 segundos. Consulte [esta sección](../building-journeys/testing-the-journey.md).

## Mecanismos de protección y limitaciones {#guardrails-limitations}

* Una actividad **[!UICONTROL Reaction]** debe colocarse **inmediatamente** después de una [actividad de acción del canal](journeys-message.md) en el lienzo de recorrido.
* No puede usar una actividad **[!UICONTROL Reaction]** si no hay ninguna actividad de acción del canal antes de ella.
* No se admite la colocación de una actividad **[!UICONTROL Wait]** o cualquier otra actividad entre la acción del canal y la actividad **[!UICONTROL Reaction]**, lo que puede provocar que la reacción no funcione según lo esperado.
* Los eventos de reacción solo pueden rastrear mensajes enviados dentro del mismo recorrido. No pueden realizar el seguimiento de mensajes que tienen lugar en un recorrido diferente.
* Los eventos de reacción rastrean los clics en vínculos del tipo &quot;rastreado&quot;. No se tienen en cuenta los vínculos de baja de suscripción y de página espejo.
* El seguimiento de las aperturas de correo electrónico se realiza con una imagen de 0 píxeles incluida en el correo electrónico. Si los clientes de correo electrónico (como Gmail) bloquean imágenes, no se tendrán en cuenta las aperturas de correo electrónico.
