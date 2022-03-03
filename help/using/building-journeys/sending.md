---
title: Inicio de la ejecución del recorrido
description: Obtenga información sobre cómo iniciar el recorrido y enviar mensajes
source-git-commit: dee8dbac067dac851af02d87a3dece1ba2b29376
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 8%

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

Cuando el mensaje tiene un contenido definido y publicado, está listo para enviarse a través de un [recorrido](journey.md).

>[!NOTE]
>
>Puede añadir un mensaje que aún esté en modo borrador a un recorrido, pero asegúrese de que el mensaje se publica antes de publicar el recorrido.

Una vez enviado un mensaje, puede monitorizar su ejecución a través de varios indicadores. [Obtenga más información sobre la monitorización de la ejecución de mensajes](../message-monitoring.md).

## Programar mensajes {#schedule-messages}

Los mensajes se pueden programar mediante el **[!UICONTROL Read Segment]** actividad en un [recorrido](journey.md). Puede especificar cuándo ingresará el segmento al recorrido. [Descubra más información sobre la actividad Leer segmento](read-segment.md).

Para realizar esto, siga los pasos a continuación:

1. Editar un recorrido, arrastrar y soltar un **[!UICONTROL Read Segment]** y comience a configurarla. [Descubra más información sobre la configuración de la actividad Leer segmento](read-segment.md#configuring-segment-trigger-activity).

1. Haga clic en el **[!UICONTROL Edit journey schedule]** para acceder a las propiedades del recorrido.

   ![](assets/message-read-segment-schedule.png)

1. Configure las variables **[!UICONTROL Scheduler type]** campo: seleccione el valor que desee en la lista para que el segmento introduzca el recorrido en una fecha u hora específica o de forma recurrente.

   >[!NOTE]
   >
   >La variable **[!UICONTROL Schedule]** solo está disponible cuando **[!UICONTROL Read Segment]** se ha colocado la actividad en el lienzo.

   ![](assets/message-read-segment-scheduler.png)

1. Si selecciona **[!UICONTROL Once]**, defina una fecha y hora específicas en las que el segmento ingresará al recorrido.

   ![](assets/message-read-segment-scheduler-once.png)

1. Si selecciona un método recurrente, edite la fecha y la hora de inicio. También puede definir una fecha y hora de finalización opcionales.

   ![](assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >De forma predeterminada, los segmentos entran en el recorrido **[!UICONTROL As soon as possible]**, es decir, 1 hora después de publicar el recorrido.

1. Haga clic en **[!UICONTROL OK]** para guardar los cambios.

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
