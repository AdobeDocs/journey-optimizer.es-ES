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
source-git-commit: 5eddbb1f9ab53f1666ccd8518785677018e10f6f
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 20%

---

# Eventos generales {#general-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_custom"
>title="Eventos unitarios"
>abstract="Los eventos permiten activar sus recorridos de forma unitaria para enviar mensajes, en tiempo real, al particular que entra en el recorrido. Para este tipo de evento, solo puede añadir una etiqueta y una descripción. La configuración de eventos la realiza un ingeniero de datos y no se puede editar."

>[!CONTEXTUALHELP]
>id="ajo_journey_event_business_canvas"
>title="Eventos empresariales"
>abstract="Estos eventos le permiten iniciar un recorrido utilizando un evento no relacionado con el perfil. Cuando se active ese evento, podrá enviar mensajes a un público de perfiles. Para este tipo de evento, solo puede añadir una etiqueta y una descripción. La configuración de eventos la realiza un usuario técnico y no se puede editar."

Los eventos le permiten almacenar en déclencheur sus recorridos de forma unitaria para enviar mensajes, en tiempo real, a la persona que entra en el recorrido.

Para este tipo de evento, solo puede añadir una etiqueta y una descripción. El resto de la configuración no se puede editar. Lo ha realizado el usuario técnico. Consulte [esta página](../event/about-events.md).

Obtenga más información acerca del rendimiento de eventos y las tasas de procesamiento de recorridos en [esta sección](entry-management.md#journey-processing-rate).

![](assets/general-events.png)

Al eliminar un evento empresarial, se agrega automáticamente una actividad **Leer audiencia**. Para obtener más información sobre los eventos empresariales, consulte [esta sección](../event/about-events.md)

## Escucha de eventos durante un tiempo específico {#events-specific-time}

Una actividad de evento colocada en el recorrido escucha eventos indefinidamente. Para escuchar un evento solo durante un tiempo determinado, debe configurar un tiempo de espera para el evento.

El recorrido escuchará el evento durante el tiempo especificado en el tiempo de espera. Si se recibe un evento durante ese período, la persona fluirá en la ruta del evento. Si no es así, el cliente fluirá a la ruta de tiempo de espera si está definida o continuará ese recorrido.

Si no se define ninguna ruta de tiempo de espera, la configuración de tiempo de espera actuará como una actividad de espera, lo que hace que el perfil espere durante un período de tiempo, que podría detenerse si se produce un evento antes del final de esa espera. Si desea que los perfiles se excluyan de ese recorrido después del tiempo de espera, deberá establecer una ruta de tiempo de espera.

Para configurar un tiempo de espera para un evento, siga estos pasos:

1. Activar la opción **[!UICONTROL Definir el tiempo de espera del evento]** desde las propiedades de evento.

1. Especifique la cantidad de tiempo que el recorrido esperará el evento. La duración máxima es de **90 días**.

1. Cuando no se recibe ningún evento dentro del tiempo de espera especificado, se recomienda enviar a los individuos a una ruta de tiempo de espera. Para esto, habilite la opción **[!UICONTROL Establecer una ruta de tiempo de espera]**. En ese caso, el recorrido continúa para el individuo una vez que se alcanza el tiempo de espera. Se recomienda habilitar siempre la opción **[!UICONTROL Establecer una ruta de tiempo de espera]**.

   ![](assets/event-timeout.png)

En este ejemplo, el recorrido envía un primer correo electrónico de bienvenida a un cliente después de que entre en el vestíbulo. A continuación, envía un correo electrónico de descuento en la comida solo si el cliente entra en el restaurante dentro del día siguiente. Por lo tanto, configuramos el evento del restaurante con un tiempo de espera de 1 día:

* Si el evento del restaurante se recibe menos de 1 día después del correo electrónico de bienvenida, se envía el correo electrónico de descuento en la comida.
* Si no se recibe ningún evento de restaurante al día siguiente, la persona pasa por la ruta de tiempo de espera.

Tenga en cuenta que si desea configurar un tiempo de espera en varios eventos colocados después de una actividad de **[!UICONTROL Wait]**, solo debe configurar el tiempo de espera en uno de estos eventos.

El tiempo de espera definido se aplica a todos los eventos colocados después de la actividad **[!UICONTROL Wait]**:

* Si se recibe un evento dentro de la duración del tiempo de espera, el individuo fluye a la ruta del evento recibido.
* Si no se recibe ningún evento dentro de la duración del tiempo de espera, el individuo fluye a la rama de tiempo de espera del evento en la que se ha definido el tiempo de espera.

![](assets/event-timeout-group.png)
