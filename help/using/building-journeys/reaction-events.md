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
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: d08afb72-92f6-4856-88e3-11ec34313c2fid: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: e57d1da4-32c2-4cc6-945c-9feb219156ffid: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1030
ht-degree: 7%

---

# Eventos de reacción {#reaction-events}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar la actividad de reacción para responder a los datos de seguimiento de mensajes, como aperturas y clics, dentro del mismo recorrido, y configure rutas de tiempo de espera para personas que no interactúen.

>[!ENDSHADEBOX]

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

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo usar la actividad de evento de reacción integrada en Adobe Journey Optimizer para bifurcar las rutas de recorrido en función de los datos de participación de mensajes en tiempo real, como las aperturas de correo electrónico y los clics en vínculos.

**Intenciones:**
* Añada una actividad Reaction para responder a las aperturas de mensajes o a los clics dentro de un recorrido
* Configure una duración de tiempo de espera y una ruta de reserva para los perfiles que no interactúen
* Cree una ruta paralela con una actividad de espera para gestionar los no respondedores
* Seleccione una actividad de acción específica del canal ascendente para escucharla

**Glosario:**
* **Evento de reacción**: una actividad de evento de recorrido integrada que escucha datos de seguimiento en tiempo real (aperturas, clics) de un mensaje enviado anteriormente en el mismo recorrido *(específico del producto)*
* **Ruta de tiempo de espera**: Una rama de recorrido secundaria que siguen los perfiles si no producen la reacción esperada dentro del período de tiempo de espera definido *(específico del producto)*

**Protecciones:**
* La actividad Reacción debe colocarse inmediatamente después de una actividad de acción del canal; no se puede colocar ninguna otra actividad entre ellas.
* No se puede utilizar una actividad de reacción si no hay ninguna actividad de acción del canal antes de ella en la ruta.
* Los eventos de reacción solo pueden rastrear mensajes enviados dentro del mismo recorrido; no se admite el seguimiento entre recorridos.
* Los eventos de reacción no rastrean los vínculos de baja de suscripción ni los vínculos de páginas espejo.
* Las aperturas de correo electrónico dependen de una imagen de seguimiento de 0 píxeles; si el cliente de correo electrónico bloquea las imágenes (por ejemplo, Gmail), las aperturas no se registrarán.
* El intervalo de tiempo de espera del evento es de 40 segundos a 90 días; el valor mínimo en el modo de prueba es también de 40 segundos.

**Terminología:**
* Nombre canónico: Eventos de reacción — Acrónimo: none — variantes: actividad de reacción, evento de seguimiento de participación
* Sinónimos: &quot;Evento de reacción&quot; = &quot;evento de participación de mensaje&quot; = &quot;evento de seguimiento&quot;
* No confunda: &quot;Evento de reacción&quot; ≠ &quot;evento externo&quot; (los eventos de reacción están integrados y vinculados a mensajes del mismo recorrido; los eventos externos provienen de fuera del recorrido).

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Puede un evento de reacción rastrear un mensaje enviado en un recorrido diferente?** — No; los eventos de reacción solo rastrean los mensajes enviados dentro del mismo recorrido.
* **Q: ¿Cómo administro los perfiles que no abren ni hacen clic en un mensaje?** — Añada una ruta paralela junto a la actividad Reacción con una actividad Espera; los perfiles que no reaccionen dentro de la duración de espera seguirán esa segunda ruta.
* **Q: ¿los eventos de reacción rastrean los clics en el vínculo de cancelación de suscripción?** — No; solo se capturan los tipos de vínculos rastreados. Se excluyen los vínculos de baja de suscripción y de página espejo.
* **Q: ¿Qué sucede si un cliente de correo electrónico bloquea imágenes?** — Las aperturas de correo electrónico rastreadas a través de la imagen de 0 píxeles no se registrarán para los clientes que bloqueen imágenes, como Gmail.
* **Q: ¿Cuál es el intervalo de tiempo de espera válido para un evento de reacción?** — Entre 40 segundos y 90 días.

+++
