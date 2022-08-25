---
title: Uso de segmentos en un recorrido
description: Aprenda a utilizar un segmento en un recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 1780310da6d8a952dd22b9ee9a0b23516efddb5f
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 6%

---

# Uso de segmentos en un recorrido {#segment-trigger-activity}

## Añadir una actividad Leer segmento {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Leer Actividad de segmentos"
>abstract="La actividad Leer segmento le permite hacer que todas las personas que pertenecen a un segmento de Adobe Experience Platform participen en un recorrido. La entrada en un recorrido puede realizarse una vez o de forma regular."

Utilice la variable **Leer segmento** actividad para que todas las personas de un segmento entren en el recorrido. La entrada en un recorrido puede realizarse una vez o de forma regular.

Veamos como ejemplo el segmento &quot;Apertura y cierre de compra de la aplicación de Luma&quot; creado en la [Generar segmentos](../segment/about-segments.md) caso de uso. Con la actividad Leer segmento , puede hacer que todas las personas que pertenecen a este segmento ingresen a un recorrido y hacer que fluyan a recorridos personalizados que aprovechen todas las funcionalidades de recorrido: condiciones, temporizadores, eventos, acciones.

>[!NOTE]
>
>Para los recorridos que utilizan una actividad Leer segmento , existe un número máximo de recorridos que pueden iniciarse al mismo tiempo. El sistema realizará los reintentos, pero evite tener más de cinco recorridos (con Leer segmento, programados o iniciados &quot;lo antes posible&quot;) que empiecen al mismo tiempo, esparciéndolos a lo largo del tiempo, por ejemplo, entre 5 y 10 minutos.
>
>El complemento de pago de ráfaga permite enviar mensajes push muy rápidamente en grandes volúmenes para recorridos simples que incluyen un segmento de lectura y un mensaje push simple. Para obtener más información, consulte [esta sección](../building-journeys/journey-gs.md#burst)

### Configure la actividad {#configuring-segment-trigger-activity}

Los pasos para configurar la actividad Leer segmento son los siguientes:

1. Despliegue el **[!UICONTROL Orchestration]** categoría y suelte a **[!UICONTROL Read Segment]** actividad en el lienzo.

   La actividad debe colocarse como el primer paso de un recorrido.

1. Agregue un **[!UICONTROL Label]** a la actividad (opcional).

1. En el **[!UICONTROL Segment]** , seleccione el segmento de Adobe Experience Platform que entrará en el recorrido y, a continuación, haga clic en **[!UICONTROL Save]**.

   Tenga en cuenta que puede personalizar las columnas mostradas en la lista y ordenarlas.

   >[!NOTE]
   >
   >Solo las personas con la variable **Realizado** y **Existente** los estados de participación de segmentos entrarán en el recorrido. Para obtener más información sobre cómo evaluar un segmento, consulte la [Documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.

   ![](assets/read-segment-selection.png)

   Una vez agregado el segmento, la variable **[!UICONTROL Copy]** permite copiar su nombre y su ID:

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. En el **[!UICONTROL Namespace]** , elija el área de nombres que desea utilizar para identificar a las personas. [Más información sobre áreas de nombres](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Las personas que pertenecen a un segmento que no tiene la identidad seleccionada (área de nombres) entre sus distintas identidades no pueden entrar en el recorrido.

1. Configure las variables **[!UICONTROL Throttling rate]** al límite de rendimiento de la actividad de segmento de lectura.

   Este valor se almacena en la carga útil de la versión de recorrido. El valor predeterminado es 20 000 mensajes por segundo. Puede modificar este valor de 500 a 20 000 mensajes por segundo.

   >[!NOTE]
   >
   >La tasa de regulación global por simulador de pruebas se establece en 20 000 mensajes por segundo. Por lo tanto, la tasa de regulación de todos los segmentos de lectura que se ejecutan simultáneamente en el mismo simulador de pruebas suman como máximo 20 000 mensajes por segundo. No puede modificar este límite.

1. La variable **[!UICONTROL Read Segment]** actividad le permite especificar la hora a la que el segmento ingresará en el recorrido. Para ello, haga clic en el botón **[!UICONTROL Edit journey schedule]** para acceder a las propiedades del recorrido y, a continuación, configure el **[!UICONTROL Scheduler type]** campo .

   ![](assets/read-segment-schedule.png)

   De forma predeterminada, los segmentos entran en el recorrido **[!UICONTROL As soon as possible]**. Si desea que el segmento introduzca el recorrido en una fecha u hora específica o de forma recurrente, seleccione el valor que desee en la lista.

   >[!NOTE]
   >
   >Tenga en cuenta que **[!UICONTROL Schedule]** solo está disponible cuando **[!UICONTROL Read Segment]** la actividad se ha soltado en el lienzo.

   ![](assets/read-segment-schedule-list.png)

   **Lectura incremental** opción: cuando un recorrido con un **Leer segmento** se ejecuta por primera vez, todos los perfiles del segmento se incorporan al recorrido. En la siguiente incidencia, todos los perfiles entran de nuevo en el recorrido, incluso si ya estaban dentro. La instancia antigua del perfil en el recorrido se detiene y se crea una nueva. La variable **Lectura incremental** le permite dirigirse, después de la primera vez que se produzca, a las personas que ingresaron al segmento desde la última ejecución del recorrido.

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

>[!NOTE]
>
>Los recorridos de segmento Leído con una sola toma se mueven al estado Finalizado 30 días después de la ejecución del recorrido. Para segmentos de lectura programados, son 30 días después de la ejecución de la última ocurrencia.

### Prueba y publicación del recorrido {#testing-publishing}

La variable **[!UICONTROL Read Segment]** actividad le permite probar el recorrido en un perfil unitario o en 100 perfiles de prueba aleatorios seleccionados entre los perfiles cualificados para el segmento.

Para ello, active el modo de prueba y, a continuación, seleccione la opción que desee en el panel izquierdo.

![](assets/read-segment-test-mode.png)

A continuación, puede configurar y ejecutar el modo de prueba como de costumbre. [Obtenga información sobre cómo probar un recorrido](testing-the-journey.md).

Una vez ejecutada la prueba, la variable **[!UICONTROL Show logs]** permite ver los resultados de la prueba según la opción de prueba seleccionada:

* **[!UICONTROL Single profile at a time]**: los registros de prueba muestran la misma información que al utilizar el modo de prueba unitaria. Para obtener más información, consulte [esta sección](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Up to 100 profiles at once]**: los registros de prueba permiten realizar un seguimiento de la progresión de la exportación de segmentos desde Adobe Experience Platform, así como del progreso individual de todas las personas que ingresaron al recorrido.

   Tenga en cuenta que probar el recorrido utilizando hasta 100 perfiles a la vez no permite rastrear el progreso de las personas en el recorrido mediante el flujo visual.

   ![](assets/read-segment-log.png)

Una vez realizadas las pruebas correctamente, puede publicar el recorrido (consulte [Publicación del recorrido](publishing-the-journey.md)). Las personas que pertenezcan al segmento introducirán el recorrido en la fecha y hora especificadas en las propiedades del recorrido **[!UICONTROL Scheduler]** para obtener más información.

>[!NOTE]
>
>Para los recorridos recurrentes basados en segmentos, el recorrido se cerrará automáticamente una vez que se ejecute su última incidencia. Si no se ha especificado ninguna fecha y hora de finalización, deberá cerrar el recorrido manualmente a las nuevas entradas para finalizarlo.

## Segmentación de audiencias en recorridos basados en segmentos

Los recorridos basados en segmentos siempre comienzan con un **Leer segmento** actividad para recuperar personas que pertenecen a un segmento de Adobe Experience Platform.

La audiencia que pertenece al segmento se recupera una vez o de forma regular.

Después de entrar en el recorrido, puede crear casos de uso de orquestación de audiencia, para que los individuos del segmento inicial fluyan a diferentes ramas del recorrido.

**Segmentación**

Puede utilizar condiciones para realizar segmentaciones utilizando la variable **Condición** actividad. Por ejemplo, puede hacer que VIP personas tomen una ruta en particular y que no VIP flujo en otra ruta.

La segmentación puede basarse en:

* datos de origen de datos
* el contexto de los eventos que forman parte de los datos de recorrido, por ejemplo: ¿hizo una persona clic en el mensaje recibido hace una hora?
* una fecha, por ejemplo: ¿estamos en junio cuando una persona pasa por el recorrido?
* una hora, por ejemplo: ¿es la mañana en la zona horaria de la persona?
* un algoritmo que divide la audiencia que fluye en el recorrido en función de un porcentaje, por ejemplo: 90 % - 10 % para excluir un grupo de control

![](assets/read-segment-audience1.png)

**Exclusión**

Igual **Condición** actividad utilizada para la segmentación (consulte más arriba) también le permite excluir parte de la población. Por ejemplo, puede excluir VIP personas haciendo que fluyan a una rama con un paso final justo después.

Esta exclusión podría ocurrir justo después de la recuperación de segmentos, con fines de recuento de población o a lo largo de un recorrido de varios pasos.

![](assets/read-segment-audience2.png)

**Union**

Los recorridos le permiten crear N ramas y unirlas después de una segmentación.

Como resultado, puede hacer que dos audiencias regresen a una experiencia común.

Por ejemplo, después de seguir una experiencia diferente durante diez días en un recorrido, los clientes VIP y no VIP pueden regresar a la misma ruta.

Después de una unión, puede dividir de nuevo la audiencia realizando una segmentación o una exclusión.

![](assets/read-segment-audience3.png)
