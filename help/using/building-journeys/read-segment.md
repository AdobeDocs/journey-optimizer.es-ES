---
title: Uso de segmentos en un recorrido
description: Aprenda a utilizar un segmento en un recorrido
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: 2e85e966dcff87717ce4a5f426f9e66526dab7c4
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 4%

---

# Uso de segmentos en un recorrido {#segment-trigger-activity}

## Acerca de la actividad Leer segmento {#about-segment-trigger-actvitiy}

La actividad Leer segmento le permite hacer que todas las personas que pertenecen a un segmento de Adobe Experience Platform participen en un recorrido. La entrada en un recorrido puede realizarse una vez o de forma regular.

Veamos como ejemplo el segmento &quot;Apertura y cierre de compra de la aplicación de Luma&quot; creado en el caso de uso [Segmentos de compilación](../segment/about-segments.md). Con la actividad Leer segmento , puede hacer que todas las personas que pertenecen a este segmento ingresen a un recorrido y hacer que fluyan a recorridos personalizados que aprovechen todas las funcionalidades de recorrido: condiciones, temporizadores, eventos, acciones.

>[!NOTE]
>
>El complemento de pago de ráfaga permite enviar mensajes push muy rápidamente en grandes volúmenes para recorridos simples que incluyen un segmento de lectura y un mensaje push simple. Para obtener más información, consulte [esta sección](../building-journeys/journey-gs.md#burst)

### Configure la actividad {#configuring-segment-trigger-activity}

Los pasos para configurar la actividad Leer segmento son los siguientes:

1. Despliegue la categoría **[!UICONTROL Orchestration]** y suelte una actividad **[!UICONTROL Read Segment]** en el lienzo.

   La actividad debe colocarse como el primer paso de un recorrido.

1. Agregue un **[!UICONTROL Label]** a la actividad (opcional).

1. En el campo **[!UICONTROL Segment]**, seleccione el segmento de Adobe Experience Platform que ingresará al recorrido y haga clic en **[!UICONTROL Save]**.

   Tenga en cuenta que puede personalizar las columnas mostradas en la lista y ordenarlas.

   >[!NOTE]
   >
   >Solo las personas con los estados de participación de segmentos **Realized** y **Existing** entrarán en el recorrido. Para obtener más información sobre cómo evaluar un segmento, consulte la [Documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results).

   ![](../assets/read-segment-selection.png)

   Una vez agregado el segmento, el botón **[!UICONTROL Copy]** le permite copiar su nombre y su ID:

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](../assets/read-segment-copy.png)

1. En el campo **[!UICONTROL Namespace]**, elija el área de nombres que desea utilizar para identificar a las personas. [Obtenga más información sobre áreas de nombres](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Las personas que pertenecen a un segmento que no tiene la identidad seleccionada (área de nombres) entre sus distintas identidades no pueden entrar en el recorrido.

1. La actividad **[!UICONTROL Read Segment]** le permite especificar la hora a la que el segmento ingresará al recorrido. Para ello, haga clic en el enlace **[!UICONTROL Edit journey schedule]** para acceder a las propiedades del recorrido y, a continuación, configure el campo **[!UICONTROL Scheduler type]**.

   ![](../assets/read-segment-schedule.png)

   De forma predeterminada, los segmentos introducen el recorrido **[!UICONTROL As soon as possible]**. Si desea que el segmento introduzca el recorrido en una fecha u hora específica o de forma recurrente, seleccione el valor que desee en la lista.

   >[!NOTE]
   >
   >Tenga en cuenta que la sección **[!UICONTROL Schedule]** solo está disponible cuando se ha colocado una actividad **[!UICONTROL Read Segment]** en el lienzo.

   ![](../assets/read-segment-schedule-list.png)

### Prueba y publicación del recorrido {#testing-publishing}

La actividad **[!UICONTROL Read Segment]** le permite probar el recorrido en un perfil unitario o en 100 perfiles de prueba aleatorios seleccionados entre los perfiles cualificados para el segmento.

Para ello, active el modo de prueba y, a continuación, seleccione la opción que desee en el panel izquierdo.

![](../assets/read-segment-test-mode.png)

A continuación, puede configurar y ejecutar el modo de prueba como de costumbre. [Aprenda a probar un recorrido](testing-the-journey.md).

Una vez que se está ejecutando la prueba, el botón **[!UICONTROL Show logs]** le permite ver los resultados de la prueba según la opción de prueba seleccionada:

* **[!UICONTROL Single profile at a time]**: los registros de prueba muestran la misma información que al utilizar el modo de prueba unitaria. Para obtener más información, consulte [esta sección](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Up to 100 profiles at once]**: los registros de prueba permiten realizar un seguimiento de la progresión de la exportación de segmentos desde Adobe Experience Platform, así como del progreso individual de todas las personas que ingresaron al recorrido.

   Tenga en cuenta que probar el recorrido utilizando hasta 100 perfiles a la vez no permite rastrear el progreso de las personas en el recorrido mediante el flujo visual.

   ![](../assets/read-segment-log.png)

Una vez realizadas las pruebas correctamente, puede publicar el recorrido (consulte [Publicación del recorrido](publishing-the-journey.md)). Las personas que pertenezcan al segmento introducirán el recorrido en la fecha y hora especificadas en la sección **[!UICONTROL Scheduler]** de propiedades del recorrido.

>[!NOTE]
>
>Para los recorridos recurrentes basados en segmentos, el recorrido se cerrará automáticamente una vez que se ejecute su última incidencia. Si no se ha especificado ninguna fecha y hora de finalización, deberá cerrar el recorrido manualmente a las nuevas entradas para finalizarlo.


## Segmentación de audiencias en recorridos basados en segmentos

Los recorridos basados en segmentos siempre comienzan con una actividad **Leer segmento** para recuperar personas que pertenecen a un segmento de Adobe Experience Platform.

La audiencia que pertenece al segmento se recupera una vez o de forma regular.

Después de entrar en el recorrido, puede crear casos de uso de orquestación de audiencia, para que los individuos del segmento inicial fluyan a diferentes ramas del recorrido.

**Segmentación**

Puede utilizar condiciones para realizar la segmentación mediante la actividad **Condition**. Por ejemplo, puede hacer que VIP personas tomen una ruta en particular y que no VIP flujo en otra ruta.

La segmentación puede basarse en:

* datos de origen de datos
* el contexto de los eventos que forman parte de los datos de recorrido, por ejemplo: ¿hizo una persona clic en el mensaje que recibió hace una hora?
* una fecha, por ejemplo: ¿estamos en junio cuando una persona pasa por el recorrido?
* una hora, por ejemplo: ¿es la mañana en la zona horaria de la persona?
* un algoritmo que divide la audiencia que fluye en el recorrido en función de un porcentaje, por ejemplo: 90 % - 10 % para excluir un grupo de control

![](../assets/read-segment-audience1.png)

**Exclusión**

La misma actividad **Condition** utilizada para la segmentación (ver arriba) también le permite excluir parte de la población. Por ejemplo, puede excluir VIP personas haciendo que fluyan a una rama con un paso final justo después.

Esta exclusión podría ocurrir justo después de la recuperación de segmentos, con fines de recuento de población o a lo largo de un recorrido de varios pasos.

![](../assets/read-segment-audience2.png)

**Union**

Los recorridos le permiten crear N ramas y unirlas después de una segmentación.

Como resultado, puede hacer que dos audiencias regresen a una experiencia común.

Por ejemplo, después de seguir una experiencia diferente durante diez días en un recorrido, los clientes VIP y no VIP pueden regresar a la misma ruta.

Después de una unión, puede dividir de nuevo la audiencia realizando una segmentación o una exclusión.

![](../assets/read-segment-audience3.png)
