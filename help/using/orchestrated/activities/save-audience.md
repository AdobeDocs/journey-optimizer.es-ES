---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Guardar audiencia
description: Aprenda a utilizar la actividad Guardar audiencia en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 3%

---

# Guardar público {#save-audience}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](../configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](../gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](../create-orchestrated-campaign.md)<br/><br/>[Organice las actividades](../orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabaje con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](../build-query.md)<br/><br/>[Edite expresiones](../edit-expressions.md)<br/><br/>[Redireccionamiento](../retarget.md) | [Empiece con las actividades](about-activities.md)<br/><br/>Actividades:<br/>[Y únase](and-join.md) - [Generar audiencia](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades de canal](channels.md) - [Combinar](combine.md) - [Anulación de duplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - <b>[Guardar](save-audience.md)</b> - [División](split.md) [Espera](wait.md) |

{style="table-layout:fixed"}

+++


La actividad **[!UICONTROL Guardar audiencia]** es una actividad de **[!UICONTROL segmentación]** que le permite actualizar una audiencia existente o crear una nueva a partir de la población generada anteriormente en la campaña orquestada. Una vez creadas, estas audiencias se añaden a la lista de audiencias de la aplicación y se puede acceder a ellas desde el menú **[!UICONTROL Audiencias]**.

Esta actividad es especialmente útil para preservar segmentos de audiencia calculados dentro de la misma campaña orquestada, lo que los hace disponibles para su reutilización en campañas futuras. Normalmente está conectado a otras actividades de segmentación, como **[!UICONTROL Generar audiencia]** o **[!UICONTROL Combinar]**, para capturar y guardar la población resultante.

## Configuración de la actividad Guardar audiencia {#save-audience-configuration}

Siga estos pasos para configurar la actividad **Guardar audiencia**:

1. Agregue una actividad **Guardar audiencia** a su campaña orquestada.

1. En la lista desplegable **Modo**, seleccione la acción que desee realizar:

   * **Crear o actualizar una audiencia existente**: defina una **etiqueta de audiencia**. Si la audiencia ya existe, se actualiza; de lo contrario, se crea una nueva.

   * **Actualizar una audiencia existente**: elija la **audiencia** que desee actualizar de la lista de audiencias existentes.

1. Seleccione el **modo de actualización** que se aplica a las audiencias existentes:

   * **Reemplazar contenido de audiencia por datos nuevos**: se reemplaza todo el contenido de audiencia y se pierden datos antiguos. Solo se conservan los datos de la transición entrante de la actividad **Guardar audiencia**. Esta opción borra el tipo de audiencia y la dimensión de segmentación de la audiencia actualizada.

   * **Audiencia completa con nuevos datos**: El contenido de audiencia anterior se conserva y los datos de la transición entrante de la actividad **Guardar audiencia** se agregan a ella.

1. Marque la opción **Generar una transición saliente** si desea agregar una transición después de la actividad **Guardar audiencia**.

El contenido de la audiencia guardada está disponible en la vista de detalles de la audiencia, a la que se puede acceder desde el menú **Audiencias**. Las columnas disponibles en esta vista corresponden a las columnas de la transición entrante de la actividad de la campaña orquestada **Guardar audiencia**.

## Ejemplo {#save-audience-example}

El siguiente ejemplo ilustra una actualización de audiencia simple desde la segmentación. Un planificador ejecuta la campaña orquestada una vez al mes. Una consulta recupera todos los perfiles suscritos a las diferentes aplicaciones disponibles. La actividad **Guardar audiencia** actualiza la audiencia eliminando perfiles que han cancelado la suscripción al servicio desde la última ejecución de campaña orquestada y agregando perfiles recién suscritos.
