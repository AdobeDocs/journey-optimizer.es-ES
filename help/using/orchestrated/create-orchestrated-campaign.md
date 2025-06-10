---
solution: Journey Optimizer
product: journey optimizer
title: Creación de campañas orquestadas con Journey Optimizer
description: Obtenga información sobre cómo crear una campaña orquestada con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 6574735581de0872e78e8e05efea5c6a50dc59b1
workflow-type: tm+mt
source-wordcount: '1739'
ht-degree: 21%

---


# Creación de una campaña organizada {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Lista de campañas de orquestadas"
>abstract="La pestaña de **varios pasos** enumera todas las campañas orquestadas. Haga clic en el nombre de una campaña orquestada para editarla. Utilice el botón **Crear campaña orquestada** para añadir una nueva campaña orquestada."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicie su primera campaña orquestada | Consultar la base de datos | Actividades de campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/><b>[Cree y configure la campaña](create-orchestrated-campaign.md)</b><br/><br/>[Orqueste actividades](orchestrate-activities.md)<br/><br/>[Envíe mensajes con campañas orquestadas](send-messages.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [División](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

## Creación de la campaña {#create}

Para crear una campaña orquestada, siga estos pasos:

1. Para crear una **campaña orquestada**, vaya al menú **Campañas**.

1. Haga clic en el botón **[!UICONTROL Crear campaña orquestada]** en la esquina superior derecha de la pantalla.

1. En el cuadro de diálogo **Propiedades** de la campaña orquestada, seleccione la plantilla que desee utilizar para crear la campaña orquestada (también puede utilizar la plantilla integrada predeterminada). [Más información sobre las plantillas de campañas orquestadas](#campaign-templates).

1. Introduzca una etiqueta para la campaña organizada. Además, le recomendamos encarecidamente que agregue una descripción a su campaña orquestada, en el campo dedicado de la sección **[!UICONTROL Opciones adicionales]** de la pantalla.

1. Expanda la sección **[!UICONTROL Opciones adicionales]** para configurar más opciones para la campaña orquestada.

1. Haga clic en el botón **[!UICONTROL Crear campaña orquestada]** para confirmar la creación de la campaña orquestada.

La campaña orquestada se habrá creado y estará disponible en la lista de flujos de trabajo. Ahora puede acceder a su lienzo visual y empezar a agregar, configurar y organizar las tareas que va a realizar. [Aprenda a organizar actividades de campañas orquestadas](orchestrate-activities.md).

## Configuración de la campaña {#settings}

<!--Overview of new admin settings> schemas, execution fields, merge policy. [Learn more](configuration-steps.md)-->

Al crear una campaña orquestada u organizar actividades de campaña orquestadas en el lienzo, puede acceder a la configuración avanzada relacionada con la campaña orquestada. Por ejemplo, puede establecer una zona horaria específica para la campaña orquestada, administrar cómo debe comportarse la campaña orquestada en caso de error o administrar el retraso después del cual debe purgarse el historial de campañas orquestadas.

Estos ajustes están preconfigurados en la plantilla seleccionada al crear la campaña orquestada, pero se pueden editar según sea necesario para esta campaña orquestada específica.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

### Propiedades de la campaña orquestada {#properties}

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

### Configuración de la segmentación  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Configuración de la segmentación"
>abstract="En esta sección, puede seleccionar la dimensión de segmentación para segmentar los perfiles de la campaña orquestada y elegir mantener los resultados del flujo de trabajo entre dos ejecuciones. Esta opción solo debe utilizarse parar realizar pruebas y nunca debe habilitarse en una campaña orquestada de producción."

* **[!UICONTROL Dimensión de segmentación]**: Seleccione la dimensión de segmentación que se utilizará para segmentar los perfiles: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc.

* **[!UICONTROL Mantener el resultado de poblaciones provisionales entre dos ejecuciones]**: De forma predeterminada, solo se conservan las tablas de trabajo de la última ejecución de la campaña orquestada. Las tablas de trabajo de ejecuciones anteriores se depuran mediante una campaña técnica orquestada, que se ejecuta diariamente.

  Si esta opción está activada, las tablas de trabajo se conservarán incluso después de ejecutar la campaña orquestada. Puede utilizarlo con fines de prueba y, por lo tanto, **solo** debe usarse en entornos de ensayo o desarrollo. Nunca se debe comprobar en una campaña orquestada de producción.

### Configuración de ejecución  {#exec-settings}

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

### Configuración de la administración de errores  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Configuración de la administración de errores"
>abstract="En esta sección, puede definir cómo la campaña orquestada debe administrar los errores durante su ejecución. Puede optar por poner en pausa el proceso, ignorar un determinado número de errores o detener la ejecución de la campaña orquestada."

* **[!UICONTROL Administración de errores]**: Este campo permite definir las acciones que deben realizarse si una tarea de campaña orquestada tiene errores. Hay tres opciones posibles:

   * **[!UICONTROL Suspender el proceso]**: La campaña orquestada se pone en pausa automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reanude la campaña orquestada con los botones **[!UICONTROL Reanudar]**.
   * **[!UICONTROL Ignorar]**: El estado de la tarea que activó el error cambia a **[!UICONTROL Fallido]**, pero la campaña orquestada mantiene el estado **[!UICONTROL Iniciado]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Anular el proceso]**: la campaña orquestada se detiene automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reinicie la campaña orquestada con los botones **[!UICONTROL Start]**.

* **[!UICONTROL Errores consecutivos]**: Este campo está disponible cuando el valor **[!UICONTROL Ignorar]** está seleccionado en el campo **[!UICONTROL En caso de errores]**. Puede especificar el número de errores que se pueden omitir antes de que se detenga el proceso. Una vez alcanzado este número, el estado de la campaña orquestada cambia a **[!UICONTROL Failed]**. Si el valor de este campo es 0, la campaña orquestada nunca se detiene, independientemente del número de errores.

## Uso de plantillas de campañas orquestadas {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Plantillas de campañas orquestadas"
>abstract="Las plantillas de campañas orquestadas contienen ajustes y actividades preconfiguradas que se pueden reutilizar para crear nuevas campañas orquestadas."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Propiedades de la campaña orquestada"
>abstract="Las plantillas de campañas orquestadas contienen ajustes y actividades preconfiguradas que se pueden reutilizar para crear nuevas campañas orquestadas. En esta pantalla, introduzca la etiqueta de la plantilla de campaña orquestada y configure sus ajustes, como el nombre interno, la carpeta y las carpetas de ejecución, la zona horaria y el grupo de supervisores."

Las plantillas de campañas orquestadas contienen ajustes y actividades preconfiguradas que se pueden reutilizar para crear nuevas campañas orquestadas. Puede seleccionar la plantilla de la campaña orquestada desde las propiedades de la campaña orquestada al crear una campaña orquestada. De forma predeterminada, se proporciona una plantilla vacía.

Puede crear una plantilla a partir de una campaña orquestada existente o crear una nueva plantilla desde cero. Ambos métodos se detallan a continuación.

>[!BEGINTABS]

>[!TAB Crear una plantilla a partir de una campaña orquestada existente]

Para crear una plantilla de campaña orquestada a partir de una campaña orquestada existente, siga estos pasos:

1. Abra el menú **Campaign** y vaya a la campaña orquestada para guardarla como plantilla.
1. Haga clic en los tres puntos a la derecha del nombre de la campaña orquestada y elija **Copiar como plantilla**.
1. En la ventana emergente, confirme la creación de la plantilla.
1. En el lienzo de la plantilla de campaña orquestada, compruebe, añada y configure las actividades según sea necesario.
1. Vaya a la configuración, en el botón **Configuración**, para cambiar el nombre de la plantilla de campaña orquestada e introduzca una descripción.
1. Seleccione la **carpeta** y la **carpeta de ejecución** de la plantilla. La carpeta es la ubicación donde se guarda la plantilla de campaña orquestada. La carpeta de ejecución es la carpeta en la que se guardan las campañas orquestadas creadas en función de esta plantilla.
1. Guarde los cambios.

La plantilla de campaña orquestada ya está disponible en la lista de plantillas. Puede crear una campaña orquestada basada en esta plantilla. Esta campaña orquestada se preconfigura con la configuración y las actividades definidas en la plantilla.


>[!TAB Crear una plantilla desde cero]


Para crear una plantilla de campaña orquestada desde cero, siga estos pasos:

1. Abra el menú **Campaign** y vaya a la ficha **Plantillas**. Puede ver la lista de plantillas de campaña organizadas disponibles.
1. Haga clic en el botón **[!UICONTROL Crear plantilla]** en la esquina superior derecha de la pantalla.
1. Introduzca la etiqueta y abra las opciones adicionales para introducir una descripción de la plantilla de campaña orquestada.
1. Seleccione la carpeta y la carpeta de ejecución de la plantilla. La carpeta es la ubicación donde se guarda la plantilla de campaña orquestada. La carpeta de ejecución es la carpeta en la que se guardan las campañas orquestadas creadas en función de esta plantilla.
1. Haga clic en el botón **Crear** para confirmar la configuración.
1. En el lienzo de la plantilla de campaña orquestada, añada y configure las actividades según sea necesario.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Guarde los cambios.

La plantilla de campaña orquestada ya está disponible en la lista de plantillas. Puede crear una campaña orquestada basada en esta plantilla. Esta campaña orquestada se preconfigura con la configuración y las actividades definidas en la plantilla.

>[!ENDTABS]
