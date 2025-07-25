---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Guardar público
description: Aprenda a utilizar la actividad Guardar público en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: c040ad5433d041f0f4f83fce46bc02662b77648f
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 45%

---

# Guardar público {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Guardar actividad de audiencia"
>abstract="La actividad **Guardar público** es una actividad de **Segmentación** que le permite actualizar un público existente o crear uno nuevo a partir de la población generada anteriormente en la campaña organizada. Una vez creados, estos públicos se añaden a la lista de públicos de la aplicación y se puede acceder a ellos desde el menú **Públicos**."


+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carga de archivos](../file-upload-schema.md)</li><li>[Ingesta de datos](../ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña organizada](../gs-campaign-creation.md)<br/><br/>[Creación y programación de las campañas](../create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](../orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabajo con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](../build-query.md)<br/><br/>[Edición de expresiones](../edit-expressions.md)<br/><br/>[Resegmentación](../retarget.md) | [Introducción a las actividades](about-activities.md)<br/><br/>Actividades:<br/>[AND-join](and-join.md) - [Generar público](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades del canal](channels.md) - [Combinar](combine.md) - [Deduplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - <b>[Guardar público](save-audience.md)</b> - [División](split.md) - [Esperar](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

La actividad **[!UICONTROL Guardar audiencia]** es una actividad de **[!UICONTROL Segmentación]** que se usa para crear una audiencia nueva o actualizar una existente en función de la población generada anteriormente en la campaña orquestada. Una vez guardada, la audiencia se agrega a la lista de audiencias de aplicación y se puede acceder a ella desde el menú **[!UICONTROL Audiencias]**.

Normalmente se utiliza para capturar segmentos de audiencia creados dentro del mismo flujo de trabajo de campaña, lo que los hace disponibles para su reutilización en campañas futuras. Normalmente, está conectado a otras actividades de segmentación, como **[!UICONTROL Generar audiencia]** o **[!UICONTROL Combinar]**, para guardar la población de destino final.

## Configuración de la actividad Guardar público {#save-audience-configuration}

Siga estos pasos para configurar la actividad **[!UICONTROL Guardar público]**:

1. Añada la actividad **[!UICONTROL Guardar público]** a su campaña organizada.

1. Escriba una **[!UICONTROL etiqueta de público]** que identifique el público guardado.

1. Elija un **[!UICONTROL campo de asignación de perfiles&#x200B;]** de su dimensión de segmentación de campañas.

   ➡️ [Siga los pasos detallados en esta página para crear su dimensión de segmentación de campaña](../target-dimension.md)

   ![](../assets/save-audience-1.png)

1. Haga clic en **[!UICONTROL Agregar asignaciones de audiencia]** si desea asociar la audiencia guardada con campos de identidad adicionales.

   ![](../assets/save-audience-2.png)

1. Finalice la configuración, guarde y publique la campaña organizada. Así se generará y almacenará su público.

El contenido de la audiencia guardada está disponible en la vista de detalles de la audiencia, a la que se puede acceder desde el menú **[!UICONTROL Audiencias]**, o se puede seleccionar al segmentar una audiencia, por ejemplo, con una actividad **[!UICONTROL Leer audiencia]**.

![](../assets/save-audience-4.png)


## Ejemplo {#save-audience-example}

En el siguiente ejemplo se muestra cómo crear un público simple mediante la segmentación. Una consulta identifica a todos los destinatarios que reservaron un viaje en los últimos 30 días filtrando esta población dentro de la campaña orquestada. Al elegir **Destinatarios - CRMID** como **dimensión de segmentación**, la audiencia se dirige a cada evento de reserva individual en lugar de solo al destinatario en su conjunto. A continuación, la actividad **[!UICONTROL Guardar público]** captura estos perfiles para crear un público reutilizable de compradores recientes.

![](../assets/save-audience-3.png)
