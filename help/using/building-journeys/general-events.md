---
solution: Journey Optimizer
product: journey optimizer
title: Eventos generales
description: Aprenda a utilizar eventos generales
feature: Journeys, Events
topic: Content Management
role: User
level: Intermediate
keywords: personalizado, general, eventos, recorrido
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/jKMddtFlzmUinPK5-onY2u-kRAd1MD126biQVwq3aAg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1253
ht-degree: 12%

---

# Eventos generales {#general-events}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar eventos generales para almacenar en déclencheur los recorridos de forma unitaria en tiempo real y configurar los tiempos de espera de evento y las rutas de tiempo de espera para detectar un evento solo durante un período definido.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Eventos unitarios"
>abstract="Los eventos permiten activar sus recorridos de forma unitaria para enviar mensajes, en tiempo real, al particular que entra en el recorrido. Para este tipo de evento, solo puede añadir una etiqueta y una descripción. La configuración de eventos la realiza un ingeniero de datos y no se puede editar."

>[!CONTEXTUALHELP]
>id="ajo_journey_event_business_canvas"
>title="Eventos empresariales"
>abstract="Estos eventos le permiten iniciar un recorrido utilizando un evento no relacionado con el perfil. Cuando se active ese evento, podrá enviar mensajes a un público de perfiles. Para este tipo de evento, solo puede añadir una etiqueta y una descripción. La configuración de eventos la realiza un usuario técnico y no se puede editar."

Los eventos permiten activar sus recorridos de forma unitaria para enviar mensajes, en tiempo real, al particular que entra en el recorrido.

Para este tipo de evento, solo puede añadir una etiqueta y una descripción. El resto de la configuración no se puede editar. Lo ha realizado el usuario técnico. Consulte [esta página](../event/about-events.md).

Obtenga más información acerca del rendimiento de eventos y las tasas de procesamiento de recorridos en [esta sección](entry-management.md#journey-processing-rate).

![Panel de configuración de eventos generales con selección y configuración de eventos](assets/general-events.png)

Al eliminar un evento empresarial, se agrega automáticamente una actividad **Leer audiencia**. Para obtener más información sobre los eventos empresariales, consulte [esta sección](../event/about-events.md)

## Escucha de eventos durante un tiempo específico {#events-specific-time}

Una actividad de evento colocada en el recorrido escucha eventos indefinidamente. Para escuchar un evento solo durante un tiempo determinado, debe configurar un tiempo de espera para el evento.

El recorrido escuchará el evento durante el tiempo especificado en el tiempo de espera. Si se recibe un evento durante ese período, la persona fluirá en la ruta del evento. Si no es así, el cliente fluirá a la ruta de tiempo de espera si está definida o continuará ese recorrido.

Si no se define ninguna ruta de tiempo de espera, la configuración de tiempo de espera actuará como una actividad de espera, lo que hace que el perfil espere durante un período de tiempo, que podría detenerse si se produce un evento antes del final de esa espera. Si desea que los perfiles se excluyan de ese recorrido después del tiempo de espera, deberá establecer una ruta de tiempo de espera.

Para configurar un tiempo de espera para un evento, siga estos pasos:

1. Activar la opción **[!UICONTROL Definir el tiempo de espera del evento]** desde las propiedades de evento.

1. Especifique la cantidad de tiempo que el recorrido esperará el evento. La duración máxima es de **90 días**.

1. Cuando no se recibe ningún evento dentro del tiempo de espera especificado, se recomienda enviar a los individuos a una ruta de tiempo de espera. Para esto, habilite la opción **[!UICONTROL Establecer una ruta de tiempo de espera]**. En ese caso, el recorrido continúa para el individuo una vez que se alcanza el tiempo de espera. Se recomienda habilitar siempre la opción **[!UICONTROL Establecer una ruta de tiempo de espera]**.

   ![Configuración del tiempo de espera del evento con opciones de ruta de tiempo de espera y duración](assets/event-timeout.png)

En este ejemplo, el recorrido envía un primer correo electrónico de bienvenida a un cliente después de que entre en el vestíbulo. A continuación, envía un correo electrónico de descuento en la comida solo si el cliente entra en el restaurante dentro del día siguiente. Por lo tanto, configuramos el evento del restaurante con un tiempo de espera de 1 día:

* Si el evento del restaurante se recibe menos de 1 día después del correo electrónico de bienvenida, se envía el correo electrónico de descuento en la comida.
* Si no se recibe ningún evento de restaurante al día siguiente, la persona pasa por la ruta de tiempo de espera.

Tenga en cuenta que si desea configurar un tiempo de espera en varios eventos colocados después de una actividad de **[!UICONTROL Wait]**, solo debe configurar el tiempo de espera en uno de estos eventos.

El tiempo de espera definido se aplica a todos los eventos colocados después de la actividad **[!UICONTROL Wait]**:

* Si se recibe un evento dentro de la duración del tiempo de espera, el individuo fluye a la ruta del evento recibido.
* Si no se recibe ningún evento dentro de la duración del tiempo de espera, el individuo fluye a la rama de tiempo de espera del evento en la que se ha definido el tiempo de espera.

![Varios eventos con configuraciones de tiempo de espera en el recorrido](assets/event-timeout-group.png)

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo usar eventos generales (unitarios y empresariales) en recorrido para almacenar en déclencheur la entrega de mensajes en tiempo real a nivel individual, incluido cómo configurar tiempos de espera de evento y rutas de tiempo de espera.

**Intenciones:**
* Añada una actividad de evento general a un lienzo de recorrido para almacenar en déclencheur la entrada de perfil en tiempo real
* Configuración del tiempo de espera de un evento para limitar la duración de la escucha de un evento por parte de un recorrido
* Configure una ruta de tiempo de espera para administrar perfiles que no almacenen en déclencheur el evento esperado a tiempo
* Distinguir entre eventos unitarios y eventos empresariales, y comprender cuándo se agregan automáticamente
* Combine tiempos de espera de evento con actividades de espera para controlar el comportamiento del tiempo de espera de varios eventos

**Glosario:**
* **Evento unitario**: evento que almacena en déclencheur el recorrido de un individuo a la vez, en tiempo real *(específico del producto)*
* **Evento empresarial**: evento no relacionado con perfiles que déclencheur un recorrido para una audiencia de perfiles y agrega automáticamente una actividad Leer audiencia *(específica del producto)*
* **Tiempo de espera del evento**: Un tiempo configurable (hasta 90 días) después del cual el recorrido deja de esperar un evento específico y enruta el perfil a una ruta de tiempo de espera *(específica del producto)*
* **Ruta de tiempo de espera**: Una rama de recorrido opcional que los perfiles siguen cuando el evento esperado no se recibe dentro de la ventana de tiempo de espera *(específico del producto)*

**Protecciones:**
* La etiqueta y la descripción del evento son los únicos campos editables para un evento general en el lienzo; el resto de la configuración la realiza un usuario técnico y no se puede cambiar desde el recorrido
* La duración máxima del tiempo de espera del evento es de 90 días
* Cuando hay varios eventos después de una actividad Wait, el tiempo de espera debe configurarse solo en uno de esos eventos; el tiempo de espera definido se aplica a todos los eventos después de Wait
* Si no se define ninguna ruta de tiempo de espera, el tiempo de espera actúa como una actividad de Espera; los perfiles que no reciben el evento permanecen en la recorrido hasta que transcurre el tiempo de espera

**Terminología:**
* Nombre canónico: General event — Acrónimo: none — variantes: unitary event, custom event
* Sinónimos: &quot;evento general&quot; = &quot;evento unitario&quot; (en el contexto de la actividad de lienzo)
* No confunda: &quot;evento empresarial&quot; ≠ &quot;evento unitario&quot;: un evento empresarial se dirige a una audiencia de perfiles, mientras que un evento unitario se dirige a una sola persona

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Puedo cambiar la configuración del evento desde el lienzo de recorrido?** — No; solo la etiqueta y la descripción pueden editarse en el lienzo. La configuración completa del evento la establece un usuario técnico y no se puede modificar desde la recorrido.
* **Q: ¿Qué sucede si no se recibe ningún evento antes de que expire el tiempo de espera?** — Si se define una ruta de tiempo de espera, el perfil fluye a esa ruta. Si no se establece ninguna ruta de tiempo de espera, el tiempo de espera se comporta como una actividad de Espera y el perfil continúa el recorrido después del período de tiempo de espera.
* **Q: ¿Cuál es la duración máxima del tiempo de espera del evento?** — 90 días.
* **Q: ¿Cuándo debo habilitar la opción de ruta de tiempo de espera?** — Habilítelo siempre si desea que los perfiles salgan de esa rama después del tiempo de espera; sin una ruta de tiempo de espera, los perfiles permanecen en el recorrido esperando el evento.
* **Q: ¿En qué se diferencia un evento empresarial de un evento unitario en el lienzo de recorrido?** — Al eliminar un evento empresarial, se añade automáticamente una actividad Leer audiencia, ya que los eventos empresariales se dirigen a varios perfiles simultáneamente, en lugar de a un único individuo.

+++
