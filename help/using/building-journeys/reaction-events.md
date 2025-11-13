---
solution: Journey Optimizer
product: journey optimizer
title: Eventos de reacciones
description: Más información sobre los eventos de reacción
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, eventos, reaction, seguimiento, platform
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 20%

---

# Eventos de reacción {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Eventos de reacción"
>abstract="Esta actividad permite reaccionar ante los datos de seguimiento relacionados con un mensaje enviado dentro del mismo recorrido. Capturamos esta información en tiempo real en el momento en que se comparte con Adobe Experience Platform."

Entre las diferentes actividades de eventos disponibles en la paleta, se encuentra el evento **[!UICONTROL Reactions]** integrado. Esta actividad permite reaccionar ante los datos de seguimiento relacionados con un mensaje enviado dentro del mismo recorrido. Capturamos esta información en tiempo real en el momento en que se comparte con Adobe Experience Platform.

Puede reaccionar a los mensajes en los que se hace clic o que se abren.

También puede utilizar este mecanismo para realizar una acción cuando no haya ninguna reacción a los mensajes. Para ello, cree una segunda ruta paralela a la actividad de reacción y añada una actividad de espera. Si no hay ninguna reacción durante el periodo definido en la actividad de espera, se elige la segunda ruta. Puede elegir enviar, por ejemplo, un mensaje de seguimiento.

Tenga en cuenta que solo puede utilizar una actividad de reacción en el lienzo si hay una actividad de acción del canal antes (correo electrónico y push).

Consulte [Acerca de las actividades de acción](../building-journeys/about-journey-activities.md#action-activities).

![Configuración de evento de reacción con selección de canal y opciones de tipo de evento](assets/journey45.png)

Estos son los pasos para configurar los eventos de reacción:

1. Agregue una **[!UICONTROL Etiqueta]** a la reacción. Este paso es opcional.
1. En la lista desplegable, seleccione la actividad de acción a la que desee reaccionar. Puede seleccionar cualquier actividad de acción colocada en los pasos anteriores de la ruta.
1. En función de la acción seleccionada, elija a qué desea reaccionar.
1. Puede definir un tiempo de espera de evento (entre 40 y 90 días) y una ruta de tiempo de espera. Esto crea una segunda ruta para las personas que no reaccionaron dentro de la duración definida. Al probar un recorrido que usa un evento de reacción, el modo de prueba **[!UICONTROL Tiempo de espera]** es el valor predeterminado y mínimo de 40 segundos. Consulte [esta sección](../building-journeys/testing-the-journey.md).

>[!NOTE]
>
>
>Los eventos de reacción no pueden rastrear mensajes que se producen en un recorrido diferente.
>
>Los eventos de reacción rastrean los clics en vínculos del tipo &quot;rastreado&quot;. No se tienen en cuenta los vínculos de baja de suscripción y de página espejo.

>[!IMPORTANT]
>
>Los clientes de correo electrónico como Gmail permiten el bloqueo de imágenes. El seguimiento de las aperturas de correo electrónico se realiza con una imagen de 0 píxeles incluida en el correo electrónico. Si las imágenes están bloqueadas, las aperturas de correo electrónico no se tendrán en cuenta.
