---
title: Informe global de correo electrónico
description: Aprenda a utilizar los datos del informe global de correo electrónico
feature: Informes
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 1%

---

# Informe global de correo electrónico {#email-global-report}

El correo electrónico **[!UICONTROL Global report]** solo se dirige a un envío de correo electrónico específico.

En la pestaña **[!UICONTROL Executions]** del menú **[!UICONTROL Messages]**, seleccione **[!UICONTROL Global view]** y, en el menú avanzado del envío seleccionado, seleccione **[!UICONTROL Global report]**.

![](../assets/global_report_3.png)

El correo electrónico **[!UICONTROL Global report]** se divide en distintas utilidades que detallan el éxito y los errores del envío. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte esta [sección](global-report.md#modify-dashboard).

![](../assets/global_report_4.png)

**[!UICONTROL Email performance]** detalla la información principal relativa a su mensaje con KPI:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivery Rate]**: Porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Bounce Rate]**: Porcentaje de correos electrónicos devueltos en comparación con los correos electrónicos enviados.

* **[!UICONTROL Error Rate]**: Porcentaje de errores que se produjeron durante una entrega que impiden que se envíe en comparación con los correos electrónicos enviados.

* **[!UICONTROL Open Rate]**: Porcentaje de mensajes abiertos.

* **[!UICONTROL Click Rate]**: Porcentaje de clics en una entrega.

* **[!UICONTROL Spam Complaint Rate]**: Porcentaje de correos electrónicos marcados como correo no deseado por los destinatarios comparados con los mensajes enviados. Para obtener más información sobre las quejas, consulte la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

* **[!UICONTROL Unsubscribe Rate]**: Porcentaje de bajas únicas en comparación con el número de mensajes enviados. Este indicador no se basa en el número de clics en el vínculo de baja de suscripción, sino en el número de bajas de suscripción iniciadas por los destinatarios. Obtenga más información sobre las bajas de suscripción en esta [página](../consent.md).

El **[!UICONTROL Email - Tracking statistics]** contiene los datos disponibles para la actividad de destinatario para su envío:

* **[!UICONTROL Opens]**: Número de veces que se abrió la entrega en una entrega.

* **[!UICONTROL Unique Opens]**: Porcentaje de envíos abiertos.

* **[!UICONTROL Open Rate]**: Número total de correos electrónicos abiertos comparados con el número de correos electrónicos enviados.

* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

* **[!UICONTROL Unique Clicks]**: número de destinatarios que hicieron clic en un contenido en un correo electrónico.

* **[!UICONTROL Click through rate]**: Porcentaje de usuarios que interactuaron con el recorrido.

El gráfico **[!UICONTROL Sending Statistics]** detalla el éxito de su envío:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

![](../assets/global_report_5.png)

Los widgets **[!UICONTROL Bounce Reasons]** y **[!UICONTROL Bounce categories]** contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Hard bounce]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Soft bounce]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignored]**: Número total de mensajes temporales, como fuera de la oficina, o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

Para obtener más información sobre las devoluciones, consulte la página [Lista de supresión](../suppression-list.md).

El gráfico y la tabla **[!UICONTROL Error Reasons]** permiten ver qué error se produjo durante el envío.

![](../assets/global_report_6.png)

El gráfico y la tabla **[!UICONTROL Email - Top recipient domain]** detallan qué dominios son los más utilizados por los destinatarios para abrir el correo electrónico.

El gráfico y la tabla **[!UICONTROL Email - Top Url]** detallan qué direcciones URL del envío son las más visitadas.

El **[!UICONTROL Open vs Click]** identifica la interacción de los destinatarios con el envío:

* **[!UICONTROL Unique Clicks]**: número de destinatarios que hicieron clic en un contenido en un correo electrónico.

* **[!UICONTROL Unique Opens]**: Número de destinatarios que abrieron la entrega.


