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
source-git-commit: 31d9189e8afd732875556b9caaa8e874f53597bb
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 13%

---

# Eventos generales {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Eventos unitarios"
>abstract="Los eventos permiten activar sus recorridos de forma unitaria para enviar mensajes, en tiempo real, al particular que entra en el recorrido. Para este tipo de evento, solo puede añadir una etiqueta y una descripción. La configuración de eventos la realiza un ingeniero de datos y no se puede editar."

Los eventos le permiten almacenar en déclencheur sus recorridos de forma unitaria para enviar mensajes, en tiempo real, a la persona que entra en el recorrido.

Para este tipo de evento, solo puede añadir una etiqueta y una descripción. El resto de la configuración no se puede editar. Lo ha realizado el usuario técnico. Consulte [esta página](../event/about-events.md).

![](assets/general-events.png)

Cuando se elimina un evento empresarial, se agrega automáticamente un **Leer audiencia** actividad. Para obtener más información sobre los eventos empresariales, consulte [esta sección](../event/about-events.md)

## Escucha de eventos durante un tiempo específico {#events-specific-time}

Una actividad de evento colocada en el recorrido escucha eventos indefinidamente. Para escuchar un evento solo durante un tiempo determinado, debe configurar un tiempo de espera para el evento.

El recorrido escuchará el evento durante el tiempo especificado en el tiempo de espera. Si se recibe un evento durante ese período, la persona fluirá en la ruta del evento. Si no es así, el cliente fluirá a la ruta de tiempo de espera si está definida o continuará ese recorrido.

Si no se define ninguna ruta de tiempo de espera, la configuración de tiempo de espera actuará como una actividad de espera, lo que hace que el perfil espere durante un período de tiempo, que podría detenerse si se produce un evento antes del final de esa espera. Si desea que los perfiles se excluyan de ese recorrido después del tiempo de espera, deberá establecer una ruta de tiempo de espera.

Para configurar un tiempo de espera para un evento, siga estos pasos:

1. Activar el **[!UICONTROL Definir el tiempo de espera del evento]** en las propiedades de evento.

1. Especifique la cantidad de tiempo que el recorrido esperará el evento. La duración máxima es de 29 días.

1. Si desea enviar a las personas a una ruta de tiempo de espera cuando no se reciba ningún evento dentro del tiempo de espera especificado, habilite la opción **[!UICONTROL Establecer una ruta de tiempo de espera]** opción. Si esta opción no está habilitada, el recorrido continuará para el individuo una vez que se alcance el tiempo de espera.

   ![](assets/event-timeout.png)

En este ejemplo, el recorrido envía una primera notificación push de bienvenida a un cliente. A continuación, envía una notificación push de descuento en la comida solo si el cliente entra en el restaurante dentro del día siguiente. Por lo tanto, configuramos el evento del restaurante con un tiempo de espera de 1 día:

* Si el evento del restaurante se recibe menos de 1 día después de la notificación push de bienvenida, se envía la actividad push de descuento en la comida.
* Si no se recibe ningún evento de restaurante al día siguiente, la persona pasa por la ruta de tiempo de espera.

Tenga en cuenta que si desea configurar un tiempo de espera en varios eventos colocados después de una **[!UICONTROL Esperar]** actividad, solo debe configurar el tiempo de espera en uno de estos eventos.

El tiempo de espera se aplicará a todos los eventos colocados después de **[!UICONTROL Esperar]** actividad. Si no se recibe ningún evento antes del tiempo de espera especificado, los individuos fluirán en una sola ruta de tiempo de espera o continuarán ese recorrido a través de la rama que sale de la actividad en la que se han definido esos ajustes de tiempo de espera.

![](assets/event-timeout-group.png)
