---
solution: Journey Optimizer
product: journey optimizer
title: Acerca de los públicos de Adobe Experience Platform
description: Aprenda a trabajar con los públicos de Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 78b95ccd-bc28-46cd-937a-f68e3f34cc1e
source-git-commit: 1ad534b7877f0ac6c1f50e29f41af708e83b34c9
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 22%

---

# Activación de audiencia en [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puede seleccionar en campañas y recorridos cualquier audiencia generada mediante definiciones de segmento, carga personalizada, flujos de trabajo de composición o Composición de audiencia federada.

>[!AVAILABILITY]
>
>El uso de audiencias y atributos de la composición de audiencias no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield. [Aprenda a utilizar los atributos de enriquecimiento de audiencias en Journey Optimizer](../audience/about-audiences.md#enrichment)

## Retraso de activación de audiencias {#activation}

Las audiencias están listas para usarse en Journey Optimizer justo después de completarse la ingesta. Aunque esto suele ocurrir en menos de una hora, está sujeto a cierta variabilidad. Las audiencias resultantes de las composiciones deben estar disponibles 24 horas después de la publicación.

Para las audiencias resultantes de los trabajos de segmentación por lotes, la activación puede retrasarse debido a la variabilidad de la ingesta por lotes. Para los recorridos de lectura-audiencia programados a diario, puede definir un intervalo de tiempo en las propiedades del recorrido para garantizar que los datos de audiencia nuevos estén disponibles antes de la ejecución del recorrido. Si el trabajo de segmentación no se completa en el intervalo de tiempo definido, el recorrido se omitirá hasta la siguiente ocurrencia. [Aprenda a programar un recorrido de lectura-audiencia](../building-journeys/read-audience.md)

## Carga personalizada y composición de audiencia federada

Para las audiencias de carga personalizada y de composición de audiencia federada, tenga en cuenta las siguientes protecciones:

* **Compatibilidad con vista previa y prueba:** En la actualidad, la vista previa y la prueba no son compatibles con las audiencias creadas mediante la carga de CSV o la composición de audiencias federada. Tenga esto en cuenta al planificar las campañas.

* **Segmentación de nuevos perfiles:** Cuando no se encuentra una coincidencia entre un registro y un perfil de UPS, se crea un nuevo perfil vacío. Este perfil está vinculado a los atributos de enriquecimiento que se almacenan en el lago de datos. Dado que este nuevo perfil está vacío, los campos de segmentación que se suelen utilizar en Journey Optimizer (por ejemplo, personalEmail.address, mobilePhone.number) están vacíos y, por lo tanto, no se pueden utilizar para la segmentación.

  Para resolver esto, puede especificar el &quot;campo de ejecución&quot; (o la &quot;dirección de ejecución&quot; según el canal) en la configuración del canal como &quot;identityMap&quot;. Esto garantizará que el atributo elegido como identidad en el momento de la creación de la audiencia sea el que se use para la segmentación en Journey Optimizer.

* **Registros activados y vinculación de identidad:** Todos los registros de la audiencia están activados, incluidos los duplicados. Durante la próxima exportación de perfiles de UPS, estos registros se vincularán con la identidad. Como resultado, el número de registros activados puede diferir del número de perfiles después de la vinculación de identidad.

## Audiencias de destino en [!DNL Journey Optimizer]

Puede aprovechar los públicos en **[!DNL Journey Optimizer]** de maneras diferentes:

* Elija un público para una **campaña**, donde el mensaje se envía a todos los particulares que pertenecen al público seleccionado. [Obtenga información sobre cómo definir el público de una campaña](../campaigns/create-campaign.md#define-the-audience-audience).

* Use una actividad de orquestación **Leer audiencia** en un recorrido para hacer que todos los individuos de la audiencia entren al recorrido y reciban los mensajes incluidos en el recorrido. Supongamos que tiene un público de “clientes plata”. Con esta actividad, puede hacer que todos los “clientes plata” entren en un recorrido y se les envíe una serie de mensajes personalizados. [Obtenga información sobre cómo configurar la actividad Leer público](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

  >[!NOTE]
  >
  >Cualquier recorrido que utilice una audiencia de la composición de audiencias o una carga personalizada en la actividad &quot;Leer audiencia&quot; tendrá atributos de perfil tan recientes como la última evaluación por lotes. Esto incluye consentimientos/supresiones en el recorrido.

* Utilice la actividad **Condición** en un recorrido para crear condiciones basadas en el abono del público. [Aprenda a utilizar los públicos en condiciones](../building-journeys/condition-activity.md#using-a-segment).

* Utilice la actividad de evento **Calificación de audiencias** en un recorrido para hacer que los individuos entren o avancen en el recorrido según las entradas y salidas de audiencias de Adobe Experience Platform. Por ejemplo, puede hacer que todos los “clientes plata” nuevos entren en el recorrido para enviarles mensajes. Para obtener más información sobre cómo utilizar esta actividad, consulte [Obtener información sobre cómo configurar una actividad Calificación de público](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >Debido a la naturaleza de lote de las audiencias creadas mediante flujos de trabajo de composición, carga personalizada o Composición de audiencia federada, no puede segmentar estas audiencias en una actividad &quot;Calificación de audiencias&quot;. En esta actividad solo se pueden aprovechar las audiencias creadas con definiciones de segmento.
