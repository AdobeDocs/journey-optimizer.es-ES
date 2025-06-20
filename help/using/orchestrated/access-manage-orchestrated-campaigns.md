---
solution: Journey Optimizer
product: journey optimizer
title: Acceso y administración de campañas orquestadas
description: Conozca los principios clave de la creación de campañas organizadas con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b42d317-cd01-4c6a-b61e-5b03e5a8ff3c
source-git-commit: cd42bca1a36344f688b2d90e1c0b96a9ef2a53ce
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 21%

---

# Acceso y administración de campañas orquestadas {#orchestrated-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campaña orquestada"
>abstract="En esta pantalla, puede acceder a la lista completa de campañas orquestadas, comprobar su estado actual, las fechas de la última/próxima ejecución y crear una nueva campaña orquestada."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_campaign_action"
>title="Acción"
>abstract="Esta sección enumera todas las acciones utilizadas dentro de la campaña orquestada."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/><b>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md)</b> | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Orqueste actividades](orchestrate-activities.md)<br/><br/>[Envíe mensajes con campañas orquestadas](send-messages.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [División](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

## Acceso a campañas organizadas

Vaya al menú **[!UICONTROL Campañas]** y seleccione la pestaña **[!UICONTROL Orquestación]** para acceder a la lista completa de campañas orquestadas.

![imagen que muestra el inventario de campañas orquestadas](assets/inventory.png){zoomable="yes"}{zoomable="yes"}

Cada campaña orquestada en la lista muestra información como el [estado](#status) actual de la campaña, el canal asociado y las etiquetas, o la última vez que se modificó. Puede personalizar las columnas mostradas haciendo clic en el botón ![Configurar diseño](assets/do-not-localize/inventory-configure-layout.svg).

Además, hay una barra de búsqueda y filtros disponibles para facilitar la búsqueda dentro de la lista. Por ejemplo, puede filtrar las campañas orquestadas para mostrar solo las asociadas a un canal o etiqueta determinados, o las creadas durante un intervalo de fechas específico.

## ¿Qué hay dentro de una campaña orquestada? {#gs-ms-campaign-inside}

El lienzo de campaña orquestado es una representación de lo que se supone que debe suceder. Describe las diversas tareas que se realizan y cómo se relacionan entre sí.

![imagen que muestra un lienzo de campaña orquestado](assets/canvas-example.png){zoomable="yes"}{zoomable="yes"}

Cada campaña orquestada contiene:

* **Actividades**: una actividad es una tarea que se va a realizar. Las distintas actividades disponibles se representan en el diagrama mediante iconos. Cada actividad tiene propiedades específicas y otras propiedades que son comunes a todas las actividades.

  En un diagrama de campaña orquestada, una actividad determinada puede producir varias tareas, en particular cuando hay un bucle o una acción recurrente.

* **Transiciones**: las transiciones vinculan una actividad de origen a una actividad de destino y definen su secuencia.

* **Tablas de trabajo**: la tabla de trabajo contiene toda la información que transmite la transición. Cada campaña orquestada utiliza varias tablas de trabajo. Los datos transmitidos en estas tablas se pueden utilizar en todo el ciclo de vida de la campaña organizada.

## Estados de campañas {#status}

Las campañas orquestadas pueden tener varios estados:

* **[!UICONTROL Borrador]**: se ha creado la campaña orquestada. Aún no se ha publicado.
* **[!UICONTROL Publicación]**: La campaña orquestada se está publicando.
* **[!UICONTROL Activo]**: la campaña orquestada se ha publicado y se está ejecutando.
* **[!UICONTROL Programado]**: La ejecución de la campaña orquestada se ha programado.
* **[!UICONTROL Completada]**: la ejecución de la campaña orquestada ha finalizado. El estado Completado se asigna automáticamente hasta 3 días después de que una campaña haya completado el envío de mensajes sin errores.
* **[!UICONTROL Cerrada]**: este estado se muestra cuando se ha detenido una campaña recurrente.
<!--Comment une campaign devient Closed?
[CPR] : A vérifier avec Fred si cette fonctionalité est toujours d'actualité. Normalement c'est sur action de l'utilisateur sur une campaine récurrente only
= pas trouvé-->
* **[!UICONTROL Archivada]**: se archivó la campaña orquestada. Todas las campañas archivadas se eliminan en una reprogramación móvil 30 días después de la última fecha de modificación. Puede duplicar una campaña archivada si es necesario para seguir trabajando en ella.
<!--Comment une campaign devient Archived?
[CPR] : Soit par action manuel sur une campagne en statut "final" (Completed, Closed, Stopped, etc. ...)
= pas trouvé -->
* **[!UICONTROL Detenido]**: la ejecución de la campaña orquestada se ha detenido. Para volver a iniciar la campaña, debe duplicarla.

## Duplicación y eliminación de campañas orquestadas {#duplicate-delete}

En algunos casos, es posible que deba duplicar una campaña orquestada, por ejemplo para ejecutar una campaña que se haya detenido o para cambiar la frecuencia de ejecución de una campaña programada. Para ello, haga clic en la imagen ![que muestra el botón Más acciones](assets/do-not-localize/rule-builder-icon-more.svg) en el inventario de campañas y seleccione **[!UICONTROL Duplicar]**

<!--Une fois une campaign Scheduled, on ne peut plus changer l'execution frequency = la solution est de dupliquer la campaign ?
[CPR] : Actuellement oui, mais on est en discussion pour pouvoir revenir en mode "draft" et quelles seraient les actions à nouveau disponibles. A vérifier avec Fred-->

Para eliminar una campaña, haga clic en la imagen ![que muestra el botón Más acciones](assets/do-not-localize/rule-builder-icon-more.svg) y luego seleccione **[!UICONTROL Eliminar]**.

>[!NOTE]
>
>Solo se pueden eliminar **[!UICONTROL Borradores]** campañas.
