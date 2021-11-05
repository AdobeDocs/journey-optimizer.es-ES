---
title: Informe en vivo por correo electrónico
description: Aprenda a utilizar los datos del informe en directo de correo electrónico
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 1ddfbf1a-3cd5-446a-b0fb-76b81b88c1b4
source-git-commit: f0e34e040dd0e0ba2fa8293f4290ab55e1781426
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 2%

---

# Informe en vivo por correo electrónico {#email-live-report}

El correo electrónico **[!UICONTROL Live report]** solo segmenta un envío de correo electrónico específico.

En el **[!UICONTROL Executions]** de la pestaña **[!UICONTROL Messages]** seleccione **[!UICONTROL Live view]** a continuación, en el menú avanzado del envío seleccionado, seleccione **[!UICONTROL Live report]**.

![](../assets/live_report.png)

El correo electrónico **[!UICONTROL Live report]** se divide en distintas utilidades que detallan el éxito y los errores de su envío. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](live-report.md#modify-dashboard).

![](../assets/live_report_5.png)

**[!UICONTROL Email performance]** y **[!UICONTROL Email summary]** widgets detalla la información principal relativa al mensaje con un gráfico y KPI:

* **[!UICONTROL Targeted]**: Número de perfiles de usuario que se califican como perfiles de destinatario para este envío.

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en una entrega.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Spam complaints]**: Número de mensajes clasificados como correo no deseado.

* **[!UICONTROL Unsubscriptions]**: Número de clics en el vínculo de baja de suscripción.

* **[!UICONTROL Excluded]**: Número de perfiles de usuario, excluidos de los perfiles de destino, que no recibieron el mensaje.

La variable **[!UICONTROL Sending Statistics]** La utilidad detalla el éxito de la entrega:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

![](../assets/live_report_6.png)

La variable **[!UICONTROL Error Reasons]** El gráfico y la tabla permiten ver qué error se produjo durante el envío.

La variable **[!UICONTROL Bounce Reasons]** y **[!UICONTROL Bounce categories]** los widgets contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Hard bounce]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Soft bounce]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignored]**: El número total de mensajes temporales, como fuera de la oficina o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

![](../assets/live_report_8.png)

>[!NOTE]
>
>Las métricas y las utilidades de Ofertas solo están disponibles si se ha insertado una decisión en un mensaje de correo electrónico. Para obtener más información sobre la gestión de decisiones, consulte esta [página](../offers/get-started/starting-offer-decisioning.md).

La variable **[!UICONTROL Offers statistic]** y **[!UICONTROL Offers statistics]** a lo largo del tiempo, los widgets miden el éxito y el impacto de su oferta en la audiencia de destino. Detalla la información principal relativa al mensaje con KPI:

* **[!UICONTROL Offer sent]**: Número total de envíos para la oferta.

* **[!UICONTROL Offer impression]**: Número de veces que la oferta se abrió en una entrega.

* **[!UICONTROL Offer clicks]**: Número de veces que se hizo clic en una oferta en una entrega.

>[!NOTE]
>
>Los perfiles con **[!UICONTROL Suppressed]** o **[!UICONTROL Not allowed]** se excluyen durante el proceso de envío de mensajes. Por lo tanto, mientras que la variable **Informes de recorrido** mostrará estos perfiles como si se hubieran movido a través del recorrido ([Leer segmento](../building-journeys/read-segment.md) y [Mensaje](../building-journeys/journeys-message.md) actividades), **Informes de correo electrónico** no los incluirá en la variable **[!UICONTROL Sent]** las métricas tal y como están filtradas antes del envío por correo electrónico.
>
>Obtenga más información sobre [Lista de supresión](../suppression-list.md) y [Lista de permitidos](../allow-list.md). Para averiguar el motivo de todos los casos de exclusión, puede usar la variable [Servicio de consultas de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.
