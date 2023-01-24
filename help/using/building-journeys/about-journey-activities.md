---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a actividades de recorrido
description: Introducción a actividades de recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, actividades, introducción, eventos, acción
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 17%

---

# Introducción a actividades de recorrido {#about-journey-activities}

Combine las distintas actividades de evento, orquestación y acción para crear sus escenarios de canal cruzado de varios pasos.

## Actividades de eventos {#event-activities}

Los eventos son los déclencheur de un recorrido personalizado, como una compra en línea. Una vez que alguien entra en un recorrido, se mueve como individuo, y no hay dos individuos que se muevan a la misma velocidad o a lo largo de la misma ruta. Cuando se inicia el recorrido con un evento, el recorrido se activa cuando se recibe el evento. Cada persona del recorrido sigue, individualmente, los siguientes pasos definidos en el recorrido.

Eventos configurados por el usuario técnico (consulte [esta página](../event/about-events.md)) se muestran en la primera categoría de la paleta, en la parte izquierda de la pantalla. Las siguientes actividades de eventos están disponibles:

* [Eventos generales](../building-journeys/general-events.md)
* [Reacción](../building-journeys/reaction-events.md)
* [Clasificación del segmento](../building-journeys/segment-qualification-events.md)

![](assets/journey43.png)

Inicie el recorrido arrastrando y soltando una actividad de evento. También puede hacer doble clic en él.

![](assets/journey44.png)

## Actividades de orquestación {#orchestration-activities}

Las actividades de organización son condiciones diferentes que ayudan a determinar el siguiente paso del recorrido. Puede ser si la persona tiene un caso de soporte abierto o no, el pronóstico del tiempo en su ubicación actual, si completó una compra o no, o si alcanzó 10 000 puntos de lealtad.

En la paleta, en la parte izquierda de la pantalla, están disponibles las siguientes actividades de organización:

* [Condición](../building-journeys/condition-activity.md)
* [Espera](../building-journeys/wait-activity.md)
* [Leer segmento](../building-journeys/read-segment.md)

![](assets/journey49.png)

## Actividades de acción {#action-activities}

Las acciones son lo que desea que ocurra como resultado de algún tipo de déclencheur, como enviar un mensaje. Es el recorrido que experimenta el cliente.

Desde la paleta, en la parte izquierda de la pantalla, debajo **[!UICONTROL Eventos]** y **[!UICONTROL Organización]**, puede encontrar la variable **[!UICONTROL Acciones]** categoría. Las siguientes actividades de acción están disponibles:

* [Correo electrónico, SMS, push](../building-journeys/journeys-message.md)
* [Acciones personalizadas](../building-journeys/using-custom-actions.md)
* [Salto](../building-journeys/jump.md)

![](assets/journey58.png)

Estas actividades representan los diferentes canales de comunicación disponibles. Puede combinarlas para crear un escenario multicanal.

Si ha configurado acciones personalizadas, estas también aparecerán aquí. [Más información](../building-journeys/using-custom-actions.md)).

## Prácticas recomendadas {#best-practices}

La mayoría de las actividades le permiten definir un **[!UICONTROL Etiqueta]**. Esto agrega un sufijo al nombre que aparecerá debajo de la actividad en el lienzo. Esto resulta útil si utiliza la misma actividad varias veces en el recorrido y desea identificarlos más fácilmente. También facilitará la depuración en caso de errores y facilitará la lectura de los informes. También puede añadir una **[!UICONTROL Descripción]**.

![](assets/journey59bis.png)

Cuando se produce un error en una acción o condición, se detiene el recorrido de un individuo. La única manera de continuar es marcar la casilla **[!UICONTROL Añada una ruta alternativa en caso de tiempo de espera o error]**. Consulte [esta sección](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
