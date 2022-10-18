---
solution: Journey Optimizer
product: journey optimizer
title: Finalización de un recorrido
description: Finalización de un recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 57bdeadc-5801-4036-a272-c622634d5281
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '861'
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

Los recorridos unitarios (comenzando por un evento o una calificación de segmento) incluyen una protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante 5 minutos. Por ejemplo, si un evento déclencheur un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.


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

### Recorrido final{#end-tag}

Durante la creación de un recorrido, se muestra una &quot;etiqueta final&quot; al final de cada ruta. Un usuario no puede agregar este nodo, no se puede eliminar y solo se puede cambiar su etiqueta. Marca el final de cada ruta del recorrido. Si el recorrido tiene varias rutas, le recomendamos que agregue una etiqueta a cada extremo para facilitar la lectura de los informes. Consulte [esta página](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

### Cierre de un recorrido{#close-journey}

Un recorrido puede cerrarse por los siguientes motivos:

* El recorrido se cierra manualmente mediante la variable **[!UICONTROL Cerca de nuevas entradas]** botón.
* Un recorrido basado en segmentos de una toma que ha terminado de ejecutarse.
* Después de la última aparición de un recorrido basado en segmentos recurrentes.

Al cerrar un recorrido manualmente, se garantiza que los clientes que ya hayan entrado en el recorrido puedan finalizar su ruta, pero que los nuevos usuarios no puedan entrar en el recorrido. Cuando se cierra un recorrido (por cualquiera de los motivos anteriores), aparece el estado **[!UICONTROL Cerrado]**. El recorrido deja de permitir que entren nuevos individuos en el recorrido. Las personas que ya están en el recorrido pueden terminar el recorrido normalmente. Después del tiempo de espera global predeterminado de 30 días, el recorrido cambiará a la variable **Finalizado** estado. Consulte esta [sección](../building-journeys/journey-gs.md#global_timeout).

No se puede reiniciar ni eliminar una versión de recorrido cerrada. Puede crear una nueva versión o duplicarla. Solo se pueden eliminar los recorridos finalizados.

Para cerrar un recorrido de la lista de recorridos, haga clic en el botón **[!UICONTROL Elipsis]** botón situado a la derecha del nombre del recorrido y seleccione **[!UICONTROL Cerca de nuevas entradas]**.

![](assets/journey-finish-quick-action.png)

También puede:

1. En el **[!UICONTROL Recorridos]** , haga clic en el recorrido que desee cerrar.
1. En la parte superior derecha, haga clic en la flecha hacia abajo.

   ![](assets/finish_drop_down_list.png)

1. Haga clic en **[!UICONTROL Cerca de nuevas entradas]** y confirme en el cuadro de diálogo.

### Detener un recorrido{#stop-journey}

En caso de que necesite detener el progreso de todas las personas en el recorrido, puede detenerlo. Al detener el recorrido, se agotará el tiempo de espera de todas las personas del recorrido. Sin embargo, detener un recorrido implica que a las personas que ya entraron en un recorrido se les detiene en su progreso. Básicamente el recorrido está apagado. Si desea poner fin a un recorrido, le recomendamos que lo cierre.

No se puede reiniciar una versión de recorrido detenida.

Cuando se detiene, el estado del recorrido se establece en **[!UICONTROL Detenido]**.

Puede detener un recorrido, por ejemplo, si un especialista en marketing se da cuenta de que el recorrido está dirigido a una audiencia incorrecta o si una acción personalizada que supuestamente debe enviar mensajes no funciona correctamente. Para detener un recorrido de la lista de recorridos, haga clic en el botón **[!UICONTROL Elipsis]** botón situado a la derecha del nombre del recorrido y seleccione **[!UICONTROL Stop]**.

![](assets/journey-finish-quick-action.png)

También puede:

1. En el **[!UICONTROL Recorridos]** , haga clic en el recorrido que desee detener.
1. En la parte superior derecha, haga clic en la flecha abajo.
   ![](assets/finish_drop_down_list.png)
1. Haga clic en **[!UICONTROL Stop]** y confirme en el cuadro de diálogo.
