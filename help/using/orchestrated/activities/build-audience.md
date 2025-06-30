---
solution: Journey Optimizer
product: journey optimizer
title: Uso de la actividad Generar audiencia
description: Aprenda a utilizar la actividad Generar audiencia en una campaña organizada
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 3f4652445bb52850d7480e844c77a4b67dc4db10
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 27%

---

# Generar público {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Actividad generar público"
>abstract="La actividad **Crear público** le permite definir el público que participará en la campaña orquestada. Al enviar mensajes en el contexto de una campaña orquestada, la audiencia de mensajes no se define en la actividad del canal, sino en una actividad de **Generar audiencia**."

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicio de su primera campaña organizada | Consultar la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](../gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](../configuration-steps.md)<br/><br/>[Pasos clave para la creación de campañas orquestadas](../gs-campaign-creation.md) | [Crear una campaña orquestada](../create-orchestrated-campaign.md)<br/><br/>[Organizar actividades](../orchestrate-activities.md)<br/><br/>[Enviar mensajes con campañas orquestadas](../send-messages.md)<br/><br/>[Iniciar y supervisar la campaña](../start-monitor-campaigns.md)<br/><br/>[Creación de informes](../reporting-campaigns.md) | [Trabaje con el Modeler de consultas](../orchestrated-rule-builder.md)<br/><br/>[Cree su primera consulta](../build-query.md)<br/><br/>[Editar expresiones](../edit-expressions.md) | [Empiece con las actividades](about-activities.md)<br/><br/>Actividades:<br/>[Y únase](and-join.md) - [Generar audiencia](build-audience.md) - [Cambiar dimensión](change-dimension.md) - [Combinar](combine.md) - [Anulación de duplicación](deduplication.md) - [Enriquecimiento](enrichment.md) - [Bifurcación](fork.md) - [Reconciliación](reconciliation.md) - [División](split.md) - [Espera](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Como especialista en marketing, puede crear segmentos de audiencia complejos a través de una interfaz intuitiva, lo que le permite dirigirse a los usuarios en función de una amplia gama de criterios y comportamientos para adaptar las campañas de forma más eficaz.

Para ello, use la actividad de segmentación **[!UICONTROL Generar audiencia]**. Esta actividad define la audiencia que entra en la campaña orquestada. Al enviar mensajes como parte de una campaña orquestada, la audiencia se define en la actividad **[!UICONTROL Generar audiencia]**, no dentro de la campaña orquestada.

## Configuración de la actividad Generar público {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Público"
>abstract="Seleccione el público, del mismo modo que utiliza un público a la hora de diseñar un nuevo envío."

Siga estos pasos para configurar la actividad **[!UICONTROL Generar público destinatario]**:

1. Añadir una actividad **[!UICONTROL Generar público destinatario]**.

   ![](../assets/build-audience.png)

1. Definir una **[!UICONTROL etiqueta]**.

1. Configure su audiencia siguiendo los pasos detallados en las pestañas a continuación.

1. Elija la **[!UICONTROL Dimensión de segmentación]**. La dimensión de segmentación permite definir la población a la que se dirige la operación: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc. De forma predeterminada, el público destinatario se selecciona entre los destinatarios.

1. Haga clic en **[!UICONTROL Continuar]**.

1. Utilice el modelador de consultas para definir la consulta. [Obtenga más información acerca del modelador de consultas en esta sección](../orchestrated-rule-builder.md)

1. Especifique si se debe generar una transición saliente cuando la audiencia está vacía.

## Ejemplos{#build-audience-examples}

Este es un ejemplo de una campaña orquestada con dos actividades **[!UICONTROL Generar audiencia]**. El primer segmenta a los perfiles que tienen artículos en el carro, seguidos de un envío de correo electrónico. El segundo segmenta los perfiles con una lista de deseos, seguida de una entrega de SMS.

![](../assets/build-audience-2.png)
