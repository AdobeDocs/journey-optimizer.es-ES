---
solution: Journey Optimizer
product: journey optimizer
title: Acceso y administración de campañas orquestadas
description: Conozca los principios clave de la creación de campañas organizadas con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 435b4a7eee9428c7f0efeb62c72b39c0e2aaabba
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 27%

---


# Acceso y administración de campañas orquestadas {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campaña orquestada"
>abstract="En esta pantalla, puede acceder a la lista completa de campañas orquestadas, comprobar su estado actual, las fechas de la última/próxima ejecución y crear una nueva campaña orquestada."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicie su primera campaña orquestada | Consultar la base de datos | Actividades de campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/><b>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md)</b> | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Orqueste actividades](orchestrate-activities.md)<br/><br/>[Envíe mensajes con campañas orquestadas](send-messages.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [División](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Puede crear campañas orquestadas en un lienzo visual para diseñar procesos multicanal como segmentación, ejecución de campañas o procesamiento de archivos.

## Acceso a campañas organizadas

En el menú **[!UICONTROL Campañas]**, vaya a la pestaña Varios pasos para acceder a la lista completa de campañas orquestadas.

Cada campaña orquestada en la lista muestra información sobre su [estado actual](#status), la última vez que se ejecutó o modificó, y la siguiente fecha y hora de ejecución programada.

Puede personalizar las columnas mostradas haciendo clic en el icono **[!UICONTROL Configurar la columna para un diseño personalizado]** situado en la esquina superior derecha de la lista. Esto le permite agregar información adicional a la lista, como la última actividad con error para cada campaña orquestada o la dimensión de segmentación aplicada.

Además, hay una barra de búsqueda y filtros disponibles para facilitar la búsqueda dentro de la lista. Por ejemplo, puede filtrar las campañas orquestadas para mostrar solo las que pertenecen a una campaña o las procesadas durante un intervalo de fechas específico.

Para duplicar o eliminar una campaña orquestada, haga clic en el botón de puntos suspensivos y seleccione **[!UICONTROL Duplicar]** o **[!UICONTROL Eliminar]**.

>[!NOTE]
>
>Cuando una campaña orquestada está en curso, puede duplicarla, pero no puede eliminarla.

## ¿Qué hay dentro de una campaña orquestada? {#gs-ms-campaign-inside}

El lienzo de campaña orquestado es una representación de lo que se supone que debe suceder. Describe las diversas tareas que se realizan y cómo se relacionan entre sí.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Cada campaña orquestada contiene:

* **Actividades**: una actividad es una tarea que se va a realizar. Las distintas actividades disponibles se representan en el diagrama mediante iconos. Cada actividad tiene propiedades específicas y otras propiedades que son comunes a todas las actividades.

  En un diagrama de campaña orquestada, una actividad determinada puede producir varias tareas, en particular cuando hay un bucle o una acción recurrente.

* **Transiciones**: las transiciones vinculan una actividad de origen a una actividad de destino y definen su secuencia.

* **Tablas de trabajo**: la tabla de trabajo contiene toda la información que transmite la transición. Cada campaña orquestada utiliza varias tablas de trabajo. Los datos transmitidos en estas tablas se pueden utilizar en todo el ciclo de vida de la campaña organizada.

## Estados y ciclo vital {#status}

Las campañas pueden tener varios estados:

* **[!UICONTROL Borrador]**: la campaña orquestada se ha creado y guardado.
* **[!UICONTROL En curso]**: la campaña orquestada se está ejecutando.
* **[!UICONTROL Finalizado]**: la ejecución de la campaña orquestada ha finalizado.
* **[!UICONTROL En pausa]**: La campaña orquestada se ha pausado.
* **[!UICONTROL Erróneo]**: la campaña orquestada encontró un error. Abra la campaña orquestada y acceda a los registros y tareas para identificar el error y resolverlo.
