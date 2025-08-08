---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las campañas organizadas
description: Obtenga información sobre cómo empezar con campañas organizadas
short-description: Descubra las funciones clave y los casos de uso de la campaña orquestada.
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 86bd6a100644a0f50aa9e18fd7023dec11c05bfe
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 24%

---


# Introducción a las campañas organizadas {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campaigns_overview_orchestrated"
>abstract="<b>Orquestación de campañas</b><br/>Divida, combine, enriquezca y manipule conjuntos de datos relacionales para definir su público<br/><br/> <b>Aproveche los datos de varias entidades</b><br/>Descubra cómo las campañas orquestadas pueden aprovechar los conjuntos de datos relacionales para enriquecer los datos para la segmentación y personalización<br/><br/><b>Segmentación ad hoc y recuentos exactos</b><br/>Cree su segmento paso a paso con recuentos exactos<br/><br/><b>Canales disponibles</b><br/>Correo electrónico, SMS, notificaciones push, Correo directo"

La organización de campañas en [!DNL Adobe Journey Optimizer] potencia campañas de marketing sofisticadas iniciadas por la marca en todos los canales, lo que le ayuda a aumentar la participación, los ingresos y la lealtad de los clientes a escala.

Aunque el marketing multicanal es esencial, las campañas orquestadas lo hacen fluido. Con una interfaz visual de arrastrar y soltar, puede diseñar y automatizar flujos de trabajo de marketing complejos, desde la segmentación hasta la entrega de mensajes, en varios canales. Todo sucede en un entorno intuitivo, creado para la velocidad, el control y la eficacia.

![](assets/canvas-example-diagram.png){zoomable="yes"}

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

## Campañas y recorridos organizados

Aunque la visualización de campañas orquestadas tiene similitudes con los recorridos, resuelve diferentes propósitos y casos de uso:

* **Recorridos**: lienzo de 1 a 1 en el que cada perfil viaja por los diferentes pasos a su propio ritmo. El estado de cada cliente se mantiene dentro de su contexto para almacenar en déclencheur las acciones en tiempo real.

* **Campañas orquestadas**: a diferencia de los recorridos, las campañas orquestadas funcionan con un lienzo por lotes que calcula los segmentos. Todos los perfiles se procesan juntos al mismo tiempo.

Ambos lienzos están optimizados para sus respectivos casos de uso: el lienzo de Recorrido publica recorridos que tienden a permanecer activos durante un período de tiempo más largo, mientras que el lienzo de campaña está diseñado para ejecuciones iterativas e incrementales de una campaña por lotes.

## ¿Qué hay dentro de una campaña orquestada? {#gs-ms-campaign-inside}

El lienzo de campaña orquestada es una representación de lo que se supone que debe suceder. Describe las diversas tareas que se realizan y cómo se relacionan entre sí.

![imagen que muestra un lienzo de campaña orquestado](assets/canvas-example.png)

Cada campaña orquestada contiene:

* **Actividades**: una actividad es una tarea que se va a realizar. Las distintas actividades disponibles se representan en el diagrama mediante iconos. Cada actividad tiene propiedades específicas y otras propiedades que son comunes a todas las actividades.

  En un diagrama de campaña orquestada, una actividad determinada puede producir varias tareas, en particular cuando hay un bucle o una acción recurrente.

* **Transiciones**: las transiciones vinculan una actividad de origen a una actividad de destino y definen su secuencia.

* **Tablas de trabajo**: estas contienen toda la información de la transición. Cada campaña orquestada utiliza varias tablas de trabajo. Los datos transmitidos en estas tablas se pueden utilizar en todo el ciclo de vida de la campaña orquestada.

## Vamos a profundizar

Ahora que comprende lo que son las campañas orquestadas, es hora de profundizar en estas secciones de documentación para empezar a trabajar con la función.

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
<img alt="Poco frecuente" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>Trabajo con actividades</strong></a>
</div>
<p></td>
</tr></table>
