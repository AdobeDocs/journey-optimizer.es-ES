---
solution: Journey Optimizer
product: journey optimizer
title: Inicio y monitorización de campañas organizadas con Adobe Journey Optimizer
description: Obtenga información sobre cómo iniciar y monitorizar campañas orquestadas con Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 5e52573689ab06084441390299b01e112e699244
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 54%

---

# Inicio y monitorización de sus campañas organizadas {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Publicar campaña orquestada"
>abstract="Para iniciar su campaña, debe publicarla. Asegúrese de que se borran todos los errores antes de la publicación."

+++ Índice

| Bienvenido a campañas orquestadas | Inicie su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Creación y programación de las campañas](create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](orchestrate-activities.md)<br/><br/><b>[Inicio y monitorización de las campañas](start-monitor-campaigns.md)</b><br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabajo con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](build-query.md)<br/><br/>[Edición de expresiones](edit-expressions.md)<br/><br/>[Resegmentación](retarget.md) | [Introducción a las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[AND-join](activities/and-join.md) - [Generar público](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades del canal](activities/channels.md) - [Combinar](activities/combine.md) - [Deduplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar público](activities/save-audience.md) - [División](activities/split.md) - [Esperar](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

Una vez creada la campaña organizada y tras haber diseñado las tareas que se realizarán en el lienzo, puede publicarla y monitorizar cómo se ejecuta.

También puede ejecutar la campaña en modo de prueba para comprobar su ejecución y el resultado de las diferentes actividades.

## Prueba de la campaña antes de publicarla {#test}

[!DNL Journey Optimizer] le permite probar campañas orquestadas antes de lanzarse. Cuando se crea una campaña, entra al estado **Borrador** de forma predeterminada. En este estado, puede ejecutar la campaña manualmente para probar el flujo.

>[!IMPORTANT]
>
>Todas las actividades del lienzo se ejecutan excepto las actividades de **[!UICONTROL Guardar audiencia]** y las actividades del canal. No hay ningún impacto funcional en los datos o en la audiencia**.

Para probar una campaña, haga lo siguiente:

1. Abra la campaña orquestada.
2. Haga clic en **[!UICONTROL inicio]**.

![](assets/campaign-start.png){zoomable="yes"}

Cada actividad de la campaña se ejecuta secuencialmente hasta que se llega al final del diagrama.

Durante la prueba, puede controlar la ejecución de la campaña mediante la barra de acciones del lienzo. A partir de ahí, puede realizar lo siguiente:

* **Detenga** la ejecución en cualquier momento.
* **Inicie** la ejecución de nuevo.
* **Reanudar** la ejecución si se había pausado anteriormente.

El icono **[!UICONTROL Alertas]** / **[!UICONTROL Advertencia]** de la barra de herramientas de lienzo le notifica de los problemas, incluidas las advertencias que pueden aparecer de forma proactiva antes de la ejecución y los errores que se producen durante o después de la ejecución.

![](assets/campaign-warning.png){zoomable="yes"}

También puede identificar rápidamente las actividades fallidas mediante los [indicadores visuales de estado](#activities) que se muestran directamente en cada actividad. Para obtener información detallada sobre la resolución de problemas, abra los [registros de la campaña](#logs-tasks), que proporcionan información detallada sobre el error y su contexto.

Si ha agregado actividades de canal en el lienzo, puede obtener una vista previa y probar el contenido de sus mensajes con el botón **[!UICONTROL Simular contenido]**. [Aprenda a trabajar con actividades de canal](activities/channels.md)

Una vez validada, la campaña se puede publicar.

## Publicación de la campaña {#publish}

Una vez que la campaña se haya probado y esté lista, haga clic en **[!UICONTROL Publicar]** para activarla.

![](assets/campaign-publish.png){zoomable="yes"}

>[!NOTE]
>
>Si el botón **[!UICONTROL Publicar]** está deshabilitado (atenuado), acceda a los registros de la barra de acciones y compruebe los mensajes de error. Todos los errores deben corregirse antes de poder publicar una campaña.

El flujo visual se reinicia y los perfiles reales comienzan a fluir a través del recorrido en tiempo real.

Si la acción de publicación falla (por ejemplo, debido a la falta de contenido de mensaje), se le alerta y debe corregir el problema antes de volver a intentarlo. Si la publicación se realiza correctamente, la campaña comenzará a ejecutarse (inmediatamente o según lo programado), pasará del estado **Borrador** al estado **Activo** y pasará a ser de &quot;Solo lectura&quot;.

## Monitorización de la ejecución de campañas {#monitor}

### Monitorización del flujo visual {#flow}

Mientras se ejecuta (en modo de prueba o activo), el flujo visual muestra cómo se mueven los perfiles a través del recorrido en tiempo real. Se muestra el número de perfiles que pasan de una tarea a otra.

![](assets/workflow-execution.png){zoomable="yes"}

Los datos que pasan de una actividad a otra se almacenan en una tabla de trabajo temporal. Estos datos se pueden mostrar para cada transición. Para inspeccionar los datos transferidos entre actividades:

1. Seleccione una transición.
1. En el panel de propiedades, haga clic en **[!UICONTROL Esquema de vista previa]** para ver el esquema de la tabla de trabajo. Seleccione **[!UICONTROL Vista previa de resultados]** para ver los datos transportados.

![](assets/transition.png){zoomable="yes"}

### Indicadores de ejecución de la actividad {#activities}

Los indicadores visuales de estado le ayudan a comprender el rendimiento de cada actividad:

| Indicador visual | Descripción |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | La actividad se está ejecutando actualmente. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | La actividad requiere su atención. Esto puede implicar confirmar el envío de una entrega o tomar las medidas necesarias. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | La actividad ha encontrado un error. Para resolver el problema, abra los registros de la campaña orquestada para obtener más información. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | La actividad se ha ejecutado correctamente. |

### Registros y tareas {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Registros y tareas"
>abstract="La pantalla **Registros y tareas** proporciona un historial de la ejecución de la campaña orquestada, registrando todas las acciones del usuario y los errores encontrados."

La monitorización de registros y tareas es un paso clave para analizar las campañas orquestadas y asegurarse de que se ejecutan correctamente. Puede acceder a los registros y las tareas desde el botón **[!UICONTROL Registros]**, que está disponible en los modos de prueba y en directo en la barra de herramientas de lienzo o en el panel de propiedades de cada actividad.

La pantalla **[!UICONTROL Registros y tareas]** proporciona un historial de la ejecución de la campaña organizada, registrando todas las acciones del usuario y los errores encontrados.

![](assets/workflow-logs.png){zoomable="yes"}

Hay dos tipos de información disponibles:

* La pestaña **[!UICONTROL Registro]** contiene el historial cronológico de todas las operaciones y errores.
* La pestaña **[!UICONTROL Tareas]** detalla la secuencia de ejecución paso a paso de las actividades.

En ambas pestañas, puede elegir las columnas mostradas y su orden, aplicar filtros y utilizar el campo de búsqueda para encontrar rápidamente la información deseada.
