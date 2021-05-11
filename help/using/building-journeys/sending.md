---
title: Inicio de la ejecución del recorrido
description: Obtenga información sobre cómo iniciar el recorrido y enviar mensajes
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 7%

---


# Ejecución de recorrido {#message-execution}

![](../assets/do-not-localize/badge.png)

## Probar el recorrido

Puede probar el recorrido con perfiles de prueba. Se recomienda realizar este paso para validar la configuración y los mensajes.

Obtenga más información en esta [sección](testing-the-journey.md).

## Activar el recorrido

Debe publicar el recorrido para activarlo.

![](../assets/jo-journeyuc2_32bis.png)

Obtenga más información en esta [sección](publishing-the-journey.md).


Una vez publicado, puede monitorizar su recorrido con las herramientas de informes dedicadas para medir la efectividad de su recorrido.

![](../assets/jo-dynamic_report_journey_12.png)

[Más información sobre los informes](../reports/live-report.md)

## Entrega de mensajes {#send-messages}

Cuando el mensaje tiene un contenido definido y se publica, está listo para enviarse a través de un [recorrido](journey.md).

>[!NOTE]
>
>Puede añadir un mensaje que aún esté en modo borrador a un recorrido, pero asegúrese de que el mensaje se publica antes de publicar el recorrido.

Una vez enviado un mensaje, se puede monitorizar su ejecución mediante varios indicadores. [Obtenga más información sobre la supervisión de la ejecución](../message-monitoring.md) de mensajes.

## Programar mensajes {#schedule-messages}

Los mensajes se pueden programar a través de la actividad **[!UICONTROL Read segment]** en un [recorrido](journey.md). Puede especificar cuándo ingresará el segmento al recorrido. [Obtenga más información sobre la actividad](read-segment.md) Leer segmento .

Para realizar esto, siga los pasos a continuación:

1. Edite un recorrido, arrastre y suelte una actividad **[!UICONTROL Read segment]** y comience a configurarla. [Obtenga más información sobre la configuración de la actividad](read-segment.md#configuring-segment-trigger-activity) Leer segmento .

1. Haga clic en el enlace **[!UICONTROL Edit journey schedule]** para acceder a las propiedades del recorrido.

   ![](../assets/message-read-segment-schedule.png)

1. Configure el campo **[!UICONTROL Scheduler type]**: seleccione el valor que desee en la lista para que el segmento introduzca el recorrido en una fecha u hora específica o de forma recurrente.

   >[!NOTE]
   >
   >La sección **[!UICONTROL Schedule]** solo está disponible cuando se ha colocado una actividad **[!UICONTROL Read Segment]** en el lienzo.

   ![](../assets/message-read-segment-scheduler.png)

1. Si selecciona **[!UICONTROL Once]**, defina una fecha y hora específicas en la que el segmento ingresará al recorrido.

   ![](../assets/message-read-segment-scheduler-once.png)

1. Si selecciona un método recurrente, edite la fecha y la hora de inicio. También puede definir una fecha y hora de finalización opcionales.

   ![](../assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >De forma predeterminada, los segmentos introducen el recorrido **[!UICONTROL As soon as possible]**, es decir, 1 hora después de publicar el recorrido.

1. Haga clic en **[!UICONTROL OK]** para guardar los cambios.

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
