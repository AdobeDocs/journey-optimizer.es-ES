---
title: Informe de recorrido en vivo
description: Aprenda a utilizar los datos del informe de recorrido en directo
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 8cb36038b2aeddd1662dcb7c84b36d9bc1265982
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 2%

---

# Informe de recorrido en vivo {#journey-live-report}

Se puede acceder al informe de recorrido en directo directamente desde el recorrido con la variable **[!UICONTROL Live report]** botón.

![](../assets/report_1.png)

El recorrido **[!UICONTROL Live report]** se muestra con las siguientes pestañas:

* [Recorrido](#journey-live)
* [Correo electrónico](#email-live)
* [Push](#push-live)

El recorrido **[!UICONTROL Live report]** se divide en distintas utilidades que detallan el éxito y los errores de su recorrido. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](live-report.md#modify-dashboard).

## ficha recorrido {#journey-live}

Desde su recorrido **[!UICONTROL Live report]**, el **[!UICONTROL Journey]** le proporciona una vista clara de los datos de seguimiento más importantes sobre su recorrido.

![](../assets/report_journey_2.png)

**[!UICONTROL Journey Performance]** le permite ver la ruta de sus perfiles de destino paso a paso a través de su recorrido.

La variable **[!UICONTROL Journey Statistics]** muestra los siguientes KPI:

* **[!UICONTROL Entered profiles]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Exited profiles]**: Número total de personas que salieron del recorrido.

* **[!UICONTROL Failed individual journeys]**: Número total de recorridos individuales que no se ejecutaron correctamente.

![](../assets/report_journey_3.png)

La variable **[!UICONTROL Event executed over the last 24 hours]** y **[!UICONTROL Events]** las utilidades permiten ver cuál de los eventos se ejecutó correctamente mediante el número de resumen, el gráfico y la tabla.

![](../assets/report_journey_4.png)

La variable **[!UICONTROL Action executed over the last 24 hours]** y **[!UICONTROL Actions executed and errors]** las utilidades representan la acción más exitosa y los errores que se produjeron cuando se activaron las acciones. Los números del gráfico de acción, la tabla y el resumen contienen los datos disponibles para acciones como:

* **[!UICONTROL Actions executed]**: Número total de acciones ejecutadas correctamente para un recorrido.

* **[!UICONTROL Error in actions]**: Número total de errores que se produjeron en las acciones.

<!--
![](../assets/live_report_7.png)

>[!NOTE]
>
>The Offers widgets and metrics are only available if a decision was inserted in an email. For more information on Decision Management, refer to this [page](../offers/get-started/starting-offer-decisioning.md).

The **[!UICONTROL Offers statistic]** and **[!UICONTROL Offers statistics]** over time widgets measure your offer's success and impact on your targeted audience. It detail the main information relative to your message with KPIs:

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression]**: Number of times the offer was opened in a delivery.

* **[!UICONTROL Offer clicks]**: Number of times an offer was clicked on in a delivery.
-->

## Ficha Correo electrónico {#email-live}

Desde su recorrido **[!UICONTROL Live report]**, el **[!UICONTROL Email]** La pestaña detalla la información principal relativa a los envíos de correo electrónico realizados en el recorrido.

Para obtener un informe detallado sobre un envío de correo electrónico específico, consulte la [Enviar informe activo por correo electrónico](email-live-report.md) para obtener más información.

![](../assets/report_email_1.png)

La variable **[!UICONTROL Email Sending Statistics]** La utilidad detalla la información principal relativa al mensaje:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Sending metrics by Email]** tabla y **[!UICONTROL Email Summary]** graph detalla el éxito de la entrega:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en una entrega.

* **[!UICONTROL Unsubscribe]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Spam complaints]**: Número de veces que un mensaje se declaró como correo no deseado o no deseado.

![](../assets/report_email_2.png)

La variable **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** y **[!UICONTROL Hard and bounce - by Email]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Hard bounce]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Soft bounce]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignored]**: El número total de mensajes temporales, como fuera de la oficina o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

La variable **[!UICONTROL Error Reasons]** El gráfico y la tabla permiten ver qué error se produjo durante el envío.

## Ficha Insertar {#push-live}

Desde su recorrido **[!UICONTROL Live report]**, el **[!UICONTROL Push]** detalla la información principal relativa a los envíos push realizados en el recorrido.

Para obtener un informe detallado sobre una entrega push específica, consulte la [Insertar informe activo](push-live-report.md) para obtener más información.

![](../assets/report_push_1.png)

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** y **[!UICONTROL Sending metrics - by Push]** widgets detalla la información principal relativa a su mensaje:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Actions]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

* **[!UICONTROL Engagements]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

La variable **[!UICONTROL Error Reasons]** El gráfico y la tabla permiten ver qué error se produjo durante el envío.

![](../assets/report_push_2.png)

La variable **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** y **[!UICONTROL Breakdown by platform]** gráficos y tablas detallan el éxito de la notificación push en función del sistema operativo.

La variable **[!UICONTROL Sending statistics - Failed]** permite ver cuántos errores y rechazos se han producido.
