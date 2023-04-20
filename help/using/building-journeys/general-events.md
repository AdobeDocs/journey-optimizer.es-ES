---
solution: Journey Optimizer
product: journey optimizer
title: Eventos generales
description: Aprenda a utilizar eventos generales
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: personalizado, general, eventos, recorrido
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 20%

---

# Eventos generales {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Eventos generales"
>abstract="Los Eventos le permiten activar sus recorridos de forma unitaria para enviar mensajes, en tiempo real, a la persona que entra en el recorrido. Para este tipo de evento, solo puede añadir una etiqueta y una descripción. La configuración de eventos la realiza un ingeniero de datos y no se puede editar."

Los Eventos le permiten activar sus recorridos de forma unitaria para enviar mensajes, en tiempo real, a la persona que entra en el recorrido.

Para este tipo de evento, solo puede añadir una etiqueta y una descripción. El resto de la configuración no se puede editar. Lo realizó el usuario técnico. Consulte [esta página](../event/about-events.md).

![](assets/general-events.png)

Cuando se coloca un evento empresarial, se agrega automáticamente un **Leer segmento** actividad. Para obtener más información sobre los eventos comerciales, consulte [esta sección](../event/about-events.md)

## Escucha de eventos durante un tiempo específico {#events-specific-time}

Una actividad de evento ubicada en el recorrido escucha eventos indefinidamente. Para escuchar un evento solo durante un tiempo determinado, debe configurar un tiempo de espera para el evento.

El recorrido escuchará el evento durante el tiempo especificado en el tiempo de espera. Si se recibe un evento durante ese periodo, la persona fluirá en la ruta del evento. Si no es así, el cliente pasará a una ruta de tiempo de espera o finalizará su recorrido.

Para configurar un tiempo de espera para un evento, siga estos pasos:

1. Active la variable **[!UICONTROL Definir el tiempo de espera del evento]** de las propiedades del evento.

1. Especifique la cantidad de tiempo que el recorrido esperará al evento.

1. Si desea enviar a las personas a una ruta de tiempo de espera cuando no se reciba ningún evento dentro del tiempo de espera especificado, habilite la variable **[!UICONTROL Establecer una ruta de tiempo de espera]** . Si esta opción no está activada, el recorrido finalizará para el individuo una vez que se alcance el tiempo de espera.

   ![](assets/event-timeout.png)

En este ejemplo, el recorrido envía una primera notificación push de bienvenida a un cliente. A continuación, envía una notificación push de descuento en la comida solo si el cliente entra en el restaurante en el día siguiente. Por lo tanto, configuramos el evento del restaurante con un tiempo de espera de 1 día:

* Si el evento del restaurante se recibe menos de 1 día después de la notificación push de bienvenida, se envía la actividad push de descuento por comida.
* Si no se recibe ningún evento de restaurante en el día siguiente, la persona pasa por la ruta de tiempo de espera.

Tenga en cuenta que si desea configurar un tiempo de espera en varios eventos posicionados después de una **[!UICONTROL Espera]** , debe configurar el tiempo de espera solo en uno de estos eventos.

El tiempo de espera se aplicará a todos los eventos posicionados después del **[!UICONTROL Espera]** actividad. Si no se recibe ningún evento antes del tiempo de espera especificado, las personas fluirán en una única ruta de tiempo de espera o finalizarán su recorrido.

![](assets/event-timeout-group.png)
