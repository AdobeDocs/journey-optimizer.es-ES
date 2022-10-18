---
solution: Journey Optimizer
product: journey optimizer
description: Obtenga información sobre las actividades de recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 239b3d72-3be0-4a82-84e6-f219e33ddca4
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 22%

---

# Acerca de las actividades de recorrido {#about-journey-activities}

Combine las distintas actividades de evento, orquestación y acción para crear sus escenarios de canal cruzado de varios pasos.

## Actividades de eventos {#event-activities}

Los eventos configurados por el usuario técnico (consulte [esta página](../event/about-events.md)) se muestran en la primera categoría de la paleta, en la parte izquierda de la pantalla. Las siguientes actividades de eventos están disponibles:

* [Eventos generales](../building-journeys/general-events.md)
* [Reacción](../building-journeys/reaction-events.md)
* [Clasificación del segmento](../building-journeys/segment-qualification-events.md)

![](assets/journey43.png)

Inicie el recorrido arrastrando y soltando una actividad de evento. También puede hacer doble clic en él.

![](assets/journey44.png)

## Actividades de organización {#orchestration-activities}

En la paleta, en la parte izquierda de la pantalla, están disponibles las siguientes actividades de organización:

* [Condición](../building-journeys/condition-activity.md)
* [Espera](../building-journeys/wait-activity.md)
* [Leer segmento](../building-journeys/read-segment.md)

![](assets/journey49.png)

## Actividades de acción {#action-activities}

Desde la paleta, en la parte izquierda de la pantalla, debajo **[!UICONTROL Eventos]** y **[!UICONTROL Organización]**, encontrará la variable **[!UICONTROL Acciones]** categoría. Las siguientes actividades de acción están disponibles:

* [Correo electrónico, SMS, push](../building-journeys/journeys-message.md)
* [Acciones personalizadas](../building-journeys/using-custom-actions.md)
* [Salto](../building-journeys/jump.md)

![](assets/journey58.png)

Estas actividades representan los diferentes canales de comunicación disponibles. Puede combinarlas para crear un escenario multicanal.

Si ha configurado acciones personalizadas, estas aparecerán aquí (consulte [esta página](../building-journeys/using-custom-actions.md)).

## Prácticas recomendadas {#best-practices}

La mayoría de las actividades le permiten definir un **[!UICONTROL Etiqueta]**. Esto agrega un sufijo al nombre que aparecerá debajo de la actividad en el lienzo. Esto resulta útil si utiliza la misma actividad varias veces en el recorrido y desea identificarlos más fácilmente. También facilitará la depuración en caso de errores y facilitará la lectura de los informes. También puede añadir una **[!UICONTROL Descripción]**.

![](assets/journey59bis.png)

Cuando se produce un error en una acción o condición, se detiene el recorrido de un individuo. La única manera de continuar es marcar la casilla **[!UICONTROL Añada una ruta alternativa en caso de tiempo de espera o error]**. Consulte [esta sección](../building-journeys/using-the-journey-designer.md#paths).

![](assets/journey42.png)
