---
solution: Journey Optimizer
product: journey optimizer
title: Creación y programación de campañas organizadas con Journey Optimizer
description: Obtenga información sobre cómo crear y programar una campaña organizada con Adobe Journey Optimizer
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 66%

---


# Creación y programación de una campaña organizada {#create-first-campaign}

Cree una campaña orquestada en [!DNL Adobe Journey Optimizer] y configure su programación de ejecución para controlar cuándo se inicia y con qué frecuencia se ejecuta. Elija iniciar la campaña inmediatamente, en una fecha y a una hora específicas o de forma recurrente mediante opciones de programación flexibles como frecuencias diarias, semanales o mensuales.

## Crear la campaña {#create}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Lista de campañas orquestadas"
>abstract="La pestaña **Orquestación** enumera todas las campañas orquestadas. Haga clic en el nombre de una campaña orquestada para editarla. Utilice el botón **Crear campaña orquestada** para añadir una nueva campaña orquestada."

Para crear una campaña orquestada, siga estos pasos:

1. Vaya al menú **[!UICONTROL Campañas]** y seleccione la pestaña **[!UICONTROL Orquestación]**.

1. Haga clic en el botón **[!UICONTROL Crear campaña]** y seleccione el tipo de campaña **[!UICONTROL Orquestación - Marketing]**.

   ![](assets/create-modal.png)

1. Defina las propiedades de la campaña. Para ello, haga clic en el ![icono de configuración de la campaña](assets/do-not-localize/campaign-settings.svg) junto al nombre de la campaña.

   ![](assets/inventory-create.png)

   1. Escriba un **[!UICONTROL Nombre]** y **[!UICONTROL Descripción]** para la campaña.

   1. Seleccione una **[!UICONTROL política de combinación]** para su campaña.

      En [!DNL Adobe Experience Platform], cada audiencia está ligada a una política de combinación específica, que define cómo se combina la información del perfil para formar un perfil combinado. Al seleccionar una política de combinación en la actividad Leer audiencia, solo están disponibles las audiencias basadas en la misma política de combinación. De forma predeterminada, el sistema utiliza la política de combinación predeterminada, pero puede cambiarla si es necesario. Para obtener más información sobre las políticas de combinación, consulte la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.

   1. Utilice el campo **[!UICONTROL Etiquetas]** para asignar etiquetas unificadas de Adobe Experience Platform a su campaña. Esto le permite clasificarlas fácilmente y mejorar la búsqueda desde la lista Campañas orquestadas. [Descubra cómo trabajar con etiquetas](../start/search-filter-categorize.md#tags).

   1. Haga clic en **[!UICONTROL Guardar]**.

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
* Si desea enviar un mensaje recurrente en la campaña orquestada, debe utilizar una opción **Scheduling** y establecer la frecuencia de ejecución. La actividad de envío recurrente no le permite definir una programación.

Para configurar la programación de la campaña, siga estos pasos:

1. Abra la campaña y haga clic en el botón **[!UICONTROL Lo antes posible]**.

   ![](assets/create-schedule.png)

1. Seleccione una frecuencia de ejecución para la campaña y configure las opciones disponibles. La configuración varía en función de la frecuencia seleccionada:

   +++Una vez

   Ejecute la campaña una sola vez en una fecha y a una hora especificadas.

   * **[!UICONTROL Fecha]**: seleccione la fecha en la que se debe ejecutar la campaña.
   * **[!UICONTROL Hora]**: seleccione la hora específica a la que se debe ejecutar la campaña.

   +++

   +++Cada día

   Ejecute la campaña todos los días o en los días seleccionados.

   * **[!UICONTROL Periodicidad diaria]**: elija la frecuencia con la que debe ejecutarse la campaña:
      * **[!UICONTROL Todos los días]**: ejecuta la campaña todos los días de la semana, incluidos los fines de semana.
      * **[!UICONTROL Días laborables]**: ejecuta la campaña solamente de lunes a viernes.
      * **[!UICONTROL Durante un período específico]**: ejecuta la campaña diariamente dentro de un intervalo de fechas definido (por ejemplo, del 1 al 15 de julio). La campaña no se ejecutará fuera de este intervalo.
      * **[!UICONTROL En días seleccionados de la semana]**: ejecuta la campaña solamente durante los días especificados de la semana (por ejemplo, lunes, miércoles, viernes).

   * **[!UICONTROL Hora de inicio]**: defina la hora a la que la campaña debe ejecutarse cada día.

   +++

   +++Varias veces al día

   Ejecute la campaña varias veces en el mismo día. Puede elegir horas específicas o establecer una frecuencia periódica.

   * **[!UICONTROL Horas seleccionadas]**: seleccione las horas específicas en que se debe ejecutar la campaña y configure su periodicidad diaria (se ejecutará todos los días de la semana o en determinados días).
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
      * **[!UICONTROL Todos los días]**: ejecuta la campaña todos los días naturales del mes, incluidos los fines de semana.
      * **[!UICONTROL Último día del mes]**: ejecuta la campaña solamente el último día natural de cada mes (por ejemplo, el 31 de enero, 28/29 de febrero).
      * **[!UICONTROL Día específico del mes (por ejemplo, el 15)]**: ejecuta la campaña un día especificado (por ejemplo, el 15 de cada mes).
      * **[!UICONTROL Primer/último o enésimo día de la semana]** (por ejemplo, primer lunes): ejecuta la campaña un día de la semana especificado (por ejemplo, el 15 de cada semana).
      * **[!UICONTROL Días seleccionados de la semana]**: ejecuta la campaña un día especificado.

   * **[!UICONTROL Hora de inicio]**: establezca la hora a la que se debe ejecutar la campaña.

   +++

1. Use la configuración **[!UICONTROL Período de validez]** para definir una fecha específica de inicio y finalización que limite la ejecución de la campaña a un período de tiempo limitado.

1. Para las programaciones recurrentes, haga clic en el botón **[!UICONTROL Previsualizar horas de inicio]** para obtener una vista previa de las próximas fechas y horas de ejecución exactas según la configuración actual. Esto valida la programación antes de la activación y garantiza que la campaña se ejecute según lo esperado.

>[!NOTE]
>
>Al programar campañas en [!DNL Adobe Journey Optimizer], asegúrese de que la fecha y la hora de inicio se ajusten al primer envío deseado. En el caso de las campañas recurrentes, si ya ha pasado la hora programada inicial, las campañas se transferirán a la siguiente franja horaria disponible según sus reglas de periodicidad.

En el siguiente ejemplo, la actividad está configurada para que la campaña orquestada se ejecute dos veces al día a las 9 y las 12 de la mañana, todos los días de la semana del 1 de octubre de 2025 al 1 de enero de 2026.

![Planificador configurado para ejecutar la campaña dos veces al día a las 09:00 y a las 12:00](assets/scheduler-sample.png){width="50%" align="left"}

## Próximos pasos {#next}

Una vez configurados los ajustes y la programación de la campaña, puede empezar a organizar las diferentes tareas que va a realizar. [Obtenga información sobre cómo organizar actividades de campaña](../orchestrated/orchestrate-activities.md)
