---
solution: Journey Optimizer
product: journey optimizer
title: Monitorización del rendimiento del desafío de fidelidad
description: Aprenda a utilizar los paneles de informes de Retos de fidelidad para rastrear las métricas de tarea y rendimiento de desafíos en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
source-git-commit: 0104f7b79145d7defee673fc6c9cd7d86fef3201
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 2%

---

# Monitorización del rendimiento del desafío de fidelidad {#loyalty-reporting}

>[!BEGINSHADEBOX]

**Tabla de contenido**

[Introducción a los retos de fidelización](get-started.md)

**Crear y administrar desafíos**

* [Acceder y administrar desafíos y tareas](access-loyalty-challenges.md)
* [Crear desafíos](create-challenges.md)
* [Creación de tareas](create-tasks.md)
* **Supervisar el rendimiento del desafío de lealtad** ◀︎ **Usted está aquí**

+++Configuración e integración

<!-- * [Configure loyalty challenges](loyalty-admin.md) -->
* [Datos y conjuntos de datos de fidelización](loyalty-data-and-datasets.md)
* [Referencia de API de retos de fidelización](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

+++

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta privada**. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](../rn/releases.md).

Los informes de Desafíos de fidelidad proporcionan paneles de nivel de desafío para que pueda realizar un seguimiento de métricas clave como el rendimiento de funnel de la audiencia, las tasas de finalización de tareas, la emisión de recompensas y el impacto en los ingresos. Todos los datos proceden de Adobe Customer Journey Analytics y se presentan en una interfaz personalizada y diseñada específicamente.

<!--
A direct **Analyze in CJA** button will be added to the reporting interface before the feature reaches general availability.
-->

## Acceso a informes de fidelidad {#access-reports}

Para abrir los paneles de informes de fidelidad, vaya a **[!UICONTROL Desafíos de fidelidad (Beta)]** en Journey Optimizer y seleccione **[!UICONTROL Informes de fidelidad]** en el panel de navegación izquierdo.

![](assets/reporting-home.png)

La interfaz de informes proporciona tres vistas, cada una con un nivel de detalle diferente. La **[Información general](#overview)** muestra un resumen de todos tus desafíos activos. Debajo, dos pestañas permiten cambiar entre vistas más granulares:

* **[Desafíos](#challenges-view)**: Un desglose por desafío con capacidad de desglose,
* **[Tareas](#tasks-view)**: una vista de nivel de tarea de las métricas de ingresos y finalización.

Puede ajustar el intervalo de fechas para todas las vistas utilizando el selector de fechas en la parte superior de la página. También hay disponibles ajustes preestablecidos de fecha estándar.

![](assets/reporting-date.png)

## Información general {#overview}

La página **Información general** muestra las métricas agregadas en todos los desafíos activos durante el período seleccionado.

![](assets/reporting-overview.png)

En la parte superior de la página se muestran las métricas siguientes:

**Miembros socio** - Cantidad de miembros del programa de fidelidad que estuvieron activos durante el período seleccionado.
**Suscripciones a desafíos**: número total de nuevas inscripciones a desafíos en todos los desafíos.
**Ingresos** - Ingresos totales vinculados a la actividad de desafío durante el período.
**Tasa promedio de finalización** - Porcentaje de clientes inscritos que completaron al menos un desafío.

Debajo de estas métricas, una cronología de **participación en el desafío diario** muestra cómo evolucionó la participación en el desafío a lo largo del período, trazando tres series:

* Clientes que **iniciaron** un desafío,
* Clientes que se movieron al estado **en curso**,
* Clientes que **completaron** un desafío.

## Vista de retos {#challenges-view}

La ficha **Desafíos** desglosa el rendimiento por desafío individual. Cada reto se muestra con columnas clave como Tipo, Estado, Inscripción, Finalización, etc. La lista se ordena por la fecha de la última modificación y muestra diez desafíos a la vez. Utilice el botón **Siguiente** de la parte inferior para buscar más información.

![](assets/reporting-challenges-tab.png)

Seleccione cualquier desafío de la lista para abrir su vista de detalles. El informe incluye varios bloques de métricas, como ingresos totales, inscripción, tasa de finalización y gráficos de tendencias, así como un desglose diario.

+++Ejemplo de informe de desafío

![](assets/reporting-challenge-report.png)

+++

## Vista de tareas {#tasks-view}

La ficha **Tareas** proporciona una vista de desafío cruzado del rendimiento de las tareas. Puede alternar entre tareas principales por ingresos y tareas principales por finalizaciones para centrarse en la métrica más relevante para usted.

La pestaña también resalta las 6 tareas principales por ingresos, lo que proporciona una vista rápida de qué tareas obtienen el mayor valor.

Debajo del gráfico radial, una lista de tareas muestra todas las tareas con columnas clave como Finalizaciones, Ingresos y los desafíos a los que pertenece cada tarea. La lista se ordena por ingresos y muestra diez tareas a la vez. Utilice el botón **Siguiente** para buscar más información.

![](assets/reporting-task-report.png)
