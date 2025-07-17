---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Obtenga información sobre cómo crear un esquema relacional en Adobe Experience Platform cargando un DDL
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: ea5ef4005be90973046d3f94ea4c2b92eb89ffb4
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 1%

---

# Carga de archivo {#file-upload-schema}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](activities/save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

Defina el modelo de datos relacionales necesario para las campañas orquestadas creando esquemas como **Suscripciones de fidelización**, **Transacciones de fidelización** y **Recompensas de fidelización**. Cada esquema debe incluir una clave principal, un atributo de versiones y las relaciones adecuadas para hacer referencia a entidades como **Destinatarios** o **Marcas**.

Los esquemas se pueden crear manualmente a través de la interfaz o importar de forma masiva mediante un archivo DDL.

En esta sección se proporciona una guía paso a paso sobre cómo crear un esquema relacional en Adobe Experience Platform cargando un archivo DDL (lenguaje de definición de datos). El uso de un archivo DDL permite definir la estructura del modelo de datos por adelantado, incluidas tablas, atributos, claves y relaciones.

## Cargar un archivo DDL{#ddl-upload}

Al cargar un archivo DDL, puede definir la estructura del modelo de datos por adelantado, incluidas tablas, atributos, claves y relaciones.

1. Inicie sesión en Adobe Experience Platform.

1. Vaya a **Administración de datos** > **Esquema**.

1. Haz clic en **Crear esquema**.

1. Se le pedirá que seleccione entre dos tipos de esquema:

   * **Standard**
   * **Relacional**, se usa específicamente para campañas orquestadas

   ![](assets/admin_schema_1.png)

1. Seleccione **Cargar archivo DDL** para definir un diagrama de relación de entidad y crear esquemas.

   La estructura de la tabla debe contener:
   * Al menos una clave principal
   * Un identificador de versión, como un campo `lastmodified` de tipo `datetime` o `number`.

1. Arrastre y suelte su archivo DDL y haga clic en **[!UICONTROL Siguiente]**.

1. Escriba su **[!UICONTROL nombre de esquema]**.

1. Configure cada esquema y sus columnas, asegurándose de que se especifica una clave principal.

   Un atributo, como `lastmodified`, debe designarse como descriptor de versión. Este atributo, normalmente de tipo `datetime`, `long` o `int`, es esencial para los procesos de ingesta a fin de garantizar que el conjunto de datos se actualice con la última versión de datos.

   ![](assets/admin_schema_2.png)

1. Haga clic en **[!UICONTROL Listo]** una vez finalizado.

Ahora puede comprobar las definiciones de tabla y campo dentro del lienzo. [Obtenga más información en la sección siguiente](#entities)

## Definición de relaciones {#relationships}

Para definir conexiones lógicas entre tablas dentro del esquema, siga los pasos a continuación.

1. Acceda a la vista de lienzo del modelo de datos y elija las dos tablas que desea vincular

1. Haga clic en el botón ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) junto a Source Join y, a continuación, arrastre y guíe la flecha hacia Target Join para establecer la conexión.

   ![](assets/admin_schema_5.png)

1. Complete el formulario proporcionado para definir el vínculo y haga clic en **Aplicar** una vez configurado.

   ![](assets/admin_schema_3.png)

   **Cardinalidad**:

   * **1-N**: una incidencia de la tabla de origen puede tener varias incidencias correspondientes de la tabla de destino, pero una incidencia de la tabla de destino puede tener como máximo una incidencia correspondiente de la tabla de origen.

   * **N-1**: una incidencia de la tabla de destino puede tener varias incidencias correspondientes de la tabla de origen, pero una incidencia de la tabla de origen puede tener como máximo una incidencia correspondiente de la tabla de destino.

   * **1-1**: una incidencia de la tabla de origen puede tener como máximo una incidencia correspondiente de la tabla de destino.

1. Todos los vínculos definidos en el modelo de datos se representan como flechas en la vista de lienzo. Haga clic en una flecha entre dos tablas para ver los detalles, realizar ediciones o quitar el vínculo según sea necesario.

   ![](assets/admin_schema_6.png)

1. Utilice la barra de herramientas para personalizar y ajustar el lienzo.

   ![](assets/toolbar.png)

   * **Acercar**: amplíe el lienzo para ver los detalles del modelo de datos con mayor claridad.

   * **Alejar**: reduzca el tamaño del lienzo para obtener una vista más amplia del modelo de datos.

   * **Ajustar vista**: ajuste el zoom para ajustar todos los esquemas dentro del área visible.

   * **Filtro**: elija qué esquema mostrar en el lienzo.

   * **Forzar diseño automático**: organiza automáticamente los esquemas para mejorar la organización.

   * **Mostrar mapa**: cambie una superposición de mapa mínimo para que sea más fácil navegar por diseños de esquema grandes o complejos.

1. Haga clic en **Guardar** una vez finalizado. Esta acción crea los esquemas y los conjuntos de datos asociados y habilita el conjunto de datos para su uso en campañas orquestadas.

1. Haga clic en **[!UICONTROL Abrir trabajos]** para supervisar el progreso del trabajo de creación. Este proceso puede tardar un par de minutos, según el número de tablas definidas en el archivo DDL.

   ![](assets/admin_schema_4.png)

## Esquema de vínculo {#link-schema}

Establezca una relación entre el esquema **transacciones de fidelidad** y el esquema **Destinatarios** para asociar cada transacción con el registro de cliente correcto.

1. Vaya a **[!UICONTROL Esquemas]** y abra las **transacciones de fidelización** que creó anteriormente.

1. Haga clic en **[!UICONTROL Agregar relación]** desde las **[!UICONTROL propiedades de campo]** del cliente.

   ![](assets/schema_1.png)

1. Seleccione **[!UICONTROL Varios a uno]** como la relación **[!UICONTROL Tipo]**.

1. Vínculo al esquema **Recipients** existente.

   ![](assets/schema_2.png)

1. Escriba un **[!UICONTROL nombre de relación del esquema actual]** y **[!UICONTROL nombre de relación del esquema de referencia]**.

1. Haga clic en **[!UICONTROL Aplicar]** para guardar los cambios.

Continúe creando una relación entre el esquema **recompensas por fidelidad** y el esquema **Marcas** para asociar cada entrada de recompensa con la marca adecuada.

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