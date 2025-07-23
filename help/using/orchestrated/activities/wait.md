---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Esperar en campañas organizadas
description: Aprenda a utilizar la actividad Esperar en campañas organizadas
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 85%

---

# Esperar {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Actividad Esperar"
>abstract="La actividad **Esperar** se utiliza para retrasar la transición de una actividad a otra."


+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](../gs-schemas.md)</li><li>[Esquema manual](../manual-schema.md)</li><li>[Esquema de carga de archivos](../file-upload-schema.md)</li><li>[Ingesta de datos](../ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](../access-manage-orchestrated-campaigns.md) | [Pasos clave para crear una campaña organizada](../gs-campaign-creation.md)<br/><br/>[Creación y programación de las campañas](../create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](../orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabajo con el generador de reglas](../orchestrated-rule-builder.md)<br/><br/>[Creación de su primera consulta](../build-query.md)<br/><br/>[Edición de expresiones](../edit-expressions.md)<br/><br/>[Resegmentación](../retarget.md) | [Introducción a las actividades](about-activities.md)<br/><br/>Actividades:<br/>[AND-join](and-join.md) - [Generar público](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Actividades del canal](channels.md) - [Combinar](combine.md) - [Deduplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [Guardar público](save-audience.md) - [División](split.md) - <b>[Esperar](wait.md)</b> |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

La actividad **[!UICONTROL Esperar]** es un componente de **[!UICONTROL Control de flujo]** que se usa para introducir un retraso entre dos actividades en una campaña organizada. Esto le ayuda a garantizar que las actividades de seguimiento estén mejor sincronizadas y sean más relevantes para la participación del usuario.

Por ejemplo, puede esperar unos días después de un envío de correo electrónico para rastrear aperturas y clics antes de enviar un mensaje de seguimiento.

## Configuración{#wait-configuration}

Siga estos pasos para configurar la actividad **[!UICONTROL Esperar]**:

1. Añada una actividad **[!UICONTROL Esperar]** a la campaña organizada.

1. Seleccione el tipo de espera que mejor se adapte a sus necesidades:

   * **[!UICONTROL Duración]**: especifique un retraso en segundos, minutos, horas o días antes de continuar con la siguiente actividad.

   * **[!UICONTROL Tiempo fijo]**: establezca una fecha y hora específicas después de la cual comienza la siguiente actividad.

   ![](../assets/wait_activity.png)

## Ejemplo{#wait-example}

El siguiente ejemplo ilustra la actividad **[!UICONTROL Esperar]** en un caso de uso típico.  Se envía un correo electrónico con un código promocional a los perfiles que celebran su cumpleaños. Después de 29 días, se envía un SMS al mismo grupo como recordatorio de que el código de promoción de cumpleaños está a punto de caducar.

![](../assets/wait-example.png)
