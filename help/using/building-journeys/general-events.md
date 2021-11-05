---
solution: Journey Orchestration
title: Eventos generales
description: Aprenda a utilizar eventos generales
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: b1813122-7031-452e-9ac5-a4ea7c6dc57c
source-git-commit: 3c21d797c85c2dabbec77f109b160fbd77170da5
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 1%

---

# Eventos generales {#section_ofg_jss_dgb}

Para este tipo de evento, solo puede añadir una etiqueta y una descripción. El resto de la configuración no se puede editar. Lo realizó el usuario técnico. Consulte [esta página](../event/about-events.md).

![](../assets/general-events.png)

Cuando se coloca un evento empresarial, se agrega automáticamente un **Leer segmento** actividad. Para obtener más información sobre los eventos comerciales, consulte [esta sección](../event/about-events.md)

## Listening to events during a specific time {#events-specific-time}

Una actividad de evento ubicada en el recorrido escucha eventos indefinidamente. Para escuchar un evento solo durante un tiempo determinado, debe configurar un tiempo de espera para el evento.

El recorrido escuchará el evento durante el tiempo especificado en el tiempo de espera. Si se recibe un evento durante ese periodo, la persona fluirá en la ruta del evento. Si no es así, el cliente pasará a una ruta de tiempo de espera o finalizará su recorrido.

Para configurar un tiempo de espera para un evento, siga estos pasos:

1. Activate the **[!UICONTROL Define the event timeout]** option from the event properties.

1. Especifique la cantidad de tiempo que el recorrido esperará al evento.

1. If you want to send the individuals into a timeout path when no event is received within the specified timeout, enable the **[!UICONTROL Set a timeout path]** option. If this option is not enabled, the journey will end for the individual once the timeout is reached.

   ![](../assets/event-timeout.png)

En este ejemplo, el recorrido envía una primera notificación push de bienvenida a un cliente. A continuación, envía una notificación push de descuento en la comida solo si el cliente entra en el restaurante en el día siguiente. Por lo tanto, configuramos el evento del restaurante con un tiempo de espera de 1 día:

* Si el evento del restaurante se recibe menos de 1 día después de la notificación push de bienvenida, se envía la actividad push de descuento por comida.
* Si no se recibe ningún evento de restaurante en el día siguiente, la persona pasa por la ruta de tiempo de espera.

Note that if you want to configure a timeout on multiple events positioned after a **[!UICONTROL Wait]** activity, you need to configure the timeout on one of these events only.

El tiempo de espera se aplicará a todos los eventos posicionados después del **[!UICONTROL Wait]** actividad. Si no se recibe ningún evento antes del tiempo de espera especificado, las personas fluirán en una única ruta de tiempo de espera o finalizarán su recorrido.

![](../assets/event-timeout-group.png)
