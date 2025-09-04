---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad AND-join
description: Aprenda a utilizar la actividad AND-join en una campaña organizada
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 84%

---


# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Actividad AND-join"
>abstract="La actividad **And-join** le permite sincronizar varias ramas de ejecución de una campaña orquestada. Se activa una vez que hayan finalizado todas las actividades anteriores. Esto le permite asegurarse de que determinadas actividades se completen antes de continuar con la ejecución de la campaña orquestada."

La actividad **[!UICONTROL AND-join]** es una actividad de **[!UICONTROL control de flujo]**. Permite sincronizar varias ramas de ejecución de una campaña orquestada.

Esta actividad solo activa su transición saliente una vez que se activan todas las transiciones entrantes; es decir, una vez que todas las actividades anteriores han finalizado. Esto le permite asegurarse de que ciertas actividades han finalizado antes de continuar ejecutando la campaña orquestada.

## Configuración de la actividad And-join{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Combinación de opciones"
>abstract="Seleccione las actividades que desea unir. En el menú desplegable **Conjunto principal**, elija qué población de transición entrante desea conservar."

Siga estos pasos para configurar la actividad **[!UICONTROL AND-join]**:

![](../assets/workflow-andjoin.png)

1. Añada varias actividades, como las del canal, para formar al menos dos ramas de ejecución diferentes.

1. Inserte una actividad **[!UICONTROL AND-join]** en una cualquiera de las ramas.

1. En la sección **[!UICONTROL Combinación de opciones]**, seleccione todas las actividades anteriores que desea unir.

1. En el menú desplegable **[!UICONTROL Conjunto principal]**, elija qué población de transición de entrada desea conservar.

## Ejemplo{#and-join-example}

Este ejemplo ilustra dos ramas coordinadas de la campaña, cada una con un envío por correo electrónico, una segmentada a los miembros Gold y otra a los Silver. **[!UICONTROL AND-join]** se activa una vez que se activan ambas transiciones de entrada, y el SMS se envía solo después de que se completan ambos envíos de correo electrónico, después de un retraso de 7 días.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
