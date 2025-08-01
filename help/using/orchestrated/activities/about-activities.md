---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con actividades de campaña organizadas
description: Obtenga información sobre cómo organizar actividades de campaña
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: e71cbc5b29a31e2f23b408ae8c8b73379a44275d
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 59%

---

# Acerca de las actividades de campaña organizadas {#orchestrated-campaign-activities}


+++ Índice

| Bienvenido a campañas orquestadas | Inicie su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carga de archivos](../file-upload-schema.md)</li><li>[Ingesta de datos](../ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña orquestada](../gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](../create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](../orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabajo con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](../build-query.md)<br/><br/>[Edición de expresiones](../edit-expressions.md)<br/><br/>[Resegmentación](../retarget.md) | <b>[Introducción a las actividades](about-activities.md)</b><br/><br/>Actividades:<br/>[AND-join](and-join.md) - [Generar público](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades del canal](channels.md) - [Combinar](combine.md) - [Deduplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [Guardar público](save-audience.md) - [División](split.md) - [Esperar](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

Las actividades de las campañas organizadas se agrupan en tres categorías. Dependiendo del contexto, las actividades disponibles pueden diferir.

Todas las actividades se detallan en las secciones siguientes:

* [Actividades de segmentación](#targeting)
* [Actividades del canal](#channel)
* [Actividades de control de flujo](#flow-control)

![Lista de actividades disponibles en el lienzo](../assets/orchestrated-activities.png){width="80%" align="left"}

## Actividades de segmentación {#targeting}

Estas actividades son específicas de la segmentación. Le permiten crear uno o más públicos destinatarios al definir públicos y dividirlos o combinarlos mediante operaciones de intersección, unión o exclusión.

![Lista de actividades de segmentación](../assets/targeting-activities.png){width="40%" align="left"}

* [Generar público](build-audience.md): defina la población de destinatarios. Puede seleccionar un público destinatario existente o utilizar el generador de reglas para definir su propia consulta.
* [Cambiar dimensión](change-dimension.md): cambie la dimensión de segmentación mientras está creando su campaña orquestada.
* [Combinar](combine.md): realice la segmentación en la población entrante. Puede utilizar una unión, una intersección o una exclusión.
* [Deduplicación](deduplication.md): elimine duplicados en los resultados de las actividades entrantes.
* [Enrichment](enrichment.md): defina datos adicionales para procesar en su campaña orquestada. Con esta actividad, puede aprovechar la transición entrante y configurar la actividad para completar la transición saliente con datos adicionales.
* [Reconciliación](reconciliation.md): defina el vínculo entre los datos de Journey Optimizer y los datos de una tabla de trabajo, por ejemplo, los datos cargados desde un archivo externo.
* [División](split.md): segmente la población entrante en varios subconjuntos.

## Actividades del canal {#channel}

Adobe Journey Optimizer le permite automatizar y ejecutar campañas de marketing en múltiples canales. Puede combinar actividades de canal en el lienzo para crear campañas orquestadas entre canales que puedan almacenar en déclencheur acciones basadas en el comportamiento del cliente. Las siguientes actividades de **canal** están disponibles: correo electrónico y SMS. [Aprenda a crear una acción de canal en el contexto de una campaña organizada](channels.md).

## Actividades de control de flujo {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Actividad Finalizar"
>abstract="La actividad **End** le permite marcar de forma gráfica el final de una campaña orquestada. Esta actividad no tiene impacto funcional y, por lo tanto, es opcional."

![Lista de actividades de control de flujo](../assets/flow-control-activities.png){width="30%" align="left"}

Las siguientes actividades son específicas para organizar y ejecutar campañas orquestadas. Su tarea principal es coordinar las otras actividades:

* [And-join](and-join.md): sincronice varias ramas de ejecución de una campaña orquestada.
* [Bifurcación](fork.md): crear transiciones de salida para iniciar varias actividades al mismo tiempo.
* [Espera](wait.md): Pone en pausa momentáneamente la ejecución de una parte de una campaña orquestada.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>La actividad **End** marca de forma gráfica el final de una campaña orquestada. Esta actividad no tiene impacto funcional y, por lo tanto, es opcional.
