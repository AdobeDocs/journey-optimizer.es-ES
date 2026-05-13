---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las campañas organizadas
description: Obtenga información sobre cómo empezar con campañas organizadas
short-description: Descubra las funciones clave y los casos de uso de la campaña orquestada.
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/ePbw3PWwBuZl5A3bdBzM0gb4koCEH09WUX0P-g8z3VM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 909
ht-degree: 0%

---

# Introducción a las campañas organizadas {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campaigns_overview_orchestrated"
>abstract="<b>Organización de campaña</b><br/>Divida, combine, enriquezca y manipule conjuntos de datos relacionales para definir su audiencia<br/><br/> <b>Aproveche los datos de varias entidades</b><br/>Descubra cómo las campañas orquestadas pueden aprovechar los conjuntos de datos relacionales para enriquecer los datos para la segmentación y personalización<br/><br/><b>Segmentación ad hoc y recuentos exactos</b><br/>Cree su segmento paso a paso con recuentos exactos<br/><br/><b>Canales disponibles</b><br/>Correo electrónico, SMS, notificaciones push, Correo directo"

La orquestación de campaña de [!DNL Adobe Journey Optimizer] potencia campañas sofisticadas iniciadas por la marca en todos los canales, tanto **marketing** como **transaccional**. Las campañas de marketing le ayudan a impulsar la participación, los ingresos y la lealtad de los clientes a escala. Los mensajes transaccionales no requieren la inclusión y son adecuados para comunicaciones en las que el tiempo es importante, como interrupciones, emergencias o cancelaciones.

>[!IMPORTANT]
>
>Para acceder a Campaign Orchestration, la licencia debe incluir **Journey Optimizer - Campañas y Recorridos** o el paquete **Journey Optimizer - Campañas**. Póngase en contacto con su representante de Adobe para confirmar su licencia y actualizarla si es necesario.

Aunque el marketing multicanal es esencial, las campañas orquestadas lo hacen fluido. Con una interfaz visual de arrastrar y soltar, puede diseñar y automatizar flujos de trabajo de marketing complejos, desde la segmentación hasta la entrega de mensajes, en varios canales. Todo sucede en un entorno intuitivo, creado para la velocidad, el control y la eficacia.

![](assets/canvas-example-diagram.png){zoomable="yes"}

➡️ [Descubra campañas orquestadas en vídeo](#video-oc)

## Funcionalidades principales

La organización de campañas se basa en cuatro pilares clave:

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="Audiencias a la carta" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b>Las audiencias a petición</b><br/>consultan instantáneamente entre conjuntos de datos para crear segmentos de audiencia usando cualquier combinación de tipos de datos y dimensiones.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentación y envío de varias entidades" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b>Segmentación y envío de varias entidades</b><br/>Vaya más allá de las campañas basadas en personas: use entidades como catálogos de productos, ubicaciones de tiendas o datos de servicio para segmentar con precisión.<br/><br/>
Admitir el envío de varios niveles, donde se envía un mensaje por perfil y por entidad secundaria asociada. Estas entidades secundarias pueden incluir direcciones de contacto, reservas, suscripciones, contratos u otros datos vinculados. Por ejemplo, esto permite enviar campañas a todas las direcciones conocidas de un perfil o a todas las reservas asociadas con ese perfil.</td></tr>
<tr style="border: 0;">
<td><img alt="Visibilidad y precisión previas al envío" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b>Visibilidad y precisión previas al envío</b><br/>Obtenga recuentos de segmentación exactos y un ámbito de campaña completo antes del lanzamiento, lo que garantiza precisión y confianza.</td></tr>
<tr style="border: 0;">
<td><img alt="Flujos de trabajo de campaña de varios pasos" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b>Flujos de trabajo de campañas de varios pasos</b><br/>Diseña campañas de varios pasos, desde mensajes diarios hasta campañas complejas como promociones de temporada o lanzamientos de productos importantes.</td></tr>
</table>

>[!NOTE]
>
>Para obtener más información sobre los canales admitidos, consulte la tabla de esta sección: [Canales en recorridos y campañas](../channels/gs-channels.md#channels).
>
>Los canales disponibles varían en función del modelo de licencia y los complementos.

## Campañas y recorridos organizados

Aunque la visualización de campañas orquestadas tiene similitudes con los recorridos, resuelve diferentes propósitos y casos de uso:

* **Recorridos**: lienzo de 1 a 1 en el que cada perfil viaja por los diferentes pasos a su propio ritmo. El estado de cada cliente se mantiene dentro de su contexto para almacenar en déclencheur las acciones en tiempo real.

* **Campañas orquestadas**: a diferencia de los recorridos, las campañas orquestadas funcionan con un lienzo por lotes que calcula los segmentos. Todos los perfiles se procesan juntos al mismo tiempo.

Ambos lienzos están optimizados para sus respectivos casos de uso: el lienzo de Recorrido publica recorridos que tienden a permanecer activos durante un período de tiempo más largo, mientras que el lienzo de campaña está diseñado para ejecuciones iterativas e incrementales de una campaña por lotes.

## ¿Qué hay dentro de una campaña orquestada? {#gs-ms-campaign-inside}

El lienzo de campaña orquestada es una representación de lo que se supone que debe suceder. Describe las diversas tareas que se deben realizar y cómo se vinculan entre sí.

![imagen que muestra un lienzo de campaña orquestado](assets/canvas-example.png)

Cada campaña orquestada contiene:

* **Actividades**: una actividad es una tarea que se va a realizar. Las [diversas actividades](activities/about-activities.md) se representan en el lienzo mediante iconos. Cada actividad tiene propiedades específicas y otras propiedades que son comunes a todas las actividades.

  En un lienzo de campaña orquestado, una actividad determinada puede producir varias tareas, en particular cuando hay un bucle o acciones recurrentes.

* **Transiciones**: las transiciones vinculan una actividad de origen a una actividad de destino y definen su secuencia.

* **Tablas de trabajo**: La tabla de trabajo contiene toda la información que contiene la transición. Cada campaña orquestada utiliza varias tablas de trabajo. Los datos transmitidos en estas tablas se pueden utilizar en todo el ciclo de vida de la campaña orquestada.

Una campaña orquestada típica de nivel básico sigue este patrón: **Generar audiencia → Bifurcar → Canal A + Canal B**.

Este método permite dirigirse a la misma audiencia con dos ramas paralelas en una sola ejecución de campaña; por ejemplo, una rama que utiliza un correo electrónico de marketing y otra que utiliza un correo electrónico transaccional. Cada rama es independiente y puede utilizar una configuración de canal, contenido de mensaje o categoría diferentes.

➡️ [Aprenda a utilizar la actividad de bifurcación](activities/fork.md)

➡️ [Comprender el marketing frente a los mensajes transaccionales](activities/channels.md#marketing-vs-transactional)

## Vídeo de introducción {#video-oc}

Conozca los conceptos y las capacidades clave disponibles con las campañas orquestadas.


>[!VIDEO](https://video.tv.adobe.com/v/3471538/?learn=on&enablevpops)


## Vamos a profundizar

Ahora que comprende cuáles son las campañas orquestadas, es hora de profundizar en estas secciones de documentación para empezar a trabajar con la función.

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="Acceso y administración de campañas" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>Pasos de configuración</strong></a>
</div>
<p>
</td>
<td>
<a href="create-orchestrated-campaign.md">
<img alt="Posible cliente" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong>Crear una campaña orquestada</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="Poco Frecuente" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>Trabajar con actividades</strong></a>
</div>
<p></td>
</tr></table>

## Recursos adicionales

* **[Cree su primera regla](build-query.md)**: domine el generador de reglas para crear consultas de destino y segmentar sus audiencias con precisión mediante datos relacionales.
* **[Crear esquemas relacionales](gs-schemas.md)**: aprenda a configurar esquemas relacionales para aprovechar datos de varias entidades en sus campañas.
* **[Informes para campañas orquestadas](reporting-campaigns.md)** - Rastrea y analiza el rendimiento de tu campaña con métricas y perspectivas detalladas para informes.
* **[Iniciar y supervisar campañas](start-monitor-campaigns.md)**: conozca las prácticas recomendadas para iniciar campañas y supervisar su ejecución en tiempo real.
* **[Protecciones y limitaciones](guardrails.md)**: revise las protecciones, limitaciones y prácticas recomendadas importantes para garantizar un rendimiento óptimo de la campaña.
* **[Preguntas más frecuentes](orchestrated-campaigns-faq.md)**: encuentre respuestas a preguntas comunes sobre las características, funcionalidades y casos de uso de las campañas orquestadas.
* **[Tutoriales de campañas orquestadas](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/create-campaigns/orchestrated-campaigns/introduction-to-orchestrated-campaigns){target="_blank"}**: explore tutoriales de vídeo paso a paso que cubren características y prácticas recomendadas.
