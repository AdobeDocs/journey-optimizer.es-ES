---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Obtenga información sobre cómo introducir datos en Adobe Experience Platform desde fuentes compatibles como SFTP, almacenamiento en la nube o bases de datos.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: 3dc0bf4acc4976ca1c46de46cf6ce4f2097f3721
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 6%

---

# Ingesta de datos {#ingest-data}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales</br> <ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](activities/save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

Adobe Experience Platform permite la ingesta de datos desde fuentes externas, al tiempo que le ofrece la capacidad de estructurar, etiquetar y mejorar los datos entrantes mediante los servicios de Experience Platform. Puede ingerir datos de una variedad de fuentes, como aplicaciones de Adobe, almacenamiento basado en la nube, bases de datos y muchas otras.

## Con almacenamiento en la nube {#ingest}


>[!IMPORTANT]
>
>Cada conjunto de datos de Adobe Experience Platform solo admite un flujo de datos activo a la vez. Para obtener instrucciones de configuración detalladas sobre cómo cambiar las fuentes de datos, consulte esta [sección](#cdc-ingestion).


Puede configurar un flujo de datos para introducir datos de una fuente de Amazon S3 en Adobe Experience Platform. Una vez configurado, el flujo de datos permite la ingesta automatizada y programada de datos estructurados y admite actualizaciones en tiempo real.

1. Desde el menú **[!UICONTROL Conexiones]**, acceda al menú **[!UICONTROL Fuentes]**.

1. Seleccione la categoría **[!UICONTROL Cloud Storage]**, luego Amazon S3 y haga clic en **[!UICONTROL Agregar datos]**.

   ![](assets/admin_sources_1.png)

1. Conecte su cuenta S3:

   * Con una cuenta existente

   * Con una cuenta nueva

   [Obtenga más información en la documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3#connect)

   ![](assets/admin_sources_2.png)

1. Elija su carpeta **[!UICONTROL Formato de datos]**, **[!UICONTROL Delimitador]** y **[!UICONTROL Tipo de compresión]**.

1. Navegue por el origen de S3 conectado hasta que encuentre las carpetas deseadas, por ejemplo **recompensas de fidelidad** y **transacciones de fidelidad**.

1. Seleccione la carpeta que contiene los datos.

   Al seleccionar una carpeta, se garantiza que todos los archivos actuales y futuros con la misma estructura se procesen automáticamente. Sin embargo, para seleccionar un solo archivo es necesario cargar manualmente cada incremento de datos nuevo.

   ![](assets/S3_config_2.png)

1. Elija su carpeta **[!UICONTROL Formato de datos]**, **[!UICONTROL Delimitador]** y **[!UICONTROL Tipo de compresión]**. Revise los datos de ejemplo para comprobar su precisión y, a continuación, haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/S3_config_1.png)

1. Marque **[!UICONTROL Habilitar la captura de datos modificados]** para seleccionar entre conjuntos de datos asignados a esquemas relacionales que tienen una clave principal y un descriptor de versión definidos.

1. Seleccione su [conjunto de datos](#entities) creado anteriormente y haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/S3_config_3.png)

1. En la ventana **[!UICONTROL Mapping]**, compruebe que cada atributo del archivo de origen esté asignado correctamente con los campos correspondientes del esquema de destino.

   Haga clic en **[!UICONTROL Siguiente]** una vez finalizado.

   ![](assets/S3_config_4.png)

1. Configure el flujo de datos **[!UICONTROL Programar]** según la frecuencia que desee.

1. Haga clic en **[!UICONTROL Finalizar]** para crear el flujo de datos. Se ejecutará automáticamente según la programación definida.

1. En el menú **[!UICONTROL Conexiones]**, seleccione **[!UICONTROL Fuentes]** y acceda a la pestaña **[!UICONTROL Flujos de datos]** para rastrear la ejecución del flujo, revisar los registros ingeridos y solucionar cualquier error.

   ![](assets/S3_config_5.png)

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
