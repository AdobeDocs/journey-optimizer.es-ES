---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a actividades de recorrido
description: Introducción a actividades de recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: recorridos, actividades, introducción, eventos, acción
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 865f8c3a2a598bdb90ab3cb85104684c160a560f
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 17%

---

# Introducción a actividades de recorrido {#about-journey-activities}

Combine las distintas actividades de evento, orquestación y acción para crear sus escenarios de canal cruzado de varios pasos.

## Actividades de eventos {#event-activities}

Los eventos son el déclencheur de un recorrido personalizado, como una compra en línea. Una vez que alguien entra en un recorrido, se mueve como un individuo, y no dos individuos se mueven a la misma velocidad o a lo largo del mismo camino. Cuando se inicia el recorrido con un evento, el recorrido se activa cuando se recibe el evento. Cada persona del recorrido sigue, individualmente, los siguientes pasos definidos en el recorrido.

Eventos configurados por el usuario técnico (consulte [esta página](../event/about-events.md)) se muestran todos en la primera categoría de la paleta, en el lado izquierdo de la pantalla. Las siguientes actividades de eventos están disponibles:

* [Eventos generales](../building-journeys/general-events.md)
* [Reacción](../building-journeys/reaction-events.md)
* [Calificación de audiencias](../building-journeys/audience-qualification-events.md)

![](assets/journey43.png)

Inicie el recorrido arrastrando y soltando una actividad de evento. También puede hacer doble clic en él.

![](assets/journey44.png)

## Actividades de orquestación {#orchestration-activities}

Las actividades de orquestación son condiciones diferentes que ayudan a determinar el siguiente paso del recorrido. Puede ser si la persona tiene un caso de soporte abierto o no, la previsión meteorológica en su ubicación actual, si completó una compra o no, o alcanzó los 10 000 puntos de lealtad.

En la paleta, en el lado izquierdo de la pantalla, están disponibles las siguientes actividades de orquestación:

* [Condición](../building-journeys/condition-activity.md)
* [Espera](../building-journeys/wait-activity.md)
* [Leer audiencia](../building-journeys/read-audience.md)

![](assets/journey49.png)

## Actividades de acción {#action-activities}

Las acciones son lo que desea que ocurra como resultado de algún tipo de déclencheur, como enviar un mensaje. Es el recorrido que el cliente experimenta.

En la paleta, en el lado izquierdo de la pantalla, debajo de **[!UICONTROL Eventos]** y **[!UICONTROL Orquestación]**, puede encontrar el **[!UICONTROL Acciones]** categoría. Estas son las actividades de acción disponibles:

* [Correo electrónico, SMS, push](../building-journeys/journeys-message.md)
* [Acciones personalizadas](../building-journeys/using-custom-actions.md)
* [Salto](../building-journeys/jump.md)

![](assets/journey58.png)

Estas actividades representan los diferentes canales de comunicación disponibles. Puede combinarlas para crear un escenario de canales cruzados.

Si ha configurado acciones personalizadas, estas también aparecerán aquí. [Más información](../building-journeys/using-custom-actions.md)).

## Prácticas recomendadas {#best-practices}

### Añadir una etiqueta

La mayoría de las actividades de le permiten definir una **[!UICONTROL Etiqueta]**. Esto añade un sufijo al nombre que aparecerá bajo su actividad en el lienzo. Esto resulta útil si utiliza la misma actividad varias veces en el recorrido y desea identificarla más fácilmente. También facilita la depuración en caso de errores y la lectura de los informes. También puede añadir un **[!UICONTROL Descripción]**.

![](assets/journey-action-label.png)

>[!NOTE]
>
>En algunas actividades, su ID también se puede ver en el panel. Este ID se puede utilizar en los informes como una clave más estable que la etiqueta, la cual puede cambiar.

### Administrar los parámetros avanzados {#advanced-parameters}

La mayoría de las actividades muestran una serie de parámetros avanzados o técnicos que no se pueden modificar.

![](assets/journey-advanced-parameters.png)

Para mejorar la legibilidad, puede ocultar estos parámetros con la variable **[!UICONTROL Ocultar campos de solo lectura]** botón.

![](assets/journey-hide-read-only-fields.png)

En algunos contextos particulares, puede anular los valores de estos parámetros para un uso específico. Para forzar un valor, haga clic en el icono **[!UICONTROL Habilitar la sustitución de parámetros]** a la derecha del campo. [Más información](../configuration/primary-email-addresses.md#journey-parameters)

![](assets/journey-enable-parameter-override.png)

### Añadir una ruta alternativa

Cuando se produce un error en una acción o condición, se detiene el recorrido de un individuo. La única manera de continuar es marcar la casilla **[!UICONTROL Añadir una ruta alternativa en caso de tiempo de espera o error]**. Consulte [esta sección](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
