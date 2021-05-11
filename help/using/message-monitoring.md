---
title: Monitorización de la ejecución de mensajes
description: Conozca las directrices de monitorización
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Monitorización de mensajes {#monitor-message-execution}

![](assets/do-not-localize/badge.png)

Para asegurarse de que los mensajes se ejecutan, envían y envían correctamente, [!DNL Journey Optimizer] ofrece capacidades para supervisar los mensajes que se publican y activan actualmente. Puede ver el rendimiento de sus mensajes en recorridos <!--and APIs--> en tiempo real desde la lista **[!UICONTROL Executions]**.

Para acceder a esta lista, en la página de inicio **[!DNL Journey Optimizer]**, seleccione **[!UICONTROL Messages]** y haga clic en la pestaña **[!UICONTROL Executions]**.

Esta ficha proporciona dos vistas: **[!UICONTROL Live view]** y **[!UICONTROL Global view]**.

* La pestaña **[!UICONTROL Live view]** proporciona una **información general en tiempo real de todos los mensajes ejecutados** activados por uno o más [recorridos](building-journeys/journey.md) **solo en las últimas 24 horas**.

   ![](assets/message-execution-tab-live.png)

   Esta lista se actualiza automáticamente cada sesenta segundos. Si no se ha producido ninguna ejecución en las últimas 24 horas para un mensaje específico, todas las columnas mostrarán valores nulos (0) para ese mensaje.

* La pestaña **[!UICONTROL Global view]** proporciona una **descripción general de todos los mensajes ejecutados** activados por uno o más [recorridos](building-journeys/journey.md) **desde la fecha de inicio del mensaje**.

   ![](assets/message-execution-tab-global.png)

   Esta lista se actualiza automáticamente cada noventa minutos. Los datos se acumulan con el tiempo desde cada fecha de inicio de mensaje.

Si un recorrido publica un mensaje pero aún no lo ha activado, no aparece en ninguna de las pestañas. Solo se enumeran los siguientes elementos:
* Mensajes que se han activado, pero que aún no se han iniciado (pendientes).
* Mensajes que se han activado y que se están ejecutando (en curso).

Para los mensajes multicanal, se muestra una fila por canal para cada mensaje.

![](assets/message-execution-multichannel.png)

Si se ha utilizado un mensaje en varios recorridos, la columna **[!UICONTROL Source]** muestra **[!UICONTROL Multiple]**.

De forma predeterminada, los mensajes se muestran a partir de la fecha de ejecución más reciente. Haga clic en el icono **[!UICONTROL Filters]** para buscar en los mensajes según el canal, la fecha de inicio o la fecha de finalización.

![](assets/message-execution-tab-filters.png)

La segunda columna <!--**[!UICONTROL Quick action]**-->permite abrir el [mensaje](create-message.md) correspondiente y acceder al [Informe activo](reports/live-report.md) si está en el **[!UICONTROL Live view]** o al [Informe global](reports/global-report.md) si está en el **[!UICONTROL Global view]**.

![](assets/message-execution-open-live-report.png)

Para cada ejecución de mensaje, se muestran varios indicadores:

* **[!UICONTROL Message label]**: Título del mensaje que definió al  [crear el mensaje](create-message.md).
* **[!UICONTROL Execution ID]**: Identificador generado automáticamente.
* **[!UICONTROL Source]**: Nombre del recorrido que aprovecha ese mensaje.
* **[!UICONTROL Start date]**: Fecha y hora en que se ejecutó el mensaje desde el recorrido.
* **[!UICONTROL Excluded]**: Número de perfiles que se han excluido del objetivo inicial debido a reglas de exclusión.
* **[!UICONTROL Sent]**: Número de mensajes que se han enviado.
* **[!UICONTROL Delivered]**: Número de mensajes entregados correctamente en el buzón del destinatario (correo electrónico) o en el dispositivo (push) sin generar un rechazo o ningún otro error de envío.
* **[!UICONTROL Bounces]**: Número de mensajes que no se pueden enviar debido a un error de entrega. [Obtenga más información sobre las devoluciones](suppression-lists.md#delivery-failures).
* **[!UICONTROL Opens]**: Número de mensajes que se han abierto.
* **[!UICONTROL Clicks]**: Número de clics en los vínculos de un correo electrónico.

   >[!NOTE]
   >
   >Los clics no existen para las notificaciones push: cuando un usuario hace clic en una notificación push, abre la aplicación, que solo puede considerarse como una apertura.

* **[!UICONTROL Errors]**: Número de mensajes que no se pueden enviar debido a un error técnico.

Al hacer clic en cada hipervínculo, se abrirá la vista de resumen del mensaje correspondiente. [Obtenga más información sobre los mensajes](create-message.md).
