---
solution: Journey Optimizer
product: journey optimizer
title: fin de recorrido
description: Descubra cómo termina un recorrido en Journey Optimizer
feature: Journeys
role: User
level: Intermediate
keywords: volver a entrar, recorrido, finalizar, en directo, detener
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: a536336ec7b37ffa0cd860c2c7479c75365eff00
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Finalizar un recorrido {#journey-ending}

Un recorrido puede finalizar para un individuo en dos contextos específicos:

* El individuo alcanza la última actividad de una ruta y luego se mueve a la [etiqueta final](#end-tag).
* El individuo alcanza una actividad **Condition** (o una actividad **Wait** con una condición) y no coincide con ninguna de las condiciones.

El usuario puede volver a entrar en el recorrido si se le permite volver a entrar. Ver [esta página](../building-journeys/journey-properties.md#entrance)

Para finalizar un recorrido activo, le recomendamos que lo cierre. La llegada de nuevos clientes al recorrido se bloqueará. Los perfiles que ya han introducido en el recorrido pueden experimentarlo hasta el final. Ver [esta sección](#close-journey)

Sólo puede detener un recorrido si se ha producido una emergencia y es necesario finalizar inmediatamente todo el procesamiento en un recorrido. Las personas que ya han entrado en un recorrido se detienen en su progreso. Ver [esta sección](../building-journeys/journey.md#stop-journey)

>[!IMPORTANT]
>
>No puede reiniciar un recorrido [cerrado](#close-journey) o [detenido](#stop-journey).


## Etiqueta de fin de recorrido {#end-tag}

Durante la creación de un recorrido, se muestra una etiqueta Fin al final de cada ruta. Este nodo no lo puede añadir un usuario, no se puede eliminar y solo se puede cambiar su etiqueta. Marca el final de cada trayectoria del recorrido. Si el recorrido tiene varias rutas, le recomendamos que agregue una etiqueta a cada extremo para facilitar la lectura de los informes. Más información sobre [informes de recorrido](../reports/live-report.md).

![](assets/journey-end.png)

## Cerrar un recorrido {#close-journey}

Un recorrido se puede cerrar por los siguientes motivos:

* El recorrido se cierra manualmente mediante el botón [**[!UICONTROL Cerrar a nuevas entradas]**](#close-to-new-entrances).
* Un recorrido basado en segmentos de una sola toma que ha terminado de ejecutarse y ha alcanzado el tiempo de espera global de 91 días.
* Después de la última aparición de un recorrido recurrente basado en audiencias.

Cerrar un recorrido manualmente garantiza que los clientes que ya han introducido el recorrido puedan finalizar su ruta, pero que los nuevos usuarios no puedan entrar en el recorrido. Cuando un recorrido está cerrado (por cualquiera de las razones anteriores), tendrá el estado **[!UICONTROL Cerrado]**. El recorrido deja de permitir que nuevas personas entren en el recorrido. Los perfiles que ya están en el recorrido pueden finalizar el recorrido normalmente. Después del tiempo de espera global predeterminado de 91 días, el recorrido cambiará al estado **Finalizado**.

Después del tiempo de espera global de recorrido de **91 días**, un recorrido de audiencia de lectura cambia al estado **Finalizado**. Este comportamiento se establece para 91 días, ya que toda la información sobre los perfiles que ingresaron al recorrido se elimina 91 días después de haber ingresado. Las personas que siguen en el recorrido se ven afectadas automáticamente. Salen del recorrido después del tiempo de espera de 91 días.  Más información sobre [el tiempo de espera global de recorrido](../building-journeys/journey-properties.md#global_timeout).

No se puede reiniciar ni eliminar una versión de recorrido cerrado. Puede crear una nueva versión del mismo o duplicarlo. Solo se pueden eliminar los recorridos finalizados.

### Cerca de nuevas entradas {#close-to-new-entrances}

Para cerrar un recorrido de la lista de recorridos, haga clic en el botón **[!UICONTROL Puntos suspensivos]** que se encuentra a la derecha del nombre del recorrido y seleccione **[!UICONTROL Cerca de nuevas entradas]**.

![](assets/journey-finish-quick-action.png)

También puede:

1. En la lista **[!UICONTROL Recorridos]**, haga clic en el recorrido que desee cerrar.
1. En la parte superior derecha, haga clic en la flecha hacia abajo.

   ![](assets/finish_drop_down_list.png)

1. Haga clic en **[!UICONTROL Cerrar a nuevas entradas]** y confirme en el cuadro de diálogo.

>[!TIP]
>
>Un recorrido basado en segmentos de una sola toma mantiene el estado **Activo** incluso después de ejecutarse una vez. Los perfiles no volverán a entrar una vez que se hayan completado, pero el recorrido permanecerá en el estado **Activo** hasta que caduque el tiempo de espera global predeterminado. Puede cerrarlo antes manualmente con la opción **Cerrar a nuevas entradas**.


## Detener un recorrido {#stop-journey}

En caso de que necesite detener el progreso de todos los individuos en el recorrido, puede detenerlo. Deteniendo el tiempo de espera de recorrido de todos los individuos del recorrido. Sin embargo, detener un recorrido implica que todas las personas que ya han entrado en un recorrido se detengan en su progreso. El recorrido está básicamente apagado. Si desea finalizar un recorrido, se recomienda [cerrarlo](#close-journey).

Cuando está detenido, el estado del recorrido se establece en **[!UICONTROL Detenido]**.

Puede detener un recorrido, por ejemplo, si un experto en marketing se da cuenta de que el recorrido se dirige a la audiencia incorrecta o si una acción personalizada que se supone que debe enviar mensajes no funciona correctamente. Para detener un recorrido de la lista de recorridos, haga clic en el botón **[!UICONTROL Puntos suspensivos]** que se encuentra a la derecha del nombre del recorrido y seleccione **[!UICONTROL Detener]**.

![](assets/journey-finish-quick-action.png)

También puede:

1. En la lista **[!UICONTROL Recorridos]**, haga clic en el recorrido que desee detener.
1. En la parte superior derecha, haga clic en la flecha hacia abajo.

   ![](assets/finish_drop_down_list2.png)

1. Haga clic en **[!UICONTROL Detener]** y confirme en el cuadro de diálogo.
