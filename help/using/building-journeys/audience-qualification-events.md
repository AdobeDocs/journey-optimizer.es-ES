---
solution: Journey Optimizer
product: journey optimizer
title: Eventos de calificación de público
description: Aprenda a utilizar y configurar eventos de cualificación de audiencias
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: calificación, eventos, audiencia, recorrido, plataforma
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: 284c4896b923eac1d360b61d97cbe560d747ea4f
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 5%

---

# Eventos de calificación de público {#segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Eventos de calificación de público"
>abstract="Esta actividad permite que un recorrido escuche las entradas y salidas de perfiles en públicos de Adobe Experience Platform para que los particulares entren o avancen en un recorrido."

## Acerca de los eventos de calificación de público{#about-segment-qualification}

Esta actividad permite al recorrido escuchar las entradas y salidas de perfiles en audiencias de Adobe Experience Platform para hacer que los individuos entren o avancen en un recorrido. Para obtener más información sobre la creación de audiencias, consulte esta [sección](../audience/about-audiences.md).

Supongamos que tiene un público de “clientes plata”. Con esta actividad, puede hacer que todos los clientes nuevos de Silver Ingresen a un recorrido y les envíen una serie de mensajes personalizados.

Este tipo de evento se puede colocar como primer paso o más tarde en el recorrido.

➡️ [Descubra esta funcionalidad en vídeo](#video)

### Mecanismos de protección y recomendaciones {#important-notes-segment-qualification}

Siga las protecciones y recomendaciones que se indican a continuación para crear recorridos de calificación de audiencias. Consulte también [Prácticas recomendadas de calificación de audiencias](#best-practices-segments).


* Los recorridos de cualificación de audiencias están diseñados principalmente para trabajar con audiencias de streaming. Esta combinación garantiza una mejor experiencia en tiempo real. Se recomienda encarecidamente usar **audiencias de streaming** en la actividad de calificación de audiencias.

  Sin embargo, si desea utilizar atributos basados en la ingesta por lotes en la audiencia de flujo continuo o en una audiencia por lotes para un recorrido de calificación de audiencias, considere el lapso de tiempo para la evaluación/activación de audiencias. Una audiencia por lotes o una audiencia de streaming que use atributos ingeridos por lotes estará lista para usar en la actividad **Calificación de audiencias** aproximadamente **2 horas** después de que finalice el trabajo de segmentación. Este trabajo se ejecuta una vez al día a la hora definida por el administrador de la organización de Adobe.

* Las audiencias de Adobe Experience Platform se calculan una vez al día (**audiencias por lotes**) o en tiempo real (para audiencias de **emisión**, con la opción Audiencias de alta frecuencia de Adobe Experience Platform).

   * Si la audiencia seleccionada se transmite por secuencias, las personas que pertenecen a esta audiencia pueden entrar en el recorrido en tiempo real.
   * Si la audiencia es por lotes, las personas recién cualificadas para esta audiencia podrían entrar en el recorrido cuando el cálculo de audiencia se ejecute en Adobe Experience Platform.

  Se recomienda usar audiencias de streaming en una actividad **Calificación de audiencias**. Para los casos de uso por lotes, utilice una actividad **[Leer audiencia](read-audience.md)**.

  >[!NOTE]
  >
  >Debido a la naturaleza de lote de las audiencias creadas mediante flujos de trabajo de composición y cargas personalizadas, estas audiencias no pueden segmentarse en una actividad &quot;Calificación de audiencias&quot;. En esta actividad solo se pueden aprovechar las audiencias creadas con definiciones de segmento.


* Los grupos de campos de evento de experiencia no se pueden usar en recorridos que comiencen por una actividad **Leer audiencia**, una **Calificación de audiencia** o un **Evento empresarial**.

* Cuando se usa una actividad **Calificación de audiencias** en un recorrido, esa actividad puede tardar hasta 10 minutos en estar activa y en escuchar los perfiles que entran o salen de la audiencia.


>[!CAUTION]
>
>Las [protecciones para la segmentación y los datos del perfil del cliente en tiempo real](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=es){target="_blank"} también se aplican a Adobe Journey Optimizer.



### Configuración de la actividad {#configure-segment-qualification}

Para configurar la actividad **[!UICONTROL Calificación de audiencias]**, siga estos pasos:

1. Despliegue la categoría **[!UICONTROL Events]** y suelte una actividad **[!UICONTROL Audience Qualification]** en el lienzo.

   ![](assets/segment5.png)

1. Agregue una **[!UICONTROL Etiqueta]** a la actividad. Este paso es opcional.

1. Haga clic en el campo **[!UICONTROL Audiencia]** y seleccione las audiencias que desee aprovechar.

   >[!NOTE]
   >
   >Puede personalizar las columnas mostradas en la lista y ordenarlas.

   ![](assets/segment6.png)

   Una vez agregada la audiencia, el botón **[!UICONTROL Copiar]** le permite copiar su nombre e ID:

   `{"name":"Loyalty membership","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. En el campo **[!UICONTROL Comportamiento]**, elija si desea escuchar las entradas de la audiencia, las salidas o ambos.

   >[!NOTE]
   >
   >**[!UICONTROL Entrar]** y **[!UICONTROL Salir]** corresponden a los estados de participación de audiencia **Realizado** y **Salido** de Adobe Experience Platform. Para obtener más información sobre cómo evaluar una audiencia, consulte la [documentación del servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. Seleccione un área de nombres. Esto solo es necesario si el evento se coloca como el primer paso del recorrido. De forma predeterminada, el campo está rellenado previamente con el último área de nombres utilizado.

   >[!NOTE]
   >
   >Solo puede seleccionar un área de nombres de identidad basada en personas. Si ha definido un área de nombres para una tabla de búsqueda (por ejemplo: área de nombres ProductID para una búsqueda de productos), no estará disponible en la lista desplegable **Área de nombres**.

   ![](assets/segment7.png)

La carga útil contiene la siguiente información de contexto, que puede utilizar en condiciones y acciones:

* el comportamiento (entrada, salida)
* la marca de tiempo de la calificación
* el id de audiencia

Cuando utilice el editor de expresiones en una condición o acción que siga a una actividad **[!UICONTROL Calificación de audiencias]**, tendrá acceso al nodo **[!UICONTROL AudienceQualification]**. Puede elegir entre **[!UICONTROL Última hora de calificación]** y **[!UICONTROL estado]** (entrada o salida).

Consulte [Actividad de condición](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Un nuevo recorrido que incluye un evento de **Calificación de audiencias** entrará en funcionamiento diez minutos después de su publicación. Este intervalo de tiempo corresponde al intervalo de actualización de caché del servicio dedicado. Por lo tanto, debe esperar diez minutos antes de utilizar este recorrido.

## Prácticas recomendadas {#best-practices-segments}

La actividad **[!UICONTROL Calificación de audiencias]** permite la entrada inmediata a recorridos de personas que cumplen o no los requisitos de una audiencia de Adobe Experience Platform.

La velocidad de recepción de esta información es alta. Las mediciones muestran una velocidad de 10 000 eventos recibidos por segundo. Como resultado, asegúrese de comprender cómo pueden producirse los picos de entrada, cómo evitarlos y cómo preparar su recorrido para ellos.

### Audiencias por lotes {#batch-speed-segment-qualification}

Cuando utilice la calificación de audiencia para una audiencia por lotes, tenga en cuenta que se produce un pico de entrada en el momento del cálculo diario. El tamaño del pico depende del número de individuos que entran (o salen) de la audiencia diariamente.

Además, si la audiencia por lotes se crea recientemente y se utiliza inmediatamente en un recorrido, el primer lote de cálculo puede hacer que un gran número de personas entre en el recorrido.

### Audiencias transmitidas {#streamed-speed-segment-qualification}

Cuando se utiliza la calificación de audiencia para audiencias transmitidas, hay menos riesgo de grandes picos de entradas/salidas debido a la evaluación continua de la audiencia. Sin embargo, si la definición de audiencia hace que un gran volumen de clientes se clasifique simultáneamente, podría seguir ocurriendo un pico.

Evite utilizar la apertura y el envío de eventos con la segmentación de flujo continuo. En su lugar, utilice señales reales de actividad del usuario como clics, compras o datos de señalizaciones. Para la lógica de frecuencia o supresión, utilice reglas empresariales en lugar de enviar eventos. [Más información](../audience/about-audiences.md#open-and-send-event-guardrails)

Para obtener más información sobre la segmentación de transmisión, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/methods/streaming-segmentation){target="_blank"}.

### Cómo evitar sobrecargas {#overloads-speed-segment-qualification}

Estas son algunas prácticas recomendadas para evitar sobrecargar sistemas aprovechados en recorridos (fuentes de datos, acciones personalizadas, actividades de acción del canal):

* No utilice una audiencia por lotes inmediatamente después de crearla en una actividad **[!UICONTROL Calificación de audiencias]**. Esto evita el primer pico de cálculo. Si está a punto de usar una audiencia que nunca se ha calculado, aparecerá una advertencia amarilla en el lienzo de recorrido.

  ![](assets/segment-error.png)

* Establezca una regla de límite para las fuentes de datos y las acciones utilizadas en los recorridos para evitar sobrecargarlos. Obtenga más información en [Documentación de Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target="_blank"}. Tenga en cuenta que la regla de límite no tiene reintento. Si necesita volver a intentarlo, use una ruta alternativa en el recorrido marcando la casilla **[!UICONTROL Agregar una ruta alternativa en caso de tiempo de espera o error]** en condiciones o acciones.

* Antes de usar la audiencia en un recorrido de producción, evalúe el volumen de personas que cumplen los requisitos para esta audiencia diariamente. Para ello, compruebe el menú **[!UICONTROL Audiencia]**, abra la audiencia y observe el gráfico de **[!UICONTROL Perfiles a lo largo del tiempo]**.

  ![](assets/segment-overload.png)

## Vídeo práctico {#video}

Comprenda los casos de uso aplicables para los recorridos de calificación de audiencias en este vídeo. Obtenga información sobre cómo crear un recorrido con la calificación de audiencias y las prácticas recomendadas que se deben aplicar.

>[!VIDEO](https://video.tv.adobe.com/v/3425028?quality=12)
