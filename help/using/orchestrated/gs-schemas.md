---
solution: Journey Optimizer
product: journey optimizer
title: Pasos de configuración
description: Obtenga información sobre cómo crear un esquema relacional en Adobe Experience Platform cargando un DDL
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 81f0338935ee36b152963f2b1c0e7989b86f5f8a
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 5%

---

# Introducción a esquemas y conjuntos de datos{#gs-schemas}

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

Esta guía muestra el proceso de creación de un esquema relacional, configuración de un conjunto de datos para campañas organizadas e ingesta de datos.

![](assets/do-not-localize/schema_admin.png)

1. Crear [esquema relacional manualmente](manual-schema.md) o [con un archivo DDL](file-upload-schema.md)

   Defina la estructura del modelo de datos, incluidas las tablas, los atributos y las relaciones. Elija crear el esquema manualmente en la interfaz de usuario o cargar un archivo DDL para una configuración más rápida.

1. [Esquema de vínculo] (file-upload-md)

   establezca relaciones entre los esquemas para garantizar la coherencia de los datos y habilitar consultas entre entidades. Por ejemplo, vincule las transacciones de lealtad a los destinatarios o las recompensas a las marcas.

1. [Ingesta de datos](ingest-data.md)

   Incluya datos en Adobe Experience Platform desde fuentes compatibles como SFTP, almacenamiento en la nube o bases de datos.

