---
solution: Journey Optimizer
product: journey optimizer
title: Programación e inicio de campañas orquestadas con Adobe Journey Optimizer
description: Obtenga información sobre cómo programar e iniciar campañas orquestadas con Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 94ec0430995c26d6c0eaa68f523675997ed0a327
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 3%

---

# Programación e inicio de campañas orquestadas {#start-monitor}

<!--
<audio controls><source src="../ms/assets/do-not-localize/sound.mp3" type="audio/mpeg">Your browser does not support the audio element.</audio> -->

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Publicación de la campaña orquestada"
>abstract="Para iniciar su campaña, debe publicarla. Asegúrese de que todas las advertencias se borran antes de la publicación."

Una vez que haya creado las tareas orquestadas y diseñadas para realizarlas en el lienzo, puede publicarlas y monitorizar cómo se ejecutan.

## Inicio de una campaña orquestada {#start}

Para iniciar una campaña orquestada, vaya a la pestaña **[!UICONTROL Varios pasos]** en el menú de **[!UICONTROL Campaña]**, seleccione la campaña que desee iniciar y, a continuación, haga clic en el botón **[!UICONTROL Iniciar]** en la esquina superior derecha del lienzo.

Una vez que se está ejecutando la campaña orquestada, cada actividad del lienzo se ejecuta en un orden secuencial, hasta que se llega al final de la campaña orquestada.

Puede realizar un seguimiento del progreso de los perfiles de destino en tiempo real mediante un flujo visual. Esto le permite identificar rápidamente el estado de cada actividad y el número de perfiles en transición entre ellas.

![](assets/workflow-execution.png){zoomable="yes"}

## Transiciones de campaña organizadas {#transitions}

En las campañas organizadas, los datos que pasan de una actividad a otra a través de transiciones se almacenan en una tabla de trabajo temporal. Estos datos se pueden mostrar para cada transición. Para ello, seleccione una transición para abrir sus propiedades en el lado derecho de la pantalla.

* Haga clic en **[!UICONTROL Vista previa del esquema]** para mostrar el esquema de la tabla de trabajo.
* Haga clic en **[!UICONTROL Previsualizar resultados]** para visualizar los datos transportados en la transición seleccionada.

![](assets/transition.png){zoomable="yes"}

## Monitorización de la ejecución de actividades {#activities}

Los indicadores visuales de la esquina superior derecha de cada cuadro de actividad permiten comprobar su ejecución:

| Indicador visual | Descripción |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | La actividad se está ejecutando. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | La actividad requiere su atención. Esto puede implicar confirmar el envío de una entrega o realizar la acción necesaria. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | La actividad ha encontrado un error. Para resolver el problema, abra los registros de campaña organizados para obtener más información. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | La actividad se ha ejecutado correctamente. |

## Monitorización de registros y tareas {#logs-tasks}

La monitorización de registros y tareas de flujos de trabajo es un paso clave para analizar las campañas orquestadas y asegurarse de que se ejecutan correctamente. Se puede acceder a ellos desde el icono **[!UICONTROL Logs]** que está disponible en la barra de herramientas de acciones y en el panel de propiedades de cada actividad.

El menú **[!UICONTROL Registros y tareas]** proporciona un historial de la ejecución de la campaña orquestada, registrando todas las acciones del usuario y los errores encontrados.
![](assets/workflow-logs.png){zoomable="yes"}

Hay dos tipos de información disponibles:

* La pestaña **[!UICONTROL Log]** contiene el historial de ejecución de todas las actividades de campaña orquestadas. Indexa las operaciones realizadas y los errores de ejecución por orden cronológico.
* La ficha **[!UICONTROL Tareas]** detalla la secuencia de ejecución de las actividades.

En ambas pestañas, puede elegir las columnas mostradas y su orden, aplicar filtros y utilizar el campo de búsqueda para encontrar rápidamente la información deseada.

## Comandos de ejecución de campaña organizados {#execution-commands}

La barra de acciones de la esquina superior derecha proporciona comandos que le permiten administrar la ejecución de la campaña orquestada. Puede hacer lo siguiente:

* **[!UICONTROL Iniciar]** / **[!UICONTROL Reanudar]** la ejecución del   campaña orquestada, que luego adquiere el estado En curso. Si la campaña orquestada se ha pausado, se reanuda, pero se inicia y las actividades iniciales se activan.

* **[!UICONTROL Pausar]** la ejecución de la campaña orquestada, que luego adquiere el estado Paused. No se activará ninguna actividad nueva hasta que se reanude, pero las operaciones en curso no se suspenden.

* **[!UICONTROL Detener]** una campaña orquestada que se está ejecutando y que luego pasará al estado Finalizado. Las operaciones en curso se interrumpen si es posible. No puede continuar desde la campaña orquestada desde el mismo lugar en el que se detuvo.
