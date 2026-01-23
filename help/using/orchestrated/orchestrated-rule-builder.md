---
solution: Journey Optimizer
product: journey optimizer
title: Trabajo con el generador de reglas
description: Aprenda a crear reglas para sus campañas organizadas
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
version: Campaign Orchestration
source-git-commit: f85fab10da9cea7c8fd8f83c9e01b6ba06a19e8c
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 76%

---


# Trabajo con el generador de reglas {#orchestrated-rule-builder}

Las campañas organizadas incluyen un generador de reglas que simplifica el proceso de filtrado de la base de datos en función de varios criterios. El generador de reglas administra consultas muy complejas y largas de forma eficaz, lo que ofrece una mayor flexibilidad y precisión.

También admite filtros predefinidos dentro de las condiciones, lo que le permite detallar las consultas con facilidad mientras utiliza expresiones avanzadas y operadores para estrategias completas de segmentación de público y segmentación.

## Acceso al generador de reglas

El generador de reglas está disponible en todos los contextos en los que necesita definir reglas para filtrar los datos.

| Uso | Ejemplo |
|  ---  |  ---  |
| **Crear audiencias**: especifique la población a la que quiera dirigirse en sus campañas orquestadas con una actividad de **[!UICONTROL Crear audiencia]** y cree nuevas audiencias adaptadas a sus necesidades sin esfuerzo. [Aprenda sobre la generación de público](../orchestrated/activities/build-audience.md). | ![Imagen que muestra cómo acceder a la interfaz de generación de públicos](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **Crear condición en el lienzo de campaña**: aplique reglas dentro del lienzo de campaña usando una actividad **[!UICONTROL División]** para alinearse con los requisitos específicos. [Aprenda a utilizar una actividad División](../orchestrated/activities/split.md) | ![Imagen que muestra cómo acceder a las opciones de personalización del flujo de trabajo](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **Crear filtros avanzados**: Genere reglas para filtrar los datos mostrados en listas como registros de campañas o dimensiones de segmentación. | ![Imagen que muestra cómo personalizar filtros de lista](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## Interfaz del generador de reglas {#interface}

El generador de reglas proporciona un lienzo central en el que se genera la consulta y un panel de propiedades que proporciona información sobre la regla.

![Imagen que muestra la interfaz del generador de reglas](assets/rule-builder-interface.png)

* En el **lienzo central** es donde se añaden y combinan los diferentes componentes para generar la regla. [Descubra cómo generar una regla](../orchestrated/build-query.md)

* El panel **[!UICONTROL Propiedades de regla]** proporciona información sobre la regla. Le permite realizar varias operaciones para comprobar la regla y asegurarse de que se adapta a sus necesidades.

  Este panel se muestra al armar una consulta para crear un público. [Aprenda a comprobar y validar su consulta](build-query.md#check-and-validate-your-query)
