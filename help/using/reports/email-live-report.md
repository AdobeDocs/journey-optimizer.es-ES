---
title: Informe en vivo por correo electrónico
description: Aprenda a utilizar los datos del informe en directo de correo electrónico
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: c54e4443c0a8b6c2e427fa007adf5d800b2ba3b5
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---

# Informe en vivo por correo electrónico {#email-live-report}

El correo electrónico **[!UICONTROL Live report]** solo se dirige a un envío de correo electrónico específico.

En la pestaña **[!UICONTROL Executions]** del menú **[!UICONTROL Messages]**, seleccione **[!UICONTROL Live view]** y, en el menú avanzado del envío seleccionado, seleccione **[!UICONTROL Live report]**.

![](../assets/live_report.png)

El correo electrónico **[!UICONTROL Live report]** se divide en distintas utilidades que detallan el éxito y los errores del envío. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte esta [sección](live-report.md#modify-dashboard).

![](../assets/live_report_5.png)

**[!UICONTROL Email performance]** y las  **[!UICONTROL Email summary]** utilidades detallan la información principal relativa al mensaje con un gráfico y KPI:

* **[!UICONTROL Sent]**: Número total de envíos para la entrega.

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

* **[!UICONTROL Opens]**: Número de veces que se abrió un mensaje en una entrega.

* **[!UICONTROL Clicks]**: Número de veces que se hizo clic en un contenido en una entrega.

El gráfico **[!UICONTROL Sending Statistics]** detalla el éxito de su envío:

* **[!UICONTROL Delivered]**: Número de mensajes enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Bounces]**: Total de errores acumulados durante la entrega y el procesamiento automático de devoluciones en relación con la cantidad total de mensajes enviados.

* **[!UICONTROL Errors]**: Número total de errores que se han producido durante una entrega que impiden que se envíe a perfiles.

![](../assets/live_report_6.png)

El gráfico y la tabla **[!UICONTROL Error Reasons]** permiten ver qué error se produjo durante el envío.

Los widgets **[!UICONTROL Bounce Reasons]** y **[!UICONTROL Bounce categories]** contienen los datos disponibles relacionados con los mensajes devueltos, como:

* **[!UICONTROL Hard bounce]**: El número total de errores permanentes, como una dirección de correo electrónico incorrecta. Esto implica un mensaje de error que indica explícitamente que la dirección no es válida, como Usuario desconocido.

* **[!UICONTROL Soft bounce]**: El número total de errores temporales, como una bandeja de entrada completa.

* **[!UICONTROL Ignored]**: El número total de mensajes temporales, como fuera de la oficina o un error técnico, por ejemplo, si el tipo de remitente es administrador de correo.

>[!NOTE]
>
>Los perfiles con estado **[!UICONTROL Suppressed]** o **[!UICONTROL Not allowed]** se excluyen durante el proceso de envío de mensajes. Por lo tanto, mientras que los **informes de Recorrido** mostrarán estos perfiles como si se hubieran movido a través del recorrido ([Leer segmento](../building-journeys/read-segment.md) y [Mensaje](../building-journeys/journeys-message.md)), los **Informes de correo electrónico** no los incluirán en las métricas **[!UICONTROL Sent]** ya que se filtrarán antes de enviarlos por correo electrónico.
>
>Obtenga más información sobre la [lista de supresión](../suppression-list.md) y la [Lista de permitidos](../allow-list.md). Para averiguar el motivo de todos los casos de exclusión, puede utilizar el [Servicio de consulta de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html).
