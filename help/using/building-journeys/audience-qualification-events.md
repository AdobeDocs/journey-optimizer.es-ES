---
solution: Journey Optimizer
product: journey optimizer
title: Eventos de calificación de audiencias
description: Obtenga información sobre los eventos de calificación de audiencias
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: calificación, eventos, audiencia, recorrido, plataforma
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: e45ec5f0e1bbcc73892f9cde5923627886f44ef6
workflow-type: tm+mt
source-wordcount: '1081'
ht-degree: 10%

---

# Eventos de calificación de audiencias {#segment-qualification}

## Acerca de los eventos de cualificación de público{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Eventos de calificación de público"
>abstract="Esta actividad permite que un recorrido escuche las entradas y salidas de perfiles en públicos de Adobe Experience Platform para que los particulares entren o avancen en un recorrido."

Esta actividad permite al recorrido escuchar las entradas y salidas de perfiles en audiencias de Adobe Experience Platform para hacer que los individuos entren o avancen en un recorrido. Para obtener más información sobre la creación de audiencias, consulte [sección](../audience/about-audiences.md).

Supongamos que tiene un público de “clientes plata”. Con esta actividad, puede hacer que todos los clientes nuevos de Silver Ingresen a un recorrido y les envíen una serie de mensajes personalizados.

Este tipo de evento se puede colocar como primer paso o más tarde en el recorrido.

➡️ [Descubra esta función en vídeo](#video)

### Notas importantes{#important-notes-segment-qualification}

* Tenga en cuenta que las audiencias de Adobe Experience Platform se calculan una vez al día (**lote** audiencias) o en tiempo real (**transmitido** mediante la opción Audiencias de alta frecuencia de Adobe Experience Platform).

   * Si la audiencia seleccionada se transmite por secuencias, las personas que pertenecen a esta audiencia podrían entrar en el recorrido en tiempo real.
   * Si la audiencia es por lotes, las personas recién cualificadas para esta audiencia podrían entrar en el recorrido cuando el cálculo de audiencia se ejecute en Adobe Experience Platform.

  Por lo tanto, como práctica recomendada, solo se recomienda utilizar audiencias de streaming en un **Calificación de audiencia** actividad. Para casos de uso por lotes, utilice un **[Leer audiencia](read-audience.md)** actividad.

  >[!NOTE]
  >
  >Debido a la naturaleza de lote de las audiencias creadas mediante flujos de trabajo de composición y carga personalizada, no puede dirigirse a estas audiencias en una actividad &quot;Calificación de audiencias&quot;. En esta actividad solo se pueden aprovechar las audiencias creadas con definiciones de segmento.

* Los grupos de campos de evento de experiencia no se pueden usar en recorridos que comiencen por una audiencia de lectura, una calificación de audiencia o una actividad de evento empresarial.

* Cuando se utiliza una calificación de público en un recorrido, esa actividad de calificación de público puede tardar hasta 10 minutos en estar activa y en escuchar los perfiles que entran o salen del público.

### Configuración de la actividad{#cnfigure-segment-qualification}

1. Despliegue el **[!UICONTROL Eventos]** categoría y suelte un **[!UICONTROL Calificación de audiencias]** actividad en el lienzo.

   ![](assets/segment5.png)

1. Añadir un **[!UICONTROL Etiqueta]** a la actividad. Este paso es opcional.

1. Haga clic en en **[!UICONTROL Audiencia]** y seleccione las audiencias que desee aprovechar.

   >[!NOTE]
   >
   >Tenga en cuenta que puede personalizar las columnas mostradas en la lista y ordenarlas.

   ![](assets/segment6.png)

   Una vez añadida la audiencia, **[!UICONTROL Copiar]** permite copiar su nombre y su ID:

   `{"name":"Loyalty membership","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. En el **[!UICONTROL Comportamiento]** , elija si desea escuchar las entradas de audiencia, las salidas o ambos.

   >[!NOTE]
   >
   >Tenga en cuenta que **[!UICONTROL Entrar]** y **[!UICONTROL Salir]** corresponde a la **Realizado** y **cerrado** estados de participación de audiencia de Adobe Experience Platform. Para obtener más información sobre cómo evaluar una audiencia, consulte la [Documentación del Servicio de segmentación](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. Seleccione un área de nombres. Esto solo es necesario si el evento se coloca como el primer paso del recorrido. De forma predeterminada, el campo está rellenado previamente con el último área de nombres utilizado.

   >[!NOTE]
   >
   >Solo puede seleccionar un área de nombres de identidad basada en personas. Si ha definido un área de nombres para una tabla de búsqueda (por ejemplo: área de nombres ProductID para una búsqueda Product), no estará disponible en la **Área de nombres** lista desplegable.

   ![](assets/segment7.png)

La carga útil contiene la siguiente información de contexto, que puede utilizar en condiciones y acciones:

* el comportamiento (entrada, salida)
* la marca de tiempo de la calificación
* el id de audiencia

Cuando se utiliza el editor de expresiones en una condición o acción que sigue a un **[!UICONTROL Calificación de audiencias]** actividad, tiene acceso a la **[!UICONTROL AudienceQualification]** nodo. Puede elegir entre las **[!UICONTROL Última hora de clasificación]** y el **[!UICONTROL status]** (entrada o salida).

Consulte [Actividad de condición](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Un nuevo recorrido que incluye un evento de calificación de audiencia está en funcionamiento diez minutos después de su publicación. Este intervalo de tiempo corresponde al intervalo de actualización de caché del servicio dedicado. Por lo tanto, debe esperar diez minutos antes de utilizar este recorrido.

## Prácticas recomendadas {#best-practices-segments}

El **[!UICONTROL Calificación de audiencias]** La actividad de permite la entrada inmediata en recorridos de personas que cumplen o no los requisitos de una audiencia de Adobe Experience Platform.

La velocidad de recepción de esta información es alta. Las mediciones realizadas muestran una velocidad de 10 000 eventos recibidos por segundo. Como resultado, debe asegurarse de comprender cómo pueden producirse los picos de entrada, cómo evitarlos y cómo preparar su recorrido para ellos.

### Audiencias por lotes{#batch-speed-segment-qualification}

Cuando utilice la calificación de audiencia para una audiencia por lotes, tenga en cuenta que se producirá un pico de entrada en el momento del cálculo diario. El tamaño del pico dependerá del número de personas que entren (o salgan) diariamente de la audiencia.

Además, si la audiencia por lotes se crea recientemente y se utiliza inmediatamente en un recorrido, el primer lote de cálculo puede hacer que un gran número de personas entre en el recorrido.

### Audiencias transmitidas{#streamed-speed-segment-qualification}

Cuando se utiliza la calificación de audiencia para audiencias transmitidas, hay menos riesgo de obtener grandes picos de entradas/salidas debido a la evaluación continua de la audiencia. Sin embargo, si la definición de audiencia conduce a que un gran volumen de clientes cumpla los requisitos al mismo tiempo, puede haber un pico también.

Evite utilizar la apertura y el envío de eventos con la segmentación de flujo continuo. En su lugar, utilice señales reales de actividad del usuario como clics, compras o datos de señalizaciones. Para la lógica de frecuencia o supresión, utilice reglas empresariales en lugar de enviar eventos. [Más información](../audience/about-audiences.md#open-and-send-event-guardrails)

Para obtener más información sobre la segmentación de flujo continuo, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api).

### Cómo evitar sobrecargas{#overloads-speed-segment-qualification}

Estas son algunas prácticas recomendadas que ayudarán a evitar la sobrecarga de sistemas aprovechados en los recorridos (fuentes de datos, acciones personalizadas, actividades de acción del canal).

No use, en un **[!UICONTROL Calificación de audiencias]** una audiencia por lotes inmediatamente después de su creación. Evitará el primer pico de cálculo. Tenga en cuenta que si está a punto de usar una audiencia que nunca se ha calculado, aparecerá una advertencia amarilla en el lienzo de recorrido.

![](assets/segment-error.png)

Establezca una regla de límite para las fuentes de datos y las acciones utilizadas en los recorridos para evitar sobrecargarlos. Obtenga más información en [Documentación del Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target="_blank"}. Tenga en cuenta que la regla de límite no tiene reintento. Si necesita volver a intentarlo, debe utilizar una ruta alternativa en el recorrido marcando la casilla **[!UICONTROL Añadir una ruta alternativa en caso de tiempo de espera o error]** en condiciones o acciones.

Antes de usar la audiencia en un recorrido de producción, evalúe siempre primero el volumen de personas que cumplen los requisitos para esta audiencia todos los días. Para ello, puede consultar la **[!UICONTROL Audiencia]** menú, abra la audiencia y observe la **[!UICONTROL Perfiles a lo largo del tiempo]** gráfico.

![](assets/segment-overload.png)

## Vídeo explicativo {#video}

Comprenda los casos de uso aplicables para los recorridos de calificación de público. Obtenga información sobre cómo crear un recorrido con la calificación de público y qué prácticas recomendadas aplicar.

>[!VIDEO](https://video.tv.adobe.com/v/3425028?quality=12)
