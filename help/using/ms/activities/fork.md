---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Fork
description: Aprenda a utilizar la actividad Fork en una campaña orquestada
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 70%

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

La actividad **Fork** es una actividad de **control de flujo**. Permite crear transiciones salientes para el inicio de varias actividades al mismo tiempo.

## Configuración de la actividad Fork{#fork-configuration}

Siga estos pasos para configurar la actividad **Tenedor**:

![](../assets/workflow-fork.png)

1. Agregue una actividad **Fork** a su campaña orquestada.
1. Haga clic en **Agregar transición** para añadir una nueva transición saliente. De forma predeterminada, se definen dos transiciones.
1. Añada una etiqueta a cada una de las transiciones.

## Ejemplo{#fork-example}

En el siguiente ejemplo, utilizamos dos actividades **Tenedor**:

* Una antes de las dos consultas, para ejecutarlas al mismo tiempo.
* Una después de la intersección, para enviar un correo electrónico y un SMS simultáneamente a la población objetivo.

![](../assets/workflow-fork-example.png)
