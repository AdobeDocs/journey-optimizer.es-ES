---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las campañas orquestadas
description: Obtenga información sobre cómo empezar con campañas orquestadas
short-description: Descubra las características clave y los casos de uso de las campañas orquestadas
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
version: Campaign Orchestration
source-git-commit: 4d5505cbb46bdff846218bfc3657c6a6e5447af3
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 93%

---


# Introducción a las campañas orquestadas {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campaigns_overview_orchestrated"
>abstract="<b>Orquestación de campañas</b><br/>Divida, combine, enriquezca y manipule conjuntos de datos relacionales para definir su público<br/><br/> <b>Aproveche los datos de varias entidades</b><br/>Descubra cómo las campañas orquestadas pueden aprovechar los conjuntos de datos relacionales para enriquecer los datos para la segmentación y personalización<br/><br/><b>Segmentación ad hoc y recuentos exactos</b><br/>Cree su segmento paso a paso con recuentos exactos<br/><br/><b>Canales disponibles</b><br/>Correo electrónico, SMS, notificaciones push, Correo directo"

La orquestación de campañas en [!DNL Adobe Journey Optimizer] impulsa campañas de marketing sofisticadas iniciadas por la marca en todos los canales, lo que le ayuda a fomentar la participación, los ingresos y la lealtad de los clientes a escala.

>[!IMPORTANT]
>
>Para acceder a Campaign Orchestration, la licencia debe incluir **Journey Optimizer - Campañas y Recorridos** o el paquete **Journey Optimizer - Campañas**. Póngase en contacto con su representante de Adobe para confirmar su licencia y actualizarla si es necesario.

Aunque el marketing de múltiples canales es esencial, las campañas orquestadas lo hacen fluido. Con una interfaz visual de arrastrar y soltar, puede diseñar y automatizar flujos de trabajo de marketing complejos, desde la segmentación hasta el envío de mensajes, en varios canales. Todo sucede en un entorno intuitivo, creado para ofrecer velocidad, control y eficacia.

![](assets/canvas-example-diagram.png){zoomable="yes"}

➡️ [Descubra campañas orquestadas en vídeo](#video-oc)

## Funcionalidades principales

La orquestación de campañas se basa en cuatro pilares clave:

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="Públicos bajo demanda" src="assets/do-not-localize/icon-audience.svg" width="150px"></a></td><td><b>Los públicos bajo demanda</b><br/>consultan instantáneamente entre conjuntos de datos para crear segmentos de audiencia usando cualquier combinación de tipos de datos y dimensiones.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentación y envío de varias entidades" src="assets/do-not-localize/icon-entity.svg" width="150px"></a></td><td><b>Segmentación y envío de varias entidades</b><br/>Vaya más allá de las campañas basadas en personas: use entidades como catálogos de productos, ubicaciones de tiendas o datos de servicio para segmentar con precisión.<br/><br/>
Admitir el envío de varios niveles, donde se envía un mensaje por perfil y por entidad secundaria asociada. Estas entidades secundarias pueden incluir direcciones de contacto, reservas, suscripciones, contratos u otros datos vinculados. Por ejemplo, esto permite enviar campañas a todas las direcciones conocidas de un perfil o a todas las reservas asociadas con ese perfil.</td></tr>
<tr style="border: 0;">
<td><img alt="Visibilidad y precisión previas al envío" src="assets/do-not-localize/icon-visibility.svg" width="150px"></a></td><td><b>Visibilidad y precisión previas al envío</b><br/>Obtenga recuentos de segmentación exactos y un ámbito de campaña completo antes del lanzamiento, lo que garantiza precisión y confianza.</td></tr>
<tr style="border: 0;">
<td><img alt="Flujos de trabajo de campañas de varios pasos" src="assets/do-not-localize/icon-multistep.svg" width="150px"></a></td><td><b>Flujos de trabajo de campañas de varios pasos</b><br/>Diseñe campañas de varios pasos, desde mensajes diarios hasta campañas complejas como promociones de temporada o lanzamientos de productos importantes.</td></tr>
</table>


>[!NOTE]
>
>Los canales admitidos son: [Correo electrónico](../email/get-started-email.md), [SMS/MMS/RCS](../sms/get-started-sms.md), [Notificaciones push](../push/get-started-push.md).
>
>Los canales disponibles varían en función del modelo de licencia y los complementos.

## Campañas y recorridos orquestados

Aunque la visualización de campañas orquestadas tiene similitudes con los recorridos, resuelve diferentes propósitos y casos de uso:

* **Recorridos**: lienzo de 1 a 1 en el que cada perfil recorre los diferentes pasos a su propio ritmo. El estado de cada cliente se mantiene dentro de su contexto para activar acciones en tiempo real.

* **Campañas orquestadas**: a diferencia de los recorridos, las campañas orquestadas funcionan con un lienzo por lotes que calcula los segmentos. Todos los perfiles se procesan juntos al mismo tiempo.

Ambos lienzos están optimizados para sus respectivos casos de uso: el lienzo de Recorrido publica recorridos que tienden a permanecer activos durante un período de tiempo más largo, mientras que el lienzo de campaña está diseñado para ejecuciones iterativas e incrementales de una campaña por lotes.

## ¿Qué hay dentro de una campaña orquestada? {#gs-ms-campaign-inside}

El lienzo de la campaña orquestada es una representación de lo que se supone que debe suceder. Describe las diversas tareas que se realizan y cómo se relacionan entre sí.

![imagen que muestra el lienzo de una campaña orquestada](assets/canvas-example.png)

Cada campaña orquestada contiene:

* **Actividades**: una actividad es una tarea que se va a realizar. Las [diversas actividades](activities/about-activities.md) se representan en el lienzo mediante iconos. Cada actividad tiene propiedades específicas y otras que son comunes a todas las actividades.

  En un lienzo de campaña organizada, una actividad determinada puede producir varias tareas, en particular cuando hay un bucle o acciones recurrentes.

* **Transiciones**: las transiciones vinculan una actividad de origen a una actividad de destino y definen su secuencia.

* **Tablas de trabajo**: estas contienen toda la información de la transición. Cada campaña orquestada utiliza varias tablas de trabajo. Los datos que contienen estas tablas se pueden utilizar a lo largo de todo el ciclo de vida de la campaña orquestada.


## Vídeo de introducción {#video-oc}

Conozca los conceptos y las capacidades clave disponibles con las campañas orquestadas.


>[!VIDEO](https://video.tv.adobe.com/v/3471538/?learn=on&enablevpops)


## Vamos a profundizar

Ahora que ya sabe qué son las campañas orquestadas, es el momento de profundizar en estas secciones de la documentación para empezar a trabajar con esta función.

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
<div><a href="create-orchestrated-campaign.md"><strong>Creación de una campaña organizada</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="Poco frecuente" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>Trabajo con actividades</strong></a>
</div>
<p></td>
</tr></table>
