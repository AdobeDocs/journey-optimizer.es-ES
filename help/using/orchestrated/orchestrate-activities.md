---
solution: Journey Optimizer
product: journey optimizer
title: Creación de campañas orquestadas con Adobe Journey Optimizer
description: Aprenda a crear campañas orquestadas con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 6574735581de0872e78e8e05efea5c6a50dc59b1
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 1%

---

# Organización de actividades de campaña orquestadas {#orchestrate}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicie su primera campaña orquestada | Consultar la base de datos | Actividades de campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/>[Cree y configure la campaña](create-orchestrated-campaign.md)<br/><br/><b>[Orqueste actividades](orchestrate-activities.md)</b><br/><br/>[Envíe mensajes con campañas orquestadas](send-messages.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [División](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Una vez que haya [creado una campaña orquestada](gs-campaign-creation.md), ya sea desde el menú de campaña orquestada o dentro de una campaña, puede empezar a orquestar las diferentes tareas que realizará. Para ello, se proporciona un lienzo visual, que le permite construir un diagrama de campaña orquestado. Dentro de este diagrama, puede añadir varias actividades y conectarlas en un orden secuencial.

## Añadir actividades {#add}

En esta fase de la configuración, el diagrama se muestra con un icono de inicio que representa el principio de la campaña orquestada. Para agregar su primera actividad, haga clic en el botón **+** conectado al icono de inicio.

Aparecerá una lista de actividades que se pueden agregar al diagrama. Las actividades disponibles dependen de su posición dentro del diagrama de campaña orquestada. Por ejemplo, al agregar la primera actividad, puede iniciar la campaña orquestada segmentando una audiencia, dividiendo la ruta de la campaña orquestada o estableciendo una actividad **Wait** para retrasar la ejecución de la campaña orquestada. Por otro lado, después de una actividad **Generar audiencia**, puede refinar el segmento con actividades de segmentación, enviar una entrega a la audiencia con actividades de canal u organizar el proceso de campaña orquestado con actividades de control de flujo.

![](assets/orchestrated-start.png){zoomable="yes"}

Una vez que se ha agregado una actividad al diagrama, aparece un panel derecho que le permite configurar la actividad recién agregada con ajustes específicos. Encontrará información detallada sobre cómo configurar cada actividad en [esta sección](activities/about-activities.md).

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

Repita este proceso para agregar tantas actividades como desee según las tareas que desee que realice la campaña orquestada. Tenga en cuenta que también puede insertar una nueva actividad entre dos actividades. Para ello, haga clic en el botón **+** en la transición entre las actividades, seleccione la actividad deseada y configúrela en el panel derecho.

Para quitar una actividad, selecciónela en el lienzo y haga clic en el icono **Eliminar** en las propiedades de la actividad.

>[!TIP]
>
>Tiene la opción de personalizar el nombre de las transiciones entre cada actividad. Para ello, seleccione la transición y cambie su etiqueta en el panel derecho.

## La barra de herramientas {#toolbar}

La barra de herramientas situada en la esquina superior derecha del lienzo proporciona opciones para manipular fácilmente las actividades y navegar en el lienzo:

* **Modo de selección múltiple**: seleccione varias actividades para eliminarlas todas a la vez o cópielas y péguelas. Consulte [esta sección](#copy).
* **Rotar**: cambie el lienzo verticalmente.
* **Ajustar a pantalla**: adapta el nivel de zoom del lienzo a la pantalla.
* **Alejar** / **Acercar**: Aleja o en el lienzo.
* **Mostrar mapa**: abre una instantánea del lienzo en el que se muestra que se encuentra.

![](assets/orchestrated-toolbar.png){zoomable="yes"}{width="50%"}

## Administrar actividades {#manage}

Al agregar actividades, los botones de acción están disponibles en el panel de propiedades, lo que le permite realizar varias operaciones.

![](assets/activity-action.png){zoomable="yes"}

Puede hacer lo siguiente:

* **Eliminar** la actividad del lienzo.
* **Deshabilitar/Habilitar** la actividad. Cuando se ejecuta la campaña orquestada, las actividades deshabilitadas y las siguientes actividades en la misma ruta no se ejecutan y la campaña orquestada se detiene.
* **Pausar/reanudar** la actividad. Cuando se ejecuta la campaña orquestada, se pausa en la actividad pausada. No se ejecutan la tarea correspondiente ni todas las que la siguen en la misma ruta.
* **Copie** la actividad. Consulte [esta sección](#copy).
* Acceda a los **registros y tareas** de la actividad.

Varias actividades **Targeting**, como **Combine** o **Deduplication**, le permiten procesar la población restante e incluirla en una transición saliente adicional. Por ejemplo, si está usando una actividad **Split**, el complemento consiste en la población que no coincide con ninguno de los subconjuntos definidos anteriormente. Para usar esta capacidad, active la opción **Generar complemento**.

## Mover o copiar actividades {#move-copy}

### Copiar y pegar actividades {#copy}

Puede copiar actividades de campañas orquestadas y pegarlas en cualquier flujo de trabajo. La campaña orquestada de destino puede estar en una pestaña diferente del explorador.

Para copiar actividades, tiene dos opciones:

* copie una actividad con el botón acción.

  ![](assets/orchestrated-copy-1.png){zoomable="yes"}{width="70%"}

* copie varias actividades con el botón de la barra de herramientas.

  ![](assets/orchestrated-copy-2.png){zoomable="yes"}{width="70%"}

Para pegar las actividades copiadas, haga clic en el botón **+** de una transición y seleccione &quot;Pegar actividad X&quot;.

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

<!--
### Move activities and their child nodes {#move}

Journey Optimizer allows you to move an activity, along with the entire content of its child nodes (including all transitions and activities within it) to the end of another transition within the same orchestrated campaign.

This process disconnects the activity and everything in its outbound transition from the initial location, moving it to the new target transition.

To move an activity:

1. Select the activity you wish to move.
1. In the activity's properties pane, click the **Move** button.
1. Select the transition where you want to place the activity and its outbound transition, then confirm.

![](assets/activity-move.png)


## Execution options {#execution}

All activities allow you to manage their execution options. Select an activity and click on the **Execution options** button. This lets you define the activity's execution mode and behavior in case of errors.

![](assets/workflow-execution-options.png){zoomable="yes"}{width="70%"}


### Properties

The **Execution** field allows you to define the action to be carried out when the task is started.

The **Maximum execution duration** field allows you to specify a duration such as "30s" or "1h". If the activity is not finished after the duration specified has been elapsed, an alert is triggered. This has no impact on how the orchestrated campaign functions.

The **Time zone** field allows you to select the time zone of the activity. Adobe Journey Optimizer allows you to manage the time differences between multiple countries on the same instance. The setting applied is configured when the instance is created.

**The Affinity** field allows you to force an orchestrated campaign or an orchestrated campaign activity to execute on a particular machine. To do this, you must specify one or several affinities for the orchestrated campaign or activity in question.

The **Behavior** field allows you to define the procedure to follow if asynchronous tasks are used.

### Error management

The **In case of error** field allows you to specify the action to be carried out should the activity encounter an error.

### Initialization script

The **Initialization script** lets you initialize variables or modify activity properties. Click the **Edit code** button and type the snippet of code to execute. The script is called when the activity executes. 

## Example {#example}

Here is an orchestrated campaign example designed to send an email to all customers (other than VIP customers) with an email who are interested in coffee machines.

![](assets/workflow-example.png){zoomable="yes"}{zoomable="yes"}

To achieve this, activities below have been added:

* A **[!UICONTROL Fork]** activity that divides the orchestrated campaign into three paths (one for each set of customer),
* **[!UICONTROL Build audience]** activities to target the three sets of customers:

    * Customers with an email,
    * Customers belonging to the pre-existing "Interrested in Coffee Machine(s)" audience,
    * Customers belonging to the pre-existing "VIP ro reward" audience.

* A **[!UICONTROL Combine]** activity that groups together customers with an email and those interested in coffee machines,
* A **[!UICONTROL Combine]** activity that excludes VIP customers,
* An **[!UICONTROL Email delivery]** activity that sends an email to the resulting customers. 

Once you have completed the orchestrated campaign, add en **[!UICONTROL End]** activity at the end of the diagram. This activity allow you to visually mark the end of a workflow and has no functional impact.

After successfully designing the orchestrated campaign diagram, you can execute the orchestrated campaign and track the progress of its various tasks. [Learn how to start an orchestrated campaign and monitor its execution](start-monitor-campaigns.md)
-->