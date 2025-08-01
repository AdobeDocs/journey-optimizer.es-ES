---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Obtenga información sobre cómo crear un esquema relacional en Adobe Experience Platform cargando un DDL
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 88eb1438-0fe5-4a19-bfb6-2968a427e9e8
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 57%

---

# Creación de esquemas relacionales mediante un archivo DDL {#file-upload-schema}

+++ Índice

| Bienvenido a campañas orquestadas | Inicie su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Creación y programación de las campañas](create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabajo con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](build-query.md)<br/><br/>[Edición de expresiones](edit-expressions.md)<br/><br/>[Resegmentación](retarget.md) | [Introducción a las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[AND-join](activities/and-join.md) - [Generar público](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades del canal](activities/channels.md) - [Combinar](activities/combine.md) - [Deduplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar público](activities/save-audience.md) - [División](activities/split.md) - [Esperar](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

Defina el modelo de datos relacionales necesario para las campañas orquestadas creando esquemas como **Suscripciones de fidelización**, **Transacciones de fidelización** y **Recompensas de fidelización**. Cada esquema debe incluir una clave principal, un atributo de versiones y las relaciones adecuadas para hacer referencia a entidades como **Destinatarios** o **Marcas**.

Los esquemas se pueden crear manualmente a través de la interfaz o importar de forma masiva mediante un archivo DDL.

En esta sección se proporciona una guía paso a paso sobre cómo crear un esquema relacional en Adobe Experience Platform cargando un archivo DDL (lenguaje de definición de datos). El uso de un archivo DDL permite definir la estructura de su modelo de datos por adelantado, incluidas las tablas, los atributos, las claves y las relaciones.

1. [Cargar un archivo DDL](#ddl-upload) para crear esquemas relacionales y definir su estructura.

1. [Defina relaciones](#relationships) entre tablas en su modelo de datos.

1. [Vincular esquemas](#link-schema) para conectar los datos relacionales con entidades de perfil existentes como Destinatarios o Marcas.

1. [Ingresar datos](ingest-data.md) en su conjunto de datos desde fuentes compatibles.

## Cargar un archivo DDL{#ddl-upload}

Al cargar un archivo DDL, puede definir la estructura del modelo de datos por adelantado, incluidas tablas, atributos, claves y relaciones.

Se admiten las cargas de archivos de esquema basados en Excel. Descargue la [plantilla proporcionada](assets/template.zip) para preparar fácilmente sus definiciones de esquema.

+++Se admiten las siguientes funciones al crear esquemas relacionales en Adobe Experience Platform

* **ENUM**\
  Los campos ENUM son compatibles con la creación de esquemas manual y basada en DDL, lo que permite definir atributos con un conjunto fijo de valores permitidos.

* **Etiqueta de esquema para el control de datos**\
  El etiquetado es compatible a nivel de campo de esquema para aplicar políticas de gobernanza de datos como el control de acceso y las restricciones de uso. Para obtener más información, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=es).

* **Clave compuesta**\
  Las claves principales compuestas son compatibles con las definiciones de esquema relacional, lo que permite el uso de varios campos juntos para identificar registros de forma exclusiva.

+++

1. Inicie sesión en Adobe Experience Platform.

1. Vaya al menú **Administración de datos** > **Esquema**.

1. Haga clic en **Crear esquema**.

1. Seleccione **[!UICONTROL Relacional]** como su **Tipo de esquema**.

   ![](assets/admin_schema_1.png)

1. Seleccione **[!UICONTROL Cargar archivo DDL]** para definir un diagrama de relación de entidades y crear esquemas.

   La estructura de la tabla debe contener:
   * Al menos una clave principal
   * Un identificador de versión, como un campo de tipo `lastmodified`, `datetime` o `number`.
   * Para la ingesta de Change Data Capture (CDC), una columna especial denominada `_change_request_type` de tipo `String`, que indica el tipo de cambio de datos (por ejemplo, insertar, actualizar, eliminar) y habilita el procesamiento incremental


   >[!IMPORTANT]
   >
   > Cualquier esquema usado para la segmentación debe incluir al menos un campo de identidad de tipo `String` con un **área de nombres de identidad** asociado.\
   >Esto garantiza la compatibilidad con las capacidades de segmentación y resolución de identidades de Adobe Journey Optimizer.

1. Arrastre y suelte su archivo DDL y haga clic en **[!UICONTROL Siguiente]**.

   Tenga en cuenta que el tamaño máximo admitido para un archivo DDL es de 10 MB.

1. Escriba su **[!UICONTROL Nombre de esquema]**.

1. Configure cada esquema y sus columnas, asegurándose de especificar una clave principal.

   Un atributo, como `lastmodified`, debe designarse como descriptor de versión. Este atributo, normalmente de tipo `datetime`, `long` o `int`, es esencial para los procesos de ingesta, a fin de garantizar que el conjunto de datos se actualice con la última versión de datos.

   ![](assets/admin_schema_2.png)

1. Haga clic en **[!UICONTROL Listo]** cuando haya finalizado.

Ahora puede comprobar las definiciones de tabla y campo dentro del lienzo. [Más información en la siguiente sección](#entities)

## Definición de relaciones {#relationships}

Para definir conexiones lógicas entre tablas dentro del esquema, siga los pasos que se indican a continuación.

1. Acceda a la vista de lienzo del modelo de datos y elija las dos tablas que desea vincular

1. Haga clic en el botón ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) junto a Unión de origen, y a continuación, arrastre y guíe la flecha hacia Unión de destino para establecer la conexión.

   ![](assets/admin_schema_5.png)

1. Complete el formulario proporcionado para definir el vínculo y haga clic en **Aplicar** una vez configurado.

   ![](assets/admin_schema_3.png)

   **Cardinalidad**:

   * **1-N**: una ocurrencia de la tabla de origen puede tener varias ocurrencias correspondientes de la tabla de destino, pero una ocurrencia de la tabla de destino puede tener como máximo una ocurrencia correspondiente de la tabla de origen.

   * **N-1**: una ocurrencia de la tabla de destino puede tener varias ocurrencias correspondientes de la tabla de origen, pero una ocurrencia de la tabla de origen puede tener como máximo una ocurrencia correspondiente de la tabla de destino.

   * **1-1**: una ocurrencia de la tabla de origen puede tener como máximo una ocurrencia correspondiente de la tabla de destino.

1. Todos los vínculos definidos en el modelo de datos se representan como flechas en la vista de lienzo. Haga clic en la flecha entre dos tablas para ver los detalles, realizar ediciones o quitar el vínculo según sea necesario.

   ![](assets/admin_schema_6.png)

1. Utilice la barra de herramientas para personalizar y ajustar el lienzo.

   ![](assets/toolbar.png)

   * **Aumentar**: amplíe el lienzo para ver los detalles del modelo de datos con mayor claridad.

   * **Reducir**: reduzca el tamaño del lienzo para obtener una vista más amplia del modelo de datos.

   * **Ajustar vista**: ajuste el zoom para ajustar todos los esquemas dentro del área visible.

   * **Filtro**: elija qué esquema desea mostrar en el lienzo.

   * **Forzar diseño automático**: organiza automáticamente los esquemas para mejorar la organización.

   * **Mostrar mapa**: active una superposición del minimapa para que sea más fácil navegar por diseños de esquema grandes o complejos.

1. Haga clic en **Guardar** cuando haya terminado. Esta acción crea los esquemas y los conjuntos de datos asociados y habilita el conjunto de datos para su uso en campañas organizadas.

1. Haga clic en **[!UICONTROL Abrir trabajos]** para supervisar el progreso del trabajo de creación. Este proceso puede tardar un par de minutos, según el número de tablas definidas en el archivo DDL.

   También puede acceder a sus trabajos relacionales si abre la ventana **[!UICONTROL Cargar archivo DDL]** y selecciona **[!UICONTROL Ver todos los trabajos relacionales]**.

   ![](assets/admin_schema_4.png)

## Vincular esquemas {#link-schema}

>[!IMPORTANT]
>
> El sistema solo reconoce las relaciones definidas explícitamente dentro del archivo DDL. Las relaciones de entidad que existan fuera del archivo DDL se ignorarán y no se procesarán.

Establezca una relación entre el esquema **Transacciones de lealtad** y el esquema **Destinatarios** para asociar cada transacción con el registro de cliente correcto.

1. Vaya a **[!UICONTROL Esquemas]** y abra las **Transacciones de lealtad** que creó anteriormente.

1. Haga clic en **[!UICONTROL Añadir relación]** desde las **[!UICONTROL Propiedades de campo]** del cliente.

   ![](assets/schema_1.png)

1. Seleccione **[!UICONTROL Varios a uno]** como la relación **[!UICONTROL Tipo]**.

1. Vincúlese al esquema **Destinatarios** existente.

   ![](assets/schema_2.png)

1. Escriba un **[!UICONTROL Nombre de relación del esquema actual]** y un **[!UICONTROL Nombre de relación del esquema de referencia]**.

1. Haga clic en **[!UICONTROL Aplicar]** para guardar los cambios.

Continúe creando una relación entre el esquema **recompensas por lealtad** y el esquema **Marcas** para asociar cada entrada de recompensa con la marca adecuada.

![](assets/schema_3.png)


<!--### Setting Up Change data capture ingestion {#cdc-ingestion}

If you need to change the data source, you must delete the existing dataflow and create a new one pointing to the same dataset with the new source.

When using Change Data Capture (CDC), it is essential that the source and dataset remain in sync to ensure accurate incremental updates. Follow the steps below:

1. **Schema Requirements**
   - Your schema must include:
     - A **primary key** (e.g., `transaction_id`)
     - A **versioning field** (e.g., `lastmodified` or an incrementing `version_id`)
   - Enable the dataset for **Orchestrated Campaigns** if needed.

2. **CDC Dataflow Setup**
   - During dataflow creation, after choosing your source and files:
     - **Enable the CDC option**
     - Select your CDC-ready dataset
     - Confirm field mappings (especially version field)

3. **Keep Source and Target in Sync**
   - The source system must consistently update the version field so the platform can detect changes accurately.

Once set up, the platform will automatically ingest **only changed or new records** each time the flow runs.
-->
