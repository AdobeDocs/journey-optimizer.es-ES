---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con actividades de campaña orquestadas
description: Aprenda a organizar actividades de campaña
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: 28284b3d42a0e78add3470ef128dd740f9cc9dfd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 29%

---

# Acerca de las actividades de campañas organizadas {#orchestrated-campaign-activities}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](../configuration-steps.md)<br/><br/>[Pasos clave para la creación de campañas orquestadas](../gs-campaign-creation.md) | [Crear una campaña orquestada](../create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](../orchestrate-activities.md)<br/><br/>[Iniciar y supervisar la campaña](../start-monitor-campaigns.md)<br/><br/>[Informes](../reporting-campaigns.md) | [Trabaje con el Modeler de consultas](../orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](../build-query.md)<br/><br/>[Editar expresiones](../edit-expressions.md) | [Empiece con las actividades](about-activities.md)<br/><br/>Actividades:<br/>[Y únase](and-join.md) - [Generar audiencia](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades de canal](channels.md) - [Combinar](combine.md) - [Anulación de duplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [División](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Las actividades de campaña organizadas se agrupan en tres categorías. Dependiendo del contexto, las actividades disponibles pueden diferir.

Todas las actividades se detallan en las secciones siguientes:

* [Actividades de segmentación](#targeting)
* [Actividades del canal](#channel)
* [Actividades de control de flujo](#flow-control)

![Lista de actividades disponibles en el lienzo](../assets/orchestrated-activities.png){width="80%" align="left"}

## Actividades de segmentación {#targeting}

Estas actividades son específicas de la segmentación. Le permiten crear uno o más públicos destinatarios al definir públicos y dividirlos o combinarlos mediante operaciones de intersección, unión o exclusión.

![Lista de actividades de segmentación](../assets/targeting-activities.png){width="40%" align="left"}

* [Generar audiencia](build-audience.md): defina la población objetivo. Puede seleccionar una audiencia existente o utilizar el modelador de consultas para definir su propia consulta.
* [Cambiar dimensión](change-dimension.md): cambie la dimensión de segmentación mientras crea la campaña orquestada.
* [Combinar](combine.md): realice la segmentación en la población entrante. Puede utilizar una unión, una intersección o una exclusión.
* [Anulación de duplicación](deduplication.md): elimine duplicados en los resultados de las actividades entrantes.
* [Enrichment](enrichment.md): defina datos adicionales para procesar en su campaña orquestada. Con esta actividad, puede aprovechar la transición entrante y configurar la actividad para completar la transición saliente con datos adicionales.
* [Reconciliación](reconciliation.md): defina el vínculo entre los datos de Journey Optimizer y los datos de una tabla de trabajo, por ejemplo, los datos cargados desde un archivo externo.
* [Split](split.md): Segmente la población entrante en varios subconjuntos.

## Actividades del canal {#channel}

Adobe Journey Optimizer le permite automatizar y ejecutar campañas de marketing en varios canales. Puede combinar actividades de canal en el lienzo para crear campañas orquestadas en canales múltiples que puedan almacenar en déclencheur acciones basadas en el comportamiento del cliente. Las siguientes actividades de **Canal** están disponibles: Correo electrónico y SMS. [Aprenda a crear una acción de canal en el contexto de una campaña organizada](channels.md).

## Actividades de control de flujo {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Actividad Finalizar"
>abstract="La actividad **Finalizar** le permite marcar de forma gráfica el final de una campaña orquestada. Esta actividad no tiene impacto funcional y, por lo tanto, es opcional."

![Lista de actividades de control de flujo](../assets/flow-control-activities.png){width="30%" align="left"}

Las siguientes actividades son específicas para organizar y ejecutar campañas orquestadas. Su tarea principal es coordinar las otras actividades:

* [And-join](and-join.md): sincronice varias ramas de ejecución de una campaña orquestada.
* [Bifurcación](fork.md): cree transiciones salientes para iniciar varias actividades al mismo tiempo.
* [Espera](wait.md): Pone en pausa momentáneamente la ejecución de una parte de una campaña orquestada.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>La actividad **End** marca de forma gráfica el final de una campaña orquestada. Esta actividad no tiene impacto funcional y, por lo tanto, es opcional
