---
solution: Journey Optimizer
product: journey optimizer
title: Informe global de la campaña
description: Aprenda a utilizar los datos del informe global de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 94d6ebe6e0ad5fa48eaad9d8cfa8cff584f2b819
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Informe global de la campaña {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Informe global de la campaña"
>abstract="El informe global de campaña permite medir el impacto de las campañas durante un período de tiempo seleccionado. El informe se divide en distintos widgets que detallan el éxito y los errores de la campaña. Cada tablero de informes se puede modificar cambiando el tamaño de los widgets o eliminándolos."

>[!AVAILABILITY]
>
>La experiencia actual de creación de informes se eliminará a partir de enero de 2025. Después de esta fecha, la nueva experiencia de creación de informes pasará a ser el estándar. Recomendamos que se familiarice con las nuevas funciones y características para garantizar una transición sin problemas. [Introducción a la nueva interfaz de informes de Journey Optimizer.](report-gs-cja.md)

Los informes globales, a los que se puede acceder desde la ficha **Todo el tiempo**, muestran los eventos que se produjeron hace al menos dos horas y cubren los eventos que se produjeron durante un período de tiempo seleccionado. En comparación, los informes en directo se centran en los eventos que han tenido lugar en las últimas 24 horas, con un intervalo de tiempo mínimo de dos minutos desde que se produjo el evento.

Se puede acceder directamente al informe global de Campaign desde la campaña con el botón **[!UICONTROL Ver informe]**.

![](assets/campaign_report_global_5.png)

La página de la campaña **[!UICONTROL Informe global]** se mostrará con las siguientes fichas:

* [Campaign](#campaign-global)
* [Correo electrónico](#email-global)
* [En la aplicación](#inapp-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [Web](#web-tab)
* [Correo directo](#direct-mail-global)

El **[!UICONTROL informe global]** de la campaña está dividido en diferentes widgets que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte esta [sección](../reports/global-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global.md)

## Pestaña Campaña {#campaign-global}

### Envío {#delivery-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_delivery_global"
>title="Estadísticas de Campaign"
>abstract="El widget de estadísticas de Campaign detalla la información principal relativa a la campaña, como los perfiles introducidos y las acciones enviadas."

![](assets/campaign_report_global_1.png)

Los KPI **[!UICONTROL Estadísticas de campaña]** sirven como un panel completo, que ofrece un desglose detallado de las métricas clave relacionadas con su campaña. Esto incluye información esencial, como la cantidad de perfiles y las acciones entregadas, lo que proporciona una comprensión exhaustiva del rendimiento y la participación de su campaña.

+++ Obtenga más información sobre las métricas de estadísticas de Campaign

* **[!UICONTROL Audiencia]**: Número de perfiles de destino.

* **[!UICONTROL Acciones entregadas]**: Número total de veces únicas que se entregó una acción.

* **[!UICONTROL Acciones con errores en %]**: porcentaje de veces únicas que una acción ha fallado comparado con el número total de veces únicas que se ha entregado una acción.

+++

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../content-management/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.


### Experimentation report {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Success metric"
>abstract="The total value of the Success metric, previously selected when creating your Experiments, divided by the number of profiles."

![](assets/experimentation_report_3.png)

The **[!UICONTROL Experimentation]** tab provides key insights into the performance of each variant, and identifies the most successful one.

Note that defining the best performer might take some time, it will be represented by this icon ![](assets/experimentation_report_1.png).

+++Learn more on the different metrics and widgets available for the Experimentation report.

The **[!UICONTROL Experiment result]** widget details the performance of each variant. You can change your baseline by selecting one of the treatment from the **[!UICONTROL Baseline]** the drop-down. The best treatment will be represented with a star icon.

For a deep-dive in these results and how to interpret them, refer to [this page](../content-management/get-started-experiment.md#interpret-results).

The table presents the following metrics:

* **[!UICONTROL Lift over baseline]**: Measure of the percentage improvement in conversion rate of a given treatment over the baseline.

* **[!UICONTROL Confidence]**: Evidence that a given treatment is the same as the baseline treatment. [Learn more](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Unique outbound clicks]**: Total count of clicks across outbound channels.

* **[!UICONTROL Profiles]**: Number of profiles targeted for this treatment.

* **[!UICONTROL Unique outbound clicks/profiles]**: Total value of the Success metric, previously selected when creating your Experiments, divided by the number of profiles.

The **[!UICONTROL Confidence interval]** graph measures uncertainty around improvement. It details the percentage difference in performance between the baseline and the best performing treatment. [Learn more](../content-management/experiment-calculations.md#confidence-intervals). 

![](assets/experimentation_report_4.png)

The last widget provides data related to the **[!UICONTROL Success metric]** you previously selected for your Treatments. You have the option to select a different targeted metric from the **[!UICONTROL Metric]** drop-down menu to track alternative data.
    
>[!CAUTION]
>
>When working with experimentation filtered metrics, please note that changing the Metric selection from the drop-down on the comparison page for experimentation will not retain the filter value. For example, switching from "Clicks" to "Unique clicks" will lead to the loss of the applied filter, rendering the comparison inaccurate or invalid.

+++
-->

## Pestaña de correo electrónico {#email-global}

### Correo electrónico: estadísticas de envío {#sending-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_statistics"
>title="Correo electrónico: Estadísticas de envío"
>abstract="La tabla Correo electrónico: Estadísticas de envío resume los datos esenciales sobre sus correos electrónicos, como los segmentados o enviados."

![](assets/campaign_email_sending.png)

La tabla **[!UICONTROL Estadísticas de envío de correo electrónico]** proporciona un resumen completo de los datos esenciales relacionados con sus campañas de correo electrónico. Detalla métricas clave como el tamaño de la audiencia objetivo y la cantidad de correos electrónicos enviados correctamente, lo que ofrece perspectivas valiosas sobre la eficacia y el alcance de los correos electrónicos.

+++ Más información sobre las métricas de estadísticas de envío de correo electrónico

* **[!UICONTROL Destinatarios]**: Número total de correos electrónicos procesados durante el proceso de envío.

* **[!UICONTROL Enviado]**: Número total de envíos del correo electrónico.

* **[!UICONTROL Entregado]**: número de correos electrónicos enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de entrega]**: Porcentaje de correos electrónicos enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de salida hacia otro sitio]**: Porcentaje de correos electrónicos que se rebotaron en comparación con los enviados.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío para evitar que se enviara a los perfiles.

* **[!UICONTROL Tasa de errores]**: Porcentaje de errores que se produjeron durante el proceso de envío que impiden su envío en comparación con los correos electrónicos enviados.

* **[!UICONTROL Reintentos]**: número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Excluido]**: número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

### Correo electrónico: Estadísticas de seguimiento {#tracking-statistics-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_tracking_statistics"
>title="Correo electrónico: Estadísticas de seguimiento"
>abstract="La tabla Correo electrónico: Estadísticas de seguimiento proporciona datos sobre la actividad del perfil del Correo electrónico."

![](assets/campaign_email_tracking.png)

La tabla **[!UICONTROL Correo electrónico: estadísticas de seguimiento]** ofrece una cuenta detallada de la actividad de perfil relacionada con sus campañas de correo electrónico. Esto incluye métricas sobre aperturas, clics y otros indicadores de participación relevantes, lo que ofrece una vista completa de cómo los perfiles interactúan con el contenido del correo electrónico.

+++ Más información sobre el Correo electrónico: métricas de estadísticas de seguimiento

* **[!UICONTROL Aperturas]**: Número de veces que se abrió el correo electrónico.

* **[!UICONTROL Aperturas únicas]**: Porcentaje de correos electrónicos abiertos.

* **[!UICONTROL Tasa de apertura]**: Cantidad total de correos electrónicos abiertos en comparación con la cantidad de correos electrónicos enviados.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en sus correos electrónicos.

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de un correo electrónico.

* **[!UICONTROL tasa de clics únicos]**: porcentaje de usuarios que interactuaron con sus correos electrónicos.

* **[!UICONTROL Cancelaciones de suscripciones]**: número de clics en el vínculo de cancelación de suscripción.

* **[!UICONTROL Quejas por correo no deseado]**: Número de veces que un mensaje se declaró como correo no deseado.

+++

### Correo electrónico: rendimiento del envío {#sending-performance-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_performance"
>title="Correo electrónico: rendimiento del envío"
>abstract="El gráfico Correo electrónico: rendimiento del envío presenta datos completos sobre los correos electrónicos enviados, ofreciendo perspectivas sobre métricas clave como envíos y rechazos, lo que permite realizar un análisis detallado del proceso de entrega del correo electrónico."

![](assets/campaign_email_sending_performance.png)

El gráfico **[!UICONTROL Correo electrónico: rendimiento de envío]** proporciona una vista completa de los datos relacionados con los correos electrónicos enviados y ofrece detalles sobre métricas clave como envíos y devoluciones. Esto permite un análisis detallado del proceso de envío de correo electrónico, lo que proporciona información valiosa sobre la eficacia y el rendimiento de sus campañas de correo electrónico.

+++ Más información sobre el Correo electrónico: envío de métricas de rendimiento

* **[!UICONTROL Entregado]**: Número de correos electrónicos enviados correctamente, en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Reintentos]**: número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío para evitar que se enviara a los perfiles.

+++

### Correo electrónico: motivos de rechazo y categorías {#bounces-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_categories"
>title="Correo electrónico: Categorías de Rechazo"
>abstract="Los gráficos y la tabla Correo electrónico: Categorías de rechazo proporcionan datos sobre errores tanto temporales como permanentes."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_reasons"
>title="Correo electrónico: motivos de los Rechazos"
>abstract="El correo electrónico: los gráficos y la tabla Motivos de rechazos contienen los datos disponibles relacionados con los mensajes rechazados."

![](assets/campaign_email_bounces.png)

Los widgets **[!UICONTROL Correo electrónico - Razones de rechazo]** y **[!UICONTROL Correo electrónico - Categorías de rechazo]** compilan los datos disponibles relacionados con los mensajes rechazados, proporcionando una información detallada sobre las razones y categorías específicas detrás de los rechazos de correo electrónico.

Para obtener más información sobre las devoluciones, consulte la página [Lista de supresión](../reports/suppression-list.md).

+++ Más información sobre las métricas Correo electrónico: categorías de rechazo

* **[!UICONTROL Rechazo grave]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Devolución suave]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Omitido]**: El número total de mensajes temporales, como Fuera de la oficina, o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

+++


### Correo electrónico: motivos del error {#errors-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_error_reasons"
>title="Correo electrónico: motivos del error"
>abstract="El correo electrónico: los gráficos y la tabla Motivos de error permiten le permiten identificar los errores específicos que se produjeron durante el envío."

![](assets/campaign_email_error_reasons.png)

Los gráficos y la tabla **[!UICONTROL Motivos del error]** ofrecen visibilidad de los errores específicos que se produjeron durante el proceso de envío y proporcionan información valiosa sobre la naturaleza y la incidencia de los errores.

Puede elegir entre cambiar de una tabla, un gráfico de barras o un anillo.

### Correo electrónico: Motivos excluidos {#excluded-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_excluded_reasons"
>title="Correo electrónico: Motivos excluidos"
>abstract="Los gráficos y la tabla Motivos excluidos ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos del público destinatario, no recibieran el mensaje."

![](assets/campaign_email_excluded.png)

Los gráficos y la tabla de **[!UICONTROL Motivos de exclusión]** presentan una vista completa de los diferentes factores que tuvieron como resultado la exclusión de perfiles de usuario de la audiencia de destino, lo que hizo que no se recibiera el mensaje.

Consulte [esta página](exclusion-list.md) para obtener una lista completa de motivos de exclusión.

### Enviados y entregados por dominios {#sent-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sent_domains"
>title="Enviados y entregados por dominios"
>abstract="La tabla y el gráfico Enviados y entregados por dominios ofrecen un desglose de los correos electrónicos categorizados por dominios, presentando una visión en profundidad del rendimiento general de sus comunicaciones por correo electrónico."

![](assets/campaign_email_sent_domains.png)

La tabla y el gráfico de **[!UICONTROL Enviados y entregados por dominios]** proporcionan un desglose detallado de los mensajes de correo electrónico en el nivel de dominio, lo que ofrece una perspectiva completa del rendimiento de los mismos.

+++ Más información sobre las Métricas de Enviado y entregado por dominios

* **[!UICONTROL Enviado]**: Número total de envíos del correo electrónico.

* **[!UICONTROL Entregado]**: Número de correos electrónicos enviados correctamente, en relación con el número total de correos electrónicos enviados.

+++

### Rechazos y errores por dominios {#bounces-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounces_domains"
>title="Rechazos y errores por dominios"
>abstract="El gráfico y la tabla Rechazos y errores por dominios proporcionan un desglose granular a nivel de dominio, ofreciendo perspectivas sobre errores específicos encontrados durante el proceso de envío del correo electrónico."

![](assets/campaign_email_bounce_domains.png)

El gráfico y la tabla **[!UICONTROL Devoluciones y errores por dominios]** ofrecen un desglose a nivel de dominio de los errores específicos encontrados durante el proceso de envío, lo que proporciona un análisis detallado de los problemas que se produjeron.

+++ Más información sobre las Métricas Devoluciones y errores por dominios

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío y que impidieron que el correo electrónico se enviara a los perfiles.

+++

### Aperturas y clics por dominios {#opens-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_open_domains"
>title="Aperturas y clics por dominios"
>abstract="El gráfico y la tabla Aperturas y clics por dominios ofrecen un desglose detallado a nivel de dominio, presentando una vista completa de cómo su público interactúa con sus correos electrónicos."

![](assets/campaign_email_open_domains.png)

El gráfico y la tabla **[!UICONTROL Abrir y clics por dominios]** muestran un desglose a nivel de dominio de la participación de sus perfiles con su correo electrónico, lo que proporciona información valiosa sobre cómo los distintos dominios interactúan con su contenido.

+++ Más información sobre las métricas Abrir y clics por dominios

* **[!UICONTROL Aperturas]**: Número de veces que se abrió el correo electrónico.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

+++

### Motivos de rechazo por dominio {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounces_reasons_domains"
>title="Motivos de rechazo por dominio"
>abstract="El gráfico y la tabla Motivos de rechazo por dominio proporcionan un desglose a nivel de dominio, ofreciendo una visión completa de los errores temporales y permanentes. Este análisis detallado le proporciona información valiosa sobre las razones específicas de los mensajes rechazados."

![](assets/campaign_email_bounce_reasons_domains.png)

El gráfico y la tabla de **[!UICONTROL motivos de rechazo por dominio]** ofrecen un desglose de datos a nivel de dominio sobre los errores temporales y permanentes, lo que proporciona información detallada sobre los motivos detrás de los mensajes rechazados.

+++ Más información sobre los Motivos de rechazo por métricas de dominio

* **[!UICONTROL Aperturas]**: Número de veces que se abrió el correo electrónico.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

+++

### Correo electrónico: URL principal {#top-url-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_top_url"
>title="Correo electrónico: URL principal"
>abstract="Correo electrónico: el gráfico y la tabla URL principal ofrecen una visión general de las direcciones URL dentro del correo electrónico que reciben el mayor tráfico de visitantes, lo que le permite identificar los vínculos más populares."

![](assets/campaign_email_topurl.png)

El gráfico y la tabla de **[!UICONTROL Correo electrónico: URL principal]** proporcionan una visión general de las direcciones URL del correo electrónico que atraen el mayor tráfico de visitantes. Esto le permite identificar y priorizar los vínculos más populares, lo que mejora su comprensión de la participación del perfil con contenido específico en los correos electrónicos.

### Correo electrónico: Dominio del mejor destinatario {#top-recipient-email}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_best_recipient"
>title="Correo electrónico: Dominio del mejor destinatario"
>abstract="Correo electrónico: el gráfico y la tabla Dominio del mejor destinatario proporcionan un desglose detallado de los dominios que los destinatarios utilizan con más frecuencia para abrir el correo electrónico, lo que ofrece información valiosa sobre el comportamiento de los destinatarios."

![](assets/campaign_email_best_recipient.png)

>[!CAUTION]
>
> El widget **[!UICONTROL Correo electrónico: mejor dominio de destinatario]** tiene una tasa de precisión del 99,95 %.

El gráfico y la tabla **[!UICONTROL Correo electrónico: mejor dominio de destinatario]** ofrecen un desglose detallado de los dominios que los perfiles usan con más frecuencia para abrir sus correos electrónicos. Esto proporciona una valiosa perspectiva del comportamiento del perfil, lo que le ayuda a comprender las plataformas preferidas.

+++ Más información sobre el correo electrónico: las mejores métricas de dominio de destinatario

* **[!UICONTROL Entregado]**: Número de correos electrónicos enviados correctamente, en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Tasa de entrega]**: Porcentaje de correos electrónicos enviados correctamente.

* **[!UICONTROL Tasa de devoluciones + errores]**: porcentaje de correos electrónicos que rebotaron en comparación con los enviados.

+++

### Correo electrónico: optimización {#optimized-email}

![](assets/campaign_email_optimized.png)

>[!NOTE]
>
>Los widgets **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]** solo están disponibles si la opción Optimización del tiempo de envío está activada para el correo electrónico. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

Los widgets **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]** detallan la información principal relativa a su mensaje, estén optimizados o no.

+++ Más información sobre las Métricas de optimización del tiempo de envío

* **[!UICONTROL Enviado]**: Número total de envíos.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

* **[!UICONTROL Entregado]**: número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

+++

### Correo electrónico: ofertas {#email-offers}

![](assets/campaign_email_offers.png)

Los widgets **[!UICONTROL Estadísticas de ofertas]**, **[!UICONTROL Estadísticas de ofertas a lo largo del tiempo]** y **[!UICONTROL Estadísticas detalladas de ofertas]** miden el éxito de la oferta y el impacto en la audiencia de destino.

+++ Más información sobre el Correo electrónico: métricas de ofertas

* **[!UICONTROL Oferta enviada]**: Número total de envíos de la oferta.

* **[!UICONTROL Impresión de oferta]**: Número de veces que se abrió la oferta en sus correos electrónicos.

* **[!UICONTROL Clics en ofertas]**: Número de veces que se hizo clic en una oferta en sus correos electrónicos.

* **[!UICONTROL Nombre de ubicación]**: Nombre de la ubicación usada para mostrar la oferta. Para obtener más información sobre la ubicación, consulte esta [página](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Nombre de oferta]**: Nombre de la oferta agregada en la entrega. Para obtener más información sobre la ubicación, consulte esta [página](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Oferta enviada]**: Número total de envíos de la oferta.

* **[!UICONTROL Tasa de impresión de ofertas]**: Porcentaje de ofertas abiertas comparado con el número de ofertas enviadas.

+++

## Pestaña en la aplicación {#inapp-global}

En el **[!UICONTROL informe global]** de la campaña, la ficha **[!UICONTROL En la aplicación]** detalla la información principal relativa a los mensajes en la aplicación enviados en la campaña.

### Rendimiento en la aplicación {#in-app-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_performance"
>title="Rendimiento en la aplicación"
>abstract="Los KPI de rendimiento en la aplicación proporcionan información esencial sobre la participación de los visitantes en los mensajes de la aplicación."

![](assets/campaign_inapp_performance.png)

Los KPI de **[!UICONTROL rendimiento en la aplicación]** proporcionan información esencial sobre la participación de los visitantes en los mensajes en la aplicación, y proporcionan métricas esenciales para evaluar la eficacia y el impacto de las campañas en la aplicación.

+++ Obtenga más información sobre las métricas de rendimiento en la aplicación.

* **[!UICONTROL Impresiones únicas]**: número de usuarios únicos a los que se entregó el mensaje en la aplicación.

* **[!UICONTROL Impresiones]**: número total de mensajes en la aplicación entregados a todos los usuarios.

* **[!UICONTROL Interacciones]**: número total de interacciones con su mensaje en la aplicación. Esto incluye cualquier acción realizada por los usuarios, como clics, rechazos o cualquier otra interacción.

+++

### Interacciones por tipo {#interactions-type}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_interactions"
>title="Interacciones por tipo"
>abstract="La tabla Interacciones por tipo detalla la interacción de los usuarios con el mensaje de la aplicación mediante el seguimiento de cualquier clic, rechazo o interacción."

![](assets/campaign_inapp_interactions.png)

Los gráficos y la tabla de **[!UICONTROL Interacciones por tipo]** proporcionan una descripción detallada de cómo interactuaron los perfiles con el mensaje en la aplicación, el seguimiento de acciones como clics, rechazos o cualquier otra forma de participación.

### Resumen de la aplicación {#in-app-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_summary"
>title="Resumen de la aplicación"
>abstract="El gráfico de resumen de la aplicación ilustra la progresión de las impresiones e interacciones de la aplicación durante el período especificado."

![](assets/campaign_inapp_summary.png)

El gráfico **[!UICONTROL Resumen en la aplicación]** ilustra la progresión de las impresiones e interacciones en la aplicación durante el período especificado, lo que proporciona una visión general del rendimiento de los mensajes en la aplicación.

+++ Más información sobre las Métricas de resumen en la aplicación

* **[!UICONTROL Impresiones únicas]**: número de usuarios únicos a los que se entregó el mensaje en la aplicación.

* **[!UICONTROL Impresiones]**: número total de mensajes en la aplicación entregados a todos los usuarios.

* **[!UICONTROL Interacciones]**: número total de interacciones con su mensaje en la aplicación. Esto incluye cualquier acción realizada por los usuarios, como clics, rechazos o cualquier otra interacción.

+++

## Pestaña de notificación push {#push-global}

En el **[!UICONTROL informe global]** de la campaña, la ficha **[!UICONTROL Notificación push]** detalla la información principal relativa a las notificaciones push enviadas en la campaña.

### Notificación push: estadísticas de envío {#push-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_statistics"
>title="Notificación push: estadísticas de envío"
>abstract="La tabla Estadísticas de envío de notificaciones push resume los datos esenciales sobre las notificaciones push, como los mensajes dirigidos o enviados."

![](assets/campaign_push_sending.png)

La tabla **[!UICONTROL Notificación push: estadísticas de envío]** proporciona un resumen conciso de los datos esenciales relacionados con las notificaciones push, incluidas métricas clave como el número de mensajes de destino y el número de mensajes enviados correctamente.

+++ Más información sobre las Notificaciones push: envío de métricas de estadísticas

* **[!UICONTROL Tiempo de ejecución]**: tiempo de inicio de cada ejecución de la notificación push recurrente. Para enviar solo una o varias notificaciones push recurrentes, selecciónelas en la lista desplegable **[!UICONTROL Hora de ejecución]**.

* **[!UICONTROL Objetivos]**: Número total de notificaciones push procesadas durante el análisis.

* **[!UICONTROL Enviado]**: Número total de envíos para la notificación push.

* **[!UICONTROL Entregado]**: Número de notificaciones push enviadas correctamente, en relación con el número total de notificaciones push enviadas.

* **[!UICONTROL Tasa de entrega]**: porcentaje de notificaciones push enviadas correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de notificaciones push.

* **[!UICONTROL Tasa de devoluciones]**: porcentaje de notificaciones push que rebotaron en comparación con las notificaciones push enviadas.

* **[!UICONTROL Errores]**: Número total de errores que impidieron que se enviara a los perfiles.

* **[!UICONTROL Tasa de errores]**: Porcentaje de errores que se produjeron durante el envío, en comparación con las notificaciones push enviadas.

* **[!UICONTROL Excluido]**: número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

### Notificación push: estadísticas de seguimiento {#push-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_tracking_statistics"
>title="Notificación push: estadísticas de seguimiento"
>abstract="Las Estadísticas de seguimiento push proporcionan datos sobre la actividad del perfil de su notificación push."

![](assets/campaign_push_tracking.png)

El widget **[!UICONTROL Notificación push: estadísticas de seguimiento]** ofrece una instantánea detallada de la actividad del perfil vinculada a las notificaciones push, lo que proporciona información esencial sobre la participación y la eficacia de las notificaciones push.

+++ Más información sobre las Notificaciones push: métricas de estadísticas de seguimiento

* **[!UICONTROL Tiempo de ejecución]**: tiempo de inicio de cada ejecución de la notificación push recurrente. Para enviar solo una o varias notificaciones push recurrentes, selecciónelas en la lista desplegable **[!UICONTROL Hora de ejecución]**.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió la notificación push.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación de inserción entregada, por ejemplo, clic en el botón o despido.

+++

### Notificación push: resumen del envío {#push-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_summary"
>title="Notificación push: resumen del envío"
>abstract="El gráfico Resumen del envío de notificaciones push muestra los datos disponibles para las notificaciones push enviadas."

![](assets/campaign_push_sending_summary.png)

El gráfico **[!UICONTROL Notificación push: resumen de envío]** ofrece una representación dinámica que muestra un análisis de su actividad de notificaciones push. Esta representación gráfica proporciona un desglose completo de las notificaciones push enviadas.

+++ Más información sobre las Notificaciones push: envío de métricas de resumen

* **[!UICONTROL Aperturas]**: Número de veces que se abrió la notificación push.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación de inserción entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados y procesamiento automático de devoluciones en relación con el número total de notificaciones push enviadas.

* **[!UICONTROL Entregado]**: Número de notificaciones push enviadas correctamente, en relación con el número total de notificaciones push enviadas.

* **[!UICONTROL Errores]**: Número total de errores que impidieron que se enviara a los perfiles.

+++

### Notificación push: optimización {#push-optimized}

>[!NOTE]
>
>Los widgets **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]** solo están disponibles si la opción Optimización del tiempo de envío está activada para la notificación push. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

Los widgets **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]** detallan la información principal relativa a su mensaje, estén optimizados o no.

+++ Más información sobre las Notificaciones push: enviar métricas de optimización de tiempo

* **[!UICONTROL Entregado]**: Número de notificaciones push enviadas correctamente, en relación con el número total de notificaciones push enviadas.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió la notificación push.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación de inserción entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de notificaciones push enviadas.

+++

### Notificación push: motivos del error {#error-reasons-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_error_reasons"
>title="Notificación push: motivos del error"
>abstract="Los gráficos y la tabla Motivos del error le permiten identificar los errores específicos que se produjeron durante el proceso de envío."

![](assets/campaign_push_error_reasons.png)

La tabla y los gráficos de **[!UICONTROL Motivos del error]** le permiten identificar los errores específicos que se produjeron durante el proceso de envío de las notificaciones push, lo que ofrece una perspectiva detallada de los problemas que se detectaron durante el proceso.

### Notificación push: motivos de exclusión {#excluded-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_excluded_reasons"
>title="Notificación push: motivos de exclusión"
>abstract="Los gráficos y la tabla Motivos excluidos ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos del público destinatario, no recibieran el mensaje."

![](assets/campaign_push_excluded.png)

Los gráficos y la tabla de **[!UICONTROL razones de exclusión]** muestran las diferentes razones que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran sus notificaciones push.

Consulte [esta página](exclusion-list.md) para obtener una lista completa de motivos de exclusión.

### Notificación push: desglose por plataforma {#breakdown-platform-push}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_breakdown_platform"
>title="Notificación push: desglose por plataforma"
>abstract="La notificación push: los gráficos y la tabla Desglose por plataforma proporcionan un desglose del éxito de las notificaciones push en función del sistema operativo del perfil."

![](assets/campaign_push_breakdown.png)

El gráfico y la tabla de **[!UICONTROL Notificación push: desglose por plataforma]** proporcionan un análisis detallado del éxito de sus notificaciones push, y ofrecen perspectivas basadas en el sistema operativo de su perfil. Este desglose mejora su comprensión del rendimiento de las notificaciones push en las distintas plataformas.

+++ Más información sobre las notificaciones push: desglose por métricas de plataforma

* **[!UICONTROL Objetivos]**: Número total de notificaciones push procesadas durante el análisis.

* **[!UICONTROL Entregado]**: Número de notificaciones push enviadas correctamente, en relación con el número total de notificaciones push enviadas.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió la notificación push.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación de inserción entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados y procesamiento automático de devoluciones en relación con el número total de notificaciones push enviadas.

* **[!UICONTROL Errores]**: Número total de errores que impidieron que se enviara a los perfiles.

* **[!UICONTROL Excluido]**: número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

## Pestaña SMS {#sms-global}

En el **[!UICONTROL informe global]** de la campaña, la ficha **[!UICONTROL SMS]** detalla la información principal relativa a los mensajes SMS enviados en la campaña.

### SMS: estadísticas de envío {#sms-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_sending_statistics"
>title="SMS: estadísticas de envío"
>abstract="La tabla SMS: estadísticas del envío resume los datos esenciales sobre sus mensajes SMS, como los mensajes segmentados o los entregados."

![](assets/campaign_sms_sending.png)

La tabla **[!UICONTROL SMS - estadísticas de envío]** proporciona un resumen conciso de los datos esenciales relacionados con sus mensajes SMS, que incluye métricas clave como el número de mensajes dirigidos y el recuento de mensajes enviados correctamente.

+++ Más información sobre SMS: métricas de estadísticas de envío

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución de su mensaje SMS recurrente. Para enviar solo uno o varios mensajes SMS recurrentes, selecciónelos en la lista desplegable **[!UICONTROL Tiempo de ejecución]**.

* **[!UICONTROL Segmentado]**: número de perfiles de usuario que cumplen los requisitos como perfiles de destinatario.

* **[!UICONTROL Excluido]**: número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

* **[!UICONTROL Enviado]**: Número total de envíos para sus mensajes SMS.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes SMS enviados.

* **[!UICONTROL Errores]**: Número total de errores que impidieron que se enviara a los perfiles.

+++

### SMS: estadísticas de seguimiento {#sms-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_sms_tracking_statistics"
>title="SMS: estadísticas de seguimiento"
>abstract="El widget SMS: estadísticas de seguimiento proporciona información general completa de la información esencial relacionada con la interacción de sus visitantes con su URL."

![](assets/campaign_sms_tracking.png)

El widget **[!UICONTROL SMS - Estadísticas de seguimiento]** proporciona una descripción detallada de la información clave relacionada con la participación de los visitantes con las direcciones URL, lo que ofrece perspectivas sobre la eficacia de los mensajes SMS.

+++ Más información sobre SMS: métricas de estadísticas de seguimiento

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución de su SMS recurrente. Para enviar solo uno o varios SMS recurrentes, selecciónelos en la lista desplegable **[!UICONTROL Tiempo de ejecución]**.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un mensaje SMS.

+++

### SMS: rendimiento por fecha {#sms-perfomance-date}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_performance"
>title="SMS: rendimiento por fecha"
>abstract="El widget SMS: rendimiento por fecha proporciona información clave sobre los mensajes a través de una representación gráfica."

![](assets/campaign_sms_performance.png)

El widget **[!UICONTROL Rendimiento de SMS por fecha]** ofrece una descripción detallada de la información clave relacionada con sus mensajes, presentada a través de un gráfico, que proporciona información sobre las tendencias de rendimiento en períodos de tiempo específicos.

+++ Más información sobre SMS: rendimiento por métricas de fecha

* **[!UICONTROL Enviado]**: Número total de envíos para sus mensajes SMS.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes SMS enviados.

* **[!UICONTROL Errores]**: Número total de errores que impidieron que se enviara a los perfiles.

+++

### SMS: motivos del error {#sms-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_error_reasons"
>title="SMS: motivos del error"
>abstract="SMS: los gráficos y la tabla Motivos de error le permiten identificar los errores específicos que se produjeron durante el proceso de envío."

![](assets/campaign_sms_error_reasons.png)

Los gráficos y la tabla **[!UICONTROL Motivos del error]** le permiten identificar los errores específicos que se produjeron durante el proceso de envío de sus mensajes SMS, lo que facilita un análisis exhaustivo de cualquier problema que se haya encontrado.

### SMS: motivos de exclusión {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_excluded_reasons"
>title="SMS: motivos de exclusión"
>abstract="Los gráficos y la tabla Motivos excluidos ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos del público destinatario, no recibieran el mensaje."

![](assets/campaign_sms_excluded.png)

Los gráficos y la tabla **[!UICONTROL Excluye Reasons]** muestran visualmente los diversos factores que llevaron a la exclusión de perfiles de usuarios de la audiencia de destino, lo que les impidió recibir sus mensajes SMS.

Consulte [esta página](exclusion-list.md) para obtener una lista completa de motivos de exclusión.

### SMS: motivos de rechazos {#sms-bounces-reasons}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_bounces_reasons"
>title="SMS: motivos de rechazos"
>abstract="Los gráficos y la tabla Motivos de rechazos contienen los datos disponibles relacionados con los mensajes rechazados."

Los gráficos y la tabla de **[!UICONTROL Motivos de rechazos]** proporcionan una visión general completa de los datos relacionados con los mensajes SMS rechazados, lo que proporciona información valiosa sobre los motivos específicos detrás de los rechazos de mensajes SMS.

### SMS: clics por vínculos {#sms-clicks-links}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_clicks_links"
>title="SMS: clics por vínculos"
>abstract="El widget SMS: clics por vínculos proporciona información esencial de la participación de los visitantes en las direcciones URL de los mensajes."

![](assets/campaign_sms_clicks.png)

El widget **[!UICONTROL SMS - Clics por vínculos]** ofrece información esencial sobre la participación de los visitantes con las direcciones URL incluidas en los mensajes, y proporciona información valiosa sobre los vínculos que atraen más interacción.

## Pestaña web {#web-tab}

Desde su **[!UICONTROL informe global]** de Campaign, la ficha **[!UICONTROL Web]** detalla la información principal relativa a sus páginas web.

### Rendimiento web {#web-performance}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_performance"
>title="Rendimiento web"
>abstract="Los KPI de rendimiento web proporcionan información completa sobre la participación de los visitantes en las experiencias web."

![](assets/campaign_web_performance.png)

Los KPI de **[!UICONTROL rendimiento web]** ofrecen una amplia perspectiva de la participación de los visitantes en sus páginas web, e incluyen métricas clave como Impresiones e Interacciones.

+++ Más información sobre las métricas de rendimiento web

* **[!UICONTROL Impresiones únicas]**: número de usuarios únicos a los que se les entregó la experiencia web.

* **[!UICONTROL Impresiones]**: número total de experiencias web entregadas a todos los usuarios.

* **[!UICONTROL Tasa de interacción]**: porcentaje de interacciones con su página web. Esto incluye cualquier acción realizada por los usuarios, como clics o cualquier otra interacción.

+++

### Resumen web {#web-summary}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_summary"
>title="Resumen web"
>abstract="El gráfico Resumen web ilustra la progresión de las experiencias web, incluidas las impresiones, las impresiones únicas y las interacciones, durante el período especificado."

![](assets/campaign_web_summary.png)

El gráfico de **[!UICONTROL resumen web]** muestra la evolución de sus experiencias web (impresiones, impresiones únicas e interacciones) durante el período correspondiente.

+++ Más información sobre las métricas de resumen web

* **[!UICONTROL Impresiones únicas]**: número de usuarios únicos a los que se les entregó la experiencia web.

* **[!UICONTROL Impresiones]**: número total de experiencias web entregadas a todos los usuarios.

* **[!UICONTROL Interacción]**: número total de interacciones con su página web. Esto incluye cualquier acción realizada por los usuarios, como clics o cualquier otra interacción.

+++

### Interacciones por elemento {#web-interactions}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_interactions"
>title="Interacciones por elemento"
>abstract="La tabla Interacciones por elemento proporciona información clave sobre la participación de los visitantes en diferentes elementos de las páginas web."

![](assets/campaign_web_interactions.png)

La tabla **[!UICONTROL Interacciones por elemento]** presenta información completa sobre la participación de los visitantes con los distintos elementos de las páginas web, lo que ofrece información valiosa sobre las interacciones y preferencias de los usuarios.

+++ Más información sobre las Interacciones por métricas de elemento

* **[!UICONTROL Interacción]**: número total de interacciones con su página web. Esto incluye cualquier acción realizada por los usuarios, como clics o cualquier otra interacción.

* **[!UICONTROL Tasa de interacción]**: porcentaje de interacciones con su página web. Esto incluye cualquier acción realizada por los usuarios, como clics o cualquier otra interacción.

+++

## Pestaña de correo directo {#direct-mail-global}

En el **[!UICONTROL informe global]** de la campaña, la ficha **[!UICONTROL Correo directo]** detalla la información principal relativa a los mensajes de correo postal.

### Correo directo: estadísticas del envío {#direct-mail-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_sending_statistics"
>title="Correo directo: estadísticas del envío"
>abstract="La tabla Estadísticas del envío de correo directo resume los datos esenciales sobre sus mensajes de correo directo, como los mensajes segmentados o enviados."

![](assets/campaign_direct_sending.png)

La tabla **[!UICONTROL Correo directo: estadísticas de envío]** proporciona un resumen conciso de los datos esenciales relacionados con sus mensajes de correo directo, que incluye métricas clave como el número de mensajes de destino y el recuento de mensajes enviados correctamente.

+++ Más información sobre el Correo directo: métricas de estadísticas de envío

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución del correo postal recurrente. Para enviar solo uno o varios mensajes de correo postal recurrentes, selecciónelos en la lista desplegable **[!UICONTROL Tiempo de ejecución]**.

* **[!UICONTROL Segmentado]**: número de perfiles de usuario que cumplen los requisitos de perfiles de destinatario para sus mensajes de correo postal.

* **[!UICONTROL Enviado]**: Número total de envíos de sus mensajes de correo postal.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío para evitar que se enviara a los perfiles.

* **[!UICONTROL Excluido]**: número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron sus mensajes de correo postal.

+++

### Correo directo: motivos del error {#direct-mail-error}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_error_reasons"
>title="Correo directo: motivos del error"
>abstract="Los gráficos y la tabla Correo directo: motivos de error le permiten identificar los errores específicos que se produjeron durante el envío."

![](assets/direct-mail-report_1.png)

Los gráficos y la tabla de **[!UICONTROL Correo directo: razones de error]** proporcionan los medios para identificar errores específicos que se produjeron durante el proceso de envío de sus mensajes de correo postal, lo que permite un análisis detallado de cualquier problema que se haya encontrado.

### Correo directo: motivos de la exclusión {#direct-mail-excluded}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_excluded_reasons"
>title="Correo directo: motivos de la exclusión"
>abstract="Los gráficos y la tabla Motivos excluidos del correo directo ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos del público destinatario, no recibieran el mensaje."

![](assets/campaign_direct_excluded.png)

Los gráficos y la tabla de **[!UICONTROL Correo directo: razones de exclusión]** ilustran visualmente los diversos factores que resultaron en la exclusión de perfiles de usuarios de la audiencia de destino, lo que les impide recibir sus mensajes de correo postal.

Consulte [esta página](exclusion-list.md) para obtener una lista completa de motivos de exclusión.

## Recursos adicionales

* [Introducción a las campañas](../campaigns/get-started-with-campaigns.md)
* [Creación de una campaña](../campaigns/create-campaign.md)
* [Creación de campañas activadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificación o detención de una campaña](../campaigns/modify-stop-campaign.md)
* [Informe en vivo de la campaña](campaign-live-report.md)
