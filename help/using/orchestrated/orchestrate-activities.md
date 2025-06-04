---
solution: Journey Optimizer
product: journey optimizer
title: Creación de campañas orquestadas con Adobe Journey Optimizer
description: Aprenda a crear campañas orquestadas con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 7f535b87e415ae9191199b34476adb5c977b66e9
workflow-type: tm+mt
source-wordcount: '1289'
ht-degree: 1%

---

# Organización de actividades de campaña orquestadas {#orchestrate}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicie su primera campaña orquestada | Consultar la base de datos | Actividades de campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md) | [Crear una campaña orquestada](create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](orchestrate-activities.md)<br/><br/>[Enviar mensajes con campañas orquestadas](send-messages.md)<br/><br/>[Iniciar y supervisar la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el Modeler de consultas](orchestrated-query-modeler.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Editar expresiones](edit-expressions.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [División](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

Una vez que haya [creado una campaña orquestada](gs-campaign-creation.md), ya sea desde el menú de campaña orquestada o dentro de una campaña, puede empezar a orquestar las diferentes tareas que realizará. Para ello, se proporciona un lienzo visual, que le permite construir un diagrama de campaña orquestado. Dentro de este diagrama, puede añadir varias actividades y conectarlas en un orden secuencial.

## Añadir actividades {#add}

En esta fase de la configuración, el diagrama se muestra con un icono de inicio que representa el principio de la campaña orquestada. Para agregar su primera actividad, haga clic en el botón **+** conectado al icono de inicio.

Aparecerá una lista de actividades que se pueden agregar al diagrama. Las actividades disponibles dependen de su posición dentro del diagrama de campaña orquestada. Por ejemplo, al agregar la primera actividad, puede iniciar la campaña orquestada segmentando una audiencia, dividiendo la ruta de la campaña orquestada o estableciendo una actividad **Wait** para retrasar la ejecución de la campaña orquestada. Por otro lado, después de una actividad **Generar audiencia**, puede refinar el segmento con actividades de segmentación, enviar una entrega a la audiencia con actividades de canal u organizar el proceso de campaña orquestado con actividades de control de flujo.

![](assets/workflow-start.png){zoomable="yes"}

Una vez que se ha agregado una actividad al diagrama, aparece un panel derecho que le permite configurar la actividad recién agregada con ajustes específicos. Encontrará información detallada sobre cómo configurar cada actividad en [esta sección](activities/about-activities.md).

![](assets/workflow-configure-activities.png){zoomable="yes"}

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

![](assets/workflow-toolbar.png){zoomable="yes"}{width="50%"}

## Administrar actividades {#manage}

Al agregar actividades, los botones de acción están disponibles en el panel de propiedades, lo que le permite realizar varias operaciones.

![](assets/activity-action.png){zoomable="yes"}

Puede hacer lo siguiente:

* **Eliminar** la actividad del lienzo.
* **Deshabilitar/Habilitar** la actividad. Cuando se ejecuta la campaña orquestada, las actividades deshabilitadas y las siguientes actividades en la misma ruta no se ejecutan y la campaña orquestada se detiene.
* **Pausar/reanudar** la actividad. Cuando se ejecuta la campaña orquestada, se pausa en la actividad pausada. No se ejecutan la tarea correspondiente ni todas las que la siguen en la misma ruta.
* **Copie** la actividad. Consulte [esta sección](#copy).
* **Mover** una actividad y todos sus nodos secundarios a otra transición. Ver [esta sección](#move)
* Acceda a las **opciones de ejecución** de la actividad.
* Acceda a los **registros y tareas** de la actividad.

Varias actividades **Targeting**, como **Combine** o **Deduplication**, le permiten procesar la población restante e incluirla en una transición saliente adicional. Por ejemplo, si está usando una actividad **Split**, el complemento consiste en la población que no coincide con ninguno de los subconjuntos definidos anteriormente. Para usar esta capacidad, active la opción **Generar complemento**.

![](assets/workflow-split-complement.png)

## Mover o copiar actividades {#move-copy}

### Copiar y pegar actividades {#copy}

Puede copiar actividades de campañas orquestadas y pegarlas en cualquier flujo de trabajo. La campaña orquestada de destino puede estar en una pestaña diferente del explorador.

Para copiar actividades, tiene dos opciones:

* copie una actividad con el botón acción.

  ![](assets/workflow-copy.png){zoomable="yes"}{width="70%"}

* copie varias actividades con el botón de la barra de herramientas.

  ![](assets/workflow-copy-2.png){zoomable="yes"}{width="70%"}

Para pegar las actividades copiadas, haga clic en el botón **+** de una transición y seleccione &quot;Pegar actividad X&quot;.

![](assets/workflow-copy-3.png){zoomable="yes"}{width="50%"}

### Mover actividades y sus nodos secundarios {#move}

Journey Optimizer le permite mover una actividad junto con todo el contenido de sus nodos secundarios (incluidas todas las transiciones y actividades dentro de ella) al final de otra transición dentro de la misma campaña orquestada.

Este proceso desconecta la actividad y todo lo que se encuentra en su transición saliente de la ubicación inicial, lo que la mueve a la nueva transición objetivo.

Para mover una actividad:

1. Seleccione la actividad que desee mover.
1. En el panel de propiedades de la actividad, haga clic en el botón **Mover**.
1. Seleccione la transición en la que desea colocar la actividad y su transición saliente y, a continuación, confirme la selección.

![](assets/activity-move.png)

## Opciones de ejecución {#execution}

Todas las actividades permiten administrar sus opciones de ejecución. Seleccione una actividad y haga clic en el botón **Opciones de ejecución**. Esto permite definir el modo de ejecución y el comportamiento de la actividad en caso de errores.

![](assets/workflow-execution-options.png){zoomable="yes"}{width="70%"}

### Propiedades

El campo **Execution** le permite definir la acción que debe llevarse a cabo cuando se inicia la tarea.

El campo **Duración máxima de la ejecución** le permite especificar una duración como &quot;30 segundos&quot; o &quot;1h&quot;. Si la actividad no termina después de que haya transcurrido la duración especificada, se activa una alerta. Esto no afecta al funcionamiento de la campaña orquestada.

El campo **Zona horaria** le permite seleccionar la zona horaria de la actividad. Adobe Journey Optimizer le permite administrar las diferencias horarias entre varios países en la misma instancia. La configuración aplicada se configura cuando se crea la instancia.

**El campo Afinidad** le permite forzar la ejecución de una campaña orquestada o de una actividad de campaña orquestada en un equipo concreto. Para ello, debe especificar una o varias afinidades para la campaña o actividad orquestada en cuestión.

El campo **Comportamiento** le permite definir el procedimiento a seguir si se utilizan tareas asincrónicas.

### Administración de errores

El campo **En caso de error** le permite especificar la acción que debe llevarse a cabo en caso de que la actividad encuentre un error.

### Script de inicialización

El **script de inicialización** le permite inicializar variables o modificar propiedades de actividad. Haga clic en el botón **Editar código** y escriba el fragmento de código que desea ejecutar. Se llama al script cuando se ejecuta la actividad.

## Ejemplo {#example}

Este es un ejemplo de campaña orquestada diseñada para enviar un correo electrónico a todos los clientes (que no sean clientes de VIP) con un correo electrónico que estén interesados en las máquinas de café.

![](assets/workflow-example.png){zoomable="yes"}{zoomable="yes"}

Para ello, se han añadido las actividades siguientes:

* Una actividad **[!UICONTROL Fork]** que divide la campaña orquestada en tres rutas (una para cada conjunto de clientes),
* **[!UICONTROL Cree audiencias]** para segmentar los tres grupos de clientes:

   * Clientes con un correo electrónico,
   * Clientes que pertenecen a la audiencia preexistente &quot;Interesado en las máquinas de café&quot;,
   * Clientes que pertenecen a la audiencia preexistente &quot;VIP o premio&quot;.

* Una actividad **[!UICONTROL Combine]** que agrupa a clientes con un mensaje de correo electrónico y a aquellos interesados en las máquinas de café,
* Una actividad **[!UICONTROL Combine]** que excluye clientes de VIP,
* Una actividad **[!UICONTROL Email delivery]** que envía un mensaje de correo electrónico a los clientes resultantes.

Una vez que haya completado la campaña orquestada, agregue una actividad **[!UICONTROL End]** al final del diagrama. Esta actividad le permite marcar visualmente el final de un flujo de trabajo y no tiene impacto funcional.

Después de diseñar correctamente el diagrama de campaña orquestada, puede ejecutar la campaña orquestada y realizar un seguimiento del progreso de sus distintas tareas. [Aprenda a iniciar una campaña orquestada y a supervisar su ejecución](start-monitor-campaigns.md)
