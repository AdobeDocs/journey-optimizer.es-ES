---
title: Informe de recorrido en vivo
description: Aprenda a utilizar los datos del informe de recorrido en directo
feature: Informes
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: dc858fb29a9059c11fd4d3ab77954d4dac2097c3
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 2%

---

# Informe de recorrido en vivo {#journey-live-report}

Se puede acceder al informe de recorrido en directo directamente desde el recorrido con el botón **[!UICONTROL Live report]** .

![](../assets/report_1.png)

La página recorrido **[!UICONTROL Live report]** se mostrará con las siguientes pestañas:

* [Recorrido](#journey-live)
* [Correo electrónico](#email-live)
* [Push](#push-live)

El recorrido **[!UICONTROL Live report]** se divide en distintas utilidades que detallan el éxito y los errores de su recorrido. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte esta [sección](live-report.md#modify-dashboard).

## pestaña recorrido {#journey-live}

Desde el recorrido **[!UICONTROL Live report]**, la pestaña **[!UICONTROL Journey]** le ofrece una vista clara de los datos de seguimiento más importantes sobre su recorrido.

![](../assets/report_journey_2.png)

**[!UICONTROL Journey`s performance]** le permite ver la ruta de sus perfiles de destino paso a paso a través de su recorrido.

El widget **[!UICONTROL Journey`s statistics]** muestra los siguientes KPI:

* **[!UICONTROL Entered profiles]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Exited profiles]**: Número total de personas que salieron del recorrido.

* **[!UICONTROL Failed individual journey]**: Número total de recorridos individuales que no se ejecutaron correctamente.

![](../assets/report_journey_3.png)

Las utilidades **[!UICONTROL Event executed over the last 24 hours]**, **[!UICONTROL Events executed]** y **[!UICONTROL Events]** permiten ver cuál de los eventos se ejecutó correctamente mediante el número de resumen, el gráfico y la tabla.

![](../assets/report_journey_4.png)

**[!UICONTROL Action executed over the last 24 hours]** Las  **[!UICONTROL Actions executed and errors]** utilidades y representan la acción y los errores más exitosos que se produjeron cuando se activaron las acciones. Los números del gráfico de acción, la tabla y el resumen contienen los datos disponibles para acciones como:

* **[!UICONTROL Actions successfully executed]**: Número total de acciones ejecutadas correctamente para un recorrido.

* **[!UICONTROL Error in action]**: Número total de errores que se produjeron en las acciones.

## Pestaña Correo electrónico {#email-live}

Desde el recorrido **[!UICONTROL Live report]**, la pestaña **[!UICONTROL Email]** detalla la información principal relativa a los envíos de correo electrónico enviados en el recorrido.

Para obtener un informe detallado sobre un envío de correo electrónico específico, consulte la sección [Email live report](email-live-report.md) .

![](../assets/report_email_1.png)

La utilidad **[!UICONTROL Email Sending Statistics]** detalla la información principal relativa a su mensaje:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

La tabla **[!UICONTROL Sending metrics by Email]** y el gráfico **[!UICONTROL Email Summary]** detallan el éxito del envío:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en una entrega.

* **[!UICONTROL Unsubscribe]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Spam complaints]**: Número de veces que un mensaje se declaró como correo no deseado o no deseado.

![](../assets/report_email_2.png)

Los widgets **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** y **[!UICONTROL Hard and bounce - by Email]** contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Hard bounce]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Soft bounce]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignored]**: El número total de mensajes temporales, como fuera de la oficina o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

El gráfico y la tabla **[!UICONTROL Error Reasons]** permiten ver qué error se produjo durante el envío.

## Pestaña push {#push-live}

Desde el recorrido **[!UICONTROL Live report]**, la pestaña **[!UICONTROL Push]** detalla la información principal relativa a los envíos push enviados en el recorrido.

Para obtener un informe detallado sobre un envío push específico, consulte la sección [Informe activo push](push-live-report.md) .

![](../assets/report_push_1.png)

**[!UICONTROL Push notification sending performance]**,  **[!UICONTROL Push notification summary]** y las  **[!UICONTROL Sending metrics - by Push]** utilidades detallan la información principal relativa al mensaje:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Actions]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

* **[!UICONTROL Engagements]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

El gráfico y la tabla **[!UICONTROL Error Reasons]** permiten ver qué error se produjo durante el envío.

![](../assets/report_push_2.png)

Los gráficos y tablas **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** y **[!UICONTROL Breakdown by platform]** detallan el éxito de la notificación push en función del sistema operativo.

La utilidad **[!UICONTROL Sending statistics - Failed]** permite ver cuántos errores y rechazos se produjeron.
