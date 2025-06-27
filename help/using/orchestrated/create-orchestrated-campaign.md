---
solution: Journey Optimizer
product: journey optimizer
title: Cree y programe campañas orquestadas con Journey Optimizer
description: Obtenga información sobre cómo crear y programar una campaña orquestada con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 3eeb84e57af655bef669be8e9fc9ae7a024b1ab0
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 8%

---


# Creación y programación de una campaña organizada {#create-first-campaign}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/><b>[Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)</b><br/><br/>[Orqueste actividades](orchestrate-activities.md)<br/><br/>[Envíe mensajes con campañas orquestadas](send-messages.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [División](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Cree una campaña orquestada en [!DNL Adobe Journey Optimizer] y configure su programación de ejecución para controlar cuándo se inicia y con qué frecuencia se ejecuta. Elija iniciar la campaña inmediatamente, en una fecha y hora específicas o de forma recurrente mediante opciones de programación flexibles como frecuencias diarias, semanales o mensuales.

## Creación de la campaña {#create}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Lista de campañas de orquestadas"
>abstract="La pestaña **Orchestration** enumera todas las campañas orquestadas. Haga clic en el nombre de una campaña orquestada para editarla. Utilice el botón **Crear campaña orquestada** para añadir una nueva campaña orquestada."

Para crear una campaña orquestada, siga estos pasos:

1. Vaya al menú **[!UICONTROL Campañas]**, seleccione la pestaña **[!UICONTROL Orquestación]** y haga clic en **[!UICONTROL Crear campaña]**.

   ![](assets/inventory-create.png)

1. Introduzca un nombre y una descripción para la campaña.

1. *(opcional)* Utilice el campo **[!UICONTROL Etiquetas]** para asignar etiquetas unificadas de Adobe Experience Platform a su campaña. Esto le permite clasificarlas fácilmente y mejorar la búsqueda desde la lista de campañas orquestadas. [Aprenda a trabajar con etiquetas](../start/search-filter-categorize.md#tags).

1. Haga clic en **[!UICONTROL Crear]**.

La campaña orquestada se creará y aparecerá en la lista de campañas orquestadas. Puede actualizar estas propiedades en cualquier momento si hace clic en el icono ![Configuración de campaña](assets/do-not-localize/campaign-settings.svg) en el lienzo de la campaña.

## Programación de la campaña {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Planificador"
>abstract="Como administrador de campañas, puede programar campañas para que se inicien automáticamente en momentos específicos, lo que permite un tiempo preciso y datos de segmentación precisos para las comunicaciones de marketing."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="Validez del planificador"
>abstract="Puede definir un período de validez para el planificador. Puede ser permanente (predeterminado) o válido hasta una fecha específica."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="Opciones del planificador"
>abstract="Defina la frecuencia del planificador. Se puede ejecutar en un momento específico, una o varias veces al día, a la semana o al mes."

De forma predeterminada, las campañas orquestadas se inician cuando se activan manualmente y finalizan una vez ejecutadas sus actividades asociadas. Si prefiere retrasar la ejecución o ejecutar la campaña de forma recurrente, puede definir una programación para la campaña.

Tenga en cuenta las siguientes prácticas recomendadas al programar campañas orquestadas para garantizar un rendimiento óptimo y el comportamiento esperado:

* No programe una campaña orquestada para que se ejecute durante más de 15 minutos, ya que podría limitar el rendimiento general del sistema y crear bloques en la base de datos.
* Si desea enviar un mensaje de una sola vez en la campaña orquestada, puede configurarlo para que se ejecute **Una vez**.
* Si desea enviar un mensaje recurrente en la campaña orquestada, debe utilizar una opción **Scheduling** y establecer la frecuencia de ejecución. La actividad de entrega recurrente no permite definir una programación.

Para configurar la programación de campaña, siga estos pasos:

1. Abra la campaña y haga clic en el botón **[!UICONTROL Lo antes posible]**.

   ![](assets/create-schedule.png)

1. Seleccione una frecuencia de ejecución para la campaña y configure las opciones disponibles. La configuración varía en función de la frecuencia seleccionada:

   +++Una vez

   Ejecute la campaña una sola vez en una fecha y hora especificadas.

   * **[!UICONTROL Fecha]**: seleccione la fecha en la que se debe ejecutar la campaña.
   * **[!UICONTROL Hora]**: seleccione la hora específica en que se debe ejecutar la campaña.

   +++

   +++Diario

   Ejecute la campaña todos los días o en los días seleccionados.

   * **[!UICONTROL Periodicidad diaria]**: elija la frecuencia con la que debe ejecutarse la campaña:
      * **[!UICONTROL Todos los días]**: ejecuta la campaña todos los días de la semana, incluidos los fines de semana.
      * **[!UICONTROL De lunes a viernes]**: ejecuta la campaña solamente de lunes a viernes.
      * **[!UICONTROL A través de un período específico]**: ejecuta la campaña diariamente dentro de un intervalo de fechas definido (por ejemplo, del 1 al 15 de julio). La campaña no se ejecutará fuera de este intervalo.
      * **[!UICONTROL En días seleccionados de la semana]**: ejecuta la campaña solamente en los días especificados de la semana (por ejemplo, lunes, miércoles o viernes).

   * **[!UICONTROL Hora de inicio]**: defina la hora a la que la campaña debe ejecutarse cada día.

   +++

   +++Varias veces al día

   Ejecute la campaña varias veces en el mismo día. Puede elegir tiempos específicos o establecer una frecuencia periódica.

   * **[!UICONTROL Horas seleccionadas]**: seleccione las horas específicas en que la campaña debe ejecutarse y configure su periodicidad diaria (se ejecutará todos los días de la semana o en determinados días).
   * **[!UICONTROL Periódico]**: elija ejecutar la campaña cada n minutos u horas. También puede definir el intervalo de tiempo dentro del día en que se permiten las ejecuciones.

   +++

   +++Semanal

   Ejecute la campaña semanalmente, con opciones para días específicos.

   * **[!UICONTROL Frecuencia]**: elija la frecuencia con la que se debe ejecutar la campaña (por ejemplo, cada semana, cada 2 semanas).
   * **[!UICONTROL A partir de la fecha]**: seleccione la fecha en la que debe comenzar la periodicidad.
   * **[!UICONTROL Periodicidad diaria]**: elija días específicos de la semana para la ejecución (por ejemplo, todos los lunes y jueves).
   * **[!UICONTROL Hora de inicio]**: establezca la hora a la que la campaña debe ejecutarse en los días seleccionados.

   +++

   +++Mensual

   Ejecute la campaña mensualmente, con opciones para días específicos.

   * **[!UICONTROL Periodicidad mensual]**: seleccione si la campaña se ejecuta todos los meses o solo durante meses específicos.
   * **[!UICONTROL Periodicidad diaria]**:
      * **[!UICONTROL Todos los días]**: ejecuta la campaña en todos los días del mes, incluidos los fines de semana.
      * **[!UICONTROL Último día del mes]**: ejecuta la campaña solamente en el último día del calendario de cada mes (por ejemplo, el 31 de enero, 28/29 de febrero).
      * **[!UICONTROL Día específico del mes (por ejemplo, el 15)]**: ejecuta la campaña en un día especificado (por ejemplo, el 15 de cada mes).
      * **[!UICONTROL Primer/último o noveno día de la semana]** (por ejemplo, primer lunes):      Ejecuta la campaña en un día de la semana especificado (por ejemplo, el 15 de cada semana).
      * **[!UICONTROL Días seleccionados de la semana]**: ejecuta la campaña en un día especificado.

   * **[!UICONTROL Hora de inicio]**: establezca la hora a la que se debe ejecutar la campaña.

   +++

1. Use la configuración **[!UICONTROL Periodo de validez]** para definir una fecha específica de inicio y finalización que limite la ejecución de la campaña a un periodo de tiempo limitado.

1. Para las programaciones recurrentes, haga clic en el botón **[!UICONTROL Previsualizar horas de inicio]** para obtener una vista previa de las próximas fechas y horas de ejecución exactas según la configuración actual. Esto ayuda a validar la programación antes de la activación y garantiza que la campaña se ejecute según lo esperado.

>[!NOTE]
>
>Al programar campañas en [!DNL Adobe Journey Optimizer], asegúrese de que la fecha y la hora de inicio se ajusten a la primera entrega deseada. En el caso de las campañas recurrentes, si ya ha pasado la hora programada inicial, las campañas se transferirán a la siguiente franja horaria disponible según sus reglas de periodicidad.

En el siguiente ejemplo, la actividad se configura de modo que la campaña orquestada se ejecute dos veces al día a las 9 y las 12 de la mañana, todos los días de la semana del 1 de octubre de 2025 al 1 de enero de 2026.

![Programador configurado para ejecutar la campaña dos veces al día a las 09:00 y a las 12:00](assets/scheduler-sample.png){width="50%" align="left"}

## Pasos siguientes {#next}

Una vez configurados los ajustes y la programación de la campaña, puede empezar a organizar las diferentes tareas que va a realizar. [Aprenda a organizar actividades de campañas](../orchestrated/orchestrate-activities.md)
