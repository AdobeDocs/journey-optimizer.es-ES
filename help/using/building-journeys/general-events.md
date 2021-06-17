---
solution: Journey Orchestration
title: Eventos generales
description: Aprenda a utilizar eventos generales
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: 285942ec51859a4cea888d9974f79f52acf3aabf
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 2%

---

# Eventos generales {#section_ofg_jss_dgb}

Para este tipo de evento, solo puede añadir una etiqueta y una descripción. El resto de la configuración no se puede editar. Lo realizó el usuario técnico. Consulte [esta página](../event/about-events.md).

![](../assets/general-events.png)

Cuando se coloca un evento comercial, se agrega automáticamente una actividad **Leer segmento**. Para obtener más información sobre los eventos comerciales, consulte [esta sección](../event/about-events.md)

## Escucha de eventos durante una hora específica {#events-specific-time}

Una actividad de evento ubicada en el recorrido escucha eventos indefinidamente. Para escuchar un evento solo durante un tiempo determinado, debe configurar un tiempo de espera para el evento.

El recorrido escuchará el evento durante el tiempo especificado en el tiempo de espera. Si se recibe un evento durante ese periodo, la persona fluirá en la ruta del evento. Si no es así, el cliente pasará a una ruta de tiempo de espera o finalizará su recorrido.

Para configurar un tiempo de espera para un evento, siga estos pasos:

1. Active la opción **[!UICONTROL Define the event timeout]** en las propiedades de evento.

1. Especifique la cantidad de tiempo que el recorrido esperará al evento.

1. Si desea enviar a las personas a una ruta de tiempo de espera cuando no se reciba ningún evento dentro del tiempo de espera especificado, habilite la opción **[!UICONTROL Set a timeout path]**. Si esta opción no está activada, el recorrido finalizará para el individuo una vez que se alcance el tiempo de espera.

   ![](../assets/event-timeout.png)

En este ejemplo, el recorrido envía una primera notificación push de bienvenida a un cliente. A continuación, envía una notificación push de descuento en la comida solo si el cliente entra en el restaurante en el día siguiente. Por lo tanto, configuramos el evento del restaurante con un tiempo de espera de 1 día:

* Si el evento del restaurante se recibe menos de 1 día después de la notificación push de bienvenida, se envía la actividad push de descuento por comida.
* Si no se recibe ningún evento de restaurante en el día siguiente, la persona pasa por la ruta de tiempo de espera.

Tenga en cuenta que si desea configurar un tiempo de espera en varios eventos posicionados después de una actividad **[!UICONTROL Wait]** , debe configurar el tiempo de espera solo en uno de estos eventos.

El tiempo de espera se aplicará a todos los eventos posicionados después de la actividad **[!UICONTROL Wait]**. Si no se recibe ningún evento antes del tiempo de espera especificado, las personas fluirán en una única ruta de tiempo de espera o finalizarán su recorrido.

![](../assets/event-timeout-group.png)
