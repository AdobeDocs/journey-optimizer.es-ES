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
TQID: https://experienceleague.adobe.com/6myO49j2-TgkX0-diC8JDePxvMBPjZGnMYdxO466cP4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: d08afb72-92f6-4856-88e3-11ec34313c2fid: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: e57d1da4-32c2-4cc6-945c-9feb219156ffid: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: fa683eda-48de-4558-af32-2673edcd44feid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 506
ht-degree: 15%

---

# Eventos de reacción {#reaction-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Eventos de reacción"
>abstract="Esta actividad permite reaccionar ante los datos de seguimiento relacionados con un mensaje enviado dentro del mismo recorrido. Capturamos esta información en tiempo real en el momento en que se comparte con [!DNL Adobe Experience Platform]."

## Información general {#overview}

Entre las diferentes actividades de eventos disponibles en la paleta, se encuentra el evento **[!UICONTROL Reactions]** integrado. Esta actividad permite reaccionar ante los datos de seguimiento relacionados con un mensaje enviado dentro del mismo recorrido. Capturamos esta información en tiempo real en el momento en que se comparte con [!DNL Adobe Experience Platform].

Puede reaccionar a los mensajes en los que se hace clic o que se abren. Por ejemplo, puede enviar otro mensaje si una persona ha abierto el correo electrónico anterior o ha hecho clic dentro de él, o enviar un mensaje de seguimiento diferente si no ha interactuado con la comunicación.

Ver [actividades de acción](../building-journeys/about-journey-activities.md#action-activities).

Puede usar la actividad **[!UICONTROL Reacción]** para realizar una acción cuando no haya reacción a los mensajes. Para ello, cree una segunda ruta paralela a la actividad **[!UICONTROL Reaction]** y agregue una actividad **[!UICONTROL Wait]**. Si no hay ninguna reacción durante el período definido en la actividad **[!UICONTROL Wait]**, se elegirá la segunda ruta. Puede elegir enviar, por ejemplo, un mensaje de seguimiento.

## Configuración de eventos de reacción {#configure}

![Configuración de evento de reacción con selección de canal y opciones de tipo de evento](assets/journey45.png)

Siga estos pasos para configurar los eventos de reacción:

1. Coloque una actividad **[!UICONTROL Reaction]** **inmediatamente** después de una [actividad de acción del canal](journey-action.md) en el lienzo del recorrido.
1. Agregue una **[!UICONTROL Etiqueta]** a la reacción. Este paso es opcional.
1. En la lista desplegable, seleccione la actividad de acción a la que desee reaccionar. Puede seleccionar cualquier actividad de acción colocada en los pasos anteriores de la ruta.
1. En función de la acción seleccionada, elija a qué desea reaccionar.
1. Puede definir un tiempo de espera de evento (entre 40 y 90 días) y una ruta de tiempo de espera. Esto crea una segunda ruta para las personas que no reaccionaron dentro de la duración definida. Al probar un recorrido que usa un evento de reacción, el modo de prueba **[!UICONTROL Tiempo de espera]** es el valor predeterminado y mínimo de 40 segundos. Consulte [esta sección](../building-journeys/testing-the-journey.md).

## Mecanismos de protección y limitaciones {#guardrails-limitations}

* Una actividad **[!UICONTROL Reaction]** debe colocarse **inmediatamente** después de una [actividad de acción del canal](journey-action.md) en el lienzo de recorrido.
* No puede usar una actividad **[!UICONTROL Reaction]** si no hay ninguna actividad de acción del canal antes de ella.
* No se admite la colocación de una actividad **[!UICONTROL Wait]** o cualquier otra actividad entre la acción del canal y la actividad **[!UICONTROL Reaction]**, lo que puede provocar que la reacción no funcione según lo esperado.
* Los eventos de reacción solo pueden rastrear mensajes enviados dentro del mismo recorrido. No pueden realizar el seguimiento de mensajes que tienen lugar en un recorrido diferente.
* Los eventos de reacción rastrean los clics en vínculos del tipo &quot;rastreado&quot;. No se tienen en cuenta los vínculos de baja de suscripción y de página espejo.
* El seguimiento de las aperturas de correo electrónico se realiza con una imagen de 0 píxeles incluida en el correo electrónico. Si los clientes de correo electrónico (como Gmail) bloquean imágenes, no se tendrán en cuenta las aperturas de correo electrónico.
