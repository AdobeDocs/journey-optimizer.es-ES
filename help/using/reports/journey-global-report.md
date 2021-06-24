---
title: Informe global de recorrido
description: Aprenda a utilizar los datos del informe global de recorrido
feature: Informes
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: c883930674b3856f1f7857f4072419be8c9d8738
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 1%

---

# Informe global de recorrido {#journey-global-report}

Se puede acceder al informe global de recorrido directamente desde el recorrido con el botón **[!UICONTROL Global report]** .

![](../assets/global_report_1.png)

La página recorrido **[!UICONTROL Global report]** se mostrará con las siguientes pestañas:

* [Recorrido](#journey-global)
* [Correo electrónico](#email-global)
* [Push](#push-global)

El recorrido **[!UICONTROL Global report]** se divide en distintas utilidades que detallan el éxito y los errores de su recorrido. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte esta [sección](global-report.md#modify-dashboard).

## ficha recorrido {#journey-global}

Desde el recorrido **[!UICONTROL Global report]**, la pestaña **[!UICONTROL Journey]** le ofrece una vista clara de los datos de seguimiento más importantes sobre su recorrido.

![](../assets/global_report_2.png)

La utilidad **[!UICONTROL Journey Performance]** permite ver la ruta de los perfiles de destino paso a paso a través del recorrido.

El widget **[!UICONTROL Journey Statistics]** muestra los siguientes KPI:

* **[!UICONTROL Entered profiles]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Exited profiles]**: Número total de personas que salieron del recorrido.

* **[!UICONTROL Failed individual journey]**: Número total de recorridos individuales que no se ejecutaron correctamente.

![](../assets/global_report_12.png)

Las utilidades **[!UICONTROL Events received by event]**, **[!UICONTROL Events by origin]** y **[!UICONTROL Top events]** permiten ver cuál de sus **[!UICONTROL Events]** se ejecutó correctamente mediante gráficos y tablas.

![](../assets/global_report_13.png)

**[!UICONTROL Action Performance]**,  **[!UICONTROL Action Error Reasons]** y las  **[!UICONTROL Top Actions]** utilidades representan la acción y los errores más exitosos que se produjeron cuando  **[!UICONTROL Actions]** se activó el .

La tabla **[!UICONTROL Top Actions]** contiene los datos disponibles para **[!UICONTROL Actions]**, como:

* **[!UICONTROL Actions successfully executed]**: Número total de  **[!UICONTROL Actions]** ejecutados correctamente para un recorrido.

* **[!UICONTROL Error in action]**: Número total de errores que se han producido para  **[!UICONTROL Actions]**.

## Ficha Correo electrónico {#email-global}

Desde el recorrido **[!UICONTROL Global report]**, la pestaña **[!UICONTROL Email]** detalla la información principal relativa a los envíos de correo electrónico enviados en el recorrido.

Para obtener un informe detallado sobre un envío de correo electrónico específico, consulte la sección [Email global report](#email-global-report) .

![](../assets/global_report_14.png)

El gráfico **[!UICONTROL Email Sending Statistics]** detalla el éxito de su envío:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Delivery Rate]**: Porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Bounce Rate]**: Porcentaje de correos electrónicos devueltos en comparación con los correos electrónicos enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Error Rate]**: Porcentaje de errores que se produjeron durante una entrega que impiden que se envíe en comparación con los correos electrónicos enviados.

El **[!UICONTROL Email - Tracking statistics]** contiene los datos disponibles para la actividad de destinatario para su envío:

* **[!UICONTROL Opens]**: Número de veces que se abrió la entrega en una entrega.

* **[!UICONTROL Unique Opens]**: Porcentaje de envíos abiertos.

* **[!UICONTROL Open Rate]**: Número total de correos electrónicos abiertos comparados con el número de correos electrónicos enviados.

* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

* **[!UICONTROL Unique Clicks]**: número de destinatarios que hicieron clic en un contenido en un correo electrónico.

* **[!UICONTROL Click through rate]**: Porcentaje de usuarios que interactuaron con el recorrido.

* **[!UICONTROL Unsubscribe]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Spam complaints]**: Número de veces que un mensaje se declaró como correo no deseado o no deseado.

El gráfico **[!UICONTROL Sending Statistics]** contiene los datos disponibles para los correos electrónicos enviados, como:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

![](../assets/global_report_15.png)

Los widgets **[!UICONTROL Bounce Reasons]** y **[!UICONTROL Bounce categories]** contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Hard bounce]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Soft bounce]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignored]**: El número total de mensajes temporales, como fuera de la oficina o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

Para obtener más información sobre las devoluciones, consulte la página [Lista de supresión](../suppression-list.md).

![](../assets/global_report_16.png)

El gráfico y la tabla **[!UICONTROL Email - Top Url]** detallan qué direcciones URL del envío son las más visitadas.

El gráfico y la tabla **[!UICONTROL Email - Top recipient domain]** detallan qué dominios son los más utilizados por los destinatarios para abrir el correo electrónico.

## Ficha Insertar {#push-global}

Desde el recorrido **[!UICONTROL Global report]**, la pestaña **[!UICONTROL Push]** detalla la información principal relativa a los envíos push enviados en el recorrido.

Para obtener un informe detallado sobre un envío push específico, consulte este [Informe global push](#push-global-report).

![](../assets/global_report_17.png)

La tabla **[!UICONTROL Push notification - Sending statistics]** detalla la información principal relativa a las notificaciones push con gráficos y KPI:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Delivery Rate]**: Porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Bounce Rate]**: Porcentaje de notificaciones push que rebotaron en comparación con las notificaciones push enviadas.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Error Rate]**: Porcentaje de errores que se produjeron durante una entrega que impiden que se envíe comparado con las notificaciones push enviadas.

El **[!UICONTROL Push - Tracking statistics]** contiene los datos disponibles para la actividad de destinatario para su envío:

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Open Rate]**: Porcentaje de notificaciones push abiertas.

* **[!UICONTROL Actions]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

* **[!UICONTROL Engagements]**: Número total de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

* **[!UICONTROL Engagement Rate]**: Porcentaje de aperturas y acciones para esta notificación push, es decir, si el perfil abrió la notificación push o si se hizo clic en un botón.

El gráfico **[!UICONTROL Push notification summary]** contiene los datos disponibles para las notificaciones push enviadas, como:

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Actions]**: Número total de acciones realizadas en la notificación push entregada, por ejemplo, hacer clic en un botón o rechazar una solicitud.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

![](../assets/global_report_18.png)

El gráfico y la tabla **[!UICONTROL Error Reasons]** permiten ver qué error se produjo durante el envío.

![](../assets/global_report_19.png)

Los gráficos y tablas **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** y **[!UICONTROL Breakdown by platform]** detallan el éxito de la notificación push en función del sistema operativo del destinatario.
