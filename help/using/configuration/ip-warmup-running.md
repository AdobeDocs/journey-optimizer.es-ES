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
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '809'
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

1. Para cada fase, se aplica lo siguiente:

   * **[!UICONTROL Exclusión de perfil]** - Los perfiles de las ejecuciones anteriores de esa fase siempre se excluyen. Por ejemplo, si en una carrera #1 Leo se cubrió con las primeras 6300 personas objetivo, el sistema se asegurará automáticamente de que Leo no reciba el correo en la #2 de ejecución.

   * **[!UICONTROL Audiencias de campaña excluidas]** - Seleccionar las audiencias de otros <!--executed/live?-->campañas que desee excluir de la fase actual.

     Por ejemplo, es posible que esté ejecutando una fase y tenga que dividirla por cualquier motivo. En tal caso, en la fase 2, le gustaría incluir la campaña utilizada en la fase 1 en esta sección para que en la fase 2, las personas contactadas anteriormente desde la fase 1 no estén incluidas. Esto se puede hacer no solo con las campañas utilizadas en el mismo plan de calentamiento de IP, sino también desde otro plan de calentamiento de IP.

   * **[!UICONTROL Dominios y grupos excluidos]** : seleccione los dominios que desee excluir de esa fase, por ejemplo, Gmail. <!--??-->

     Después de ejecutar el calentamiento de IP durante algunos días, se da cuenta de que la reputación del ISP con un dominio dice que hotmail no es bueno y desea resolverlo con el ISP, pero no desea detener el plan de calentamiento de IP. En tal caso, puede colocar el grupo de dominios hotmail en la categoría excluida.

     >[!NOTE]
     >
     >La exclusión de dominios requiere una fase no ejecutada, por lo que es posible que tenga que dividir una fase en ejecución para agregar exclusiones. Del mismo modo, si el grupo de dominio no es un grupo de dominio OOTB, es posible que tenga que crear un grupo de dominio en Excel, cargarlo y luego excluirlo.

   ![](assets/ip-warmup-plan-phase-1.png)

1. Puede agregar una fase si es necesario: se agregará después de la última fase actual. Utilice el **[!UICONTROL Eliminar fase]** para eliminar cualquier fase no deseada.

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >No se puede deshacer la acción **[!UICONTROL Eliminar]** acción.
   >
   >Si elimina todas las fases del plan de calentamiento de IP, le recomendamos que vuelva a cargar un plan.

## Definición de las ejecuciones {#define-runs}

1. Seleccione una programación para cada ejecución. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. Seleccione una hora de finalización, que básicamente significa la ventana en la que podemos ejecutar la campaña de calentamiento en caso de que haya algún retraso en el trabajo de audiencia. Si no se especifica, se intentará en el momento de inicio y se producirá un error. Si se proporciona la hora de finalización, ejecutaremos la ejecución entre esa ventana.

1. Activar cada ejecución. Asegúrese de programar con suficiente antelación para permitir que se ejecute el trabajo de segmentación. <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >Cada ejecución debe activarse al menos 12 horas antes de la hora de envío real. De lo contrario, es posible que la segmentación no se complete. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. Si la ejecución de la campaña no se ha iniciado, puede detener una ejecución.<!--why?-->

   Una vez iniciada la ejecución de la campaña, **[!UICONTROL Detener]** El botón deja de estar disponible. <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. Para añadir una ejecución, seleccione **[!UICONTROL Agregar una ejecución a continuación]** desde el icono de tres puntos.

   ![](assets/ip-warmup-plan-run-more-actions.png)

1. En cualquier momento, si desea utilizar una campaña diferente que comience desde una ejecución específica, seleccione **[!UICONTROL Dividir en una nueva opción de fase]** desde el icono de tres puntos. Se crea una nueva fase para las ejecuciones restantes de la fase actual. Siga los pasos [superior](#define-phases) para definir la nueva fase.

   Por ejemplo, si selecciona esta opción para ejecutar #4, las ejecuciones #4 a #8 se moverán a una nueva fase.

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