---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Aprenda a crear esquemas relacionales directamente a través de la interfaz de usuario.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 8c785431-9a00-46b8-ba54-54a10e288141
source-git-commit: c5a0c6401add384685c9d7ab2c623076ea4bf793
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 7%

---

# Esquema manual {#manual-schema}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br><ul><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul><br/><br/>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](activities/save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

Los esquemas relacionales se pueden crear directamente a través de la interfaz de usuario, lo que permite una configuración detallada de atributos, claves principales, campos de versiones y relaciones.

En el siguiente ejemplo se define manualmente el esquema Membresías de fidelización para ilustrar la estructura necesaria para las campañas organizadas.

1. Inicie sesión en Adobe Experience Platform.

1. Vaya a **Administración de datos** > **Esquema**.

1. Haz clic en **Crear esquema**.

1. Se le pedirá que seleccione entre dos tipos de esquema:

   * **Standard**
   * **Relacional**, se usa específicamente para campañas orquestadas

   ![](assets/admin_schema_1.png)

1. Proporcione un **Nombre de esquema** (por ejemplo, `test_demo_ck001`).
1. Elija **Tipo de esquema**:
   &#x200B;- **Tipo de registro** (requerido para campañas AGO)
   &#x200B;- **Serie temporal** (no aplicable aquí)
1. Haga clic en **Finalizar** para continuar al lienzo de diseño de esquema.

## Seleccionar entidades y campos para importar

1. En el lienzo, agregue atributos (campos) al esquema.
1. Agregar una **clave principal** (obligatoria).
1. Agregar un atributo **Descriptor de versión** (para compatibilidad con CDC):
Debe ser del tipo **DateTime** o **Numérico** (entero, largo, corto, byte).
Ejemplo común: `last_modified`

> **¿Por qué?**: la **clave principal** identifica de forma exclusiva cada registro, y el **descriptor de versión** realiza un seguimiento de los cambios, lo que admite la recopilación de datos de cambio (CDC) y la duplicación de datos.

1. Marque los campos apropiados como **Clave principal** y **Descriptor de versión**.
1. Haga clic en **Guardar**.


<!--

## 5. Creating a Dataset

1. Navigate to **Datasets**.
1. Click on **Create Dataset**.
1. Select the schema you just created.
1. Assign a **Dataset Name** (same as schema is fine).
1. Optionally, add tags (e.g., `AGO_campaigns`).
6. Ensure the checkbox **"Relational Schema"** is checked.
7. Click **Finish**.

> **Note:** Only one dataset can be created per relational schema.


## 6. Enabling the Dataset

1. Click **Enable** for the dataset.
1. Wait a few moments for the status to show **Enabled**.

> **Why?** Without enabling, the dataset cannot be used in orchestrated campaigns or ingest data.

## 7. Creating a Data Source (S3)

1. Navigate to **Sources**.
1. Click **Create Source**.
1. Choose the source type (e.g., **S3 Bucket**).
1. Provide connection details:
    - Bucket Path (optionally include subfolder path)
1. Save the source.

## 8. Preparing and Uploading Data

1. Prepare your CSV file with:
    - Column headers matching your schema attributes
    - `last_modified` column
    - `change_type` column (`U`/`DU` for upsert, `D` for delete)

> **Important:** `change_type` is required but does not need to be defined in the schema.

1. Save the file as `.csv`.

1. Upload the file to the specified folder in your S3 bucket.


## 9. Ingesting Data from S3

1. Go to **Sources** and find your S3 source.
1. Click **Add Data**.
1. Select the uploaded file.
1. Specify the file format as **CSV** and any compression type if applicable.
1. Review the data preview (ensure `change_type`, `last_modified`, and primary key are visible).
1. Click **Next**.

### Enable Change Data Capture (CDC)

- Check **Enable Change Data Capture**.
- Select the dataset enabled for AGO campaigns.

### Field Mapping

- Fields are auto-mapped (note that `change_type` is not mapped and that's expected).
- Click **Next**.

### Scheduling

- Schedule ingestion frequency (minute, hour, day, week).
- Set start time (immediate or future).
- Click **Finish** to create the data flow.

## 10. Monitoring Data Flow

1. Navigate back to **Sources > Data Flows**.
1. Wait 4–5 minutes for the first run (initial overhead).
1. Monitor:
    - Status (Started, Completed)
    - Number of records ingested
    - Errors (if any)

> **Tip:** Ingested data first lands in the **Data Lake**.

## 11. Data Replication to Data Store

The **Data Store** is updated:

- Every **15 minutes**, or

- If **Data Lake size exceeds 5MB**

This is a background replication process.


## 12. Querying the Dataset

1. Navigate to **Query Services**.
1. Click **Create Query**.
1. Example query:

   ```sql
   SELECT * FROM test_demo_ck001;
   ```

1. Run the query.

> **Note:** If ingestion is incomplete, query will return an error. Check data flow status.

-->