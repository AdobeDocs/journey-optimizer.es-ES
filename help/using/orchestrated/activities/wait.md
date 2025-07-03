---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Espera en campañas orquestadas
description: Aprenda a utilizar la actividad Espera en campañas orquestadas
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 13%

---

# Espere {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Actividad Esperar"
>abstract="La actividad **Esperar** se utiliza para retrasar la transición de una actividad a otra."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organice las actividades](orchestrate-activities.md)<br/><br/><b>[Inicie y supervise la campaña](start-monitor-campaigns.md)</b><br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

La actividad **[!UICONTROL Wait]** es un componente **[!UICONTROL Flow control]** que se usa para producir un retraso entre dos actividades en una campaña orquestada. Esto le ayuda a garantizar que las actividades de seguimiento se realicen mejor a tiempo y sean más relevantes para la participación del usuario.

Por ejemplo, puede esperar unos días después de una entrega de correo electrónico para rastrear aperturas y clics antes de enviar un mensaje de seguimiento.

## Configuración{#wait-configuration}

Siga estos pasos para configurar la actividad **[!UICONTROL Esperar]**:

1. Agregue una actividad **[!UICONTROL Wait]** a su campaña orquestada.

1. Seleccione el tipo de espera que mejor se adapte a sus necesidades:

   * **[!UICONTROL Duración]**: especifique un retraso en segundos, minutos, horas o días antes de continuar con la siguiente actividad.

   * **[!UICONTROL Tiempo fijo]**: establezca una fecha y hora específicas después de la cual comienza la siguiente actividad.

   ![](../assets/wait_activity.png)

## Ejemplo{#wait-example}

El siguiente ejemplo ilustra la actividad **[!UICONTROL Wait]** en un caso de uso típico.  Se envía un correo electrónico con un código promocional a los perfiles que celebran su cumpleaños. Después de 29 días, se envía un SMS al mismo grupo como recordatorio de que el código de promoción de cumpleaños está a punto de caducar.

![](../assets/wait-example.png)
