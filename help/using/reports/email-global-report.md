---
title: Informe global de correo electrónico
description: Aprenda a utilizar los datos del informe global de correo electrónico
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 2bead395-082a-4fea-ad10-b2b2c5f484e9
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 1%

---

# Informe global de correo electrónico {#email-global-report}

El correo electrónico **[!UICONTROL Global report]** solo segmenta un envío de correo electrónico específico.

En el **[!UICONTROL Executions]** de la pestaña **[!UICONTROL Messages]** seleccione **[!UICONTROL Global view]** a continuación, en el menú avanzado del envío seleccionado, seleccione **[!UICONTROL Global report]**.

![](assets/global_report_3.png)

El correo electrónico **[!UICONTROL Global report]** se divide en distintas utilidades que detallan el éxito y los errores de su envío. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](global-report.md#modify-dashboard).

![](assets/global_report_4.png)

**[!UICONTROL Email performance]** detalla la información principal relativa a su mensaje con KPI:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivery Rate]**: Porcentaje de mensajes enviados correctamente.

* **[!UICONTROL Bounce Rate]**: Porcentaje de correos electrónicos devueltos en comparación con los correos electrónicos enviados.

* **[!UICONTROL Error Rate]**: Porcentaje de errores que se produjeron durante una entrega que impiden que se envíe en comparación con los correos electrónicos enviados.

* **[!UICONTROL Open Rate]**: Porcentaje de mensajes abiertos.

* **[!UICONTROL Click Rate]**: Porcentaje de clics en una entrega.

* **[!UICONTROL Spam Complaint Rate]**: Porcentaje de correos electrónicos marcados como correo no deseado por los destinatarios comparados con los mensajes enviados. Para obtener más información sobre las quejas, consulte la [Guía de prácticas recomendadas sobre la capacidad de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

* **[!UICONTROL Unsubscribe Rate]**: Porcentaje de bajas únicas en comparación con el número de mensajes enviados. Este indicador no se basa en el número de clics en el vínculo de baja de suscripción, sino en el número de bajas de suscripción iniciadas por los destinatarios. Obtenga más información sobre las bajas de suscripción en esta [página](../messages/consent.md).

La variable **[!UICONTROL Email - Tracking statistics]** contiene los datos disponibles para la actividad de destinatario para su envío:

* **[!UICONTROL Opens]**: Número de veces que se abrió la entrega en una entrega.

* **[!UICONTROL Unique Opens]**: Porcentaje de envíos abiertos.

* **[!UICONTROL Open Rate]**: Número total de correos electrónicos abiertos comparados con el número de correos electrónicos enviados.

* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en un correo electrónico.

* **[!UICONTROL Unique Clicks]**: número de destinatarios que hicieron clic en un contenido en un correo electrónico.

* **[!UICONTROL Click through rate]**: Porcentaje de usuarios que interactuaron con el recorrido.

La variable **[!UICONTROL Sending Statistics]** graph detalla el éxito de la entrega:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

![](assets/global_report_5.png)

La variable **[!UICONTROL Bounce Reasons]** y **[!UICONTROL Bounce categories]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Hard bounce]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Soft bounce]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignored]**: Número total de mensajes temporales, como fuera de la oficina, o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

Para obtener más información sobre las devoluciones, consulte la sección [Lista de supresión](../messages/suppression-list.md) página.

La variable **[!UICONTROL Error Reasons]** El gráfico y la tabla permiten ver qué error se produjo durante el envío.

![](assets/global_report_6.png)

La variable **[!UICONTROL Email - Top recipient domain]** gráfico y tabla detallan qué dominios son los más utilizados por los destinatarios para abrir el correo electrónico.

La variable **[!UICONTROL Email - Top Url]** gráfico y tabla detallan las direcciones URL de su envío que son las más visitadas.

La variable **[!UICONTROL Open vs Click]** identifica la interacción de los destinatarios con la entrega:

* **[!UICONTROL Unique Clicks]**: número de destinatarios que hicieron clic en un contenido en un correo electrónico.

* **[!UICONTROL Unique Opens]**: Número de destinatarios que abrieron la entrega.

<!--
![](assets/global_report_20.png)

>[!NOTE]
>
>The Offers widgets and metrics are only available if a decision was inserted in an email. For more information on Decision Management, refer to this [page](../offers/get-started/starting-offer-decisioning.md).

The **[!UICONTROL Offers statistic]** and **[!UICONTROL Offers statistics]** over time widgets measure your offer's success and impact on your targeted audience. It detail the main information relative to your message with KPIs:

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression]**: Number of times the offer was opened in a delivery.

* **[!UICONTROL Offer clicks]**: Number of times an offer was clicked on in a delivery.

The **[!UICONTROL Offers detailed statistic]** table contains the available data for recipient activity with your offer:

* **[!UICONTROL Placement name]**: Name of your placement used to display your offer. For more information on placement, refer to this [page](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: Name of the offer added in the delivery. For more information on placement, refer to this [page](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Total number of sends for the offer.

* **[!UICONTROL Offer impression rate]**: Percentage of opened offers compared to the number of sent offers.

* **[!UICONTROL Offer click rate]**: Percentage of users who interacted with the offer.
-->
>[!NOTE]
>
>Los perfiles con **[!UICONTROL Suppressed]** o **[!UICONTROL Not allowed]** se excluyen durante el proceso de envío de mensajes. Por lo tanto, mientras que la variable **Informes de recorrido** mostrará estos perfiles como si se hubieran movido a través del recorrido ([Leer segmento](../building-journeys/read-segment.md) y [Mensaje](../building-journeys/journeys-message.md) actividades), **Informes de correo electrónico** no los incluirá en la variable **[!UICONTROL Sent]** las métricas tal y como están filtradas antes del envío por correo electrónico.
>
>Obtenga más información sobre [Lista de supresión](../messages/suppression-list.md) y [Lista de permitidos](../messages/allow-list.md). Para averiguar el motivo de todos los casos de exclusión, puede usar la variable [Servicio de consultas de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.
