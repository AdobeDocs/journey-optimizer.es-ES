---
solution: Journey Optimizer
product: journey optimizer
title: Ejecución del plan de calentamiento de IP
description: Obtenga información sobre cómo ejecutar y supervisar un plan de calentamiento de IP
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, grupo, subdominios, capacidad de entrega
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 752ffd7f-09c2-4aa3-a067-2dbe0634709c
source-git-commit: cd95614329e6efdc7ac4b6e0a5c683757a14b379
workflow-type: tm+mt
source-wordcount: '2558'
ht-degree: 11%

---

# Ejecución del plan de calentamiento de IP {#ip-warmup-running}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción a los planes de calentamiento de IP](ip-warmup-gs.md)
* [Creación de campañas de calentamiento de IP](ip-warmup-campaign.md)
* [Creación de un plan de calentamiento de IP](ip-warmup-plan.md)
* **[Ejecución del plan de calentamiento de IP](ip-warmup-execution.md)**

>[!ENDSHADEBOX]

Una vez que haya [creó un plan de calentamiento de IP](ip-warmup-plan.md) y cargó el archivo preparado con el consultor de capacidad de entrega, puede definir las fases y ejecuciones en el plan.

Cada fase está compuesta por varias ejecuciones, a las que se asigna una sola campaña.

## Definición de las fases {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Excluir públicos de campañas"
>abstract="Seleccione campañas para excluir sus públicos de la fase actual. Esto evita que los perfiles contactados anteriormente vuelvan a ser objetivos; solo se excluirá a los que hayan recibido comunicación a través del recorrido."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Excluir grupos de dominio"
>abstract="Seleccione los dominios que desea excluir de la fase actual. La exclusión de dominios requiere una fase no ejecutada, por lo que es posible que tenga que dividir una fase en ejecución para añadir exclusiones."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-execution.html?lang=es#split-phase" text="Dividir una fase"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_phases"
>title="Defina las fases de su plan"
>abstract="Cada fase está compuesta por varias ejecuciones, a las que se asigna una sola campaña."

<!--You need to associate the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan-->

<!--![](assets/ip-warmup-plan-phase-1.png)-->

1. Seleccione la campaña que desee asociar con la primera fase del plan de calentamiento de IP.

   >[!NOTE]
   >
   >No puede seleccionar una campaña que ya esté en uso en otro plan de calentamiento de IP. Sin embargo, la misma campaña se puede utilizar en una o más fases del mismo plan de calentamiento de IP.

   ![](assets/ip-warmup-plan-select-campaign.png)

   >[!IMPORTANT]
   >
   >* Solo las campañas con el **[!UICONTROL Activación del plan de calentamiento IP]** Las opciones activadas están disponibles para seleccionarlas. [Más información](#create-ip-warmup-campaign)
   >
   >* Solo se pueden seleccionar las campañas que utilicen la misma superficie que el plan de calentamiento de IP seleccionado.

1. Una vez seleccionada una campaña para la fase actual, se muestran las secciones para excluir perfiles, audiencias de campaña y grupos de dominios.

   >[!NOTE]
   >
   >Una vez activada una ejecución, las exclusiones ya no se pueden modificar a menos que [dividir la ejecución](#split-phase) a una nueva fase.

   1. Desde el **[!UICONTROL Grupos de dominio excluidos]** , seleccione los dominios que desea excluir de esa fase.

      >[!NOTE]
      >
      >La exclusión de dominios requiere una fase sin ejecutar, por lo que es posible que necesite [dividir una fase en ejecución](#split-phase) para añadir exclusiones.

      ![](assets/ip-warmup-plan-exclude-domains.png)

      Por ejemplo, después de ejecutar el calentamiento de la IP durante algunos días, se da cuenta de que la reputación de su ISP con un dominio (por ejemplo, Adobe) no es buena y desea resolverla sin detener su plan de calentamiento de IP. En tal caso, puede excluir el grupo de dominios de Adobe.

      >[!NOTE]
      >
      >Solo puede excluir un grupo de dominio personalizado que se haya agregado a [Plantilla de plan de calentamiento de IP](ip-warmup-plan.md#prepare-file). Si no es así, actualice la plantilla con el grupo de dominios personalizados que desee excluir y [volver a cargar el plan](#re-upload-plan).

   1. Desde el **[!UICONTROL Campaña para la exclusión de perfiles]** , seleccione las campañas cuyas audiencias desee excluir de la fase actual.

      ![](assets/ip-warmup-plan-exclude-campaigns.png)

      Por ejemplo, al ejecutar la fase 1, tenía que [dividirlo](#split-phase) por cualquier razón. Por lo tanto, puede excluir la campaña utilizada en la fase 1 para que los perfiles contactados anteriormente desde la fase 1 no se incluyan en la fase 2. También puede excluir campañas de otros planes de calentamiento de IP.

   1. Desde el **[!UICONTROL Recorridos para la exclusión de perfiles]** , seleccione los recorridos con las audiencias que desee excluir de la fase actual.

+++ Para utilizar la opción Recorridos para la exclusión de perfiles, debe establecer una relación entre los esquemas Evento de comentarios de mensajes de AJO y Registro de entidad de AJO.

      1. Crear un personalizado **Área de nombres** que servirá como tipo de identidad para los pasos siguientes.

      1. Acceda a Adobe Experience Platform desde el **Esquemas** , seleccione la opción **Esquema de registro de entidad AJO** y configure el **_id** como identidad principal y seleccione el área de nombres creado anteriormente como **Área de nombres de identidad**.

      1. Desde el **Esquemas** , seleccione la opción **Esquema de evento de comentarios de mensajes AJO** y vaya a la **_messageID** field. Seleccionar **Agregar relación** y elija **Esquema de registro de entidad AJO** como el **Esquema de referencia** y su área de nombres creada anteriormente como **Área de nombres de identidad**.
+++

   1. En el **[!UICONTROL Perfiles segmentados en ejecuciones anteriores]** , puede ver que los perfiles de las ejecuciones anteriores de esa fase siempre se excluyen. Por ejemplo, si en #1 de ejecución se cubrió un perfil en las primeras 4800 personas objetivo, el sistema se asegurará automáticamente de que el mismo perfil no reciba el correo electrónico en #2 de ejecución.

      >[!NOTE]
      >
      >Esta sección no se puede editar.

1. Si es necesario, puede reemplazar la campaña utilizando **[!UICONTROL Reemplazar]** botón. También puede **[!UICONTROL Borrar]** la campaña seleccionada utilizando el **[!UICONTROL Borrar]** botón. Esta acción no solo borrará la campaña, sino también otras propiedades de nivel de fase, como la Exclusión de grupos de dominios, la Campaña, la Exclusión de Recorridos, etc. Después de borrar, puede elegir una nueva campaña inmediatamente o más tarde.

   ![](assets/ip-warmup-plan-replace-campaign.png)

   >[!NOTE]
   >
   >Esta acción solo es posible antes de activar la primera ejecución de la fase. Una vez activada una ejecución, la campaña no se puede reemplazar, a menos que [dividir la ejecución](#split-phase) a una nueva fase.

1. Puede agregar una fase si es necesario. Se añadirá después de la última fase.

   ![](assets/ip-warmup-plan-add-phase.png)

1. Utilice el **[!UICONTROL Eliminar fase]** para eliminar cualquier fase no deseada. Esta acción solo está disponible si no se ejecuta en una fase. <!--Once a run is executed, deletion is not allowed.-->

   >[!CAUTION]
   >
   >No se puede deshacer la acción **[!UICONTROL Eliminar fase]** acción.

   ![](assets/ip-warmup-plan-delete-phase.png)

   >[!NOTE]
   >
   >Si elimina todas las fases del plan de calentamiento de IP, se recomienda volver a cargar un plan. [Más información](#re-upload-plan)

## Definición de las ejecuciones {#define-runs}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_run"
>title="Definir cada ejecución"
>abstract="Defina y active cada ejecución para todas las fases."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_last_engagement"
>title="Filtrar por participación"
>abstract="Esta columna es un filtro que se dirige únicamente a los usuarios comprometidos con su marca en los últimos 20 días, por ejemplo. También puede cambiar esta configuración a través de la opción **Editar ejecución**."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_retry"
>title="Establecer un periodo de tiempo"
>abstract="Puede definir un periodo de tiempo durante el cual se puede ejecutar la campaña de calentamiento de IP en caso de que haya algún retraso en el trabajo de segmentación."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_pause"
>title="Cancelar ejecuciones con errores de público"
>abstract="Seleccione esta opción para cancelar una ejecución si los perfiles cualificados son inferiores a los perfiles de destino una vez que el público haya sido evaluado para esa ejecución."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_qualified"
>title="Ver los perfiles cualificados"
>abstract="Esta columna muestra el número de perfiles cualificados. Una vez que el público ha sido evaluado para una ejecución, si hay más perfiles objetivo que perfiles cualificados, la ejecución se sigue ejecutando, a menos que la opción **Cancelar ejecuciones activadas en caso de errores** esté habilitada. En este caso, la ejecución se cancela."

1. Seleccione una programación para cada ejecución para asegurarse de que se ejecuta a la hora especificada.

   ![](assets/ip-warmup-plan-send-time.png)

1. De forma opcional, puede definir un período de tiempo durante el cual se puede ejecutar la campaña de calentamiento de IP en caso de que haya algún retraso en la [evaluación de audiencia](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"}. Para ello, haga clic en el icono Properties en la parte superior izquierda, junto al nombre del plan y utilice la variable **[!UICONTROL Reintentar tiempo de ejecución]** para seleccionar una duración: hasta 240 minutos (4 horas).

   >[!NOTE]
   >
   >Los reintentos se producen cada 30 minutos hasta el final de la ventana de tiempo definida.

   ![](assets/ip-warmup-plan-retry-run-time.png)

   Por ejemplo, si establece una hora de envío en un día determinado a las 9 a. m. y selecciona 120 minutos como tiempo de ejecución de reintento, esto permite que se realice una ventana de oportunidad de 2 horas (de 9 a. m. a 11 a. m.) para la ejecución de cualquier retraso inesperado en la evaluación de audiencia.

   >[!NOTE]
   >
   >Si no se especifica ningún periodo de tiempo, la ejecución se intenta en el momento del envío y falla si la evaluación de la audiencia no se completa.

1. Si es necesario, seleccione **[!UICONTROL Editar ejecución]** en el icono Más acciones. Se pueden actualizar los números de direcciones de cada columna. También puede actualizar el **[!UICONTROL Último compromiso]** para dirigirse únicamente a los usuarios comprometidos con su marca durante los últimos 20 días, por ejemplo.

   >[!NOTE]
   >
   >Se recomienda modificar estos números en consulta con su experto en capacidad de entrega.

   ![](assets/ip-warmup-plan-edit-run.png)

   >[!NOTE]
   >
   >Si no desea aplicar ningún periodo de participación a una ejecución, introduzca 0 en la **[!UICONTROL Último compromiso]** field.

1. Seleccione el **[!UICONTROL Cancelar las ejecuciones activadas en caso de errores]** para cancelar una ejecución si los perfiles cualificados son inferiores a los perfiles de destino una vez que la audiencia ha sido evaluada para esa ejecución. En ese caso, la ejecución toma la **[!UICONTROL Error]** estado.

   ![](assets/ip-warmup-plan-pause.png)

1. **[!UICONTROL Activar]** la corrida. [Más información](#activate-run)

1. El estado de esta ejecución cambia a **[!UICONTROL Activo]**, lo que significa que el sistema ha aceptado la solicitud para programar la ejecución.

   >[!NOTE]
   >
   >Los diferentes estados de ejecución se enumeran en [esta sección](#monitor-plan).

1. Si la ejecución de la campaña no ha comenzado, puede cancelar una ejecución activa. Esta acción cancela realmente la programación de ejecución, no detiene el envío.

   ![](assets/ip-warmup-plan-stop-run.png)

1. Para duplicar cualquier borrador, ejecución activa o completada, seleccione **[!UICONTROL Duplicar ejecución]**. Tras la duplicación, aparece el menú Editar ejecución, que permite a los usuarios ajustar la variable **[!UICONTROL Total de perfiles de destinatario]** y el **[!UICONTROL Hora de envío]** según sea necesario.

   ![](assets/ip-warmup-duplicate.png)

## Activar ejecuciones {#activate-run}

Para activar una ejecución, seleccione la **[!UICONTROL Activar]** botón. A continuación, puede activar las siguientes ejecuciones diariamente.

Al ejecutar varios planes de calentamiento de IP de forma simultánea, todos dirigidos al mismo grupo de IP y dominios, es crucial anticipar las posibles consecuencias. Por ejemplo, si un ISP aplica un límite diario de 100 correos electrónicos, la ejecución de varios planes dirigidos a los mismos dominios puede superar este umbral.

Asegúrese de que ha programado tiempo suficiente para permitir el [evaluación de audiencia](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"} para ejecutar.

![](assets/ip-warmup-plan-activate.png)

>[!CAUTION]
>
>Cada ejecución debe activarse al menos 12 horas antes de la hora de envío real. De lo contrario, es posible que la evaluación de audiencias no se complete.

Al activar una ejecución, se crean varias audiencias automáticamente.

* Si activa la primera ejecución de una fase:

   * Un [audiencia](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=es){target="_blank"} se crea para las audiencias de campaña excluidas (si las hay), con la siguiente convención de nombres: `<warmupName>-Phase<phaseNo>-Audience Exclusion `.

   * Se crea una audiencia para los grupos de dominios excluidos (si los hay), con la siguiente convención de nombres: `<warmupName>-Phase<phaseNo>-Domain Exclusion`.

   * Se crea otra audiencia para las audiencias de recorrido excluidas (si las hay), con la siguiente convención de nombres: `<warmupName>-Phase<phaseNo>-Journey Audience Exclusion`.

  >[!NOTE]
  >
  >Las audiencias se limpian después de que el plan de calentamiento se marque como completado.
  >
  >El sistema no crea una audiencia nueva en caso de que no haya cambios en las audiencias de campaña excluidas, las audiencias de recorrido excluidas o los grupos de dominio para las fases posteriores.

* Al activar cualquier ejecución:

   * Se crea otra audiencia para el último filtro de participación, con la siguiente convención de nombres: `<warmupName>-Phase<phaseNo>_Run<runNo>-Engagement Filter`.

     >[!NOTE]
     >
     >La audiencia se limpia después de que el plan de calentamiento se marque como completado.
     >
     >El sistema no crea una audiencia nueva en caso de que no haya cambios en el último filtro de participación para las fases siguientes.

   * Un [composición de audiencia](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=es){target="_blank"} se crea de forma correspondiente a la audiencia a la que se envía la campaña, con la siguiente convención de nombres: `<warmupName>-Phase<phaseNo>-Run<runNo>`.

     >[!NOTE]
     >
     >Se crea una nueva composición de audiencia para cada ejecución. Con un límite de 10, los usuarios que ejecuten varias campañas, recorridos y planes de calentamiento de IP simultáneamente mediante composiciones de audiencia publicadas deben planificar con anticipación para mantenerse dentro de este límite para operaciones paralelas.
     >
     >La composición de la audiencia (y, por lo tanto, la audiencia de salida) se limpia cuando se activa la siguiente iteración.

   * Se crea una audiencia de salida con la siguiente convención de nombres: `IP Warmup Audience-<warmupName>-Phase<phaseNo>-Run<runNo>`.

<!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

<!--Upon activation, when the segment evaluation happens, more segments will be created by the IP warmup service and will be leveraged in an audience composition and a new audience will be created for each run splitted into the different selected domains.-->

## Monitorización del plan {#monitor-plan}

Para ejecutar correctamente su plan de calentamiento de IP, debe monitorizar los informes, activar las ejecuciones y comprobar su estado diariamente.

### Utilice la sección Aspectos destacados {#highlights}

Una vez activada la primera ejecución para una fase, la variable **[!UICONTROL Características destacadas]** se muestra la sección.

Proporciona una visión general rápida de la ejecución actual y de la próxima ejecución. Desde esta sección también puede editar y activar la siguiente ejecución.

![](assets/ip-warmup-plan-highlights.png)

### Comprobación de los estados de ejecución {#run-statuses}

El propio plan de calentamiento de la IP sirve como informe consolidado en un solo lugar. Puede comprobar elementos como el número de **[!UICONTROL Activo]** o **[!UICONTROL Completado]** se ejecuta para cada fase y visualiza el progreso de su plan de calentamiento de IP.

>[!NOTE]
>
>Como práctica recomendada, se recomienda monitorizar diariamente su plan de calentamiento de IP.

Una ejecución puede tener los siguientes estados:

* **[!UICONTROL Borrador]** : cada vez que se crea una ejecución, ya sea cuando [creación de un nuevo plan](ip-warmup-plan.md) o [adición de una ejecución](#define-runs) desde la interfaz de usuario, toma el **[!UICONTROL Borrador]** estado.
* **[!UICONTROL Activo]**: cada vez que se activa una ejecución, se necesita el **[!UICONTROL Activo]** estado. Significa que el sistema ha aceptado la solicitud para programar la ejecución, no que se haya iniciado el envío. En esta fase puede observar el estado de la ejecución activa haciendo clic en el icono **[!UICONTROL Ver estado]** dentro de la tabla. Esto le permite hacer un seguimiento de cuántos perfiles de destino cumplen los requisitos.
* **[!UICONTROL Completado]**: la ejecución de la campaña para esta ejecución ha finalizado. Para acceder a un informe de ejecución detallado, haga clic en **[!UICONTROL Ver informe]** en la tabla. Esta opción permite rastrear el estado de envío de correo electrónico de la ejecución, incluidos los desgloses específicos de los grupos de dominios para una monitorización mejorada. Tenga en cuenta que la campaña asociada a él se establecerá como Detenida.[Más información](#reports)
* **[!UICONTROL Cancelado]**: a **[!UICONTROL Activo]** la ejecución se ha cancelado utilizando **[!UICONTROL Cancelar]** botón.[Más información](#define-runs)
* **[!UICONTROL Error]**: el sistema ha encontrado un error o la campaña utilizada para la fase actual se ha detenido, o ha habilitado el **[!UICONTROL Cancelar las ejecuciones activadas en caso de errores]** y se produjo un error. Si una ejecución falla, puede programar otra ejecución para el día siguiente.

### Uso de informes {#reports}

De forma más general, para medir el impacto de su plan, puede comprobar el rendimiento de sus campañas de calentamiento de IP mediante [!DNL Journey Optimizer] informes de campaña. Para ello, para cada ejecución completada, puede hacer clic en el icono **[!UICONTROL Ver informes]** botón. Obtenga más información sobre el correo electrónico de la campaña [informe en vivo](../reports/campaign-live-report.md#email-live) y [informe global](../reports/campaign-global-report.md#email-global).

![](assets/ip-warmup-plan-reports.png)

También puede acceder a los informes desde el [Menú Campañas](../campaigns/modify-stop-campaign.md#access) ya que su plan puede utilizar diferentes campañas.


## Administrar su plan {#manage-plan}

En cualquier momento, si el plan de calentamiento de la IP no funciona como se espera, puede realizar las siguientes acciones.

### Dividir una fase {#split-phase}

Si desea añadir una nueva fase empezando desde una ejecución específica, seleccione la **[!UICONTROL La división se ejecuta en una nueva fase]** del icono Más acciones.

![](assets/ip-warmup-plan-run-split-run.png)

Se crea una nueva fase para las ejecuciones restantes de la fase actual.

Por ejemplo, si selecciona esta opción para Ejecutar #4, las ejecuciones #4 a #8 se moverán a una nueva fase justo después de la fase actual.

Siga los pasos [superior](#define-phases) para definir la nueva fase.

* Puede usar el complemento **[!UICONTROL Reemplazar]** o **[!UICONTROL Borrar]** opciones para esa nueva fase.

* También puede excluir la campaña anterior o un dominio que no tenga un buen rendimiento. Descubra cómo en [esta sección](#define-phases).

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

### Volver a cargar un plan de calentamiento de IP {#re-upload-plan}

Si el plan de calentamiento de la IP no funciona como se espera (por ejemplo, si observa que algunos ISP marcan sus mensajes como correo no deseado), puede pedirle al experto en capacidad de entrega que configure otro archivo de plan de calentamiento de IP y vuelva a cargarlo con el botón correspondiente.

![](assets/ip-warmup-re-upload-plan.png)

Todas las ejecuciones ejecutadas anteriormente serán de solo lectura. El nuevo plan se muestra en el primer plan.

Siga los pasos [superior](#define-phases) para definir las fases del nuevo plan.

>[!NOTE]
>
>Los detalles del plan de calentamiento de IP cambiarán según el archivo recién cargado. Las ejecuciones ejecutadas anteriormente (independientemente de su [status](#monitor-plan)) no se ven afectados.

Veamos un ejemplo...

* Con el plan inicial de calentamiento de IP, la Fase 2 tuvo 9 ejecuciones.

* Se ejecutaron 4 ejecuciones (sin importar si fallaron, se completaron o se cancelaron)<!--as long as a run has been attempted, it is an executed run-->).

* Si vuelve a cargar un plan nuevo, la fase 2 con las primeras 4 ejecuciones ejecutadas pasará al modo de solo lectura.

* Las 5 ejecuciones restantes (que están en estado de borrador) se mueven a una nueva fase (Fase 3) que se muestra según el plan recién cargado.

### Marcar un plan como completado {#mark-as-completed}

Si sus IP se calentaron con el volumen deseado, o si su plan no está funcionando lo suficientemente bien o si desea soltarlo para crear otro, puede marcarlo como completado.

Para ello, haga clic en el **[!UICONTROL Más]** en la parte superior derecha del plan de calentamiento de IP y seleccione **[!UICONTROL Marcar como completado]**.

![](assets/ip-warmup-plan-mark-completed.png)

Esta opción sólo está disponible si todas las ejecuciones del plan se encuentran en **[!UICONTROL Completado]** o **[!UICONTROL Borrador]** estado. Si una ejecución es **[!UICONTROL Activo]**, la opción aparece atenuada.

Los diferentes estados de ejecución se enumeran en [esta sección](#monitor-plan).

