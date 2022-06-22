---
title: Finalización de un recorrido
description: Finalización de un recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: d0d914156eaa7fe54a513ee7b4e870edbc76c846
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 2%

---

# Ciclo de vida del recorrido{#journey-lifecyle}

## Perfiles en recorridos{#profile-journey}

En un recorrido unitario:

* Si la reentrada está activada, un perfil puede introducir un recorrido varias veces, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido.

* Si la reentrada está desactivada, un perfil no puede introducir varias veces el mismo recorrido

Para obtener más información sobre la reentrada de perfiles, consulte esta [sección](../building-journeys/journey-gs.md#change-properties).

En un recorrido de segmento de lectura:

* Para recorridos no recurrentes: el perfil se introduce una vez y solo una vez en el recorrido.
* para recorridos recurrentes: el perfil introduce el recorrido en cada recurrencia, si se encuentra en el estado esperado o del segmento. Si todavía estaba en el recorrido por una recurrencia anterior, lo reiniciará desde el principio.

En los recorridos de evento empresarial que comienzan con un segmento de lectura :

Sabiendo que este recorrido se basa en la recepción de un evento empresarial, si el perfil está cualificado en el segmento esperado, introducirá el recorrido para cada evento comercial recibido, lo que significa que este perfil puede estar varias veces en el mismo recorrido, al mismo tiempo, pero en el contexto de diferentes eventos comerciales.

## final de recorrido{#journey-ending}

Un recorrido puede finalizar para un individuo en dos contextos específicos:

* La persona llega a la última actividad de una ruta.
* La persona llega a un **Condición** actividad (o **Espera** actividad con una condición) y no coincide con ninguna de las condiciones.

La persona puede volver a entrar en el recorrido si se permite la reentrada. Consulte [esta página](../building-journeys/journey-gs.md#change-properties)

Para finalizar un recorrido activo, le recomendamos que lo cierre. La llegada de nuevos clientes al recorrido será bloqueada. Los clientes que ya han entrado en el recorrido pueden experimentarlo hasta el final. Consulte [esta sección](../building-journeys/journey-end.md#close-journey)

Puede detener un recorrido solo si se ha producido una emergencia y todo el procesamiento debe finalizar inmediatamente en un recorrido. A las personas que ya entraron en un recorrido se les detiene el progreso. Consulte [esta sección](../building-journeys/journey-end.md#stop-journey)

>[!NOTE]
>
>Tenga en cuenta que no puede reanudar un recorrido cerrado o detenido.

<!--

### Journey end tag{#end-tag}

While authoring a journey, an "end node" is displayed at the end of each path. This node cannot be added by a user, cannot be removed and only its label can be changed. It marks the end of each path of the journey. If the journey has several paths, we recommend that you add a label to each end to make reports easier to read. See [this page](../reports/live-report.md).

![](assets/journey-end.png)

-->

### Actividad final{#journey-end-activity}

La variable **[!UICONTROL End]** actividad le permite marcar el final de cada ruta del recorrido. No es obligatorio, pero se recomienda para la claridad visual. Consulte [esta página](../building-journeys/end-activity.md)

![](assets/journey54.png)

### Cierre de un recorrido{#close-journey}

Un recorrido puede cerrarse por los siguientes motivos:

* El recorrido se cierra manualmente mediante la variable **[!UICONTROL Close to new entrances]** botón.
* Un recorrido basado en segmentos de una toma que ha terminado de ejecutarse.
* Después de la última aparición de un recorrido basado en segmentos recurrentes.

Al cerrar un recorrido manualmente, se garantiza que los clientes que ya hayan entrado en el recorrido puedan finalizar su ruta, pero que los nuevos usuarios no puedan entrar en el recorrido. Cuando se cierra un recorrido (por cualquiera de los motivos anteriores), aparece el estado **[!UICONTROL Closed]**. El recorrido deja de permitir que entren nuevos individuos en el recorrido. Las personas que ya están en el recorrido pueden terminar el recorrido normalmente. Después del tiempo de espera global predeterminado de 30 días, el recorrido cambiará a la variable **Finalizado** estado. Consulte esta [sección](../building-journeys/journey-gs.md#global_timeout).

No se puede reiniciar ni eliminar una versión de recorrido cerrada. Puede crear una nueva versión o duplicarla. Solo se pueden eliminar los recorridos finalizados.

Para cerrar un recorrido de la lista de recorridos, haga clic en el botón **[!UICONTROL Ellipsis]** botón situado a la derecha del nombre del recorrido y seleccione **[!UICONTROL Close to new entrances]**.

![](assets/journey-finish-quick-action.png)

También puede:

1. En el **[!UICONTROL Journeys]** , haga clic en el recorrido que desee cerrar.
1. En la parte superior derecha, haga clic en la flecha hacia abajo.

   ![](assets/finish_drop_down_list.png)

1. Haga clic en **[!UICONTROL Close to new entrances]** y confirme en el cuadro de diálogo.

### Detener un recorrido{#stop-journey}

En caso de que necesite detener el progreso de todas las personas en el recorrido, puede detenerlo. Al detener el recorrido, se agotará el tiempo de espera de todas las personas del recorrido. Sin embargo, detener un recorrido implica que a las personas que ya entraron en un recorrido se les detiene en su progreso. Básicamente el recorrido está apagado. Si desea poner fin a un recorrido, le recomendamos que lo cierre.

No se puede reiniciar una versión de recorrido detenida.

Cuando se detiene, el estado del recorrido se establece en **[!UICONTROL Stopped]**.

Puede detener un recorrido, por ejemplo, si un especialista en marketing se da cuenta de que el recorrido está dirigido a una audiencia incorrecta o si una acción personalizada que supuestamente debe enviar mensajes no funciona correctamente. Para detener un recorrido de la lista de recorridos, haga clic en el botón **[!UICONTROL Ellipsis]** botón situado a la derecha del nombre del recorrido y seleccione **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

También puede:

1. En el **[!UICONTROL Journeys]** , haga clic en el recorrido que desee detener.
1. En la parte superior derecha, haga clic en la flecha abajo.

![](assets/finish_drop_down_list.png)

1. Haga clic en **[!UICONTROL Stop]** y confirme en el cuadro de diálogo.
