---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad AND-join
description: Aprenda a utilizar la actividad AND-join en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 88%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Actividad AND-join"
>abstract="La actividad **And-join** le permite sincronizar varias ramas de ejecución de una campaña orquestada. Se activa una vez que hayan finalizado todas las actividades anteriores. Esto le permite asegurarse de que determinadas actividades se completen antes de continuar con la ejecución de la campaña orquestada."


+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carga de archivos](../file-upload-schema.md)</li><li>[Ingesta de datos](../ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña organizada](../gs-campaign-creation.md)<br/><br/>[Creación y programación de las campañas](../create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](../orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabajo con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](../build-query.md)<br/><br/>[Edición de expresiones](../edit-expressions.md)<br/><br/>[Resegmentación](../retarget.md) | [Introducción a las actividades](about-activities.md)<br/><br/>Actividades:<br/><b>[AND-join](and-join.md)</b> - [Generar público](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades del canal](channels.md) - [Combinar](combine.md) - [Deduplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [Guardar público](save-audience.md) - [División](split.md) - [Esperar](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

La actividad **[!UICONTROL AND-join]** es una actividad de **[!UICONTROL control de flujo]**. Le permite sincronizar varias ramas de ejecución de una campaña organizada.

Esta actividad solo activa su transición saliente una vez que se activan todas las transiciones entrantes; es decir, una vez que todas las actividades anteriores han finalizado. Esto le permite asegurarse de que determinadas actividades se completen antes de continuar con la ejecución de la campaña organizada.

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

Este ejemplo ilustra dos ramas coordinadas de la campaña, cada una con un envío por correo electrónico, una dirigida a los miembros Gold y otra a los Silver. **[!UICONTROL AND-join]** se activa una vez que se activan ambas transiciones de entrada, y el SMS se envía solo después de que se completan ambos envíos de correo electrónico, después de un retraso de 7 días.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
