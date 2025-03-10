---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de campañas de varios pasos
description: Obtenga información sobre cómo configurar campañas de varios pasos con Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 8%

---


# Configuración de campañas de varios pasos {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="Propiedades de campaña de varios pasos"
>abstract="En esta pantalla, elija la plantilla que desea utilizar para crear la campaña de varios pasos y especifique una etiqueta. Expanda la sección **Opciones adicionales** para configurar más opciones, como el nombre interno de la campaña en varios pasos, su carpeta, zona horaria y grupo de supervisores. Se recomienda encarecidamente seleccionar un grupo de supervisores para que los operadores sean alertados si se produce un error."

Al crear una campaña de varios pasos u organizar actividades de campaña de varios pasos en el lienzo, puede acceder a la configuración avanzada relacionada con la campaña de varios pasos. Por ejemplo, puede establecer una zona horaria específica para la campaña de varios pasos, administrar cómo debe comportarse la campaña de varios pasos en caso de error o administrar el retraso después del cual debe purgarse el historial de campaña de varios pasos.

Estos ajustes están preconfigurados en la plantilla seleccionada al crear la campaña de varios pasos, pero se pueden editar según sea necesario para esta campaña específica de varios pasos.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## Propiedades de campaña de varios pasos {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Propiedades de campaña de varios pasos"
>abstract="Esta sección proporciona propiedades de campaña genéricas de varios pasos a las que también se puede acceder al crear la campaña de varios pasos. Puede elegir la plantilla que desea utilizar para crear la campaña de varios pasos y especificar una etiqueta. Expanda la sección Opciones adicionales para configurar opciones específicas, como la carpeta de almacenamiento o la zona horaria de la campaña de varios pasos."

La sección **[!UICONTROL Properties]** proporciona una configuración genérica que se puede configurar al crear una campaña de varios pasos. Para acceder a las propiedades de una campaña existente de varios pasos, haga clic en el botón **[!UICONTROL Configuración]** disponible en la barra de acciones situada encima del lienzo de la campaña de varios pasos.


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


Estas propiedades son:

* La **[!UICONTROL etiqueta]** de la campaña de varios pasos que se muestra en la lista.
* **[!UICONTROL Nombre interno]** de la campaña de varios pasos.
* La **[!UICONTROL carpeta]** donde se debe guardar la campaña de varios pasos.
* La **[!UICONTROL zona horaria]** predeterminada para usar en todas las actividades de la campaña de varios pasos. De forma predeterminada, el huso horario de la campaña de varios pasos es el definido para el operador de Campaign actual.
Los valores posibles son:
   * **Zona horaria del servidor** para usar la de su organización de Adobe Experience Platform
   * **Zona horaria del operador** que usa la zona horaria del operador que ejecuta la campaña de varios pasos
   * **Zona horaria de la base de datos** para usar la zona horaria del servidor de la base de datos
   * Una zona horaria específica
* Cuando falla una campaña de varios pasos, los operadores que pertenecen al grupo de operadores seleccionado en el campo **[!UICONTROL Supervisor(s)]** reciben una notificación por correo electrónico.
* También puedes ingresar una **[!UICONTROL Descripción]** de tu campaña de varios pasos.

## Configuración de segmentación  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Configuración de segmentación"
>abstract="En esta sección, puede seleccionar la dimensión objetivo para los perfiles objetivo en la campaña de varios pasos y elegir mantener los resultados del flujo de trabajo entre dos ejecuciones. Esta opción solo debe utilizarse con fines de prueba y nunca debe habilitarse en una campaña de producción de varios pasos."

* **[!UICONTROL Dimensión de segmentación]**: Seleccione la dimensión de segmentación que se utilizará para segmentar los perfiles: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc.

* **[!UICONTROL Mantener el resultado de poblaciones provisionales entre dos ejecuciones]**: De forma predeterminada, solo se conservan las tablas de trabajo de la última ejecución de la campaña de varios pasos. Una campaña técnica de varios pasos, que se ejecuta diariamente, depura las tablas de trabajo de ejecuciones anteriores.

  Si esta opción está habilitada, las tablas de trabajo se conservarán incluso después de ejecutar la campaña de varios pasos. Puede utilizarlo con fines de prueba y, por lo tanto, **solo** debe usarse en entornos de ensayo o desarrollo. Nunca se debe comprobar en una campaña de producción de varios pasos.

## Configuración de ejecución  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Configuración de ejecución"
>abstract="En esta sección, puede configurar las opciones relacionadas con la ejecución del flujo de trabajo, como el número de días que se mantiene el historial de campañas de varios pasos."

* **[!UICONTROL Historial en días]**: especifica el número de días después de los cuales se debe purgar el historial. El historial contiene elementos relacionados con la campaña de varios pasos: registros, tareas, eventos (objetos técnicos vinculados a la operación de campaña de varios pasos). El valor predeterminado es de 30 días para plantillas de campaña de varios pasos listas para usar. La depuración del historial se realiza mediante la campaña técnica de varios pasos Database cleanup, que se ejecuta de forma predeterminada todos los días

  >[!IMPORTANT]
  >
  >Si el campo **[!UICONTROL Historial en días]** se deja en blanco, su valor se considerará “1”, lo que significa que el historial se purgará después de un día.

* **[!UICONTROL Afinidad predeterminada]**: Si su instalación incluye varios servidores de campañas de varios pasos, utilice este campo para especificar el servidor en el que se ejecutará la campaña de varios pasos. Esto fuerza la ejecución de esa campaña de varios pasos en un servidor en particular. Puede elegir cualquier nombre de afinidad existente, pero asegúrese de no utilizar espacios ni signos de puntuación. Si utiliza servidores diferentes, especifique nombres diferentes separados por comas.

  >[!IMPORTANT]
  >
  >Si el valor definido en este campo no existe en ningún servidor, la campaña de varios pasos permanecerá pendiente.


* **[!UICONTROL Guardar consultas SQL en el registro]**: marque esta opción para guardar las consultas SQL de la campaña de varios pasos de flujo de trabajo ahora en los registros. Esta funcionalidad se reserva únicamente a los usuarios avanzados. Se aplica a campañas de varios pasos que contienen actividades de segmentación como **[!UICONTROL Generar audiencia]**. Cuando esta opción está habilitada, las consultas SQL enviadas a la base de datos durante la ejecución de campañas de varios pasos se muestran en los registros de la campaña de varios pasos, lo que le permite analizarlas para optimizar consultas o diagnosticar problemas.

## Configuración de la administración de errores  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Configuración de la administración de errores"
>abstract="En esta sección, puede definir cómo la campaña de varios pasos debe administrar los errores durante su ejecución. Puede optar por pausar el proceso, ignorar un determinado número de errores o detener la ejecución de la campaña en varios pasos."

* **[!UICONTROL Administración de errores]**: Este campo permite definir las acciones que deben realizarse si una tarea de campaña de varios pasos contiene errores. Hay tres opciones posibles:

   * **[!UICONTROL Suspender el proceso]**: la campaña de varios pasos se pone en pausa automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reanude la campaña de varios pasos con los botones **[!UICONTROL Reanudar]**.
   * **[!UICONTROL Ignorar]**: El estado de la tarea que activó el error cambia a **[!UICONTROL Fallido]**, pero la campaña de varios pasos mantiene el estado **[!UICONTROL Iniciado]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Anular el proceso]**: la campaña de varios pasos se detiene automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reinicie la campaña de varios pasos con los botones **[!UICONTROL Start]**.

* **[!UICONTROL Errores consecutivos]**: Este campo está disponible cuando el valor **[!UICONTROL Ignorar]** está seleccionado en el campo **[!UICONTROL En caso de errores]**. Puede especificar el número de errores que se pueden omitir antes de que se detenga el proceso. Una vez alcanzado este número, el estado de la campaña de varios pasos cambia a **[!UICONTROL Failed]**. Si el valor de este campo es 0, la campaña de varios pasos nunca se detiene, independientemente del número de errores.

## Script de inicialización {#initialization-script}

El **script de inicialización** le permite inicializar variables o modificar propiedades de actividad. Haga clic en el botón **Editar código** y escriba el fragmento de código que desea ejecutar. Se llama al script cuando se ejecuta la campaña de varios pasos. Consulte la sección relacionada con [variables de eventos](event-variables.md).

