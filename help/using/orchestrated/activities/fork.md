---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Bifurcación
description: Aprenda a utilizar la actividad Bifurcación en una campaña orquestada
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/b0FyVaM0LcSz1DLGd-UEhHqBqXMWcb0rbimJA6E7WOM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29c
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 77cddc86596959e06b20154c1e51c6b84375b39b
workflow-type: tm+mt
source-wordcount: 283
ht-degree: 42%

---

# Bifurcación {#fork}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a utilizar la actividad de control de flujo Fork en una campaña orquestada para crear varias transiciones salientes que ejecuten varias actividades en paralelo.

>[!ENDSHADEBOX]

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

## Ejemplos {#fork-examples}

Este es un uso típico de la actividad **[!UICONTROL Fork]**: segmentar la misma audiencia con dos canales de correo electrónico diferentes (uno de marketing y otro transaccional) para comparar el comportamiento de entrega.

Después de que una actividad de **[!UICONTROL Generar audiencia]** seleccione la población objetivo, una **[!UICONTROL bifurcación]** crea dos ramas paralelas:

* **La rama 1** se conecta a una actividad de canal de correo electrónico de marketing. Los mensajes siguen reglas comerciales estándar y se envían únicamente a perfiles de inclusión.
* **La rama 2** se conecta a una actividad de canal de correo electrónico transaccional. Los mensajes omiten las reglas comerciales y se envían a todos los perfiles independientemente del estado de inclusión.

![](../assets/workflow-fork.png)

Este patrón es útil para comprender cómo afectan los ajustes de categoría de canal al comportamiento de entrega y para enviar diferentes tipos de mensajes a la misma audiencia en una sola ejecución de campaña.
