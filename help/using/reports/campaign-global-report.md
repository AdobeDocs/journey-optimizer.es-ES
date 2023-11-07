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
source-git-commit: 82b8c9032d6c377cb76acce4d5cc45afb0ddd6ba
workflow-type: tm+mt
source-wordcount: '3357'
ht-degree: 24%

---

# Informe global de la campaña {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Informe global de la campaña"
>abstract="El informe global de campaña permite medir el impacto de las campañas durante un período de tiempo seleccionado. El informe se divide en distintos widgets que detallan el éxito y los errores de la campaña. Cada tablero de informes se puede modificar cambiando el tamaño de los widgets o eliminándolos."

Informes globales, accesibles desde **Siempre** pestaña, muestra los eventos que se produjeron hace al menos dos horas y cubre los eventos durante un periodo de tiempo seleccionado. En comparación, los informes en directo se centran en los eventos que han tenido lugar en las últimas 24 horas, con un intervalo de tiempo mínimo de dos minutos desde que se produjo el evento.

Se puede acceder al informe global de Campaign directamente desde la campaña con la variable **[!UICONTROL Ver informe]** botón.

![](assets/campaign_report_global_5.png)

La campaña **[!UICONTROL Informe global]** se mostrará con las siguientes pestañas:

* [Campaign](#campaign-global)
* [Correo electrónico](#email-global)
* [En la aplicación](#inapp-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [Web](#web-tab)
* [Correo directo](#direct-mail-global)

La campaña **[!UICONTROL Informe global]** se divide en diferentes widgets que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](../reports/global-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global.md)

## Pestaña Campaña {#campaign-global}

### envío {#delivery-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_delivery_global"
>title="Estadísticas de Campaign"
>abstract="El widget de estadísticas de Campaign detalla la información principal relativa a la campaña, como los perfiles introducidos y las acciones enviadas."

![](assets/campaign_report_global_1.png)

El **[!UICONTROL Estadísticas de la campaña]** El widget detalla la información principal relativa a la campaña:

* **[!UICONTROL Perfiles introducidos]**: Número de perfiles que iniciaron el recorrido.

* **[!UICONTROL Acciones entregadas]**: Número total de veces que se ha entregado una acción en el recorrido.

* **[!UICONTROL Acciones con errores en %]**: Número total de veces únicas que una acción ha fallado en el recorrido comparado con el número total de veces únicas que se ha entregado una acción.

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../campaigns/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.
-->

### Informe de experimentación {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Métrica de éxito"
>abstract="El valor total de la métrica de éxito, previamente seleccionada al crear los experimentos, dividido por el número de perfiles."

![](assets/experimentation_report_3.png)

El **[!UICONTROL Experimentación]** proporciona perspectivas clave sobre el rendimiento de cada variante e identifica la que tiene más éxito.

Tenga en cuenta que la definición del mejor ejecutante puede llevar algún tiempo y se representará mediante este icono ![](assets/experimentation_report_1.png).

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe Experimentación.

El **[!UICONTROL Resultado del experimento]** widget detalla el rendimiento de cada variante. Puede cambiar la línea de base seleccionando uno de los tratamientos en la **[!UICONTROL Línea base]** la lista desplegable. El mejor tratamiento se representará con un icono de estrella.

La tabla presenta las siguientes métricas:

* **[!UICONTROL Alza sobre la línea base]**: Medida de la mejora porcentual en la tasa de conversión de un tratamiento determinado respecto al valor basal.

* **[!UICONTROL Confianza]**: Evidencia de que un tratamiento dado es el mismo que el tratamiento basal. [Más información](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Clics salientes únicos]**: Recuento total de clics en los canales salientes.

* **[!UICONTROL Perfiles]**: Número de perfiles objetivo para este tratamiento.

* **[!UICONTROL Clics/perfiles salientes únicos]**: Valor total de la métrica de éxito, seleccionada anteriormente al crear los experimentos, dividido por el número de perfiles.

El **[!UICONTROL Intervalo de confianza]** el gráfico mide la incertidumbre en torno a la mejora. Detalla la diferencia porcentual en el rendimiento entre la línea de base y el tratamiento con mejor rendimiento. [Más información](../campaigns/experiment-calculations.md#confidence-intervals).

![](assets/experimentation_report_4.png)

El último widget proporciona datos relacionados con el **[!UICONTROL Métrica de éxito]** ha seleccionado anteriormente para sus Tratamientos. Tiene la opción de seleccionar una métrica de destino diferente en la **[!UICONTROL Métrica]** menú desplegable para rastrear datos alternativos.

>[!CAUTION]
>
>Cuando trabaje con métricas filtradas de experimentación, tenga en cuenta que al cambiar la selección de métricas del menú desplegable en la página de comparación para la experimentación, no se conservará el valor de filtro. Por ejemplo, si se cambia de &quot;Clics&quot; a &quot;Clics únicos&quot;, se perderá el filtro aplicado y la comparación se volverá inexacta o no válida.

+++

Para profundizar en estos resultados y en cómo interpretarlos, consulte [esta página](../campaigns/get-started-experiment.md#interpret-results).

## Pestaña de correo electrónico {#email-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_statistics"
>title="Correo electrónico: Estadísticas de envío"
>abstract="La tabla Correo electrónico: Estadísticas de envío resume los datos esenciales sobre sus correos electrónicos, como los segmentados o enviados."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_tracking_statistics"
>title="Correo electrónico: Estadísticas de seguimiento"
>abstract="La tabla Correo electrónico: Estadísticas de seguimiento proporciona datos sobre la actividad del perfil del Correo electrónico."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_performance"
>title="Correo electrónico: Rendimiento de envío"
>abstract="El gráfico Correo electrónico: Rendimiento de envío presenta datos completos sobre los correos electrónicos enviados, ofreciendo perspectivas sobre métricas clave como envíos y rechazos, lo que permite un análisis detallado del proceso de envío de correo electrónico."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_categories"
>title="Correo electrónico: Categorías de Rechazo"
>abstract="Los gráficos y la tabla Correo electrónico: Categorías de rechazo proporcionan datos sobre errores tanto temporales como permanentes."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_reasons"
>title="Correo electrónico: motivos de los Rechazos"
>abstract="El correo electrónico: los gráficos y la tabla Motivos de rechazos contienen los datos disponibles relacionados con los mensajes rechazados."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_error_reasons"
>title="Correo electrónico: Motivos de error"
>abstract="El correo electrónico: los gráficos y la tabla Motivos de error permiten le permiten identificar los errores específicos que se produjeron durante el envío."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_excluded_reasons"
>title="Correo electrónico: Motivos excluidos"
>abstract="Los gráficos y la tabla Motivos excluidos ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos del público destinatario, no recibieran el mensaje."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_top_url"
>title="Correo electrónico: URL principal"
>abstract="Correo electrónico: el gráfico y la tabla URL principal ofrecen una visión general de las direcciones URL dentro del correo electrónico que reciben el mayor tráfico de visitantes, lo que le permite identificar los vínculos más populares."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_best_recipient"
>title="Correo electrónico: Dominio del mejor destinatario"
>abstract="Correo electrónico: el gráfico y la tabla Dominio del mejor destinatario proporcionan un desglose detallado de los dominios que los destinatarios utilizan con más frecuencia para abrir el correo electrónico, lo que ofrece información valiosa sobre el comportamiento de los destinatarios."

![](assets/campaign_report_global_2.png)

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL Correo electrónico]** Esta pestaña detalla la información principal relacionada con los envíos de correo electrónico realizados en Campaign.

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe de correo electrónico.

El **[!UICONTROL Estadísticas de envío de correo electrónico]** el gráfico detalla el éxito de su correo electrónico:

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución del correo electrónico recurrente. Para dirigirse solo a uno o varios correos electrónicos recurrentes, selecciónelos en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Objetivos]**: Número total de mensajes procesados durante el proceso de envío.

* **[!UICONTROL Enviado]**: Número total de envíos del correo electrónico.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de entrega]**: porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de devoluciones]**: porcentaje de correos electrónicos que rebotaron en comparación con los enviados.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.

* **[!UICONTROL Tasa de error]**: porcentaje de errores que se produjeron durante el proceso de envío y que impiden su envío en comparación con los correos electrónicos enviados.

* **[!UICONTROL Reintentos]**: Número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Excluido]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

El **[!UICONTROL Correo electrónico: estadísticas de seguimiento]** El widget contiene los datos disponibles para la actividad de perfil del correo electrónico:

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución del correo electrónico recurrente. Para dirigirse solo a uno o varios correos electrónicos recurrentes, selecciónelos en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió el correo electrónico.

* **[!UICONTROL Aperturas únicas]**: porcentaje de correos electrónicos abiertos.

* **[!UICONTROL Tasa de apertura]**: Número total de correos electrónicos abiertos en comparación con el número de correos electrónicos enviados.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de un correo electrónico.

* **[!UICONTROL Tasa de clics únicos]**: porcentaje de usuarios que interactuaron con el correo electrónico.

* **[!UICONTROL Baja de suscripciones]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Quejas de spam]**: Número de veces que un mensaje se declaró como correo no deseado.

El **[!UICONTROL Rendimiento de envío]** El gráfico contiene los datos disponibles para los correos electrónicos enviados, como:

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Reintentos]**: Número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.

El **[!UICONTROL Motivos del rechazo]** y **[!UICONTROL Categorías de rechazo]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Rechazo duro]**: el número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Rechazo suave]**: el número total de errores temporales, como una bandeja de entrada llena.

* **[!UICONTROL Ignorado]**: el número total de mensajes temporales, como Fuera de la oficina, o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

Para obtener más información sobre las devoluciones, consulte [Lista de supresión](../reports/suppression-list.md) página.

El **[!UICONTROL Motivos del error]** El gráfico y la tabla permiten ver qué error se produjo durante el proceso de envío.

El **[!UICONTROL Razones de exclusión]** el gráfico y la tabla muestran los diferentes motivos que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran el mensaje.

El **[!UICONTROL Correo electrónico: URL principal]** Un gráfico y una tabla detallan las direcciones URL del correo electrónico más visitadas.

El **[!UICONTROL Correo electrónico: dominio del destinatario principal]** el gráfico y la tabla detallan qué dominios son los más utilizados por los perfiles para abrir el correo electrónico.

>[!CAUTION]
>
> El **[!UICONTROL Correo electrónico: dominio del destinatario principal]** El widget tiene una tasa de precisión del 99,95 %.

El **[!UICONTROL Correo electrónico: optimizado frente a normal]** El gráfico detalla la información principal relativa al mensaje, estén optimizados o no:

* **[!UICONTROL Enviado]**: Número total de envíos.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

El **[!UICONTROL Correo electrónico: optimización del tiempo de envío]** detalla el éxito del correo electrónico según el método de envío: optimizado o normal.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

>[!NOTE]
>
>El **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]**  Los widgets solo están disponibles si la opción Optimización del tiempo de envío está activada para el correo electrónico. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

+++

## Pestaña en la aplicación {#inapp-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_performance"
>title="Rendimiento en la aplicación"
>abstract="Los KPI de rendimiento en la aplicación proporcionan información esencial sobre la participación de los visitantes en los mensajes de la aplicación."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_interactions"
>title="Interacciones por tipo"
>abstract="La tabla Interacciones por tipo detalla la interacción de los usuarios con el mensaje de la aplicación mediante el seguimiento de cualquier clic, rechazo o interacción."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_summary"
>title="Resumen de la aplicación"
>abstract="El gráfico de resumen de la aplicación ilustra la progresión de las impresiones e interacciones de la aplicación durante el período especificado."

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL En la aplicación]** Esta pestaña detalla la información principal relativa a las entregas en la aplicación enviadas en la campaña.

![](assets/campaign_report_global_6.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe en la aplicación.

El **[!UICONTROL Rendimiento en la aplicación]** Los KPI detallan la información principal relativa a la participación de los visitantes en los mensajes en la aplicación, como:

* **[!UICONTROL Impresiones únicas]**: número de usuarios únicos a los que se entregó el mensaje en la aplicación.

* **[!UICONTROL Impresiones]**: número total de mensajes en la aplicación entregados a todos los usuarios.

* **[!UICONTROL Tasa de interacciones]**: porcentaje de interacciones con el mensaje en la aplicación. Esto incluye cualquier acción realizada por los usuarios, como clics, rechazos o cualquier otra interacción.

El **[!UICONTROL Interacciones por tipo]** en los gráficos y la tabla se detalla la interacción de los usuarios con el mensaje en la aplicación mediante el seguimiento de cualquier clic, despido o interacción.

El **[!UICONTROL Resumen en la aplicación]** Este gráfico muestra la evolución de las impresiones e interacciones en la aplicación durante el periodo correspondiente.
+++

## Pestaña de notificación push {#push-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_statistics"
>title="Notificación push: estadísticas de envío"
>abstract="La tabla Estadísticas de envío de notificaciones push resume los datos esenciales sobre las notificaciones push, como los mensajes dirigidos o enviados."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_tracking_statistics"
>title="Notificación push: estadísticas de seguimiento"
>abstract="Las Estadísticas de seguimiento push proporcionan datos sobre la actividad del perfil de su notificación push."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_summary"
>title="Notificación push: resumen del envío"
>abstract="El gráfico Resumen del envío de notificaciones push muestra los datos disponibles para las notificaciones push enviadas."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_excluded_reasons"
>title="Notificación push: motivos excluidos"
>abstract="Los gráficos y la tabla Motivos excluidos ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos del público destinatario, no recibieran el mensaje."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_error_reasons"
>title="Notificación push: motivos del error"
>abstract="Los gráficos y la tabla Motivos del error le permiten identificar los errores específicos que se produjeron durante el proceso de envío."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_breakdown_platform"
>title="Notificación push: desglose por plataforma"
>abstract="Los gráficos y la tabla Desglose por plataforma proporcionan un desglose del éxito de las notificaciones push en función del sistema operativo del perfil."

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL Notificación push]** Esta pestaña detalla la información principal relativa a las entregas push enviadas en la campaña.

![](assets/campaign_report_global_3.png)Los KPI de rendimiento en la aplicación detallan la información principal relativa a la participación de los visitantes en los mensajes en la aplicación.

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe push.

El **[!UICONTROL Notificación push: estadísticas de envío]** Esta tabla detalla la información principal relativa a las notificaciones push:

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución de la notificación push recurrente. Para segmentar solo una o varias notificaciones push recurrentes, selecciónelas en el **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Objetivos]**: Número total de mensajes procesados durante el análisis.

* **[!UICONTROL Enviado]**: Número total de envíos para la notificación push.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de entrega]**: porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de devoluciones]**: porcentaje de notificaciones push que rebotaron en comparación con las notificaciones push enviadas.

* **[!UICONTROL Errores]**: Número total de errores que han impedido su envío a los perfiles.

* **[!UICONTROL Tasa de error]**: porcentaje de errores que se produjeron durante la prevención para que se enviara en comparación con las notificaciones push enviadas.

* **[!UICONTROL Excluido]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

El **[!UICONTROL Push: estadísticas de seguimiento]** contiene los datos disponibles de la actividad de perfil de la notificación push:

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución de la notificación push recurrente. Para segmentar solo una o varias notificaciones push recurrentes, selecciónelas en el **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió la notificación push.

* **[!UICONTROL Tasa de apertura]**: porcentaje de notificaciones push abiertas.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Participaciones]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

* **[!UICONTROL Tasa de participación]**: Porcentaje de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

El **[!UICONTROL Resumen de notificaciones push]** El gráfico contiene los datos disponibles para las notificaciones push enviadas, como:

* **[!UICONTROL Aperturas]**: Número de veces que se abrió la notificación push.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados y procesamiento automático de devolución en relación con el número total de mensajes enviados.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que han impedido su envío a los perfiles.

>[!NOTE]
>
>El **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]**  Los widgets solo están disponibles si la opción Optimización del tiempo de envío está activada para la notificación push. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

El **[!UICONTROL Optimizado frente a no optimizado]** El gráfico detalla la información principal relativa al mensaje, estén optimizados o no:

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Aperturas]**: Número de veces que se abrió la notificación push.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

El **[!UICONTROL Optimización del tiempo de envío]** detalla el éxito de la notificación push según el método de envío: optimizado o normal.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

El **[!UICONTROL Motivos del error]** Los gráficos y las tablas permiten ver qué error se ha producido.

El **[!UICONTROL Razones de exclusión]** los gráficos y las tablas muestran los diferentes motivos que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran el mensaje.

El **[!UICONTROL Desglose por plataforma]** el gráfico y la tabla detallan el éxito de la notificación push en función del sistema operativo del perfil.
+++

## Pestaña SMS {#sms-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_sending_statistics"
>title="SMS: estadísticas de envío"
>abstract="La tabla Estadísticas del envío de SMS resume los datos esenciales sobre sus mensajes SMS, como los mensajes segmentados o enviados."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_error_reasons"
>title="SMS: motivos de error"
>abstract="SMS: los gráficos y la tabla Motivos de error le permiten identificar los errores específicos que se produjeron durante el proceso de envío."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_performance"
>title="SMS: rendimiento por fecha"
>abstract="El widget Rendimiento por fecha de SMS proporciona información clave sobre los mensajes a través de una representación gráfica."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_excluded_reasons"
>title="SMS: motivos excluidos"
>abstract="Los gráficos y la tabla Motivos excluidos ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos del público destinatario, no recibieran el mensaje."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_bounces_reasons"
>title="SMS: motivos de rechazos"
>abstract="Los gráficos y la tabla Motivos de rechazos contienen los datos disponibles relacionados con los mensajes rechazados."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_clicks_links"
>title="SMS: clics por vínculos"
>abstract="El widget SMS: clics por vínculos proporciona información esencial sobre la participación de los visitantes en las direcciones URL de los mensajes"

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL SMS]** Esta pestaña detalla la información principal relativa a los envíos SMS enviados en la campaña.

![](assets/campaign_report_global_4.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe SMS.

El **[!UICONTROL SMS: estadísticas de envío]** La tabla detalla el éxito del mensaje SMS:

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución del mensaje SMS recurrente. Para dirigirse solo a uno o varios mensajes SMS recurrentes, selecciónelos en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Objetivos]**: número de perfiles de usuario que se califican como perfiles de destinatario.

* **[!UICONTROL Excluido]**: número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

* **[!UICONTROL Enviado]**: Número total de envíos para el mensaje SMS.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que han impedido su envío a los perfiles.

El **[!UICONTROL Rendimiento de SMS por fecha]** El widget detalla la información principal relativa al mensaje con un gráfico:

* **[!UICONTROL Enviado]**: Número total de envíos para sus mensajes SMS.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que han impedido su envío a los perfiles.

El **[!UICONTROL Razones de exclusión]** y **[!UICONTROL Razones de rechazos]** y **[!UICONTROL Motivos del error]** los gráficos y tablas permiten ver qué error y exclusiones se produjeron durante el proceso de envío.

El **[!UICONTROL SMS: clics por vínculos]** Los widgets detallan la información principal relativa a la participación de los visitantes en las direcciones URL.

+++

## Pestaña web {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_performance"
>title="Rendimiento web"
>abstract="Los KPI de rendimiento web proporcionan información completa sobre la participación de los visitantes en las experiencias web."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_summary"
>title="Resumen web"
>abstract="El gráfico Resumen web ilustra la progresión de las experiencias web, incluidas las impresiones, las impresiones únicas y las interacciones, durante el período especificado."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_interactions"
>title="Interacciones por elemento"
>abstract="La tabla Interacciones por elemento proporciona información clave sobre la participación de los visitantes en diferentes elementos de las páginas web."

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL Web]** La pestaña detalla la información principal relativa a sus páginas web.

![](assets/web-report.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe web.

El **[!UICONTROL Rendimiento web]** Los KPI detallan la información principal relativa a la participación de los visitantes en las experiencias web, como:

* **[!UICONTROL Impresiones únicas]**: número de usuarios únicos a los que se ha entregado la experiencia web.

* **[!UICONTROL Impresiones]**: número total de experiencias web entregadas a todos los usuarios.

* **[!UICONTROL Tasa de interacción]**: porcentaje de interacciones con la página web. Esto incluye cualquier acción realizada por los usuarios, como clics o cualquier otra interacción.

El **[!UICONTROL Resumen web]** Este gráfico muestra la evolución de las experiencias web (impresiones, impresiones únicas e interacciones) durante el periodo correspondiente.

El **[!UICONTROL Interacciones por elemento]** La tabla detalla la información principal relativa a la participación de los visitantes en los distintos elementos de las páginas web.
+++

## Pestaña de correo directo {#direct-mail-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_sending_statistics"
>title="Correo directo: estadísticas del envío"
>abstract="La tabla Estadísticas del envío de correo directo resume los datos esenciales sobre sus mensajes de correo directo, como los mensajes segmentados o enviados."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_error_reasons"
>title="Correo directo: motivos de error"
>abstract="Los gráficos y la tabla Correo directo: motivos de error le permiten identificar los errores específicos que se produjeron durante el envío."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_excluded_reasons"
>title="Correo directo: motivos excluidos"
>abstract="Los gráficos y la tabla Motivos excluidos del correo directo ilustran los distintos factores que llevaron a que los perfiles de usuario, excluidos del público destinatario, no recibieran el mensaje."

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL Correo directo]** Esta pestaña detalla la información principal relativa a sus envíos de correo directo.

![](assets/direct-mail-report_1.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe Correo directo.

El **[!UICONTROL Correo directo: estadísticas de envío]** Esta tabla detalla el éxito de su correo postal:

* **[!UICONTROL Tiempo de ejecución]**: Hora de inicio de cada ejecución del correo postal recurrente. Para dirigirse solo a uno o varios correos postales recurrentes, selecciónelos en la **[!UICONTROL Tiempo de ejecución]** menú desplegable.

* **[!UICONTROL Objetivos]**: número de perfiles de usuario que se califican como perfiles de destinatario para este correo postal.

* **[!UICONTROL Enviado]**: Número total de envíos para este correo postal.

* **[!UICONTROL Errores]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.

* **[!UICONTROL Excluido]**: número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron su correo postal.

El **[!UICONTROL Correo directo: razones de exclusión]** y **[!UICONTROL Correo directo: razones de error]** los gráficos y tablas permiten ver qué error y exclusiones se produjeron durante el proceso de envío.
+++

## Recursos adicionales

* [Introducción a las campañas](../campaigns/get-started-with-campaigns.md)
* [Creación de una campaña](../campaigns/create-campaign.md)
* [Creación de campañas activadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificación o detención de una campaña](../campaigns/modify-stop-campaign.md)
* [Informe en vivo de la campaña](campaign-live-report.md)
