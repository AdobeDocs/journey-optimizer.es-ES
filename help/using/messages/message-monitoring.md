---
title: Monitorización de la ejecución de mensajes
description: Conozca las directrices de monitorización
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 950f8186-07f6-4cc1-936c-d0984fb0f988
source-git-commit: d9f7c64358be3c3355337ba0db12e5b8c17bba4c
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 1%

---

# Monitorización de mensajes {#monitor-message-execution}

Para asegurarse de que los mensajes se ejecutan, envían y envían correctamente, [!DNL Journey Optimizer] ofrece funciones para supervisar los mensajes que se publican y activan actualmente. Puede ver el rendimiento de sus mensajes en los distintos recorridos <!--and APIs--> en tiempo real desde el **[!UICONTROL Executions]** lista.

➡️ [Descubra esta función en vídeo](#video)

Para acceder a esta lista, vaya a la **[!DNL Journey Optimizer]** página principal, seleccione **[!UICONTROL Messages]** y haga clic en el botón **[!UICONTROL Executions]** pestaña .

Esta ficha proporciona dos vistas: **[!UICONTROL Live view]** y **[!UICONTROL Global view]**.

* La variable **[!UICONTROL Live view]** proporciona un **información general en tiempo real de todos los mensajes ejecutados** activado por uno o más [recorridos](../building-journeys/journey.md) **solo en las últimas 24 horas**.

   ![](assets/message-execution-tab-live.png)

   Esta lista se actualiza automáticamente cada sesenta segundos. Si no se ha producido ninguna ejecución en las últimas 24 horas para un mensaje específico, todas las columnas mostrarán valores nulos (0) para ese mensaje.

* La variable **[!UICONTROL Global view]** proporciona un **descripción general de todos los mensajes ejecutados** activado por uno o más [recorridos](../building-journeys/journey.md) **desde la fecha de inicio del mensaje**.

   ![](assets/message-execution-tab-global.png)

   Esta lista se actualiza automáticamente cada noventa minutos. Los datos se acumulan con el tiempo desde cada fecha de inicio de mensaje.

Si un recorrido publica un mensaje pero aún no lo ha activado, no aparece en ninguna de las pestañas. Solo se enumeran los siguientes elementos:
* Mensajes que se han activado, pero que aún no se han iniciado (pendientes).
* Mensajes que se han activado y que se están ejecutando (en curso).

>[!NOTE]
>
>Si se ha utilizado un mensaje en varios recorridos, se muestra una fila por recorrido para cada ejecución.

De forma predeterminada, los mensajes se muestran a partir de la fecha de ejecución más reciente. Haga clic en el **[!UICONTROL Filters]** para buscar en los mensajes según el canal, la fecha de inicio o la fecha de finalización. También puede elegir excluir los eventos de prueba de su **Lista de ejecuciones**.

![](assets/message-execution-tab-filters.png)

La variable <!--**[!UICONTROL Quick action]**-->la segunda columna permite abrir la [message](create-message.md) y para acceder al [Informe Activo](../reports/live-report.md) si está en el **[!UICONTROL Live view]** o [Informe global](../reports/global-report.md) si está en el **[!UICONTROL Global view]**.

![](assets/message-execution-open-live-report.png)

Para cada ejecución de mensaje, se muestran varios indicadores:

* **[!UICONTROL Message label]**: Título del mensaje que definió [creación del mensaje](create-message.md). El ID de ejecución, que se genera automáticamente, se muestra entre paréntesis.

   <!--**[!UICONTROL Execution ID]**: Automatically generated identifier.
  **[!UICONTROL Source]**: Name of the journey leveraging that message.-->

* **[!UICONTROL Journey - Version - Action]**: Nombre del recorrido que aprovecha el mensaje, la versión del recorrido y la etiqueta de la acción que aprovecha el mensaje en el recorrido.

* **[!UICONTROL Status]**: Estado de ejecución del mensaje.

* **[!UICONTROL Start date]**: Fecha y hora en que se ejecutó el mensaje desde el recorrido.

* **[!UICONTROL Targeted]**: Número de perfiles de destino para cada ejecución de mensaje.

* **[!UICONTROL Excluded]**: Número de perfiles que se han excluido del objetivo inicial debido a reglas de exclusión.

* **[!UICONTROL Sent]**: Número de mensajes que se han enviado.

* **[!UICONTROL Delivered]**: Número de mensajes entregados correctamente en el buzón del destinatario (correo electrónico) o en el dispositivo (push) sin generar un rechazo o ningún otro error de envío.

* **[!UICONTROL Bounces]**: Número de mensajes que no se pueden enviar debido a un error de entrega. [Más información sobre devoluciones](suppression-list.md).

* **[!UICONTROL Opens]**: Número de mensajes que se han abierto.

* **[!UICONTROL Clicks]**: Número de clics en los vínculos de un correo electrónico.

   >[!NOTE]
   >
   >Los clics no existen para las notificaciones push: cuando un usuario hace clic en una notificación push, abre la aplicación, que solo puede considerarse como una apertura.

* **[!UICONTROL Errors]**: Número de mensajes que no se pueden enviar debido a un error técnico.

* **[!UICONTROL Spam complaints]**: Número de mensajes marcados como correo no deseado por los destinatarios. Obtenga más información sobre las quejas en la [Guía de prácticas recomendadas sobre la capacidad de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

Puede elegir qué columnas mostrar en la tabla. Para ello, haga clic en el botón **[!UICONTROL Customize table]** en la parte superior de la pantalla y seleccione las columnas que desee mostrar.

![](assets/message-execution-customize-table.png)

En **Vista global** solo, puede elegir si desea mostrar los datos como números, porcentajes o ambos. Haga clic en el **Formato de datos** lista desplegable para alternar entre las tres opciones.

![](assets/message-execution-data-format.png)

Al hacer clic en cada hipervínculo, se abrirá la vista de resumen del mensaje correspondiente. [Más información sobre los mensajes](create-message.md).

## Vídeo explicativo {#video}

Obtenga más información sobre los informes en directo y globales, cómo acceder y analizar el Recorrido y los informes específicos de mensajes, y cómo modificar los tableros de informes.

>[!VIDEO](https://video.tv.adobe.com/v/334108?quality=12)
