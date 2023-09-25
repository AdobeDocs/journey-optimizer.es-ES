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
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '1014'
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

Una vez que haya [creó un plan de calentamiento de IP](ip-warmup-plan.md) y cargó el archivo preparado con el consultor de capacidad de entrega, puede definir las fases y ejecuciones en el plan.

Cada fase corresponde a un periodo compuesto por varias ejecuciones, a las que se asigna una sola campaña.

Para cada ejecución, tiene un número determinado de destinatarios y programa cuándo se ejecutará esta ejecución.

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

1. De forma opcional, seleccione la ventana en la que se puede ejecutar la campaña de calentamiento de IP en caso de que haya algún retraso en la ejecución del trabajo de segmentación de audiencia. Si no se especifica ninguna hora de finalización, la ejecución se intenta en el momento de inicio y fallará si la segmentación no se ha completado.

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

## Marcar un plan como completado {#mark-as-completed}

Si el plan no está funcionando lo suficientemente bien o si desea soltarlo para crear otro, puede marcarlo como completado.

Para ello, haga clic en el **[!UICONTROL Más]** en la parte superior derecha del plan de calentamiento de IP y seleccione **[!UICONTROL Marcar como completado]**.

![](assets/ip-warmup-plan-mark-completed.png)

Esta opción sólo está disponible si todas las ejecuciones del plan se encuentran en **[!UICONTROL Correcto]** o **[!UICONTROL Borrador]** estado. No se puede ejecutar **[!UICONTROL Activo]**.

Los diferentes estados de ejecución se enumeran en [esta sección](#monitor-plan).

## Monitorización del plan {#monitor-plan}

Para medir el impacto de su plan, puede comprobar el rendimiento de sus campañas de calentamiento de IP mediante informes. Obtenga más información sobre el correo electrónico de la campaña [informe en vivo](../reports/campaign-live-report.md#email-live) y [informe global](../reports/campaign-global-report.md##email-global).

El propio plan de calentamiento de la IP también sirve como informe consolidado en un solo lugar. Puede comprobar elementos como el número de **[!UICONTROL Activo]** o **[!UICONTROL Correcto]** se ejecuta para cada fase y visualiza el progreso de su plan de calentamiento de IP.

Una ejecución puede tener los siguientes estados:

* **[!UICONTROL Borrador]** : cada vez que se crea una ejecución, ya sea cuando [carga de un plan nuevo](ip-warmup-plan.md) o [adición de una ejecución](#define-runs) desde la interfaz de usuario, toma el **[!UICONTROL Borrador]** estado.
* **[!UICONTROL Activo]**: cada vez que se activa una ejecución, se necesita el **[!UICONTROL Activo]** estado.
* **[!UICONTROL Correcto]**<!--TBC-->: la ejecución de la campaña para esta ejecución ha finalizado. <!--i.e. campaign execution has started, no error happened and emails have reached users? to check with Sid-->
* **[!UICONTROL Cancelado]**: a **[!UICONTROL Activo]** la ejecución se ha cancelado utilizando **[!UICONTROL Detener]** botón. Este botón solo está disponible si la ejecución de la campaña no se ha iniciado. [Más información](#define-runs)
* **[!UICONTROL Error]**: el sistema ha encontrado un error o la campaña utilizada para la fase actual se ha detenido<!--what should the user do in that case?-->.
