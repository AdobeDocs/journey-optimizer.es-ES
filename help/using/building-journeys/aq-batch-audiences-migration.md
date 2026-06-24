---
solution: Journey Optimizer
product: journey optimizer
title: Migrar audiencias por lotes desde recorridos de calificación de audiencias
description: Obtenga información sobre cómo migrar recorridos que utilizan audiencias por lotes en un nodo de Calificación de audiencias antes de la fecha de aplicación del 3 de agosto de 2026.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: calificación de audiencia, audiencia por lotes, obsolescencia, migración, leer audiencia, audiencia de streaming
exl-id: f3c2a7d1-b58e-4a92-c3d5-0e871f2a9b4c
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
source-git-commit: 6560a168d3ea7c6c27b47829ac4158b6a69b5d88
workflow-type: tm+mt
source-wordcount: 874
ht-degree: 0%

---


# Migrar audiencias por lotes desde recorridos de calificación de audiencias {#aq-batch-migration}

A partir del 3 de agosto de 2026, Journey Optimizer bloqueará la publicación de recorridos que utilicen una audiencia por lotes en un nodo de calificación de audiencias. Identifique el caso de uso que se muestra a continuación y siga la ruta de migración recomendada.

>[!CAUTION]
>
>**Fecha de aplicación: 3 de agosto de 2026.** Los recorridos nuevos, borradores y duplicados que utilizan una audiencia por lotes en un nodo de Calificación de audiencias no se pueden publicar después de esta fecha. Ya aparece una advertencia de validación en el lienzo de recorrido desde la versión de junio de 2026.

## Por qué este cambio {#why}

El nodo **[Calificación de audiencias](audience-qualification-events.md)** está diseñado para reaccionar en tiempo casi real a medida que los perfiles individuales entran o salen de una audiencia (los eventos de calificación llegan continuamente, uno a uno). Está dirigido a **[audiencias de transmisión](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)**.

Cuando se utiliza una audiencia por lotes con un nodo de calificación de audiencias, todos los eventos de calificación llegan simultáneamente durante la ventana de ingesta. Esto puede provocar el déclencheur de decenas de miles o millones de entradas de recorrido al mismo instante, causando una tensión grave del sistema y un comportamiento impredecible en los sistemas posteriores. Este no es el diseño previsto del nodo Calificación de audiencias.

La actividad **[Leer audiencia](read-audience.md)** es la herramienta correcta para los casos de uso por lotes: está diseñada para gestionar el procesamiento por lotes programado de una manera controlada y predecible.

## Cómo se ven afectados sus recorridos {#impact}

Un recorrido en directo que utiliza una audiencia por lotes en un nodo de Calificación de audiencias seguirá ejecutándose después del 3 de agosto de 2026. Sin embargo, si detiene, duplica o vuelve a publicar el recorrido, se bloqueará hasta que se actualice la configuración.


| Estado del recorrido | Impacto después del 3 de agosto de 2026 |
| --- | --- |
| **recorridos en vivo** | No se vio afectado. Los recorridos activos existentes siguen ejecutándose. Sin detención automática. |
| **Nuevos recorridos** | Bloqueado desde la publicación hasta que se sustituya la audiencia por lotes. |
| **recorridos de borrador** | Bloqueado desde la publicación hasta que se sustituya la audiencia por lotes. |
| **recorridos duplicados** | Bloqueado desde la publicación hasta que se sustituya la audiencia por lotes. |


## Guía de migración {#migration-paths}

Si utiliza una audiencia por lotes en un nodo de calificación de audiencias, identifique el caso de uso que aparece a continuación y siga la ruta de migración recomendada.

### Caso de uso 1: Audiencia creada en los eventos de seguimiento de mensajes de AJO {#use-case-1}

**Aspecto que tiene:** Su audiencia de calificación de audiencia utiliza condiciones basadas en envíos de correo electrónico, aperturas o clics de conjuntos de datos de seguimiento internos de Journey Optimizer; por ejemplo, *&quot;el perfil recibió un correo electrónico&quot;* o *&quot;el perfil abrió un correo electrónico.&quot;*

>[!NOTE]
>
>Desde noviembre de 2024, la segmentación de streaming ya no admite eventos de envío y apertura desde conjuntos de datos de seguimiento de Journey Optimizer. Las audiencias basadas en estos eventos ahora se evalúan en modo por lotes. [Más información sobre los métodos de evaluación de audiencia](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)

**Alternativas recomendadas:**

* **Reaccionando a aperturas o clics dentro del mismo recorrido** — Utilice el nodo **[Evento de reacción](reaction-events.md)**. Está diseñada para responder a aperturas y clics de un mensaje enviado dentro de ese mismo recorrido, sin requerir una audiencia independiente. [Ver un ejemplo de extremo a extremo con eventos de reacción](journeys-uc.md#send-multi-channel-messages)

* **Segmentación de clics entre recorridos**: cree una [audiencia de transmisión](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer) a partir de eventos de clics y use el nodo Calificación de audiencias con esa audiencia de transmisión en su lugar.

* **Supresión basada en rechazos**: use la [lista de supresión](../configuration/manage-suppression-list.md) nativa de Journey Optimizer en lugar de modelar el comportamiento de rechazos como condición de audiencia.

* **Cualquier lógica de envío/apertura restante** — Cambie a un recorrido de **[Leer audiencia](read-audience.md)** en una ejecución programada para procesar la audiencia por lotes de forma segura.


### Caso de uso 2: Recorrido de espera de nuevos datos de segmentación por lotes {#use-case-2}

**Aspecto:** Programe un recorrido para que se ejecute después de un trabajo de segmentación diario y utilice un nodo Calificación de audiencias para asegurarse de que el recorrido solo se active una vez que estén disponibles los datos de audiencia más recientes.

**Alternativa recomendada:**

Use un recorrido de **[Leer audiencia](read-audience.md)** con la opción **[!UICONTROL Déclencheur después de la evaluación de audiencia por lotes]** habilitada. Esta función integrada retrasa la ejecución del recorrido hasta que se completa el trabajo de segmentación y, a continuación, se inicia inmediatamente cuando hay datos nuevos disponibles, sin que sea necesario un nodo de calificación de audiencia. [Aprenda a configurar esta opción](read-audience.md#schedule)


### Caso de uso 3: activación de audiencia por lotes periódica grande {#use-case-3}

**Aspecto:** Activa o actualiza una audiencia grande (potencialmente millones de perfiles) de forma periódica, y el recorrido de calificación de audiencias se activa para todos los perfiles recién calificados a la vez.

**Alternativa recomendada:**

Use un recorrido de **[Leer audiencia](read-audience.md)**. Está diseñada específicamente para procesar grandes audiencias de forma masiva, gestionar perfiles en lotes controlados y ofrecer una ejecución de recorridos más predecible y fiable a escala. [Ver un ejemplo de extremo a extremo](message-to-subscribers-uc.md)

## ¿Qué sucede si ninguna de las alternativas funciona para su caso de uso? {#exceptions}

Si su caso de uso no se puede resolver mediante ninguna de las rutas de migración anteriores, póngase en contacto con su representante de Adobe. Los casos que no se puedan abordar con las alternativas existentes se revisarán individualmente.

## Recursos relacionados {#related}

* [Eventos de calificación de audiencias](audience-qualification-events.md): guía de configuración y protecciones completas
* [Leer la actividad de la audiencia](read-audience.md) — cómo configurar la entrada programada de la audiencia por lotes
* [Eventos de reacción](reaction-events.md): cómo reaccionar ante aperturas y clics dentro del mismo recorrido
* [Métodos de evaluación de audiencia](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer): se explica por lotes, streaming y segmentación de perímetros
* [Acerca de las audiencias](../audience/about-audiences.md): tipos de audiencias y cómo se crean en Journey Optimizer
* [Administrar la lista de supresión](../configuration/manage-suppression-list.md): cómo acceder y configurar la supresión de devoluciones
* [Limitaciones y protecciones de recorrido](limitations.md)
* [criterios de entrada y salida de Recorrido](entry-exit-criteria-guide.md): comprenda los patrones de entrada en tiempo real frente a los de entrada por lotes con ejemplos reales
* [Enviar mensajes multicanal](journeys-uc.md#send-multi-channel-messages): caso de uso de extremo a extremo que combina Audiencia de lectura, Eventos de reacción, correo electrónico y push
* [Enviar un mensaje a los suscriptores](message-to-subscribers-uc.md): caso de uso de un extremo al otro para la activación masiva de audiencias con Leer audiencia
