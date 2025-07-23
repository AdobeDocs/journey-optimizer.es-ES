---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Obtenga información sobre cómo introducir datos en Adobe Experience Platform desde fuentes compatibles como SFTP, almacenamiento en la nube o bases de datos.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7f1e7985-b68e-43d6-9c8f-fea2469f8af9
source-git-commit: 6447f5d1a060037c0ceaa374db20966097585f9c
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 38%

---

# Ingesta de datos {#ingest-data}

+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales</br> <ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Creación y programación de las campañas](create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabajo con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](build-query.md)<br/><br/>[Edición de expresiones](edit-expressions.md)<br/><br/>[Resegmentación](retarget.md) | [Introducción a las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[AND-join](activities/and-join.md) - [Generar público](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades del canal](activities/channels.md) - [Combinar](activities/combine.md) - [Deduplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar público](activities/save-audience.md) - [División](activities/split.md) - [Esperar](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Para cambiar el origen de datos de un conjunto de datos, primero debe eliminar el flujo de datos existente antes de crear uno nuevo que haga referencia al mismo conjunto de datos y al nuevo origen.
>
>Adobe Experience Platform aplica una estricta relación uno a uno entre flujos y conjuntos de datos. Esto le permite mantener la sincronización entre el origen y el conjunto de datos para una ingesta incremental precisa.

Adobe Experience Platform permite la ingesta de datos desde fuentes externas, al tiempo que ofrece la posibilidad de estructurar, etiquetar y mejorar los datos entrantes mediante los servicios de Experience Platform. Puede ingerir datos de una variedad de fuentes, como aplicaciones de Adobe, almacenamiento basado en la nube, bases de datos y muchas otras.

## Fuentes compatibles con campañas organizadas {#supported}

Los siguientes recursos son compatibles con las campañas orquestadas:

<table>
  <thead>
    <tr>
      <th>Tipo</th>
      <th>Fuente</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">Almacenamiento en la nube</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3">Amazon S3</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/google-cloud-storage">Almacenamiento en la nube de Google</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/sftp">SFTP</a></td>
    </tr>
      <td rowspan="4">Almacenes de datos en la nube</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/snowflake">Snowflake</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/bigquery">Google BigQuery</a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/data-landing-zone">Zona de aterrizaje de datos<a></td>
    </tr>
    <tr>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/databases/databricks">Azure Databricks</a></td>
    </tr>
    <tr>
      <td rowspan="3">Cargas basadas en archivos</td>
      <td><a href="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/local-system/local-file-upload">Carga de archivo local<a></td>
    </tr>

</tbody>
</table>

## Configuración de un flujo de datos

En este ejemplo se muestra cómo configurar un flujo de datos que ingiere datos estructurados en Adobe Experience Platform. El flujo de datos configurado admite la ingesta automatizada y programada y permite realizar actualizaciones en tiempo real.

1. Desde el menú **[!UICONTROL Conexiones]**, acceda al menú **[!UICONTROL Fuentes]**.

1. Elija su fuente según las [Fuentes compatibles con las campañas orquestadas](#supported).

   ![](assets/admin_sources_1.png)

1. Conecte su cuenta de Cloud Storage o Google Cloud Storage si elige fuentes basadas en la nube.

   ![](assets/admin_sources_2.png)

1. Elija los datos que desea introducir en Adobe Experience Platform.

   ![](assets/S3_config_1.png)

1. En la página **[!UICONTROL Detalles del conjunto de datos]**, marque **[!UICONTROL Habilitar la captura de datos de cambio]** para mostrar solo los conjuntos de datos asignados a esquemas relacionales e incluir una clave principal y un descriptor de versión.

   >[!IMPORTANT]
   >
   > Solo para **orígenes basados en archivos**, cada fila del archivo de datos debe incluir una columna `_change_request_type` con los valores `U` (actualización) o `D` (eliminación). Sin esta columna, el sistema no reconocerá los datos como compatibles con el seguimiento de cambios y no aparecerá la opción Campaña orquestada, lo que impedirá que se seleccione el conjunto de datos para el direccionamiento.

   ![](assets/S3_config_6.png)

1. Seleccione el conjunto de datos creado anteriormente y haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/S3_config_3.png)

1. Si solo usa orígenes basados en archivos, en la ventana **[!UICONTROL Seleccionar datos]**, cargue los archivos locales y obtenga una vista previa de su estructura y contenido.

   Tenga en cuenta que el tamaño máximo admitido es de 100 MB.

1. En la ventana **[!UICONTROL Asignación]**, compruebe que cada atributo del archivo de origen esté asignado correctamente con los campos correspondientes en el esquema de destino.

   Haga clic en **[!UICONTROL Siguiente]** cuando haya terminado.

   ![](assets/S3_config_4.png)

1. Configure el flujo de datos **[!UICONTROL Programar]** según la frecuencia que desee.

1. Haga clic en **[!UICONTROL Finalizar]** para crear el flujo de datos. Se ejecuta automáticamente según la programación definida.

1. En el menú **[!UICONTROL Conexiones]**, seleccione **[!UICONTROL Fuentes]** y acceda a la pestaña **[!UICONTROL Flujos de datos]** para rastrear la ejecución del flujo, revisar los registros ingeridos y solucionar cualquier error.

   ![](assets/S3_config_5.png)

