---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con actividades de campaña de varios pasos
description: Aprenda a realizar actividades de campaña de varios pasos
hide: true
hidefromtoc: true
source-git-commit: 658d82820d3f307481c44a142c38727f777fd879
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 23%

---


# Acerca de las actividades de campaña de varios pasos {#ms-campaign-activities}

Las actividades de campaña de varios pasos se agrupan en tres categorías. Dependiendo del contexto, las actividades disponibles pueden diferir.

Todas las actividades se detallan en las secciones siguientes:

* [Actividades de segmentación y administración de datos](#targeting)
* [Actividades del canal](#channel)
* [Actividades de control de flujo](#flow-control)

![](../assets/workflow-activities.png)

## Actividades de segmentación {#targeting}

Estas actividades son específicas de la segmentación. Le permiten crear uno o más públicos destinatarios al definir públicos y dividirlos o combinarlos mediante operaciones de intersección, unión o exclusión.

* [Generar audiencia](build-audience.md): defina la población objetivo. Puede seleccionar una audiencia existente o utilizar el modelador de consultas para definir su propia consulta.
* [Cambiar dimensión](change-dimension.md): cambie la dimensión de segmentación mientras está creando su campaña de varios pasos.
* [Combinar](combine.md): realice la segmentación en la población entrante. Puede utilizar una unión, una intersección o una exclusión.
* [Anulación de duplicación](deduplication.md): elimine duplicados en los resultados de las actividades entrantes.
* [Enriquecimiento](enrichment.md): defina datos adicionales para procesar en su campaña de varios pasos. Con esta actividad, puede aprovechar la transición entrante y configurar la actividad para completar la transición saliente con datos adicionales.
* [Reconciliación](reconciliation.md): defina el vínculo entre los datos de Journey Optimizer y los datos de una tabla de trabajo, por ejemplo, los datos cargados desde un archivo externo.
* [Guardar audiencia](save-audience.md): actualice una audiencia existente o cree una nueva a partir de la población calculada en sentido ascendente en una campaña de varios pasos.
* [Split](split.md): Segmente la población entrante en varios subconjuntos.

## Actividades de administración de datos {#data}

Estas actividades son específicas para manipular y enriquecer datos de población.

* [Cargar archivo](load-file.md): Trabaje con perfiles y datos almacenados en un archivo externo.
* [Actualizar datos](update-data.md): realice actualizaciones masivas en los campos de la base de datos. Varias opciones permiten personalizar la actualización de datos.

## Actividades del canal {#channel}

Adobe Journey Optimizer le permite automatizar y ejecutar campañas de marketing en varios canales. Puede combinar actividades de canal en el lienzo para crear campañas de varios pasos en canales múltiples que puedan almacenar en déclencheur acciones basadas en el comportamiento del cliente. Las siguientes actividades **Channel** están disponibles: notificaciones push por correo electrónico, SMS, Android y iOS. [Aprenda a configurar una entrega en el contexto de una campaña de varios pasos](channels.md).

## Actividades de control de flujo {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Actividad final"
>abstract="La actividad **End** le permite marcar de forma gráfica el final de una campaña de varios pasos. Esta actividad no tiene impacto funcional y, por lo tanto, es opcional."

Las siguientes actividades son específicas para organizar y ejecutar campañas de varios pasos. Su tarea principal es coordinar las otras actividades:

* [And-join](and-join.md): sincronice varias ramas de ejecución de una campaña de varios pasos.
* **Fin**: marca gráficamente el final de una campaña de varios pasos. Esta actividad no tiene impacto funcional y, por lo tanto, es opcional
* [Bifurcación](fork.md): cree transiciones salientes para iniciar varias actividades al mismo tiempo.
* [Programador](scheduler.md): Programe cuando comience la campaña de varios pasos.
* [Prueba](test.md): habilita transiciones basadas en condiciones especificadas.
* [Espera](wait.md): pausa momentáneamente la ejecución de una parte de una campaña de varios pasos.
