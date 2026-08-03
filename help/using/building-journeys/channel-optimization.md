---
solution: Journey Optimizer
product: journey optimizer
title: Optimización de canal
description: Aprenda a utilizar la optimización de canales para seleccionar automáticamente el mejor canal saliente para cada cliente en función de sus preferencias o puntuaciones de tendencia predichas por IA.
feature: Journeys, Activities, Channels Activity
topic: Content Management, Artificial Intelligence
role: User
level: Intermediate
keywords: canal, optimización, preferencia, tendencia, IA, saliente, correo electrónico, push, mensaje móvil
badge: label="Disponibilidad limitada" type="Informative"
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 82f802c504dcc97e781a6f8edf6e567a4a7c627e
workflow-type: tm+mt
source-wordcount: 1219
ht-degree: 2%

---


# Optimización de canal {#channel-optimization}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a configurar un recorrido o una acción de campaña para enviar mensajes a través del mejor canal saliente para cada cliente, utilizando la clasificación manual, las preferencias de perfil o las puntuaciones de tendencia impulsadas por IA.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>La optimización de canales está disponible actualmente para un conjunto limitado de organizaciones (disponibilidad limitada). Para obtener acceso, póngase en contacto con su representante de Adobe.

La optimización del canal permite añadir varios canales salientes (correo electrónico, push, mensaje móvil) a un único recorrido o acción de campaña, y hacer que Journey Optimizer seleccione automáticamente el mejor para cada cliente en el momento del envío.

En lugar de elegir un canal por adelantado o enviar mensajes a los clientes en todos los canales a la vez, el sistema elige el canal de mayor clasificación en el que se incluye cada cliente y regresa correctamente cuando ese canal no está disponible.

➡️ [Obtenga más información acerca de la optimización de canales en este vídeo](#video)

## Mecanismos de protección y limitaciones {#limitations}

* **Canales admitidos**: solo se admiten los canales de mensajes nativos de correo electrónico, push y móviles. Otros canales salientes como WhatsApp no son compatibles. La optimización del canal requiere el uso de las funciones nativas de correo electrónico, push y mensajería móvil de Journey Optimizer; no se admite la ejecución a través de acciones personalizadas.

* **Métrica de optimización de IA**: el modelo de IA solo se optimiza para la participación (clics). No se optimiza para pedidos, ingresos u otras métricas empresariales. Si se requiere la optimización de pedidos o ingresos, el equipo de ciencia de datos puede entrenar un modelo personalizado sin conexión y aplicarlo mediante la función de atributos de perfil del cliente.

* **Se requiere rastreo de clics para la clasificación de IA**: Al utilizar la clasificación basada en el modelo de IA, el rastreo de clics debe estar habilitado para todos los canales configurados. El modelo depende de los datos de clics para calcular las puntuaciones de tendencia; si el seguimiento está deshabilitado, el modo de clasificación de IA no puede funcionar correctamente. [Aprenda a habilitar el rastreo de clics en el correo electrónico](../email/message-tracking.md)

* **Horas tranquilas**: Cuando se combinan varios canales en una sola acción, las horas silenciosas se aplican en función de la prioridad del canal: la mensajería móvil tiene prioridad, seguida de la push y luego del correo electrónico. Para utilizar diferentes configuraciones de horas de inactividad por canal, cree acciones de recorrido independientes en lugar de combinar canales en una sola acción.

  >[!NOTE]
  >
  >Se ha planificado la compatibilidad con la configuración de horas silenciosas por canal para la versión de disponibilidad general.

* **Incompatibilidad con la optimización del tiempo de envío**: actualmente [la optimización del tiempo de envío](send-time-optimization.md) y la optimización del canal no se pueden usar juntas; elija una u otra. La IU impide que se habiliten ambas funciones simultáneamente en la misma acción.

* **Eventos de reacción**: Actualmente, los eventos de reacción en el lienzo de recorrido solo hacen referencia al primer canal de una acción multicanal.

  >[!NOTE]
  >
  >La compatibilidad para seleccionar cualquier evento de reacción válido cuando hay varios canales está planificada para la versión de disponibilidad general.

## Uso de la optimización de canales en un recorrido o una campaña {#configure}

Para añadir varios canales salientes con optimización de canal a un recorrido o una campaña, siga los pasos a continuación.

>[!BEGINTABS]

>[!TAB En un recorrido]

1. Inicie el recorrido con una actividad [Event](general-events.md) o [Read Audience](read-audience.md).

1. En la sección **[!UICONTROL Acciones]** de la paleta, arrastre y suelte una actividad **[!UICONTROL Acción]** en el lienzo.

1. Seleccione un canal saliente (correo electrónico, mensaje push o móvil) y haga clic en **[!UICONTROL Agregar]**.

   ![Agregar un canal saliente a una acción de recorrido](assets/journey-channel-optimization-add-outbound.png){width="60%"}

1. Escriba una etiqueta para su acción y haga clic en **[!UICONTROL Configurar acción]**.

>[!TAB En una campaña]

1. [Cree una campaña de acción](../campaigns/create-campaign.md) y vaya a la pestaña **[!UICONTROL Acciones]**.

1. Haga clic en el botón **[!UICONTROL Agregar acción]** y seleccione un canal saliente (mensaje de correo electrónico, push o móvil).

>[!ENDTABS]

Una vez seleccionada una acción saliente en la ficha **[!UICONTROL Acciones]**, continúe con los pasos siguientes.

1. Seleccione una configuración de canal y haga clic en **[!UICONTROL Agregar acción]** para seleccionar otro canal saliente.

   ![Agregar otro canal saliente a una acción de recorrido](assets/journey-channel-optimization-add-outbound-action.png){width="1000%"}

   >[!NOTE]
   >
   >Solo se admite una acción por tipo de canal en una única acción multicanal. Por ejemplo, no se pueden agregar dos acciones de correo electrónico independientes con configuraciones diferentes.

   Puede agregar hasta tres canales salientes (**[!UICONTROL Correo electrónico]**, **[!UICONTROL Push]**, **[!UICONTROL Mensaje móvil]**) a una sola acción o campaña de recorrido.

1. En la sección **[!UICONTROL Optimización de canal]**, establezca el método para determinar cómo el sistema selecciona el mejor canal para cada cliente. [Más información](#optimization-modes)

   ![Seleccionar un modo de optimización de canal](assets/journey-channel-optimization-modes.png){width="100%"}

1. Defina el orden del canal de reserva (para métodos manuales de clasificación y preferencias del cliente) arrastrando y soltando los canales en el orden deseado. [Más información](#fallback)

   ![Reordenar la optimización manual del canal de clasificación](assets/journey-channel-optimization-manual-reorder.png){width="90%"}

1. [Guarde y publique](publish-journey.md) su recorrido, o [revise y active](../campaigns/review-activate-campaign.md) su campaña.

## Definición del método de optimización del canal {#optimization-modes}

>[!CONTEXTUALHELP]
>id="ajo_channel_optimization_method"
>title="Definición del funcionamiento de la selección de canales"
>abstract="Elija la forma en que Journey Optimizer selecciona el mejor canal para cada cliente: **Prioridad manual**: los canales se prueban en el orden definido. La disponibilidad se determina aplicando las preferencias de suscripción y las reglas de consentimiento de marketing asociadas con las configuraciones de canal seleccionadas y todas las reglas empresariales (por ejemplo, límite de frecuencia de canal) asociadas con la campaña o el recorrido. **Atributo de perfil del cliente**: el canal que coincide con la preferencia declarada del cliente en su perfil se selecciona primero. Si no se encuentra ninguna preferencia, se aplica la prioridad manual. **Optimizado para IA**: un modelo de aprendizaje automático puntúa cada canal según la participación histórica del cliente, y se selecciona el canal disponible con mayor puntuación."

<!--
Previous content for contextual help: "The customer's first available channel, based on the selected prioritization method, is used for this action. Availability is determined by the customer's subscription preferences and marketing consent rules for the selected channel configurations, as well as any business rules — such as frequency capping — configured for the campaign or journey." TBC which to keep.

Additional content for contextual help: For **Manual priority** and **Customer profile attribute** modes, Journey Optimizer falls back through your configured channel order when the top-ranked channel cannot be used. For **AI optimized**, it falls back to a random available channel."
-->

La optimización de canales admite tres modos, cada uno de los cuales utiliza un método diferente para seleccionar el mejor canal para cada cliente en el momento del envío.

### Clasificación manual {#manual-ranking}

**[!UICONTROL Prioridad manual]** es el modo predeterminado. El orden de canal preferido se define directamente en la acción. Journey Optimizer entrega a través del primer canal de su lista en el que el cliente ha elegido y no tiene límite de frecuencia, y [vuelve](#fallback) al siguiente canal si es necesario.

![Optimización manual del canal de clasificación](assets/journey-channel-optimization-manual.png){width="90%"}

Utilice este modo cuando tenga una preferencia de canal clara y coherente y no necesite personalización por perfil.

### Preferencia del cliente {#customer-preference}

Con **[!UICONTROL Atributo de perfil del cliente]** seleccionado, Journey Optimizer lee el canal preferido declarado del cliente desde su perfil, usando el atributo `preferred` en el grupo de campos XDM [Consentimientos y preferencias](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/field-groups/profile/consents). Los valores admitidos son `email`, `push` y `sms`.

![Optimización del canal de preferencias del cliente](assets/journey-channel-optimization-profile.png){width="90%"}

Si el canal preferido no está disponible (no está configurado, no se ha elegido o no tiene límite de frecuencia), Journey Optimizer vuelve al siguiente canal de la lista [alternativa](#fallback) configurada.

Utilice este modo cuando los clientes hayan declarado explícitamente su canal de comunicación preferido.

### Clasificación basada en modelos de IA {#ai-ranking}

Si selecciona **[!UICONTROL Optimizado para IA]**, Journey Optimizer utiliza un modelo de aprendizaje automático que calcula una puntuación de tendencia por canal para cada cliente en función de su participación histórica (aperturas, clics). Las puntuaciones se almacenan en el perfil del cliente y el canal con la tendencia más alta prevista se selecciona en el momento de la entrega.

![Optimización de canal de clasificación basada en modelos de IA](assets/journey-channel-optimization-ai.png){width="70%"}

Cuando un cliente no tiene un historial de participación suficiente, el sistema vuelve a un canal disponible de forma aleatoria.

Utilice este modo para permitir que AI deduzca el canal más efectivo para cada cliente sin ninguna configuración manual.

## Comportamiento de reserva {#fallback}

Independientemente del modo de optimización, Journey Optimizer vuelve al siguiente canal disponible cuando no se puede utilizar el canal de mayor clasificación. Un canal se considera no disponible cuando se aplica cualquiera de las siguientes condiciones:

* El cliente no se incluye en el canal.
* El canal no está configurado en la acción.
* El canal ha alcanzado su límite de frecuencia.
* La preferencia de perfil del cliente o la puntuación del modelo de IA para ese canal no se rellenan.

En los modos **[!UICONTROL Prioridad manual]** y **[!UICONTROL Atributo de perfil del cliente]**, la reserva sigue la lista de prioridad de canal configurada por el especialista en marketing. En **[!UICONTROL IA optimizada]**, la reserva selecciona un canal disponible aleatorio.

## Vídeo práctico {#video}

Descubra cómo la función de optimización de canales de Adobe Journey Optimizer le ayuda a llegar a los clientes en el canal más eficaz mediante el uso manual de prioridad, atributos de perfil o el modelo de IA de Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/3492135?captions=spa&quality=12)

<!--
**Related topics**

* [Use the Action activity](journey-action.md)
* [Send-Time optimization](send-time-optimization.md)
* [Content optimization](../content-management/gs-message-optimization.md)
-->

