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
source-git-commit: 1d32db0103fd4f2afcd021cff5e8491515c86d65
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 13%

---

# Activación de audiencia en [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puede seleccionar en campañas y recorridos cualquier audiencia generada mediante definiciones de segmento, carga personalizada, flujos de trabajo de composición o Composición de audiencia federada.

## Protecciones y limitaciones {#guardrails}

* **Healthcare Shield o Privacy and Security Shield**: el uso de audiencias y atributos de la composición de audiencias no está disponible actualmente con Healthcare Shield o Privacy and Security Shield. [Aprenda a utilizar los atributos de enriquecimiento de audiencias en [!DNL Journey Optimizer]](../audience/about-audiences.md#enrichment)

* **Carga personalizada y composición de audiencia federada**: para las audiencias de carga personalizada y Composición de audiencia federada, tenga en cuenta las siguientes protecciones:

   * **Compatibilidad con vista previa y prueba:** En la actualidad, la vista previa y la prueba no son compatibles con las audiencias creadas mediante la carga de CSV o la composición de audiencias federada. Tenga esto en cuenta al planificar las campañas.

   * **Segmentación de nuevos perfiles:** Cuando no se encuentra una coincidencia entre un registro y un perfil del servicio de perfiles unificado, se crea un nuevo perfil vacío. Este perfil está vinculado a los atributos de enriquecimiento que se almacenan en el lago de datos. Dado que este nuevo perfil está vacío, los campos de segmentación que se usan normalmente en [!DNL Journey Optimizer] (por ejemplo, personalEmail.address, mobilePhone.number) están vacíos. Por lo tanto, estos campos no pueden utilizarse para la segmentación.

     Para resolver esto, puede especificar el &quot;campo de ejecución&quot; (o la &quot;dirección de ejecución&quot; según el canal) en la configuración del canal como &quot;identityMap&quot;. Esto garantiza que el atributo elegido como identidad en la creación de la audiencia sea el que se use para la segmentación en [!DNL Journey Optimizer].

   * **Registros activados y vinculación de identidad:** Todos los registros de la audiencia están activados, incluidos los duplicados. Durante la siguiente exportación de perfiles del servicio de perfil unificado, estos registros se vinculan con la identidad. Como resultado, el número de registros activados puede diferir del número de perfiles después de la vinculación de identidad.

## Retraso de activación de audiencias {#activation}

Las audiencias están listas para usarse en [!DNL Journey Optimizer] justo después de completarse la ingesta. Aunque esto suele ocurrir en menos de una hora, está sujeto a cierta variabilidad. Las audiencias resultantes de las composiciones deben estar disponibles 24 horas después de la publicación.

Para las audiencias resultantes de los trabajos de segmentación por lotes, la activación puede retrasarse debido a la variabilidad de la ingesta por lotes. Para los recorridos de lectura-audiencia programados a diario, puede definir un intervalo de tiempo en las propiedades del recorrido para garantizar que los datos de audiencia nuevos estén disponibles antes de la ejecución del recorrido.

Si el trabajo de segmentación no se completa en el intervalo de tiempo definido, el recorrido se omitirá hasta la siguiente ocurrencia. [Aprenda a programar un recorrido de lectura-audiencia](../building-journeys/read-audience.md)

## Audiencias de destino en [!DNL Journey Optimizer]

Puede aprovechar los públicos en **[!DNL Journey Optimizer]** de maneras diferentes:

* Elija un público para una **campaña**, donde el mensaje se envía a todos los particulares que pertenecen al público seleccionado. [Obtenga información sobre cómo definir el público de una campaña](../campaigns/create-campaign.md#define-the-audience-audience).

* Use una actividad de orquestación **Leer audiencia** en un recorrido para hacer que todos los individuos de la audiencia entren al recorrido y reciban los mensajes incluidos en el recorrido. Supongamos que tiene un público de “clientes plata”. Con esta actividad, puede hacer que todos los clientes de plata entren en un recorrido. A continuación, puede enviarles una serie de mensajes personalizados. [Obtenga información sobre cómo configurar la actividad Leer público](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

  Para los recorridos que utilizan audiencias de redacción de audiencias o carga personalizada, los atributos de perfil son tan nuevos como la última evaluación por lotes al introducir el recorrido. Sin embargo, después de una actividad de **Wait**, el recorrido actualiza los atributos de perfil del servicio Unified Profile Service (UPS), con lo que se obtienen los datos disponibles más recientes, lo que significa que los atributos de perfil pueden cambiar durante la ejecución del recorrido. [Más información acerca de la actualización de perfiles después de una actividad de espera](../building-journeys/wait-activity.md#profile-refresh)

* Utilice la actividad **Condición** en un recorrido para crear condiciones basadas en el abono del público. [Aprenda a utilizar los públicos en condiciones](../building-journeys/condition-activity.md#using-a-segment).

* Utilice la actividad de evento **Calificación de audiencias** en un recorrido para hacer que los individuos entren o avancen en el recorrido según las entradas y salidas de audiencias de Adobe Experience Platform. Por ejemplo, puede hacer que todos los “clientes plata” nuevos entren en el recorrido para enviarles mensajes. [Aprenda a configurar una actividad de calificación de audiencia](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >Debido a la naturaleza de lote de las audiencias creadas mediante flujos de trabajo de composición, carga personalizada o Composición de audiencia federada, no puede segmentar estas audiencias en una actividad &quot;Calificación de audiencias&quot;. En esta actividad solo se pueden aprovechar las audiencias creadas con definiciones de segmento.

## Activación de tipos de audiencia no admitidos en [!DNL Journey Optimizer]

Solo las audiencias generadas con **definición de segmento**, **composiciones de audiencia**, **carga personalizada (archivo CSV)** y **composición de audiencia federada** pueden segmentarse directamente en los recorridos y campañas de Journey Optimizer. [Más información sobre los tipos de audiencia disponibles](../audience/about-audiences.md#types)

Si necesita segmentar destinatarios a partir de una audiencia no admitida, como una audiencia de Customer Journey Analytics, debe envolverla en una nueva definición de segmento en el portal de audiencias. Encontrará información detallada sobre cómo agregar audiencias en una definición de segmento en la [documentación del Generador de segmentos](https://experienceleagu;e.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#adding-audiences){target="_blank"}

Una vez finalizado, espere a que se complete la evaluación de la segmentación para utilizarla en sus recorridos y campañas.
