---
solution: Journey Optimizer
product: journey optimizer
title: Limitaciones y protecciones de campañas organizadas
description: Obtenga información acerca de las limitaciones y protecciones de campañas orquestadas
hide: true
hidefromtoc: true
source-git-commit: 54d5b3386da4eed53fca79a2135ab54548855150
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 11%

---

# Mecanismos de protección y limitaciones {#guardrails}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Publicación de la campaña orquestada"
>abstract="Para iniciar su campaña, debe publicarla. Asegúrese de que todas las advertencias se borran antes de la publicación."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](activities/save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Limitaciones de flujo de datos a conjunto de datos

Cada conjunto de datos en Adobe Experience Platform solo se puede asociar a un flujo de datos activo a la vez. Esta cardinalidad 1:1 la aplica estrictamente la plataforma.

Si necesita cambiar las fuentes de datos (por ejemplo, de Amazon S3 a Salesforce):

Debe eliminar el flujo de datos existente conectado al conjunto de datos.

A continuación, cree un nuevo flujo de datos con el nuevo origen asignado al mismo conjunto de datos.

Esto garantiza una ingesta de datos fiable y es esencial al utilizar la captura de datos de cambio (CDC), que depende de una clave principal definida y de un atributo de versiones (por ejemplo, lastmodified) para las actualizaciones incrementales.


## Esquemas relacionales/limitaciones de ingesta de datos

* Número de esquemas: el número máximo de esquemas relacionales (tablas en el almacén de datos relacional) es 200
* Tamaño del esquema relacional: el tamaño máximo del esquema relacional para la orquestación de campaña será de 100 GB.
* Frecuencia de ingesta de datos: la frecuencia de ingesta de datos por lotes para Campaign Orchestration no debe superar uno cada quince minutos.
* Cambios/actualizaciones: las actualizaciones/cambios diarios deben ser inferiores al 20 % del total de registros para un esquema relacional determinado