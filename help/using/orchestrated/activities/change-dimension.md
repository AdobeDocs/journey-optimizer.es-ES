---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Change dimension
description: Aprenda a utilizar la actividad de la dimensión Cambiar
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 25%

---

# Cambiar dimensión {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Generación de un complemento"
>abstract="Puede generar una transición saliente adicional con la población restante, que se excluyó como duplicado. Para ello, active la opción **Generar complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Actividad cambiar dimensión"
>abstract="Esta actividad le permite cambiar la dimensión de segmentación a medida que genera un público. Desplace el eje en función de la plantilla de datos y la dimensión de entrada. Por ejemplo, puede cambiar de la dimensión “contratos” a la dimensión “clientes”."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organice las actividades](orchestrate-activities.md)<br/><br/><b>[Inicie y supervise la campaña](start-monitor-campaigns.md)</b><br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Como especialista en marketing, puede mejorar la segmentación de audiencia cambiando de una entidad de datos a una relacionada dentro de una campaña orquestada. Esto le permite ir más allá de los perfiles de usuario y centrarse en comportamientos específicos, como compras, reservas u otras interacciones.

Para lograrlo, use la actividad **[!UICONTROL Cambiar dimensión]**. Permite ajustar la dimensión de segmentación durante la campaña orquestada.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configuración de la actividad Change dimension {#configure}

Siga estos pasos para configurar la actividad **[!UICONTROL Cambiar dimensión]**:

1. Agregue una actividad **[!UICONTROL Change dimension]** a su campaña orquestada.

   ![](../assets/orchestrated-change-dimension.png)

1. Defina **[!UICONTROL Nueva dimensión de destino]**. Durante el cambio de dimensión, se guardan todos los registros.


## Ejemplo {#example}

Este caso de uso se centra en enviar un SMS a perfiles que han creado una lista de deseos durante el mes pasado.

Comience con una actividad **[!UICONTROL Generar audiencia]**, usando la dimensión de segmentación **[!UICONTROL Wishlist]** para identificar todas las listas de deseos relevantes.

A continuación, agregue una actividad **[!UICONTROL Change dimension]** para cambiar la dimensión de segmentación de **[!UICONTROL Wishlist]** a **[!UICONTROL Destinatario].** Este paso garantiza que los objetivos de la campaña orquestada sean los perfiles correctos vinculados a esas listas de deseos, lo que permite enviar el SMS a los perfiles deseados.

![](../assets/orchestrated-change-dimension-example.png)
