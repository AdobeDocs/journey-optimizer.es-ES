---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con el generador de reglas
description: Aprenda a crear reglas para sus campañas organizadas
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 87%

---


# Trabajo con el generador de reglas {#orchestrated-rule-builder}

+++ Índice

| Bienvenido a las campañas organizadas | Inicio de su primera campaña organizada | Consulta de la base de datos | Actividades de las campañas organizadas |
|---|---|---|---|
| [Empiece a usar las campañas orquestadas](gs-orchestrated-campaigns.md)<br/><br/>Cree y administre conjuntos de datos y esquemas relacionales:</br> <ul><li>[Introducción a esquemas y conjuntos de datos](gs-schemas.md)</li><li>[Esquema manual](manual-schema.md)</li><li>[Esquema de carga de archivos](file-upload-schema.md)</li><li>[Ingesta de datos](ingest-data.md)</li></ul>[Acceder y administrar campañas orquestadas](access-manage-orchestrated-campaigns.md)<br/><br/>[Pasos clave para crear una campaña orquestada](gs-campaign-creation.md) | [Creación y programación de las campañas](create-orchestrated-campaign.md)<br/><br/>[Organización de actividades](orchestrate-activities.md)<br/><br/>[Inicio y monitorización de las campañas](start-monitor-campaigns.md)<br/><br/>[Creación de informes](reporting-campaigns.md) | <b>[Trabajo con el generador de reglas](orchestrated-rule-builder.md)</b><br/><br/>[Creación de su primera consulta](build-query.md)<br/><br/>[Edición de expresiones](edit-expressions.md)<br/><br/>[Resegmentación](retarget.md) | [Introducción a las actividades](activities/about-activities.md)<br/><br/>Actividades:<br/>[AND-join](activities/and-join.md) - [Generar público](activities/build-audience.md) - [Cambiar dimensión](activities/change-dimension.md) - [Actividades del canal](activities/channels.md) - [Combinar](activities/combine.md) - [Deduplicación](activities/deduplication.md) - [Enriquecimiento](activities/enrichment.md) - [Bifurcación](activities/fork.md) - [Reconciliación](activities/reconciliation.md) - [Guardar público](activities/save-audience.md) - [División](activities/split.md) - [Esperar](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

El contenido de esta página no es definitivo y puede estar sujeto a cambios.

>[!ENDSHADEBOX]

Las campañas organizadas incluyen un generador de reglas que simplifica el proceso de filtrado de la base de datos en función de varios criterios. El generador de reglas administra consultas muy complejas y largas de forma eficaz, lo que ofrece una mayor flexibilidad y precisión.

También admite filtros predefinidos dentro de las condiciones, lo que le permite detallar las consultas con facilidad mientras utiliza expresiones avanzadas y operadores para estrategias completas de segmentación de público y segmentación.

## Acceso al generador de reglas

El modelador de consultas está disponible en todos los contextos en los que necesite definir reglas para filtrar datos.

| Uso | Ejemplo |
|  ---  |  ---  |
| **Generar públicos**: especifique la población a la que quiera dirigirse en sus campañas organizadas mediante la actividad **[!UICONTROL Generar público]** y genere sin esfuerzo nuevos públicos adaptados a sus necesidades. [Aprenda sobre la generación de público](../orchestrated/activities/build-audience.md). | ![Imagen que muestra cómo acceder a la interfaz de generación de públicos](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **Crear condición en el lienzo de campaña**: aplique reglas dentro del lienzo de campaña usando una actividad **[!UICONTROL División]** para alinearse con los requisitos específicos. [Aprenda a utilizar una actividad División](../orchestrated/activities/split.md) | ![Imagen que muestra cómo acceder a las opciones de personalización del flujo de trabajo](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **Crear filtros avanzados**: genere reglas para filtrar los datos mostrados en listas como los registros de flujo de trabajo o las dimensiones de segmentación. | ![Imagen que muestra cómo personalizar filtros de lista](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## Interfaz del generador de reglas {#interface}

El generador de reglas proporciona un lienzo central en el que se genera la consulta y un panel de propiedades que proporciona información sobre la regla.

![Imagen que muestra la interfaz del generador de reglas](assets/rule-builder-interface.png)

* En el **lienzo central** es donde se añaden y combinan los diferentes componentes para generar la regla. [Descubra cómo generar una regla](../orchestrated/build-query.md)

* El panel **[!UICONTROL Propiedades de regla]** proporciona información sobre la regla. Le permite realizar varias operaciones para comprobar la regla y asegurarse de que se adapta a sus necesidades.

  Este panel se muestra al armar una consulta para crear un público. [Aprenda a comprobar y validar su consulta](build-query.md#check-and-validate-your-query)
