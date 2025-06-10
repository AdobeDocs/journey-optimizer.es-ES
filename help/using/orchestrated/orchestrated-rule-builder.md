---
solution: Journey Optimizer
product: journey optimizer
title: Trabajar con el generador de reglas
description: Aprenda a crear reglas para sus campañas orquestadas
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: dd1a9b6e14617014756e5b4449578a1f7bf805b4
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 4%

---


# Trabajar con el generador de reglas {#orchestrated-rule-builder}

+++ Tabla de contenido

| Bienvenido a campañas orquestadas | Inicie su primera campaña orquestada | Consultar la base de datos | Actividades de campañas organizadas |
|---|---|---|---|
| [Introducción a las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>[Pasos de configuración](configuration-steps.md)<br/><br/>[Acceso y administración de campañas orquestadas](access-manage-orchestrated-campaigns.md) | [Pasos clave para la creación de campañas orquestadas](gs-campaign-creation.md)<br/><br/>[Cree y programe las actividades de la campaña](create-orchestrated-campaign.md)<br/><br/>[Orqueste actividades](orchestrate-activities.md)<br/><br/>[Envíe mensajes con campañas orquestadas](send-messages.md)<br/><br/>[Inicie y supervise la campaña](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | <b>[Trabaje con el generador de reglas](orchestrated-rule-builder.md)</b><br/><br/>[Cree su primera consulta](build-query.md)<br/><br/>[Edite expresiones](edit-expressions.md) | [Empiece con las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[Y únase](activities/and-join.md) - [Generar audiencia](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Combinar](activities/combine.md) - [Anulación de duplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [División](activities/split.md) - [Espera](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Las campañas organizadas incluyen un generador de reglas que simplifica el proceso de filtrado de la base de datos en función de varios criterios. El generador de reglas administra consultas muy complejas y largas de forma eficaz, lo que ofrece una mayor flexibilidad y precisión.

También admite filtros predefinidos dentro de las condiciones, lo que permite a los usuarios refinar las consultas con facilidad mientras utiliza expresiones avanzadas y operadores para estrategias completas de segmentación y segmentación de audiencia.

## Acceso al generador de reglas

El generador de reglas está disponible cuando se crea una consulta en una actividad **[!UICONTROL Generar audiencia]** para segmentar una audiencia. Permite especificar la población a la que desea dirigirse y crear sin esfuerzo nuevas audiencias adaptadas a sus necesidades.

![imagen que muestra una actividad de audiencia de compilación](assets/rule-builder-query.png)

## Interfaz del generador de reglas {#interface}

El generador de reglas proporciona un lienzo central en el que generar la consulta y un panel de propiedades que proporciona información sobre la regla.

![Imagen que muestra la interfaz del generador de reglas](assets/rule-builder-interface.png)

* En el **lienzo central** es donde se agregan y combinan los diferentes componentes para generar la regla. [Más información sobre cómo generar una regla](../orchestrated/build-query.md)

* El panel **[!UICONTROL Propiedades de regla]** proporciona información sobre la regla. Le permite realizar varias operaciones para comprobar la regla y asegurarse de que se adapta a sus necesidades.

  Este panel se muestra al crear una consulta para crear una audiencia. [Aprenda a comprobar y validar su consulta](build-query.md#check-and-validate-your-query)
