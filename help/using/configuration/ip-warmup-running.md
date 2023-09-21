---
solution: Journey Optimizer
product: journey optimizer
title: Ejecutar el plan de calentamiento de IP
description: Obtenga información sobre cómo ejecutar y supervisar un plan de calentamiento de IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, grupos, grupo, subdominios, capacidad de entrega
hide: true
hidefromtoc: true
source-git-commit: 11bdb3ddc666d2025133f70ab522c4ce2d676aa6
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 1%

---

# Ejecutar el plan de calentamiento de IP {#ip-warmup-running}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción al calentamiento de IP](ip-warmup-gs.md)
* [Creación de campañas de calentamiento de IP](ip-warmup-campaign.md)
* [Crear un plan de calentamiento de IP](ip-warmup-plan.md)
* **[Ejecutar el plan de calentamiento de IP](ip-warmup-running.md)**

>[!ENDSHADEBOX]

## Definición de las fases {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Seleccionar audiencias de campañas que excluir"
>abstract="Seleccione las audiencias de otras campañas que desee excluir de la fase actual."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Seleccionar grupos de dominio que excluir"
>abstract="Seleccione los dominios que desea excluir de la fase actual."

Debe asociar la campaña y la audiencia en el nivel de fase y activar algunas configuraciones según sea necesario para todas las ejecuciones asociadas con un solo elemento creativo/campaña

En el nivel de fase, el sistema garantiza que los perfiles objetivo anteriormente + nuevos se recojan y, en el nivel de iteración, el sistema garantiza que cada ejecución tenga perfiles únicos y que el recuento coincida con lo que se indica en el plan

1. Para cada fase, seleccione la campaña que desee asociar con esta fase del plan de calentamiento de IP.

   ![](assets/ip-warmup-plan-select-campaign.png)

   Recuerde lo siguiente:

   * Solo las campañas con el **[!UICONTROL Activación del plan de calentamiento IP]** opción habilitada <!--and live?--> están disponibles para su selección. [Más información](#create-ip-warmup-campaign)

   * Debe seleccionar una campaña que utilice la misma superficie que la seleccionada para el plan de calentamiento de IP actual.

   * No puede seleccionar una campaña que ya esté en uso en otra campaña de calentamiento de IP.

1. En el **[!UICONTROL Exclusión de perfil]** , puede ver que los perfiles de las ejecuciones anteriores de esa fase siempre se excluyen. Por ejemplo, si en #1 de ejecución se cubrió un perfil en las primeras 4800 personas objetivo, el sistema se asegurará automáticamente de que el mismo perfil no reciba el correo electrónico en #2 de ejecución.

1. Desde el **[!UICONTROL Audiencias de campaña excluidas]** , seleccione las audiencias de otros <!--executed/live?-->campañas que desee excluir de la fase actual.

   ![](assets/ip-warmup-plan-exclude-campaigns.png)

   Por ejemplo, al ejecutar la fase 1, tenía que [dividirlo](#split-phase) por cualquier razón. Por lo tanto, puede excluir la campaña utilizada en la fase 1, de modo que los perfiles contactados anteriormente desde la fase 1 no se incluyan en la fase 2. También puede excluir campañas de otros planes de calentamiento de IP.

1. Desde el **[!UICONTROL Dominios y grupos excluidos]** , seleccione los dominios que desea excluir de esa fase.

   ![](assets/ip-warmup-plan-exclude-domains.png)

   Por ejemplo, después de ejecutar el calentamiento de la IP durante algunos días, se da cuenta de que la reputación del ISP con un dominio (es decir, un Adobe) no es buena y desea resolverla sin detener su plan de calentamiento de la IP. En tal caso, puede excluir el grupo de dominios de Adobe.

   >[!NOTE]
   >
   >La exclusión de dominios requiere una fase no ejecutada, por lo que es posible que tenga que dividir una fase en ejecución para agregar exclusiones. Del mismo modo, si el grupo de dominios no es un grupo de dominios OOTB, debe agregar este grupo de dominios al archivo de Excel, cargarlo y luego excluir el dominio.

   ![](assets/ip-warmup-plan-phase-1.png)

1. Puede agregar una fase si es necesario. Se agregará después de la última fase actual.

1. Utilice el **[!UICONTROL Eliminar fase]** para eliminar cualquier fase no deseada.

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >No se puede deshacer la acción **[!UICONTROL Eliminar]** acción.
   >
   >Si elimina todas las fases del plan de calentamiento de IP, le recomendamos que vuelva a cargar un plan.

## Definición de las ejecuciones {#define-runs}

1. Seleccione una programación para cada ejecución. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. Seleccione un tiempo de finalización, que define la ventana dentro de la cual se puede ejecutar la campaña de calentamiento de IP en caso de que haya algún retraso en la ejecución del trabajo de segmentación de audiencia. Si no se especifica ninguna hora de finalización, la ejecución se intenta en el momento de inicio y fallará si la segmentación no se ha completado.

1. Activar cada ejecución. Asegúrese de programar con suficiente antelación para permitir que se ejecute el trabajo de segmentación. <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >Cada ejecución debe activarse al menos 12 horas antes de la hora de envío real. De lo contrario, es posible que la segmentación no se complete. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

   <!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. Si la ejecución de la campaña no se ha iniciado, puede detener una ejecución.<!--why?-->

   >[!NOTE]
   >
   >Una vez iniciada la ejecución de la campaña, **[!UICONTROL Detener]** El botón deja de estar disponible. <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. Para añadir una ejecución, seleccione **[!UICONTROL Agregar una ejecución a continuación]** desde el icono de tres puntos.

   ![](assets/ip-warmup-plan-run-more-actions.png)

## Dividir una fase {#split-phase}

En cualquier momento, si desea utilizar una campaña diferente que comience desde una ejecución específica, seleccione **[!UICONTROL Dividir en una nueva opción de fase]** desde el icono de tres puntos.

Se crea una nueva fase para las ejecuciones restantes de la fase actual. Siga los pasos [superior](#define-phases) para definir la nueva fase.

Por ejemplo, si selecciona esta opción para Ejecutar #4, las ejecuciones #4 a #8 se moverán a una nueva fase.

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

## Monitorización del plan

Una ejecución puede tener los siguientes estados<!--TBC with Medha-->:

* **[!UICONTROL Completado]**:
* **[!UICONTROL Fallido]**:
* **[!UICONTROL Cancelado]**: ha detenido la ejecución antes de que se iniciara la ejecución de la campaña.

Ventajas :

* Los informes seguirán mostrándose en el nivel de campaña con capacidades similares a las actuales. Sin embargo, el plan de calentamiento de la IP también sirve como un informe consolidado en un solo lugar de cuántas ejecuciones se realizaron, etc.

* Un solo lugar para administrar y ver el progreso del calentamiento de la IP.

* Informe consolidado en el nivel creativo/de campaña, ya que todas las ejecuciones de una fase