---
solution: Journey Optimizer
product: journey optimizer
title: Inicio y monitorización de campañas orquestadas con Adobe Journey Optimizer
description: Obtenga información sobre cómo iniciar y supervisar campañas orquestadas con Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 5ebc82f566d416a177a3278816c60d896a10eff6
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 7%

---

# Inicio y monitorización de las campañas orquestadas {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Publicación de la campaña orquestada"
>abstract="Para iniciar su campaña, debe publicarla. Asegúrese de que todas las advertencias se borran antes de la publicación."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organice las actividades](orchestrate-activities.md)<br/><br/><b>[Inicie y supervise la campaña](start-monitor-campaigns.md)</b><br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](activities/save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Una vez que haya creado las tareas orquestadas y diseñadas para realizarlas en el lienzo, puede publicarlas y monitorizar cómo se ejecutan.

También puede ejecutar la campaña en modo de prueba para comprobar su ejecución y el resultado de las diferentes actividades.

## Prueba de la campaña antes de publicar {#test}

Journey Optimizer le permite probar campañas orquestadas antes de lanzarse. En el modo de prueba, se ejecutan todas las actividades del lienzo excepto las actividades de **[!UICONTROL Guardar audiencia]** y las actividades del canal. No hay ningún impacto funcional en los datos o en la audiencia.

Para probar una campaña:

1. Abra la campaña organizada.
2. Haga clic en **[!UICONTROL Start]**.

![](assets/campaign-start.png){zoomable="yes"}

Cada actividad de la campaña se ejecuta secuencialmente hasta que se llega al final del diagrama. Durante la ejecución de la prueba, puede administrar la campaña mediante la barra de acciones del lienzo. A partir de ahí, puede:

* **Detener** la ejecución en cualquier momento.
* **Inicie** la ejecución de nuevo.
* **Reanudar** la ejecución si anteriormente se había pausado debido a un problema.

Si se produce un error o una advertencia durante la ejecución, se le notificará mediante el icono **[!UICONTROL Alertas]** / **[!UICONTROL Advertencia]** de la barra de herramientas de lienzo.

![](assets/campaign-warning.png){zoomable="yes"}

También puede identificar rápidamente las actividades fallidas mediante los [indicadores de estado visuales](#activities) que se muestran directamente en cada actividad. Para obtener información detallada sobre la solución de problemas, abra los registros de [campaign](#logs-tasks), que proporcionan información detallada sobre el error y su contexto.

## Publicación de la campaña {#publish}

Una vez que la campaña esté lista y probada, haga clic en **[!UICONTROL Publicar]** para activarla.

![](assets/campaign-publish.png){zoomable="yes"}

El flujo visual se reinicia y los perfiles reales comienzan a fluir a través del recorrido en tiempo real.

## Monitorización de la ejecución de campañas {#monitor}

### Monitorización del flujo visual {#flow}

Mientras se ejecuta (en modo de prueba o en directo), el flujo visual muestra cómo los perfiles se mueven a través del recorrido en tiempo real. Se muestra el número de perfiles que pasan de una tarea a otra.

![](assets/workflow-execution.png){zoomable="yes"}

Los datos que pasan de una actividad a otra a través de transiciones se almacenan en una tabla de trabajo temporal. Estos datos se pueden mostrar para cada transición. Para inspeccionar datos pasados entre actividades:

1. Seleccione una transición.
1. En el panel de propiedades, haga clic en **[!UICONTROL Vista previa del esquema]** para ver el esquema de la tabla de trabajo. Seleccione **[!UICONTROL Previsualizar resultados]** para ver los datos transportados.

![](assets/transition.png){zoomable="yes"}

### Indicadores de ejecución de actividad {#activities}

Los indicadores de estado visuales le ayudan a comprender el rendimiento de cada actividad:

| Indicador visual | Descripción |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | La actividad se está ejecutando. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | La actividad requiere su atención. Esto puede implicar confirmar el envío de una entrega o realizar la acción necesaria. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | La actividad ha encontrado un error. Para resolver el problema, abra los registros de campaña organizados para obtener más información. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | La actividad se ha ejecutado correctamente. |

### Registros y tareas {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Registros y tareas"
>abstract="La pantalla **Registros y tareas** proporciona un historial de la ejecución de la campaña orquestada, registrando todas las acciones del usuario y los errores encontrados."

La monitorización de registros y tareas es un paso clave para analizar las campañas orquestadas y asegurarse de que se ejecutan correctamente. Se puede acceder a los registros y las tareas desde el botón **[!UICONTROL Registros]**, que está disponible en los modos de prueba y en directo en la barra de herramientas de lienzo o en el panel de propiedades de cada actividad.

La pantalla **[!UICONTROL Registros y tareas]** proporciona un historial completo de la ejecución de la campaña, registrando todas las acciones del usuario y los errores encontrados.

![](assets/workflow-logs.png){zoomable="yes"}

Hay dos tipos de información disponibles:

* La ficha **[!UICONTROL Log]** contiene el historial cronológico de todas las operaciones y errores.
* La pestaña **[!UICONTROL Tareas]** detalla la secuencia de ejecución paso a paso de las actividades.

En ambas pestañas, puede elegir las columnas mostradas y su orden, aplicar filtros y utilizar el campo de búsqueda para encontrar rápidamente la información deseada.
