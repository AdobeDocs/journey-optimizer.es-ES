---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad AND-join
description: Aprenda a utilizar la actividad AND-join en una campaña de varios pasos
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 323472ef9d6203cbbadc44ceb17ddcc7f6207323
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 77%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Actividad AND-join"
>abstract="La actividad **And-join** le permite sincronizar varias ramas de ejecución de una campaña con varios pasos. Se activa una vez que han finalizado todas las actividades anteriores. Esto le permite asegurarse de que determinadas actividades se han completado antes de continuar con la ejecución de la campaña de varios pasos."

La actividad **Combinación-Y** es una actividad de **Control de flujo**. Permite sincronizar varias ramas de ejecución de una campaña de varios pasos.

Esta actividad solo activa su transición saliente una vez que se activan todas las transiciones entrantes; es decir, una vez que todas las actividades anteriores han finalizado. Esto le permite asegurarse de que ciertas actividades han finalizado antes de continuar ejecutando la campaña de varios pasos.

## Configuración de la actividad And-join{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Combinación de opciones"
>abstract="Seleccione las actividades que desea unir. En el menú desplegable **Conjunto principal**, elija qué población de transición entrante desea conservar."

Siga estos pasos para configurar la actividad **Combinación-Y**:

![](../assets/workflow-andjoin.png)

1. Añada varias actividades, como actividades del canal, para formar al menos dos ramas de ejecución diferentes.
1. Añada una actividad **Combinación-Y** a cualquiera de las ramas.
1. En la sección **Opciones de combinación**, compruebe todas las actividades anteriores que desee combinar.
1. En el menú desplegable **Conjunto principal**, elija qué población de transición entrante desea conservar. La transición saliente solo puede contener una de las poblaciones de transición entrantes.

## Ejemplo{#and-join-example}

El siguiente ejemplo muestra dos ramas de campaña de varios pasos con un envío de correo electrónico y SMS. La actividad Combinación-Y se activará cuando ambas transiciones entrantes estén habilitadas. Las notificaciones push solo se envían una vez finalizados ambos envíos.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
