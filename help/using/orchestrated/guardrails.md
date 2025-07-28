---
solution: Journey Optimizer
product: journey optimizer
title: Limitaciones y protecciones de campañas organizadas
description: Obtenga información acerca de las limitaciones y protecciones de campañas orquestadas
hide: true
hidefromtoc: true
exl-id: 82744db7-7358-4cc6-a9dd-03001759fef7
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 10%

---

# Mecanismos de protección y limitaciones {#guardrails}

+++ Índice

| Bienvenido a campañas orquestadas | Inicie su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Creación y programación de las campañas](create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabajo con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](build-query.md)<br/><br/>[Edición de expresiones](edit-expressions.md)<br/><br/>[Resegmentación](retarget.md) | [Introducción a las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[AND-join](activities/and-join.md) - [Generar público](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades del canal](activities/channels.md) - [Combinar](activities/combine.md) - [Deduplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar público](activities/save-audience.md) - [División](activities/split.md) - [Esperar](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Limitaciones de flujo de datos a conjunto de datos

Cada conjunto de datos en Adobe Experience Platform solo se puede asociar a un flujo de datos activo a la vez. La plataforma aplica estrictamente esta cardinalidad de 1:1.

Si necesita cambiar las fuentes de datos (por ejemplo, de Amazon S3 a Salesforce):

Debe eliminar el flujo de datos existente conectado al conjunto de datos.

A continuación, cree un nuevo flujo de datos con el nuevo origen asignado al mismo conjunto de datos.

Esto garantiza una ingesta de datos fiable y es esencial al utilizar la captura de datos de cambio (CDC), que depende de una clave principal definida y de un atributo de versiones (por ejemplo, lastmodified) para las actualizaciones incrementales.


## Esquemas relacionales/limitaciones de ingesta de datos

* Se admiten hasta 200 esquemas relacionales (tablas) en el almacén de datos relacional.

* El tamaño total de un esquema relacional utilizado para Campaign Orchestration no debe superar los 100 GB.

* La ingesta por lotes para Campaign Orchestration no debe producirse con más frecuencia que una vez cada 15 minutos.

* Los cambios diarios en un esquema relacional deben permanecer por debajo del 20 % del recuento total de registros.

## Modelado de datos

* El descriptor de versión es obligatorio en todos los esquemas, incluidas las tablas de hechos.

* Se requiere una clave principal para cada tabla.

* El nombre de tabla asignado durante la creación del conjunto de datos se utiliza en la interfaz de usuario de segmentación y en las funciones de personalización.

  Este nombre es permanente y no se puede cambiar después de crearlo.

* Actualmente no se admiten grupos de campos.

## Ingesta de datos

* Se requiere la ingesta de datos relacionales y de perfil.

* Se requiere un campo de tipo de cambio para la ingesta basada en archivos, mientras que el registro de tabla debe estar habilitado para la ingesta de Cloud DB. Esto es necesario para Change Data Capture (CDC).

* La latencia desde la ingesta hasta la disponibilidad de los datos en Snowflake varía entre 15 minutos y 2 horas, según el volumen de datos, la concurrencia y el tipo de operaciones (las inserciones son más rápidas que las actualizaciones).

* La monitorización de datos en Snowflake está en desarrollo; actualmente, no hay ninguna confirmación nativa para una ingesta correcta.

* No se admiten actualizaciones directas en Snowflake o en el conjunto de datos. Todos los cambios deben fluir a través de fuentes de CDC.

  El servicio de consultas es de solo lectura.

* ETL no es compatible: los clientes deben proporcionar los datos en el formato requerido.

* No se permiten actualizaciones parciales. Cada fila debe proporcionarse como un registro completo.

* La ingesta se basa en Query Service y Data Distiller.

## Segmentación

* La lista de valores y las enumeraciones están disponibles actualmente.

* Las audiencias guardadas son listas estáticas, su contenido refleja los datos disponibles en el momento en que se ejecuta la campaña.

* No se admite anexar a una audiencia guardada. Las actualizaciones requieren una sobrescritura completa.

* Las audiencias solo deben constar de atributos escalares; no se admiten mapas y matrices.

* La segmentación admite principalmente datos relacionales. Aunque se permite la mezcla con datos de perfil, la introducción de conjuntos de datos de perfil grandes puede afectar al rendimiento. Para evitarlo:

* Existen protecciones, como la limitación del número de atributos de perfil seleccionados en las audiencias por lotes o de streaming.

* Las audiencias de lectura no se almacenan en caché; cada campaña se ejecuta con un déclencheur de lectura completo.

  La optimización es necesaria para audiencias grandes o complejas.