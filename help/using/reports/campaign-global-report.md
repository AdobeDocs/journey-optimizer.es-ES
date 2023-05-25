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
source-git-commit: c9941a800783b399b587b952c4191ce906b70552
workflow-type: tm+mt
source-wordcount: '2262'
ht-degree: 4%

---

# Informe global de la campaña {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Informe global de la campaña"
>abstract="El informe global de campaña permite medir el impacto de las campañas durante un período de tiempo seleccionado. El informe se divide en distintos widgets que detallan el éxito y los errores de la campaña. Cada tablero de informes se puede modificar cambiando el tamaño de los widgets o eliminándolos."

Se puede acceder al informe global de Campaign directamente desde la campaña con la variable **[!UICONTROL Ver informe]** botón.

![](assets/campaign_report_global_5.png)

La campaña **[!UICONTROL Informe global]** se mostrará con las siguientes pestañas:

* [Campaign](#campaign-global)
* [Correo electrónico](#email-global)
* [En la aplicación](#inapp-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [Web](#web-tab)

La campaña **[!UICONTROL Informe global]** se divide en diferentes widgets que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](../reports/global-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global.md)

## Pestaña Campaña {#campaign-global}

### envío {#delivery-global}

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
+++

Para profundizar en estos resultados y en cómo interpretarlos, consulte [esta página](../campaigns/get-started-experiment.md#interpret-results).

## Pestaña Correo electrónico {#email-global}

![](assets/campaign_report_global_2.png)

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL Correo electrónico]** Esta pestaña detalla la información principal relacionada con los envíos de correo electrónico realizados en Campaign.

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe de correo electrónico.

El **[!UICONTROL Estadísticas de envío de correo electrónico]** el gráfico detalla el éxito de su envío:

* **[!UICONTROL Objetivos]**: Número total de mensajes procesados durante el análisis de envío.

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de entrega]**: porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de devoluciones]**: porcentaje de correos electrónicos que rebotaron en comparación con los enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

* **[!UICONTROL Tasa de error]**: porcentaje de errores que se han producido durante una entrega para evitar que se envíe en comparación con los correos electrónicos enviados.

* **[!UICONTROL Reintentos]**: Número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Excluido]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

El **[!UICONTROL Correo electrónico: estadísticas de seguimiento]** widget contiene los datos disponibles para la actividad de destinatario del envío:

* **[!UICONTROL Aperturas]**: Número de veces que se abrió la entrega en una entrega.

* **[!UICONTROL Aperturas únicas]**: porcentaje de envíos abiertos.

* **[!UICONTROL Tasa de apertura]**: Número total de correos electrónicos abiertos en comparación con el número de correos electrónicos enviados.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

* **[!UICONTROL Clics únicos]**: número de destinatarios que hicieron clic en un contenido de un correo electrónico.

* **[!UICONTROL Tasa de clics únicos]**: porcentaje de usuarios que interactuaron con el envío.

* **[!UICONTROL Baja de suscripciones]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Quejas de spam]**: Número de veces que un mensaje se declaró como correo no deseado.

El **[!UICONTROL Envío de estadísticas]** El gráfico contiene los datos disponibles para los correos electrónicos enviados, como:

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Reintentos]**: Número de correos electrónicos en cola para reintentos.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

El **[!UICONTROL Motivos del rechazo]** y **[!UICONTROL Categorías de rechazo]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Rechazo duro]**: el número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Rechazo suave]**: el número total de errores temporales, como una bandeja de entrada llena.

* **[!UICONTROL Ignorado]**: el número total de mensajes temporales, como Fuera de la oficina, o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

Para obtener más información sobre las devoluciones, consulte [Lista de supresión](../reports/suppression-list.md) página.

El **[!UICONTROL Motivos del error]** El gráfico y la tabla permiten ver qué error se produjo durante la entrega.

El **[!UICONTROL Razones de exclusión]** el gráfico y la tabla muestran los diferentes motivos que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran el mensaje.

El **[!UICONTROL Correo electrónico: URL principal]** Un gráfico y una tabla detallan qué direcciones URL del envío son las más visitadas.

El **[!UICONTROL Correo electrónico: dominio del destinatario principal]** el gráfico y la tabla detallan qué dominios son los más utilizados por los destinatarios para abrir el correo electrónico.

>[!NOTE]
>
>El **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]**  los widgets solo están disponibles si la opción Send-Time Optimization está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

El **[!UICONTROL Optimizado frente a no optimizado]** El gráfico detalla la información principal relativa al mensaje, estén optimizados o no:

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.
* **[!UICONTROL Aperturas]**: Número de veces que se abrió la entrega en una entrega.
* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

El **[!UICONTROL Optimización del tiempo de envío]** detalla el éxito de su envío según el método de envío: optimizado o normal.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.
* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.
+++

## Pestaña en la aplicación {#inapp-global}

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL En la aplicación]** Esta pestaña detalla la información principal relativa a las entregas en la aplicación enviadas en la campaña.

![](assets/campaign_report_global_6.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe en la aplicación.

El **[!UICONTROL Rendimiento en la aplicación]** Los KPI detallan la información principal relativa a la participación de los visitantes en los mensajes en la aplicación, como:

* **[!UICONTROL Impresiones únicas]**: número de usuarios únicos a los que se entregó el mensaje en la aplicación.

* **[!UICONTROL Impresiones]**: número total de mensajes en la aplicación entregados a todos los usuarios.

* **[!UICONTROL Tasa de clics]**: porcentaje de usuarios que interactuaron con los botones incluidos en el mensaje en la aplicación comparado con los usuarios que vieron el mensaje.

* **[!UICONTROL Tasa de descarte]**: porcentaje de mensajes en la aplicación que los destinatarios descartaron.

El **[!UICONTROL Resumen en la aplicación]** Este gráfico muestra la evolución de las impresiones en la aplicación durante el periodo correspondiente.

El **[!UICONTROL Clics por botón]** el gráfico y la tabla contienen los datos disponibles sobre el comportamiento del destinatario por botón:

* **[!UICONTROL Clics]**: número total de destinatarios que interactuaron con los botones incluidos en el mensaje en la aplicación.

* **[!UICONTROL Tasa de clics]**: porcentaje de usuarios que interactuaron con los botones incluidos en el mensaje en la aplicación comparado con los usuarios que vieron el mensaje.
+++

## Pestaña de notificaciones push {#push-global}

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL Notificación push]** Esta pestaña detalla la información principal relativa a las entregas push enviadas en la campaña.

![](assets/campaign_report_global_3.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe push.

El **[!UICONTROL Notificación push: estadísticas de envío]** Esta tabla detalla la información principal relativa a las notificaciones push con gráficos y KPI:

* **[!UICONTROL Objetivos]**: Número total de mensajes procesados durante el análisis de envío.

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de entrega]**: porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Tasa de devoluciones]**: porcentaje de notificaciones push que rebotaron en comparación con las notificaciones push enviadas.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

* **[!UICONTROL Tasa de error]**: porcentaje de errores que se produjeron durante una entrega y que impiden su envío en comparación con las notificaciones push enviadas.

* **[!UICONTROL Excluido]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

El **[!UICONTROL Push: estadísticas de seguimiento]** contiene los datos disponibles de la actividad del destinatario para la entrega:

* **[!UICONTROL Aperturas]**: Número de veces que se ha abierto un mensaje en una entrega.

* **[!UICONTROL Tasa de apertura]**: porcentaje de notificaciones push abiertas.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Participaciones]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

* **[!UICONTROL Tasa de participación]**: Porcentaje de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

El **[!UICONTROL Resumen de notificaciones push]** El gráfico contiene los datos disponibles para las notificaciones push enviadas, como:

* **[!UICONTROL Aperturas]**: Número de veces que se ha abierto un mensaje en una entrega.

* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

>[!NOTE]
>
>El **[!UICONTROL Optimizado frente a no optimizado]** y **[!UICONTROL Optimización del tiempo de envío]**  los widgets solo están disponibles si la opción Send-Time Optimization está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

El **[!UICONTROL Optimizado frente a no optimizado]** El gráfico detalla la información principal relativa al mensaje, estén optimizados o no:

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.
* **[!UICONTROL Aperturas]**: Número de veces que se abrió la entrega en una entrega.
* **[!UICONTROL Acciones]**: Número total de acciones en la notificación push entregada, por ejemplo, clic en el botón o despido.

El **[!UICONTROL Optimización del tiempo de envío]** detalla el éxito de su envío según el método de envío: optimizado o normal.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.
* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

El **[!UICONTROL Motivos del error]** El gráfico y la tabla permiten ver qué error se produjo durante la entrega.

El **[!UICONTROL Razones de exclusión]** el gráfico y la tabla muestran los diferentes motivos que impidieron que los perfiles de usuario, excluidos de los perfiles de destino, recibieran el mensaje.

El **[!UICONTROL Seguimiento por plataforma]**, **[!UICONTROL Envío por plataforma]** y **[!UICONTROL Desglose por plataforma]** los gráficos y tablas detallan el éxito de la notificación push según el sistema operativo del destinatario.
+++

## Pestaña SMS {#sms-global}

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL SMS]** Esta pestaña detalla la información principal relativa a los envíos SMS enviados en la campaña.

![](assets/campaign_report_global_4.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe SMS.

El **[!UICONTROL SMS: estadísticas de envío]** La tabla detalla el éxito de su envío:

* **[!UICONTROL Objetivos]**: número de perfiles de usuario que se califican como perfiles de destinatario para este envío.

* **[!UICONTROL Excluido]**: número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

El **[!UICONTROL Rendimiento de SMS por fecha]** El widget detalla la información principal relativa al mensaje con un gráfico:

* **[!UICONTROL Enviado]**: Número total de envíos para el envío.

* **[!UICONTROL Entregado]**: Número de mensajes enviados correctamente en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores]**: Número total de errores que se han producido durante una entrega para evitar que se envíe a los perfiles.

El **[!UICONTROL Razones de exclusión]**, **[!UICONTROL Razones de rechazos]** y **[!UICONTROL Motivos del error]** los gráficos y tablas permiten ver qué error y exclusiones se produjeron durante la entrega.

El **[!UICONTROL SMS: clics por vínculos]** y **[!UICONTROL SMS: estadísticas de seguimiento]** los widgets detallan la información principal relativa a la participación de los visitantes con las direcciones URL.

+++

## Pestaña web {#web-tab}

Desde la campaña **[!UICONTROL Informe global]**, el **[!UICONTROL Web]** La pestaña detalla la información principal relativa a sus páginas web.

![](assets/web-report.png)

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe web.

El **[!UICONTROL Rendimiento web]** Los KPI detallan la información principal relativa a la participación de los visitantes en las experiencias web, como:

* **[!UICONTROL Impresiones únicas]**: número de usuarios únicos a los que se ha entregado la experiencia web.

* **[!UICONTROL Impresiones]**: número total de experiencias web entregadas a todos los usuarios.

* **[!UICONTROL Tasa de clics]**: porcentaje de visitantes que interactuaron con los distintos elementos de las páginas web.

El **[!UICONTROL Resumen web]** Este gráfico muestra la evolución de las experiencias web (impresiones, impresiones únicas y clics) durante el periodo correspondiente.

El **[!UICONTROL Clics por elemento]** La tabla detalla la información principal relativa a la participación de los visitantes en los distintos elementos de las páginas web.
+++

## Recursos adicionales

* [Introducción a las campañas](../campaigns/get-started-with-campaigns.md)
* [Creación de una campaña](../campaigns/create-campaign.md)
* [Creación de campañas activadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificación o detención de una campaña](../campaigns/modify-stop-campaign.md)
* [Informe en directo de la campaña](campaign-live-report.md)
