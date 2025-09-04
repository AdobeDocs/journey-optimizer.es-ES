---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Bifurcación
description: Aprenda a utilizar la actividad Bifurcación en una campaña orquestada
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 86%

---


# Bifurcación {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="Actividad de bifurcación"
>abstract="La actividad de **bifurcación** permite crear transiciones salientes para iniciar varias actividades al mismo tiempo."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="Transiciones de la actividad de bifurcación"
>abstract="De forma predeterminada, se crean dos transiciones con una actividad de **bifurcación**. Haga clic en el botón **Añadir transición** para definir una transición de salida adicional e introducir su etiqueta."

La actividad **[!UICONTROL Bifurcación]** es un componente de **[!UICONTROL Control de flujo]** que le permite crear varias transiciones de salida, lo que permite que varias actividades se ejecuten en paralelo.

## Configuración de la actividad Bifurcación{#fork-configuration}

Siga estos pasos para configurar la actividad **[!UICONTROL Bifurcación]**:

![](../assets/workflow-fork.png)

1. Agregue una actividad **[!UICONTROL Fork]** a su campaña orquestada.

1. Defina una **[!UICONTROL Etiqueta]**.

1. Asigne una etiqueta a cada transición de salida. De forma predeterminada, se proporcionan dos transiciones.

1. Para quitar una transición, haga clic en el icono ![](../assets/do-not-localize/Smock_Delete_18_N.svg).

1. Si es necesario, haga clic en **[!UICONTROL Añadir transición]** para añadir una transición de salida adicional.
