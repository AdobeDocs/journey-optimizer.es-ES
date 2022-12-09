---
solution: Journey Optimizer
product: journey optimizer
title: Informe de Journey live
description: Aprenda a utilizar los datos del informe de recorrido en directo
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# Informe de Journey live {#journey-live-report}

Se puede acceder al informe de recorrido en directo directamente desde el recorrido con el **[!UICONTROL View report]** botón.

![](assets/report_journey.png)

El recorrido **[!UICONTROL Live report]** se muestra con las siguientes pestañas:

* [Recorrido](#journey-live)
* [Correo electrónico](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)

El recorrido **[!UICONTROL Live report]** se divide en distintas utilidades que detallan el éxito y los errores del recorrido. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](live-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](live-report.md#list-of-components-live).

## Pestaña Recorrido {#journey-live}

Desde su recorrido **[!UICONTROL Live report]**, el **[!UICONTROL Journey]** le proporciona una vista clara de los datos de seguimiento más importantes sobre su recorrido.

![](assets/journey_live_1.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe Recorrido.

**[!UICONTROL Journey Performance]** le permite ver la ruta de sus perfiles de destino paso a paso a través de su recorrido.

La variable **[!UICONTROL Journey Statistics]** muestra los siguientes KPI:

* **[!UICONTROL Entered profiles]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Exited profiles]**: Número total de personas que abandonaron el recorrido.

* **[!UICONTROL Failed individual journeys]**: Número total de recorridos individuales que no se ejecutaron correctamente.

La variable **[!UICONTROL Event executed over the last 24 hours]** y **[!UICONTROL Events]** las utilidades permiten ver cuál de los eventos se ejecutó correctamente mediante el número de resumen, el gráfico y la tabla.

La variable **[!UICONTROL Action executed over the last 24 hours]** y **[!UICONTROL Actions executed and errors]** las utilidades representan la acción más exitosa y los errores que se produjeron cuando se activaron las acciones. Los números del gráfico de acción, la tabla y el resumen contienen los datos disponibles para acciones como:

* **[!UICONTROL Actions executed]**: Número total de acciones ejecutadas correctamente para un recorrido.

* **[!UICONTROL Error in actions]**: Número total de errores que se produjeron en las acciones.
+++

## Ficha Correo electrónico {#email-live}

Desde su recorrido **[!UICONTROL Live report]**, el **[!UICONTROL Email]** pestaña detalla la información principal relativa a las entregas de correo electrónico realizadas en el recorrido.

![](assets/journey_live_2.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe Correo electrónico .

La variable **[!UICONTROL Email Sending Statistics]** La utilidad detalla la información principal relativa al mensaje:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Sending metrics by Email]** tabla y **[!UICONTROL Email Summary]** graph detalla el éxito de la entrega:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en una entrega.

* **[!UICONTROL Unsubscribe]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Spam complaints]**: Número de veces que un mensaje se declaró como correo no deseado o no deseado.

La variable **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** y **[!UICONTROL Hard and bounce - by Email]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Hard bounce]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Soft bounce]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignored]**: El número total de mensajes temporales, como fuera de la oficina o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

La variable **[!UICONTROL Error Reasons]** y **[!UICONTROL Exclude Reasons]** los gráficos y las tablas permiten ver qué error y exclusiones se produjeron durante el envío.

La variable **[!UICONTROL Email - Top recipient domain]** gráfico y tabla detallan qué dominios son los más utilizados por los destinatarios para abrir el correo electrónico.

>[!NOTE]
>
>Las métricas y las utilidades de Ofertas solo están disponibles si se ha insertado una decisión en un mensaje de correo electrónico. Para obtener más información sobre la gestión de decisiones, consulte esta [página](../offers/get-started/starting-offer-decisioning.md).

La variable **[!UICONTROL Offers statistic]** y **[!UICONTROL Offers statistics]** a lo largo del tiempo, los widgets miden el éxito y el impacto de su oferta en la audiencia de destino. Detalla la información principal relativa al mensaje con KPI:

* **[!UICONTROL Offer sent]**: Número total de envíos para la oferta.

* **[!UICONTROL Offer impression]**: Número de veces que la oferta se abrió en una entrega.

* **[!UICONTROL Offer clicks]**: Número de veces que se hizo clic en una oferta en una entrega.
+++

## Pestaña de notificaciones push {#push-live}

Desde su recorrido **[!UICONTROL Live report]**, el **[!UICONTROL Push notification]** La pestaña detalla la información principal relativa a los envíos push realizados en el recorrido.

![](assets/journey_live_3.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe push.

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** y **[!UICONTROL Sending metrics - by Push]** widgets detalla la información principal relativa a su mensaje:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Actions]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

* **[!UICONTROL Engagements]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

La variable **[!UICONTROL Error Reasons]** y **[!UICONTROL Exclude Reasons]** los gráficos y las tablas permiten ver qué error y exclusiones se produjeron durante el envío.

La variable **[!UICONTROL Sending statistics - Failed]** permite ver cuántos errores y rechazos se han producido.

La variable **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** y **[!UICONTROL Breakdown by platform]** gráficos y tablas detallan el éxito de la notificación push en función del sistema operativo.
+++

## Ficha SMS {#sms-live}

![](assets/journey_live_4.png)

+++Obtenga más información sobre las distintas métricas y utilidades disponibles para el informe SMS.

La variable **[!UICONTROL SMS - Sending statistics]** La tabla detalla el éxito de la entrega:

* **[!UICONTROL Targeted]**: Número de perfiles de usuario que se califican como perfiles de destinatario para este envío.

* **[!UICONTROL Excluded]**: Número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en una entrega.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL SMS Summary]** graph detalla el éxito de la entrega:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de la devolución.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La variable **[!UICONTROL Exclude Reasons]** los gráficos y las tablas permiten ver qué error y exclusiones se produjeron durante el envío.
+++
