---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de opciones de campaña orquestadas
description: Aprenda a configurar opciones de campaña orquestadas con Adobe Systems Journey Optimizer
hide: true
hidefromtoc: true
exl-id: a9bb3782-a4d1-43fe-ae2a-aef3f17ba588
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 8%

---

# Configuración de opciones de campaña orquestadas {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="Propiedades de campaña orquestadas"
>abstract="En esta pantalla, elija la plantilla que desea utilizar para crear el campaña orquestado y especifique una etiqueta. Expanda la **sección Opciones** adicionales para configurar más opciones, como el nombre interno del campaña orquestado, su carpeta, zona horaria y grupo supervisor. Se recomienda muy especialmente seleccionar un grupo de supervisores para que los operadores sean advertidos si se produce un error."

Al crear un campaña orquestado o al orquestar actividades de campaña orquestadas en el lienzo, puede acceder a configuraciones avanzadas relacionadas con el campaña orquestado. Por ejemplo, puede establecer una zona horaria específica para el campaña orquestado, administrar cómo debe comportarse el campaña orquestado en caso de error o administrar el retraso después del cual se debe depurar el historial de campaña orquestado.

Estos ajustes están preconfigurados en la plantilla seleccionada al crear el campaña orquestado, pero se pueden editar según sea necesario para este campaña orquestado específico.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## Propiedades de campaña orquestadas {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Propiedades de campaña orquestadas"
>abstract="En esta sección se proporcionan propiedades de campaña orquestadas genéricas a las que también se puede acceder al crear la campaña orquestada. Puede elegir la plantilla que desea utilizar para crear la campaña orquestada y especificar una etiqueta. Expanda la sección Opciones adicionales para configurar opciones específicas, como la carpeta de almacenamiento o la zona horaria de la campaña organizada."

La sección **[!UICONTROL Properties]** proporciona una configuración genérica que se puede configurar al crear una campaña orquestada. Para acceder a las propiedades de una campaña orquestada existente, haga clic en el botón **[!UICONTROL Configuración]** disponible en la barra de acciones situada encima del lienzo de la campaña orquestada.


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


Estas propiedades son:

* La **[!UICONTROL etiqueta]** de la campaña orquestada que se muestra en la lista.
* Nombre **** interno del campaña orquestado.
* El **[!UICONTROL Carpeta]** donde debe guardarse el campaña orquestado.
* Zona horaria ]**predeterminada**[!UICONTROL que se utilizará en todas las actividades del campaña orquestado. De forma predeterminada, el huso horario del campaña orquestado es el definido para el operador Campaign actual.
Los valores posibles son:
   * **Zona** horaria del servidor para usar la zona horaria de la organización Adobe Experience Platform
   * **Zona horaria** del operador para utilizar la zona horaria del operador que ejecuta la campaña orquestada
   * **Zona horaria de la base de datos** para utilizar la zona horaria del servidor de base de datos
   * Una zona horaria específica
* Cuando falla una campaña orquestada, los operadores pertenecientes a los operadores grupo seleccionados en el **[!UICONTROL campo Supervisor(es)]** son notificados por correo electrónico.
* También puede especificar un **[!UICONTROL Descripción]** del campaña orquestado.

## Configuración de la segmentación  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Configuración de la segmentación"
>abstract="En esta sección, puede seleccionar el dimensión de segmentación para destino perfiles en el campaña orquestado y elegir mantener los resultados de trabajo bajo entre dos ejecuciones. Esta opción debe utilizarse únicamente con fines de prueba y nunca debe activarse en un campaña organizado de producción."

* **[!UICONTROL Targeting dimensión]**: Seleccione el dimensión de segmentación que desea utilizar para destino perfiles: destinatarios, beneficiarios del contrato, operador, suscriptores, etc.

* **[!UICONTROL Mantener el resultado de las poblaciones provisionales entre dos ejecuciones]**: Por defecto, sólo se conservan las tablas de trabajo de la última ejecución del campaña orquestado. Las mesas de trabajo de ejecuciones anteriores se purgan mediante un campaña técnico orquestado, que se ejecuta a diario.

  Si esta opción está activada, las tablas de trabajo se conservarán incluso después de ejecutar la campaña orquestada. Puede utilizarlo con fines de prueba y, por lo tanto, solo **debe usarse** en entornos de ensayo o desarrollo. Nunca se debe comprobar en una campaña orquestada de producción.

## Configuración de ejecución  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Configuración de ejecución"
>abstract="En esta sección, puede configurar las opciones relacionadas con la ejecución del flujo de trabajo, como el número de días que se mantiene el historial de campañas orquestadas."

* **[!UICONTROL Historial en días]**: especifica el número de días después de los cuales se debe purgar el historial. El historial contiene elementos relacionados con el campaña orquestado: registros, tareas, eventos (objetos técnicos vinculados a la operación campaña orquestada). El valor predeterminado es 30 días para las plantillas de campaña orquestadas de fábrica. La depuración del historial se realiza mediante el campaña técnico de limpieza de la base de datos, que se ejecuta de forma predeterminada todos los días

  >[!IMPORTANT]
  >
  >Si el campo **[!UICONTROL Historial en días]** se deja en blanco, su valor se considerará “1”, lo que significa que el historial se purgará después de un día.

* **[!UICONTROL afinidad]** predeterminada: Si su instalación incluye varios servidores campaña orquestados, utilice este campo para especificar el servidor en el que se ejecutará la campaña orquestada. Esto fuerza la ejecución de esa campaña orquestada en un servidor en particular. Puede elegir cualquier nombre de afinidad existente, pero asegúrese de no utilizar espacios ni signos de puntuación. Si utiliza diferentes servidores, especifique nombres diferentes, separados por comas.

  >[!IMPORTANT]
  >
  >Si el valor definido en este campo no existe en ningún servidor, la campaña orquestada permanecerá pendiente.


* **[!UICONTROL Guardar consultas SQL en el registro]**: Marque esta opción para guardar las consultas SQL del workflmulti-step campaignow en los registros. Esta funcionalidad se reserva únicamente a los usuarios avanzados. Se aplica a las campañas orquestadas que contienen actividades direccionamiento gustar **[!UICONTROL Generar audiencia]**. Cuando esta opción está habilitada, las consultas SQL enviadas a la base de datos durante la ejecución del campaña orquestado se muestran en los registros del campaña orquestado, lo que le permite analizarlas para optimizar las consultas o diagnosticar problemas.

## Configuración de la administración de errores  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Configuración de la administración de errores"
>abstract="En esta sección, puede definir cómo el campaña orquestado debe administrar errores durante su ejecución. Puede optar por pausar el proceso, ignorar un cierto número de errores o detener la ejecución orquestada campaña."

* **[!UICONTROL Administración de errores]**: Este campo permite definir las acciones que deben realizarse si una tarea de campaña orquestada tiene errores. Hay tres opciones posibles:

   * **[!UICONTROL Suspender el proceso]**: La campaña orquestada se pone en pausa automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reanude la campaña orquestada con los botones **[!UICONTROL Reanudar]**.
   * **[!UICONTROL Ignorar]**: El estado de la tarea que activó el error cambia a **[!UICONTROL Fallido]**, pero la campaña orquestada mantiene el estado **[!UICONTROL Iniciado]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Anular el proceso]**: la campaña orquestada se detiene automáticamente y su estado cambia a **[!UICONTROL Fallido]**. Una vez resuelto el problema, reinicie el campaña orquestado con los botones Inicio ****.

* **[!UICONTROL Errores consecutivos]**: este campo está disponible cuando se selecciona el **[!UICONTROL valor Ignorar]** en el **[!UICONTROL campo En caso de errores]** . Puede especificar el número de errores que se pueden omitir antes de que se detenga el proceso. Una vez que se alcanza este número, el campaña organizado cambia a **[!UICONTROL Fallido]**. Si el valor de este campo es 0, la campaña orquestada nunca se detendrá independientemente del número de errores.

## Script de inicialización {#initialization-script}

La **secuencia de comandos** de inicialización permite inicializar variables o modificar actividad propiedades. Haga clic en el **botón código** Editar y escriba el fragmento de código que desea ejecutar. Se llama a la secuencia de comandos cuando se ejecuta el campaña orquestado. Consulte la sección relacionada con [evento variables](event-variables.md).
