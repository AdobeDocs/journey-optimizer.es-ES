---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a las campañas organizadas
description: Obtenga información sobre cómo empezar con campañas orquestadas
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 8f32edf905ed80ca4a23d4b9afe2805c000dacef
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 6%

---

# Introducción a las campañas organizadas {#orchestrated-camp}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| <b>[Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)</b><br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](orchestrate-activities.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | [Trabaje con el generador de reglas](orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md)<br/><br/>[Redireccionamiento](retarget.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades de canal](activities/channels.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar](activities/save-audience.md) - [División](activities/split.md) [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

La organización de campañas en [!DNL Adobe Journey Optimizer] potencia campañas de marketing sofisticadas iniciadas por la marca en todos los canales, lo que le ayuda a aumentar la participación, los ingresos y la lealtad de los clientes a escala.

Aunque el marketing multicanal es esencial, las campañas orquestadas lo hacen fluido. Con una interfaz visual de arrastrar y soltar, puede diseñar y automatizar flujos de trabajo de marketing complejos, desde la segmentación hasta la entrega de mensajes, en varios canales. Todo sucede en un entorno intuitivo, creado para la velocidad, el control y la eficacia.

Este módulo trae **orquestación de campaña por lotes** a [!DNL Journey Optimizer], lo que le permite:

* Genere y ejecute **campañas de varios pasos** (por ejemplo, promociones de temporada, lanzamientos de nuevos productos),
* Ofrecer **mensajes personalizados y coherentes** en cualquier canal,
* Coordinar la **segmentación, el procesamiento de archivos y la administración de tareas** en un solo lugar,
* Potenciar la colaboración mediante aprobaciones y asignaciones de tareas

## Funcionalidades principales

La organización de campañas se basa en cuatro pilares clave:

<table>
<tr style="border: 0;">
<td><img alt="Audiencias a la carta" src="assets/do-not-localize/icon-audience.svg"></a></td><td><b>Las audiencias a petición</b><br/>consultan instantáneamente entre conjuntos de datos para crear segmentos de audiencia usando cualquier combinación de tipos de datos y dimensiones.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentación y envío de varias entidades" src="assets/do-not-localize/icon-audience.svg"></a></td><td><b>Segmentación y envío de varias entidades</b><br/>Vaya más allá de las campañas basadas en personas: use entidades como catálogos de productos, ubicaciones de tiendas o datos de servicio para segmentar con precisión.</td></tr>
<tr style="border: 0;">
<td><img alt="Visibilidad y precisión previas al envío" src="assets/do-not-localize/icon-audience.svg"></a></td><td><b>Visibilidad y precisión previas al envío</b><br/>Obtenga recuentos de segmentación exactos y un ámbito de campaña completo antes del lanzamiento, lo que garantiza precisión y confianza.</td></tr>
<tr style="border: 0;">
<td><img alt="Flujos de trabajo de campaña de varios pasos" src="assets/do-not-localize/icon-audience.svg"></a></td><td><b>Flujos de trabajo de campañas de varios pasos</b><br/>Diseña campañas de varios pasos, desde mensajes diarios hasta campañas complejas como promociones de temporada o lanzamientos de productos importantes.</td></tr>
</table>

## Campañas y recorridos organizados

Aunque la visualización de campañas orquestadas tiene similitudes con los recorridos, resuelve diferentes propósitos y casos de uso:

* **Recorridos**: lienzo de 1 a 1 en el que cada perfil viaja por los diferentes pasos a su propio ritmo. El estado de cada cliente se mantiene dentro de su contexto para almacenar en déclencheur las acciones en tiempo real.

* **Campañas orquestadas**: a diferencia de los recorridos, las campañas orquestadas funcionan con un lienzo por lotes que calcula los segmentos. Todos los perfiles se procesan juntos al mismo tiempo.

## Requisitos previos

Antes de trabajar con campañas orquestadas, es esencial asegurarse de que tiene los permisos adecuados. El acceso a las campañas orquestadas está restringido a los usuarios asignados a un **[!UICONTROL perfil de producto]** relevante, como administrador de campañas orquestadas, aprobador de campañas orquestadas, administrador de campañas orquestadas o visor de campañas orquestadas.

Si no puede acceder a las funcionalidades de la campaña orquestada, póngase en contacto con el administrador para solicitar los permisos necesarios.

➡️[Más información acerca de perfiles de productos relacionados con Campañas orquestadas](../administration/ootb-product-profiles.md)

## Vamos a profundizar

Ahora que comprende lo que son las campañas orquestadas, es hora de profundizar en estas secciones de documentación para empezar a trabajar con la función.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="gs-campaign-creation.md">
<img alt="Acceso y administración de flujos de trabajo" src="assets/do-not-localize/workflow-access.jpeg">
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
<a href="activities/about-activities.md"><strong>Trabajar con actividades</strong></a>
</div>
<p></td>
</tr></table>
