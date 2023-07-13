---
solution: Journey Optimizer
product: journey optimizer
title: fin de recorrido
description: Descubra cómo termina un recorrido en Journey Optimizer
feature: Journeys
role: User
level: Beginner
keywords: volver a entrar, recorrido, finalizar, en directo, detener
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 3%

---

# Finalizar un recorrido{#journey-ending}

Un recorrido puede finalizar para un individuo en dos contextos específicos:

* La persona llega a la última actividad de una ruta.
* La persona llega a un **Condición** actividad (o una **Esperar** actividad con una condición ) y no coincide con ninguna de las condiciones.

La persona puede volver a entrar en el recorrido si se permite la reentrada. Consulte [esta página](../building-journeys/journey-gs.md#change-properties)

Para finalizar un recorrido activo, le recomendamos que lo cierre. La llegada de nuevos clientes al recorrido se bloqueará. Los clientes que ya han introducido el recorrido pueden experimentarlo hasta el final. Consulte [esta sección](../building-journeys/journey.md#close-journey)

Sólo puede detener un recorrido si se ha producido una emergencia y es necesario finalizar inmediatamente todo el procesamiento en un recorrido. Las personas que ya han entrado en un recorrido se detienen en su progreso. Consulte [esta sección](../building-journeys/journey.md#stop-journey)

>[!NOTE]
>
>Tenga en cuenta que no puede reanudar un recorrido cerrado o detenido.

## etiqueta de fin de recorrido{#end-tag}

Durante la creación de un recorrido, se muestra una &quot;etiqueta final&quot; al final de cada ruta. Este nodo no lo puede añadir un usuario, no se puede eliminar y solo se puede cambiar su etiqueta. Marca el final de cada trayectoria del recorrido. Si el recorrido tiene varias rutas, le recomendamos que agregue una etiqueta a cada extremo para facilitar la lectura de los informes. Consulte [esta página](../reports/live-report.md).

![](assets/journey-end.png)

<!--

### End activity{#journey-end-activity}

The **[!UICONTROL End]** activity allows you to mark the end of each path of the journey. It is not mandatory but recommended for visual clarity. See [this page](../building-journeys/end-activity.md)

![](assets/journey54.png)

-->

## Cerrar un recorrido{#close-journey}

Un recorrido se puede cerrar por los siguientes motivos:

* El recorrido se cierra manualmente a través de la **[!UICONTROL Cerca de nuevas entradas]** botón.
* Un recorrido basado en segmentos de una sola toma que ha terminado de ejecutarse.
* Después de la última aparición de un recorrido recurrente basado en audiencias.

Cerrar un recorrido manualmente garantiza que los clientes que ya han introducido el recorrido puedan finalizar su ruta, pero que los nuevos usuarios no puedan entrar en el recorrido. Cuando un recorrido está cerrado (por cualquiera de los motivos anteriores), tiene el estado **[!UICONTROL Cerrado]**. El recorrido deja de permitir que nuevas personas entren en el recorrido. Las personas que ya están en el recorrido pueden terminar el recorrido normalmente. Después del tiempo de espera global predeterminado de 30 días, el recorrido cambiará a la variable **Finalizado** estado. Consulte esta [sección](../building-journeys/journey-gs.md#global_timeout).

No se puede reiniciar ni eliminar una versión de recorrido cerrado. Puede crear una nueva versión del mismo o duplicarlo. Solo se pueden eliminar los recorridos finalizados.

Para cerrar un recorrido de la lista de recorridos, haga clic en **[!UICONTROL Puntos suspensivos]** situado a la derecha del nombre del recorrido y seleccione **[!UICONTROL Cerca de nuevas entradas]**.

![](assets/journey-finish-quick-action.png)

También puede:

1. En el **[!UICONTROL Recorridos]** , haga clic en el recorrido que desee cerrar.
1. En la parte superior derecha, haga clic en la flecha hacia abajo.

   ![](assets/finish_drop_down_list.png)

1. Clic **[!UICONTROL Cerca de nuevas entradas]** y confirme en el cuadro de diálogo.

## Detener un recorrido{#stop-journey}

En caso de que necesite detener el progreso de todos los individuos en el recorrido, puede detenerlo. Al detener el recorrido, se agotará el tiempo de espera de todos los individuos del recorrido. Sin embargo, detener un recorrido implica que todas las personas que ya han entrado en un recorrido se detengan en su progreso. El recorrido está básicamente apagado. Si desea poner fin a un recorrido, le recomendamos que lo cierre.

No se puede reiniciar una versión de recorrido detenida.

Cuando está detenido, el estado del recorrido se establece en **[!UICONTROL Detenido]**.

Puede detener un recorrido, por ejemplo, si un experto en marketing se da cuenta de que el recorrido se dirige a la audiencia incorrecta o si una acción personalizada que se supone que debe enviar mensajes no funciona correctamente. Para detener un recorrido de la lista de recorridos, haga clic en **[!UICONTROL Puntos suspensivos]** situado a la derecha del nombre del recorrido y seleccione **[!UICONTROL Detener]**.

![](assets/journey-finish-quick-action.png)

También puede:

1. En el **[!UICONTROL Recorridos]** , haga clic en el recorrido que desee detener.
1. En la parte superior derecha, haga clic en la flecha hacia abajo.
   ![](assets/finish_drop_down_list.png)
1. Clic **[!UICONTROL Detener]** y confirme en el cuadro de diálogo.
