---
solution: Journey Optimizer
product: journey optimizer
title: Creación de campañas organizadas con Adobe Journey Optimizer
description: Aprenda a generar campañas organizadas con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 855c45b5baec50865ac645eae707d5f1a5052b9b
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 86%

---

# Actividades de la campaña organizada {#orchestrate}

+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Creación y programación de las campañas](create-orchestrated-campaign.md)<br/><br/><b>[Organización de actividades](orchestrate-activities.md)</b><br/><br/>[Inicio y monitorización de las campañas](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabajo con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](build-query.md)<br/><br/>[Edición de expresiones](edit-expressions.md)<br/><br/>[Resegmentación](retarget.md) | [Introducción a las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[AND-join](activities/and-join.md) - [Generar público](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades del canal](activities/channels.md) - [Combinar](activities/combine.md) - [Deduplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar público](activities/save-audience.md) - [División](activities/split.md) - [Esperar](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

Una vez que haya [creado una campaña organizada](gs-campaign-creation.md), puede empezar a organizar las diferentes tareas que realizará. Para ello, se proporciona un lienzo visual, que le permite construir un diagrama de campaña organizada. Dentro de este diagrama, puede añadir varias actividades y conectarlas en un orden secuencial.

## Añadir actividades {#add}

En esta fase de la configuración, el diagrama se muestra con un icono de inicio que representa el principio de la campaña organizada. Para añadir su primera actividad, haga clic en el botón **+** conectado al icono de inicio.

Aparece una lista de actividades que se pueden añadir al diagrama. Las actividades disponibles dependen de su posición dentro del diagrama de campaña organizada. Por ejemplo, cuando añada la primera actividad, puede iniciar la campaña organizada segmentando un público, dividiendo la ruta de la campaña organizada o estableciendo la actividad **Esperar** para retrasar la ejecución de la campaña organizada. Por otro lado, después de la actividad **Generar público**, puede perfeccionar su objetivo con actividades de segmentación, realizar un envío a su público con actividades de canal u organizar el proceso de campaña organizada con actividades de control de flujo.

![](assets/orchestrated-start.png){zoomable="yes"}

Una vez añadida una actividad al diagrama, aparece un panel derecho que le permite configurarla con ajustes específicos. En [esta sección](activities/about-activities.md) encontrará información detallada sobre cómo configurar cada actividad.

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

Repita este proceso para añadir todas las actividades que desee en función de las tareas que quiere que realice la campaña organizada. Tenga en cuenta que también puede insertar una nueva actividad entre dos actividades. Para ello, haga clic en el botón **+** en la transición entre las actividades, seleccione la actividad deseada y configúrela en el panel derecho.

Tiene la opción de personalizar el nombre de las transiciones entre cada actividad. Para ello, seleccione la transición y cambie su etiqueta en el panel derecho.

![](assets/canvas-transition.png)

### Barra de herramientas de lienzo {#toolbar}

La barra de herramientas de lienzo proporciona opciones para manipular fácilmente las actividades y navegar en el lienzo:

![](assets/orchestrated-toolbar.png)

![Icono de modo de selección múltiple](assets/do-not-localize/canvas-multiple.svg) Seleccione varias actividades para eliminarlas todas a la vez o copiarlas y pegarlas. [Aprenda a copiar y pegar actividades](#copy)

![Icono Rotar](assets/do-not-localize/canvas-rotate.svg) Cambie el lienzo verticalmente.

![Ajustar al icono de la pantalla](assets/do-not-localize/canvas-fit.svg) Adapte el nivel de zoom del lienzo a su pantalla.

![Icono de reducir](assets/do-not-localize/canvas-zoomout.svg) ![Icono de aumentar](assets/do-not-localize/canvas-zoomin.svg) Reduzca o aumente el lienzo.

![Icono de configuración de campaña](assets/do-not-localize/canvas-map.svg) Abre una instantánea del lienzo en el que se muestra su ubicación.

### Administrar actividades {#manage}

Al añadir actividades, los botones de acción están disponibles en el panel de propiedades, lo que le permite realizar múltiiples operaciones.

![](assets/activity-action.png)

![Icono Eliminar](assets/do-not-localize/activity-delete.svg) Elimine la actividad del lienzo.

![icono Deshabilitar](assets/do-not-localize/activity-disable.svg) ![icono Habilitar](assets/do-not-localize/activity-enable.svg) Deshabilite/Habilite la actividad. Cuando se ejecuta la campaña organizada, las actividades deshabilitadas y las siguientes actividades en la misma ruta no se ejecutan y la campaña organizada se detiene.

![Icono de pausa](assets/do-not-localize/activity-pause.svg) ![Icono de reanudación](assets/do-not-localize/activity-resume.svg) Ponga en pausa/reanude la actividad. Cuando se ejecuta la campaña organizada, se pone en pausa en la actividad pausada. No se ejecutará la tarea correspondiente ni las que la siguen en la misma ruta.

Puede utilizar cualquier actividad en el lienzo como punto de interrupción para pausar la ejecución de la campaña. Esto significa que la campaña se ejecutará solamente hasta esta actividad y luego pausará la ejecución. Al pausar la ejecución, el motor de segmentación mantiene los datos temporales disponibles para que los previsualice. Puede seleccionar la transición entrante justo antes de la actividad pausada para ver los datos transportados. Obtenga más información sobre esta sección: [Supervisión de flujo visual](../orchestrated/start-monitor-campaigns.md#flow).

![Icono de copiar](assets/do-not-localize/activity-copy.svg) Copie la actividad. [Aprenda a copiar y pegar actividades](#copy)

![Icono de registros y tareas](assets/do-not-localize/activity-logs.svg) Acceda a los registros y tareas de la actividad.

Varias actividades de **Segmentación**, como **Combinar** o **Deduplicación**, le permiten procesar la población restante e incluirla en una transición de salida adicional. Por ejemplo, si está usando la actividad **División**, el complemento consiste en la población que no coincidía con ninguno de los subconjuntos definidos anteriormente. Para usar esta funcionalidad, active la opción **[!UICONTROL Generar complemento]**.

### Copiar y pegar actividades {#copy}

Puede copiar actividades y pegarlas en cualquier lienzo de la campaña organizada. La campaña de destino puede estar en una pestaña diferente del explorador.

* Para copiar una actividad, haga clic en el botón ![icono Copiar](assets/do-not-localize/activity-copy.svg) en el panel de propiedades de la actividad.
* Para copiar varias actividades, haga clic en el icono ![Icono de modo de selección múltiple](assets/do-not-localize/canvas-multiple.svg) en la barra de herramientas de lienzo.

| Copiar una actividad | Copiar varias actividades |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

Para pegar las actividades, haga clic en el botón **+** de una transición y seleccione “Pegar actividad x”.

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

## Ejemplo de diagrama {#example}

Este es un ejemplo de campaña organizada diseñada para enviar un correo electrónico a todos los clientes que han realizado una compra de al menos 100 USD, excluyendo a todos los clientes que tienen menos de 50 puntos de lealtad.

![](assets/canvas-example-diagram.png){zoomable="yes"}

Para ello, se han añadido las actividades siguientes:

* Una actividad **[!UICONTROL Bifurcación]** divide la campaña orquestada en tres rutas.
* Las actividades de **[!UICONTROL Generar público]** se dirigen a los tres grupos de clientes siguientes:

   * Clientes con un correo electrónico,
   * Clientes que han realizado una compra de al menos 100 USD,
   * Clientes que tienen menos de 50 puntos de lealtad.

* La actividad **[!UICONTROL Combinar]** agrupa a los clientes con un correo electrónico y a aquellos que han realizado una compra de al menos 100 USD,
* Una actividad **[!UICONTROL Combinar]** excluye clientes con menos de 50 puntos de lealtad,
* La actividad **[!UICONTROL Envío de correo electrónico]** envía un mensaje de correo electrónico a los clientes resultantes.

## Próximos pasos {#next}

Después de diseñar correctamente el diagrama de la campaña organizada, puede ejecutar la campaña organizada y realizar un seguimiento del progreso de sus distintas tareas. [Obtenga información sobre cómo iniciar una campaña organizada y monitorizar su ejecución](start-monitor-campaigns.md)
