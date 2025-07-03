---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad AND-join
description: Aprenda a utilizar la actividad AND-join en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 37%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Actividad AND-join"
>abstract="La actividad **And-join** le permite sincronizar varias ramas de ejecución de una campaña orquestada. Se activa una vez que hayan finalizado todas las actividades anteriores. Esto le permite asegurarse de que determinadas actividades se completen antes de continuar con la ejecución de la campaña orquestada."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organice las actividades](orchestrate-activities.md)<br/><br/><b>[Inicie y supervise la campaña](start-monitor-campaigns.md)</b><br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

La actividad **[!UICONTROL Combinación-Y]** es una actividad de **[!UICONTROL Control de flujo]**. Permite sincronizar varias ramas de ejecución de una campaña orquestada.

Esta actividad solo activa su transición saliente una vez que se activan todas las transiciones entrantes; es decir, una vez que todas las actividades anteriores han finalizado. Esto le permite asegurarse de que ciertas actividades han finalizado antes de continuar ejecutándose la campaña orquestada.

## Configuración de la actividad And-join{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Combinación de opciones"
>abstract="Seleccione las actividades que desea unir. En el menú desplegable **Conjunto principal**, elija qué población de transición entrante desea conservar."

Siga estos pasos para configurar la actividad **[!UICONTROL Combinación-Y]**:

![](../assets/workflow-andjoin.png)

1. Añada varias actividades, como actividades de canal, para crear al menos dos ramas de ejecución distintas.

1. Inserte una actividad **[!UICONTROL AND-join]** en una de las ramas.

1. En la sección **[!UICONTROL Combinar opciones]**, seleccione todas las actividades anteriores a las que desee unirse.

1. En el menú desplegable **[!UICONTROL Conjunto principal]**, elija la población de transición entrante que desea conservar.

## Ejemplo{#and-join-example}

Este ejemplo ilustra dos ramas de campaña coordinadas, cada una de las cuales incluye una entrega por correo electrónico, una dirigida a los miembros oro y otra plata. **[!UICONTROL AND-join]** se activa una vez que se activan ambas transiciones entrantes, y el SMS se enviará solo después de que se completen ambos envíos de correo electrónico, después de un retraso de 7 días.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
