---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con actividades de campaña organizadas
description: Obtenga información sobre cómo organizar actividades de campaña
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
version: Campaign Orchestration
source-git-commit: 4d5505cbb46bdff846218bfc3657c6a6e5447af3
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 61%

---


# Acerca de las actividades de campaña organizadas {#orchestrated-campaign-activities}

Las actividades de las campañas organizadas se agrupan en tres categorías. Dependiendo del contexto, las actividades disponibles pueden diferir.

Todas las actividades se detallan en las secciones siguientes:

* [Actividades de segmentación](#targeting)
* [Actividades del canal](#channel)
* [Actividades de control de flujo](#flow-control)

![Lista de actividades disponibles en el lienzo](../assets/orchestrated-activities.png){width="80%" align="left"}


>[!NOTE]
>
>* Según el modelo de licencia, los permisos y la implementación, las actividades disponibles pueden diferir.
>
>* El número de actividades en una campaña orquestada está limitado a 500.


## Actividades de segmentación {#targeting}

Estas actividades son específicas de la segmentación. Le permiten crear uno o más públicos destinatarios al definir públicos y dividirlos o combinarlos mediante operaciones de intersección, unión o exclusión.

![Lista de actividades de segmentación](../assets/targeting-activities.png){width="40%" align="left"}

Las actividades de segmentación disponibles son:

* [Generar público](build-audience.md): defina la población de destinatarios. Puede seleccionar un público destinatario existente o utilizar el generador de reglas para definir su propia consulta.
* [Cambiar dimensión](change-dimension.md): cambie la dimensión de segmentación mientras está creando su campaña orquestada.
* [Combinar](combine.md): realice la segmentación en la población entrante. Puede utilizar una unión, una intersección o una exclusión.
* [Deduplicación](deduplication.md): elimine duplicados en los resultados de las actividades entrantes.
* [Enrichment](enrichment.md): defina datos adicionales para procesar en su campaña orquestada. Con esta actividad, puede aprovechar la transición entrante y configurar la actividad para completar la transición saliente con datos adicionales.
* [Reconciliación](reconciliation.md): defina el vínculo entre los datos de Journey Optimizer y los datos de una tabla de trabajo, por ejemplo, los datos cargados desde un archivo externo.
* [División](split.md): segmente la población entrante en varios subconjuntos.

## Actividades del canal {#channel}

Adobe Journey Optimizer le permite automatizar y ejecutar campañas de marketing en múltiples canales. Puede combinar [actividades de canal](channels.md) en el lienzo para crear campañas orquestadas en canales múltiples que puedan almacenar en déclencheur acciones basadas en el comportamiento de los clientes.

Aprenda a [crear una acción de canal en una campaña organizada](channels.md).

## Actividades de control de flujo {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Actividad Finalizar"
>abstract="La actividad **Finalizar** le permite marcar de forma gráfica el final de una campaña orquestada. Esta actividad no tiene impacto funcional y, por lo tanto, es opcional."

Las siguientes actividades son específicas para organizar y ejecutar campañas orquestadas. Su principal tarea es coordinar las demás actividades.

![Lista de actividades de control de flujo](../assets/flow-control-activities.png){width="20%" align="left"}

Las actividades de control de flujo disponibles son:

* [And-join](and-join.md): sincronice varias ramas de ejecución de una campaña orquestada.
* [Bifurcación](fork.md): crear transiciones de salida para iniciar varias actividades al mismo tiempo.
* [Espera](wait.md): Pone en pausa momentáneamente la ejecución de una parte de una campaña orquestada.
  <!--* [Test](test.md): Enable transitions based on specified conditions.-->

>[!NOTE]
>La actividad **End** marca de forma gráfica el final de una campaña orquestada. Esta actividad no tiene impacto funcional y, por lo tanto, es opcional.
