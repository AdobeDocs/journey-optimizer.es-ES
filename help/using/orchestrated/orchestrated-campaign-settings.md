---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de los ajustes de la campaña orquestada
description: Obtenga información sobre cómo configurar ajustes de campañas orquestadas con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: a9bb3782-a4d1-43fe-ae2a-aef3f17ba588
source-git-commit: 450f83eb53068df10a63d39d1a43483ad3c7e803
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 27%

---

# Configuración de los ajustes de la campaña orquestada {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="Propiedades de la campaña orquestada"
>abstract="En esta pantalla, elija la plantilla que desea utilizar para crear la campaña orquestada y especifique una etiqueta. Expanda la sección **Opciones adicionales** para configurar más ajustes, como el nombre interno de la campaña de varios pasos, su carpeta, zona horaria y grupo de supervisores. Se recomienda muy especialmente seleccionar un grupo de supervisores para que los operadores sean advertidos si se produce un error."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicie su primera campaña orquestada | Consultar la base de datos | Actividades de campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md) | [Crear una campaña orquestada](create-orchestrated-campaign.md)<br/><br/><b>[Configuración de campañas orquestadas](orchestrated-campaign-settings.md)</b><br/><br/>[Organizar actividades](orchestrate-activities.md)<br/><br/>[Enviar mensajes con campañas orquestadas](send-messages.md)<br/><br/>[Iniciar y supervisar la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [División](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Al crear una campaña orquestada u organizar actividades de campaña orquestadas en el lienzo, puede acceder a la configuración avanzada relacionada con la campaña orquestada. Por ejemplo, puede establecer una zona horaria específica para la campaña orquestada, administrar cómo debe comportarse la campaña orquestada en caso de error o administrar el retraso después del cual debe purgarse el historial de campañas orquestadas.

Estos ajustes están preconfigurados en la plantilla seleccionada al crear la campaña orquestada, pero se pueden editar según sea necesario para esta campaña orquestada específica.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## Propiedades de la campaña orquestada {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Propiedades de la campaña orquestada"
>abstract="En esta sección se proporcionan propiedades genéricas de la campaña orquestada que son accesibles cuando se crea la campaña orquestada. Puede elegir la plantilla que desea utilizar para crear la campaña orquestada y especificar una etiqueta. Expanda la sección Opciones adicionales para configurar ajustes específicos, como la carpeta de almacenamiento de la campaña orquestada o la zona horaria."

La sección **[!UICONTROL Properties]** proporciona una configuración genérica que se puede configurar al crear una campaña orquestada. Para acceder a las propiedades de una campaña orquestada existente, haga clic en el botón **[!UICONTROL Configuración]** disponible en la barra de acciones situada encima del lienzo de la campaña orquestada.


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


Estas propiedades son:

* La **[!UICONTROL etiqueta]** de la campaña orquestada que se muestra en la lista.
* **[!UICONTROL Nombre interno]** de la campaña orquestada.
* La **[!UICONTROL carpeta]** en la que se debe guardar la campaña orquestada.
* La **[!UICONTROL zona horaria]** predeterminada para usar en todas las actividades de la campaña orquestada. De forma predeterminada, la zona horaria de la campaña orquestada es la definida para el operador de Campaign actual.
Los valores posibles son:
   * **Zona horaria del servidor** para usar la de su organización de Adobe Experience Platform
   * **Zona horaria del operador** que usa la zona horaria del operador que ejecuta la campaña orquestada
   * **Zona horaria de la base de datos** para usar la zona horaria del servidor de la base de datos
   * Una zona horaria específica
* Cuando falla una campaña orquestada, los operadores que pertenecen al grupo de operadores seleccionado en el campo **[!UICONTROL Supervisor(s)]** reciben una notificación por correo electrónico.
* También puedes ingresar una **[!UICONTROL Descripción]** de tu campaña orquestada.

## Configuración de la segmentación  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Configuración de la segmentación"
>abstract="En esta sección, puede seleccionar la dimensión de segmentación para segmentar los perfiles de la campaña orquestada y elegir mantener los resultados del flujo de trabajo entre dos ejecuciones. Esta opción solo debe utilizarse parar realizar pruebas y nunca debe habilitarse en una campaña orquestada de producción."

* **[!UICONTROL Dimensión de segmentación]**: Seleccione la dimensión de segmentación que se utilizará para segmentar los perfiles: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc.

* **[!UICONTROL Mantener el resultado de poblaciones provisionales entre dos ejecuciones]**: De forma predeterminada, solo se conservan las tablas de trabajo de la última ejecución de la campaña orquestada. Las tablas de trabajo de ejecuciones anteriores se depuran mediante una campaña técnica orquestada, que se ejecuta diariamente.

  Si esta opción está activada, las tablas de trabajo se conservarán incluso después de ejecutar la campaña orquestada. Puede utilizarlo con fines de prueba y, por lo tanto, **solo** debe usarse en entornos de ensayo o desarrollo. Nunca se debe comprobar en una campaña orquestada de producción.

## Configuración de ejecución  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Configuración de ejecución"
>abstract="En esta sección, puede configurar las opciones relacionadas con la ejecución del flujo de trabajo, como el número de días que se mantiene el historial de la campaña orquestada."

* **[!UICONTROL Historial en días]**: especifica el número de días después de los cuales se debe purgar el historial. El historial contiene elementos relacionados con la campaña orquestada: registros, tareas, eventos (objetos técnicos vinculados a la operación de campaña orquestada). El valor predeterminado es de 30 días para las plantillas de campaña orquestadas listas para usar. La depuración del historial la realiza la campaña técnica orquestada Database cleanup, que se ejecuta de forma predeterminada todos los días

  >[!IMPORTANT]
  >
  >Si el campo **[!UICONTROL Historial en días]** se deja en blanco, su valor se considerará “1”, lo que significa que el historial se purgará después de un día.

* **[!UICONTROL Afinidad predeterminada]**: Si su instalación incluye varios servidores de campaña organizados, utilice este campo para especificar el servidor en el que se ejecutará la campaña orquestada. Esto fuerza la ejecución de esa campaña orquestada en un servidor en particular. Puede elegir cualquier nombre de afinidad existente, pero asegúrese de no utilizar espacios ni signos de puntuación. Si utiliza servidores diferentes, especifique nombres diferentes separados por comas.

  >[!IMPORTANT]
  >
  >Si el valor definido en este campo no existe en ningún servidor, la campaña orquestada permanece pendiente.


* **[!UICONTROL Guardar consultas SQL en el registro]**: marque esta opción para guardar las consultas SQL de la campaña de varios pasos de flujo de trabajo ahora en los registros. Esta funcionalidad se reserva únicamente a los usuarios avanzados. Se aplica a campañas orquestadas que contienen actividades de segmentación como **[!UICONTROL Generar audiencia]**. Cuando esta opción está habilitada, las consultas SQL enviadas a la base de datos durante la ejecución de la campaña orquestada se muestran en los registros de la campaña orquestada, lo que permite analizarlas para optimizar consultas o diagnosticar problemas.

## Configuración de la administración de errores  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Configuración de la administración de errores"
>abstract="En esta sección, puede definir cómo la campaña orquestada debe administrar los errores durante su ejecución. Puede optar por poner en pausa el proceso, ignorar un determinado número de errores o detener la ejecución de la campaña orquestada."

* **[!UICONTROL Administración de errores]**: Este campo permite definir las acciones que deben realizarse si una tarea de campaña orquestada tiene errores. Hay tres opciones posibles:

   * **[!UICONTROL Suspender el proceso]**: La campaña orquestada se pone en pausa automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reanude la campaña orquestada con los botones **[!UICONTROL Reanudar]**.
   * **[!UICONTROL Ignorar]**: El estado de la tarea que activó el error cambia a **[!UICONTROL Fallido]**, pero la campaña orquestada mantiene el estado **[!UICONTROL Iniciado]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Anular el proceso]**: la campaña orquestada se detiene automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reinicie la campaña orquestada con los botones **[!UICONTROL Start]**.

* **[!UICONTROL Errores consecutivos]**: Este campo está disponible cuando el valor **[!UICONTROL Ignorar]** está seleccionado en el campo **[!UICONTROL En caso de errores]**. Puede especificar el número de errores que se pueden omitir antes de que se detenga el proceso. Una vez alcanzado este número, el estado de la campaña orquestada cambia a **[!UICONTROL Failed]**. Si el valor de este campo es 0, la campaña orquestada nunca se detiene, independientemente del número de errores.


