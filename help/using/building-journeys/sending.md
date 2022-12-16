---
solution: Journey Optimizer
product: journey optimizer
title: Inicio de la ejecución del recorrido
description: Obtenga información sobre cómo iniciar el recorrido y enviar mensajes
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 7%

---


# ejecución del recorrido {#message-execution}

## Prueba del recorrido

Puede probar el recorrido con perfiles de prueba. Se recomienda realizar este paso para validar la configuración y los mensajes.

Obtenga más información en esta [sección](testing-the-journey.md).

## Activar el recorrido

Debe publicar el recorrido para activarlo.

![](assets/jo-journeyuc2_32bis.png)

Obtenga más información en esta [sección](publishing-the-journey.md).


Una vez publicado, puede monitorizar su recorrido con las herramientas de informes dedicadas para medir la efectividad de su recorrido.

![](assets/jo-dynamic_report_journey_12.png)

[Más información sobre los informes](../reports/live-report.md)

## Entrega de mensajes {#send-messages}

Cuando el mensaje tiene un contenido definido, está listo para enviarse a través de un [recorrido](journey.md).

Una vez enviado un mensaje, puede monitorizar su ejecución a través de varios indicadores. [Más información sobre los informes](../global-report.md).

## Programar mensajes {#schedule-messages}

Los mensajes se pueden programar mediante el **[!UICONTROL Leer segmento]** actividad en un [recorrido](journey.md). Puede especificar cuándo ingresará el segmento al recorrido. [Descubra más información sobre la actividad Leer segmento](read-segment.md).

Para realizar esto, siga los pasos a continuación:

1. Editar un recorrido, arrastrar y soltar un **[!UICONTROL Leer segmento]** y comience a configurarla. [Descubra más información sobre la configuración de la actividad Leer segmento](read-segment.md#configuring-segment-trigger-activity).

1. Haga clic en el **[!UICONTROL Editar programación de recorrido]** para acceder a las propiedades del recorrido.

   ![](assets/message-read-segment-schedule.png)

1. Configure las variables **[!UICONTROL Tipo de planificador]** campo: seleccione el valor que desee en la lista para que el segmento introduzca el recorrido en una fecha u hora específica o de forma recurrente.

   >[!NOTE]
   >
   >La variable **[!UICONTROL Programación]** solo está disponible cuando **[!UICONTROL Leer segmento]** se ha colocado la actividad en el lienzo.

   ![](assets/message-read-segment-scheduler.png)

1. Si selecciona **[!UICONTROL Una vez]**, defina una fecha y hora específicas en las que el segmento ingresará al recorrido.

   ![](assets/message-read-segment-scheduler-once.png)

1. Si selecciona un método recurrente, edite la fecha y la hora de inicio. También puede definir una fecha y hora de finalización opcionales.

   ![](assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >De forma predeterminada, los segmentos entran en el recorrido **[!UICONTROL Lo antes posible]**, es decir, 1 hora después de publicar el recorrido.

1. Haga clic en **[!UICONTROL OK]** para guardar los cambios.

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
