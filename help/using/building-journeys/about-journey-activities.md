---
title: Acerca de las actividades de recorrido
description: Obtenga información sobre las actividades de recorrido
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 31%

---

# Acerca de las actividades de recorrido {#about-journey-activities}

![](../assets/do-not-localize/badge.png)

Combine las distintas actividades de evento, orquestación y acción para crear sus escenarios de canal cruzado de varios pasos.

## Actividades de eventos {#event-activities}

Los eventos configurados por el usuario técnico (consulte [esta página](../event/about-events.md)) se muestran en la primera categoría de la paleta, en la parte izquierda de la pantalla. Las siguientes actividades de eventos están disponibles:

* [Eventos generales](../building-journeys/general-events.md)
* [Reacción](../building-journeys/reaction-events.md)
* [Clasificación del segmento](../building-journeys/segment-qualification-events.md)

![](../assets/journey43.png)

Inicie el recorrido arrastrando y soltando una actividad de evento. También puede hacer doble clic en él.

![](../assets/journey44.png)

## Actividades de organización {#orchestration-activities}

En la paleta, en la parte izquierda de la pantalla, están disponibles las siguientes actividades de organización:

* [Condición](../building-journeys/condition-activity.md)
* [Fin](../building-journeys/end-activity.md)
* [Espera](../building-journeys/wait-activity.md)
* [Lectura de segmento](../building-journeys/read-segment.md)

![](../assets/journey49.png)

## Actividades de acción {#action-activities}

Desde la paleta, en el lado izquierdo de la pantalla, debajo de **[!UICONTROL Events]** y **[!UICONTROL Orchestration]**, se encuentra la categoría **[!UICONTROL Actions]**. Las siguientes actividades de acción están disponibles:

* [Mensaje](../building-journeys/journeys-message.md)
* [Acciones personalizadas](../building-journeys/using-custom-actions.md)
* [Salto](../building-journeys/jump.md)

![](../assets/journey58.png)

Estas actividades representan los diferentes canales de comunicación disponibles. Puede combinarlas para crear un escenario multicanal.

Si ha configurado acciones personalizadas, estas aparecerán aquí (consulte [esta página](../building-journeys/using-custom-actions.md)).

## Prácticas recomendadas {#best-practices}

La mayoría de las actividades le permiten definir un **[!UICONTROL Label]**. Esto agrega un sufijo al nombre que aparecerá debajo de la actividad en el lienzo. Esto resulta útil si utiliza la misma actividad varias veces en el recorrido y desea identificarlos más fácilmente. También facilitará la depuración en caso de errores y facilitará la lectura de los informes. También puede agregar un **[!UICONTROL Description]** opcional.

![](../assets/journey59bis.png)

Cuando se produce un error en una acción o condición, se detiene el recorrido de un individuo. La única manera para continuar es marcar la casilla **[!UICONTROL Add an alternative path in case of a timeout or an error]**. Consulte [esta sección](../building-journeys/using-the-journey-designer.md#paths).

![](../assets/journey42.png)
