---
solution: Journey Optimizer
product: journey optimizer
title: Informe global de campaña
description: Aprenda a utilizar los datos del informe Campaign Global
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1468'
ht-degree: 0%

---

# Informe global de campaña {#campaign-global-report}

Se puede acceder al informe global de campaña directamente desde la campaña con la variable **[!UICONTROL All time]** botón.

![](assets/campaign_report_global_5.png)

La campaña **[!UICONTROL Global report]** se muestra con las siguientes pestañas:

* [Campaign](#campaign-global)
* [Correo electrónico](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)

La campaña **[!UICONTROL Global report]** se divide en distintas utilidades que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](../reports/global-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global.md)

## Pestaña Campaña {#campaign-global}

### Entrega {#delivery-global}

![](assets/campaign_report_global_1.png)

La variable **[!UICONTROL Campaign's Statistics]** La utilidad detalla la información principal relativa a la campaña:

* **[!UICONTROL Entered profiles]**: Número de perfiles que iniciaron el recorrido.

* **[!UICONTROL Actions delivered]**: Número total de veces que se ha entregado una acción en el recorrido.

* **[!UICONTROL Actions failed in %]**: Número total de veces únicas que una acción ha fallado en el recorrido en comparación con la cantidad total de veces que se ha entregado una acción.

## Ficha Correo electrónico {#email-global}

![](assets/campaign_report_global_2.png)

Desde la campaña **[!UICONTROL Global report]**, el **[!UICONTROL Email]** La pestaña detalla la información principal relativa a los envíos de correo electrónico realizados en la campaña.

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe Correo electrónico .

La variable **[!UICONTROL Email Sending Statistics]** graph detalla el éxito de la entrega:

* **[!UICONTROL Targeted]**: Número total de mensajes procesados durante el análisis de envío.

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
>La variable **[!UICONTROL Optimized vs non optimized]** y **[!UICONTROL Send time optimization]**  las utilidades solo están disponibles si la opción de optimización del tiempo de envío está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

La variable **[!UICONTROL Optimized vs non optimized]** graph detalla la información principal relativa al mensaje, independientemente de si están optimizados o no:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.
* **[!UICONTROL Opens]**: Número de veces que se abrió la entrega en una entrega.
* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

La variable **[!UICONTROL Send time optimization]** detalla el éxito de la entrega en función del método de envío: optimizado o normal.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.
* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.
+++

## Pestaña de notificaciones push {#push-global}

Desde la campaña **[!UICONTROL Global report]**, el **[!UICONTROL Push notification]** detalla la información principal relativa a los envíos push realizados en la campaña.

![](assets/campaign_report_global_3.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe push.

La variable **[!UICONTROL Push notification - Sending statistics]** la tabla detalla la información principal relativa a las notificaciones push con gráficos y KPI:

* **[!UICONTROL Targeted]**: Número total de mensajes procesados durante el análisis de envío.

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
>La variable **[!UICONTROL Optimized vs non optimized]** y **[!UICONTROL Send time optimization]**  las utilidades solo están disponibles si la opción de optimización del tiempo de envío está activada para la entrega. Para obtener más información sobre la optimización del tiempo de envío, consulte [esta página](../building-journeys/journeys-message.md#send-time-optimization).

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
+++

## Ficha SMS {#sms-global}

Desde la campaña **[!UICONTROL Global report]**, el **[!UICONTROL SMS]** La pestaña detalla la información principal relativa a los envíos SMS enviados en la campaña.

![](assets/campaign_report_global_4.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe SMS.

La variable **[!UICONTROL SMS - Sending statistics]** La tabla detalla el éxito de la entrega:

* **[!UICONTROL Targeted]**: Número de perfiles de usuario que se califican como perfiles de destinatario para este envío.

* **[!UICONTROL Excluded]**: Número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL SMS Performance by date]** La utilidad detalla la información principal relativa al mensaje con un gráfico:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** y **[!UICONTROL Error Reasons]** los gráficos y las tablas permiten ver qué error y exclusiones se produjeron durante el envío.
+++

## Recursos adicionales

* [Introducción a las campañas](../campaigns/get-started-with-campaigns.md)
* [Creación de una campaña](../campaigns/create-campaign.md)
* [Creación de campañas activadas por API](../campaigns/api-triggered-campaigns.md)
* [Modificar o detener una campaña](../campaigns/modify-stop-campaign.md)
* [Informe de campaña en directo](campaign-live-report.md)
