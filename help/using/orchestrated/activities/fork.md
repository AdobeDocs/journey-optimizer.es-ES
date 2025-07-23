---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Bifurcación
description: Aprenda a utilizar la actividad Bifurcación en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 82%

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

+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carga de archivos](../file-upload-schema.md)</li><li>[Ingesta de datos](../ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña organizada](../gs-campaign-creation.md)<br/><br/>[Creación y programación de las campañas](../create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](../orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabajo con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](../build-query.md)<br/><br/>[Edición de expresiones](../edit-expressions.md)<br/><br/>[Resegmentación](../retarget.md) | [Introducción a las actividades](about-activities.md)<br/><br/>Actividades:<br/>[AND-join](and-join.md) - [Generar público](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades del canal](channels.md) - [Combinar](combine.md) - [Deduplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - <b>[Bifurcación](fork.md)</b> - [Reconciliación](reconciliation.md) - [Guardar público](save-audience.md) - [División](split.md) - [Esperar](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

La actividad **[!UICONTROL Bifurcación]** es un componente de **[!UICONTROL Control de flujo]** que le permite crear varias transiciones de salida, lo que permite que varias actividades se ejecuten en paralelo.

## Configuración de la actividad Bifurcación{#fork-configuration}

Siga estos pasos para configurar la actividad **[!UICONTROL Bifurcación]**:

![](../assets/workflow-fork.png)

1. Añada una actividad **[!UICONTROL Bifurcación]** a la campaña organizada.

1. Defina una **[!UICONTROL Etiqueta]**.

1. Asigne una etiqueta a cada transición de salida. De forma predeterminada, se proporcionan dos transiciones.

1. Para quitar una transición, haga clic en el icono ![](../assets/do-not-localize/Smock_Delete_18_N.svg).

1. Si es necesario, haga clic en **[!UICONTROL Añadir transición]** para añadir una transición de salida adicional.
