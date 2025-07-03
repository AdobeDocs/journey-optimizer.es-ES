---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Fork
description: Aprenda a utilizar la actividad Fork en una campaña orquestada
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 30%

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

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organice las actividades](orchestrate-activities.md)<br/><br/><b>[Inicie y supervise la campaña](start-monitor-campaigns.md)</b><br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

La actividad **[!UICONTROL Fork]** es un componente de **[!UICONTROL control de flujo]** que le permite crear varias transiciones salientes, lo que permite que varias actividades se ejecuten en paralelo.

## Configuración de la actividad Fork{#fork-configuration}

Siga estos pasos para configurar la actividad **[!UICONTROL Tenedor]**:

![](../assets/workflow-fork.png)

1. Agregue una actividad **[!UICONTROL Fork]** a su campaña orquestada.

1. Definir una **[!UICONTROL etiqueta]**.

1. Asigne una etiqueta a cada transición saliente. De forma predeterminada, se proporcionan dos transiciones.

1. Para quitar una transición, haga clic en el icono ![](../assets/do-not-localize/Smock_Delete_18_N.svg).

1. Si es necesario, haga clic en **[!UICONTROL Agregar transición]** para agregar una transición saliente adicional.
