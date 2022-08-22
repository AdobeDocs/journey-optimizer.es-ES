---
title: Informe global de campaña
description: Aprenda a utilizar los datos del informe Campaign Global
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 11f7ce37dc1a99de4ed29fa7793f126e259f518d
workflow-type: tm+mt
source-wordcount: '1540'
ht-degree: 4%

---

# Informe global de campaña {#campaign-global-report}

Se puede acceder al informe global de campaña directamente desde la campaña con la variable **[!UICONTROL Global view]** botón.

La campaña **[!UICONTROL Global report]** se muestra con las siguientes pestañas:

* [Campaign](#campaign-global)
* [Correo electrónico](#email-global)
* [Push](#push-global)

La campaña **[!UICONTROL Global report]** se divide en distintas utilidades que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](../reports/global-report.md#modify-dashboard).

## Pestaña Campaña {#campaign-global}

### Entrega {#delivery-global}

![](assets/campaign_report_global_1.png)

La variable **[!UICONTROL Campaign's Statistics]** La utilidad detalla la información principal relativa a la campaña:

* **[!UICONTROL Entered profiles]**: Número de perfiles que iniciaron el recorrido.

* **[!UICONTROL Actions delivered]**: Número total de veces que se ha entregado una acción en el recorrido.

* **[!UICONTROL Actions failed in %]**: Número total de veces que una acción ha fallado en el recorrido en comparación con la cantidad total de veces que se ha entregado una acción.

### Objetivos {#objectives-global}

>[!AVAILABILITY]
>
>Actualmente, la función de experimento de contenido solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

![](assets/performance_report.gif)

La variable **[!UICONTROL Objectives]** del informe de Campaign le permite ajustar mejor los informes de las entregas mediante la segmentación de una métrica específica.

La variable **[!UICONTROL Objectives]** están vinculados a **[!UICONTROL Datasets]** que definen una conexión con un sistema para recuperar información adicional. Una lista de elementos integrados **[!UICONTROL Objectives]** está disponible, pero puede agregar el suyo propio añadiendo **[!UICONTROL Dataset]**. Para ver el procedimiento detallado, consulte esta [sección](reporting-configuration.md).

Después de seleccionar los objetivos sobre los que desea establecer el objetivo, los dos **[!UICONTROL Performance overview]** y **[!UICONTROL Campaign objective]** Las utilidades proporcionan un resumen detallado del rendimiento de su envío.

Con la variable **[!UICONTROL Campaign objective]** , también puede elegir comparar su objetivo principal con otra métrica.

Tenga en cuenta que cada utilidad se puede cambiar de tamaño y eliminar si es necesario. Para obtener más información, consulte [sección](../reports/global-report.md#modify-dashboard).

### Experimento {#experimentation-global}

>[!AVAILABILITY]
>
>Actualmente, la función de experimento de contenido solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

![](assets/experimentation_report_3.png)

Desde la campaña **[!UICONTROL Global report]**, el **[!UICONTROL Experimentation]** La pestaña detalla la información principal en relación con el rendimiento de cada variante y si hay un mejor rendimiento.

Tenga en cuenta que la definición del mejor ejecutante puede tardar algún tiempo, y que se representará con este icono ![](assets/experimentation_report_1.png).

La variable **[!UICONTROL Experiment result]** widget detalla el rendimiento de cada variante. Puede cambiar su línea base seleccionando uno de los tratamientos de la **[!UICONTROL Baseline]** la lista desplegable . El mejor tratamiento se representará con un icono de estrella.

La tabla presenta las siguientes métricas:

* **[!UICONTROL Profiles]**: Número de perfiles objetivo para este tratamiento.

* **[!UICONTROL Unique outbound clicks]**: Recuento total de clics en los canales salientes.

* **[!UICONTROL Count per profile]**: Valor total de la métrica de objetivo Experimento dividido por el número de perfiles.

* **[!UICONTROL Confidence interval]**: Diferencia porcentual en el rendimiento entre el valor basal y el tratamiento de mejor rendimiento. [Más información](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Average lift]**: Mejora porcentual en la tasa de conversión de un tratamiento determinado respecto al valor basal. [Más información](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confidence]**: Evidencia de que un tratamiento determinado es el mismo que el tratamiento basal. [Más información](../campaigns/experiment-calculations.md#understand-confidence)

Para profundizar en estos resultados y cómo interpretarlos, consulte [esta página](../campaigns/get-started-experiment.md#interpret-results).

## Ficha Correo electrónico {#email-global}

Desde la campaña **[!UICONTROL Global report]**, el **[!UICONTROL Email]** La pestaña detalla la información principal relativa a los envíos de correo electrónico realizados en la campaña.

La variable **[!UICONTROL Email Sending Statistics]** graph detalla el éxito de la entrega:

* **[!UICONTROL Targeted]**: Número total de mensajes procesados durante el análisis de entregas.

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Delivery Rate]**: Porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Bounce Rate]**: Porcentaje de correos electrónicos devueltos en comparación con los correos electrónicos enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Error Rate]**: Porcentaje de errores que se produjeron durante una entrega que impiden que se envíe en comparación con los correos electrónicos enviados.

* **[!UICONTROL Retries]**: Número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Excluded]**: Número de perfiles que Adobe Journey Optimizer ha excluido.

La variable **[!UICONTROL Email - Tracking statistics]** contiene los datos disponibles para la actividad de destinatario para su envío:

* **[!UICONTROL Opens]**: Número de veces que se abrió la entrega en una entrega.

* **[!UICONTROL Unique Opens]**: Porcentaje de envíos abiertos.

* **[!UICONTROL Open Rate]**: Número total de correos electrónicos abiertos comparados con el número de correos electrónicos enviados.

* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

* **[!UICONTROL Unique Clicks]**: número de destinatarios que hicieron clic en un contenido en un correo electrónico.

* **[!UICONTROL Unique Click Rate]**: Porcentaje de usuarios que interactuaron con la entrega.

* **[!UICONTROL Unsubscriptions]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Spam complaints]**: Número de veces que un mensaje se declaró como correo no deseado o no deseado.

La variable **[!UICONTROL Sending Statistics]** El gráfico contiene los datos disponibles para los correos electrónicos enviados, como:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Retries]**: Número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Bounce Reasons]** y **[!UICONTROL Bounce categories]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Hard bounce]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Soft bounce]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignored]**: El número total de mensajes temporales, como fuera de la oficina o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

Para obtener más información sobre las devoluciones, consulte la sección [Lista de supresión](../reports/suppression-list.md) página.

La variable **[!UICONTROL Error Reasons]** El gráfico y la tabla permiten ver qué error se produjo durante el envío.

La variable **[!UICONTROL Excluded reasons]** en el gráfico y la tabla se muestran las diferentes razones que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran el mensaje.

La variable **[!UICONTROL Email - Top Url]** gráfico y tabla detallan las direcciones URL de su envío que son las más visitadas.

La variable **[!UICONTROL Email - Top recipient domain]** gráfico y tabla detallan qué dominios son los más utilizados por los destinatarios para abrir el correo electrónico.

>[!NOTE]
>
>La variable **[!UICONTROL Optimized vs non optimized]** y **[!UICONTROL Send time optimization]**  las utilidades solo están disponibles si la opción de optimización del tiempo de envío está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../messages/send-time-optimization.md).

La variable **[!UICONTROL Optimized vs non optimized]** graph detalla la información principal relativa al mensaje, independientemente de si están optimizados o no:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.
* **[!UICONTROL Opens]**: Número de veces que se abrió la entrega en una entrega.
* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

La variable **[!UICONTROL Send time optimization]** detalla el éxito de la entrega en función del método de envío: optimizado o normal.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.
* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

## Ficha Insertar {#push-global}

Desde la campaña **[!UICONTROL Global report]**, el **[!UICONTROL Push]** detalla la información principal relativa a los envíos push realizados en la campaña.

La variable **[!UICONTROL Push notification - Sending statistics]** la tabla detalla la información principal relativa a las notificaciones push con gráficos y KPI:

* **[!UICONTROL Targeted]**: Número total de mensajes procesados durante el análisis de entregas.

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Delivery Rate]**: Porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Bounce Rate]**: Porcentaje de notificaciones push que rebotaron en comparación con las notificaciones push enviadas.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Error Rate]**: Porcentaje de errores que se produjeron durante una entrega que impiden que se envíe comparado con las notificaciones push enviadas.

* **[!UICONTROL Excluded]**: Número de perfiles que Adobe Journey Optimizer ha excluido.

La variable **[!UICONTROL Push - Tracking statistics]** contiene los datos disponibles para la actividad de destinatario para su envío:

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Open Rate]**: Porcentaje de notificaciones push abiertas.

* **[!UICONTROL Actions]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

* **[!UICONTROL Engagements]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

* **[!UICONTROL Engagement Rate]**: Porcentaje de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

La variable **[!UICONTROL Push notification summary]** El gráfico contiene los datos disponibles para las notificaciones push enviadas, como:

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Actions]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

>[!NOTE]
>
>La variable **[!UICONTROL Optimized vs non optimized]** y **[!UICONTROL Send time optimization]**  las utilidades solo están disponibles si la opción de optimización del tiempo de envío está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../messages/send-time-optimization.md).

La variable **[!UICONTROL Optimized vs non optimized]** graph detalla la información principal relativa al mensaje, independientemente de si están optimizados o no:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.
* **[!UICONTROL Opens]**: Número de veces que se abrió la entrega en una entrega.
* **[!UICONTROL Actions]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

La variable **[!UICONTROL Send time optimization]** detalla el éxito de la entrega en función del método de envío: optimizado o normal.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.
* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

La variable **[!UICONTROL Error Reasons]** El gráfico y la tabla permiten ver qué error se produjo durante el envío.

La variable **[!UICONTROL Excluded reasons]** en el gráfico y la tabla se muestran las diferentes razones que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran el mensaje.

La variable **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** y **[!UICONTROL Breakdown by platform]** gráficos y tablas detallan el éxito de la notificación push en función del sistema operativo del destinatario.

## Recursos adicionales

* [Introducción a las campañas](get-started-with-campaigns.md)
* [Creación de una campaña](create-campaign.md)
* [Creación de campañas activadas por API](api-triggered-campaigns.md)
* [Modificación o detención de una campaña](modify-stop-campaign.md)
* [Informe en directo de la campaña](campaign-live-report.md)
