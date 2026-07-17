---
solution: Journey Optimizer
product: journey optimizer
title: Monitorización del rendimiento del desafío de fidelidad
description: Aprenda a utilizar los paneles de informes de Retos de fidelidad para rastrear el rendimiento y las perspectivas de los desafíos en Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Beta privada" type="Informative"
mini-toc-levels: 1
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
feature_v2: []
subfeature_v2: []
source-git-commit: 762afe791cc1fa826b7a9f35f6f54591590bab7c
workflow-type: tm+mt
source-wordcount: 592
ht-degree: 4%

---

# Monitorización del rendimiento del desafío de fidelidad {#loyalty-reporting}

>[!BEGINSHADEBOX]

**Tabla de contenido**

[Introducción a los retos de fidelización](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Crear y administrar desafíos**

* [Acceder y administrar desafíos y tareas](access-loyalty-challenges.md)
* [Crear desafíos](create-challenges.md)
* [Creación de tareas](create-tasks.md)
* **Supervisar el rendimiento del desafío de lealtad** ◀︎ **Usted está aquí**

</td>
<td style="vertical-align:top;">

**Configurar e integrar**

* [Configuración de desafíos de lealtad](loyalty-admin.md)
* [Guía de definición de recompensa](reward-definition-guide.md)
* [Guía del transformador de eventos](event-transformer-guide.md)
* [Datos y conjuntos de datos de fidelización](loyalty-data-and-datasets.md)
* [Referencia de API de retos de fidelización](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Esta característica se encuentra actualmente en **versión beta privada**. Para obtener información detallada acerca del ciclo de lanzamiento y las fases de disponibilidad, consulte [Ciclo de lanzamiento de Journey Optimizer](../rn/releases.md).

Utilice los informes Retos de fidelización para ver el rendimiento de los desafíos. Compruebe quién se inscribe, quién completa los desafíos y cuántos ingresos genera su programa, todo en un solo lugar. Los datos proceden de Adobe Customer Journey Analytics.

Para abrir los paneles de informes, vaya a **[!UICONTROL Desafíos de fidelización (Beta)]** en Journey Optimizer y seleccione **[!UICONTROL Informes de fidelización]** en el panel de navegación izquierdo.

La interfaz de informes tiene dos pestañas:

* **[Informes](#reports-view)**: números y gráficos para tus desafíos.
* **[Datos](#insights-cards)**: tarjetas que destacan lo que merece tu atención en este momento.

## Vista Informes {#reports-view}

La ficha **Informes** le ofrece una descripción general del rendimiento de su programa durante el período seleccionado. Utilice el selector de fechas en la parte superior de la página y seleccione el botón **[!UICONTROL Aplicar filtro]** para cambiar el período de informe y ver los números y gráficos actualizados.

![](assets/reporting-challenge-key.png)

El área de **métricas clave** muestra cuatro números de un vistazo. Cada métrica también muestra un cambio porcentual en comparación con el período anterior.

* **Miembros socio**: Cuántos miembros socio estaban activos durante el período.
* **Suscripciones al desafío**: Cuántas veces se inscribieron los miembros en un desafío.
* **Ingresos**: Ingresos totales vinculados a la actividad de desafío.
* **Tasa promedio de finalización**: Porcentaje de miembros inscritos que finalizaron al menos un desafío.

El panel **Últimas perspectivas** de la derecha muestra las perspectivas generadas por IA más recientes de su programa. Seleccione **[!UICONTROL Ver todo]** para abrir la ficha **Información** completa.

Debajo de las métricas clave, la sección **Desafíos** le ofrece dos vistas de la actividad del desafío.

![](assets/reporting-challenge-challenges.png)

* **Participación en el desafío**: Una cronología que muestra cuántos miembros iniciaron, están en curso y completaron desafíos durante el período.
* **Informes de desafíos**: Una tabla de todos tus desafíos con detalles como tipo, tareas, estado y números de inscripción. Utilice la barra de búsqueda para encontrar un desafío específico. Seleccione un desafío para ver su informe completo con tendencias de participación y detalles de rendimiento.

  +++Ejemplo de informe de desafío

  ![](assets/reporting-challenge-report.png)

  +++

## Pestaña Perspectivas {#insights-cards}

La pestaña **Insights** muestra tarjetas generadas por IA que marcan anomalías, tendencias y oportunidades en su programa de fidelidad. Cada tarjeta representa una sola observación y se clasifica según su importancia en relación con los datos actuales del programa.

![](assets/reporting-insights.png)

La marca de tiempo **Última rastreada** en la parte superior derecha muestra la última vez que el motor de insight procesó los datos del programa.

### Acciones de tarjeta {#insight-card-actions}

Cada tarjeta tiene un menú ![](assets/do-not-localize/Smock_More_18_N.svg) con dos acciones:

* **Descartar**: quita permanentemente la tarjeta de la lista de perspectivas.
* **Posponer**: oculta la tarjeta temporalmente. Elija posponer por **1 día**, **3 días** o **7 días**. La tarjeta vuelve a aparecer una vez finalizado el periodo de inactividad.

<!--
### Priority badges {#insight-badges}

Each card has a priority badge — **High**, **Medium**, or **Low** — based on how significant the underlying signal is relative to your current program data. These levels are relative: there are always a few **High** cards, even in a quiet week. **High** means "most relevant right now", not that a fixed threshold was crossed.
-->

### Etiquetas de categoría {#insight-category-tags}

Cada tarjeta lleva una **etiqueta category** que identifica a qué parte del programa se relaciona insight.

| Categoría | Qué cubre |
| --- | --- |
| **En todo el programa** | Estado general y rendimiento de su programa de fidelización |
| **Nivel** | Ganar tasas, movimientos y distribución entre niveles de miembros |
| **Desafío** | Actividad, tasas de finalización y anomalías para un desafío específico o entre desafíos |
| **Producto** | Rendimiento del catálogo de productos, incluidas vistas, reembolsos y tendencias de nivel de catálogo |
| **Ciclo de vida del miembro** | Cómo progresan los miembros en las fases de inscripción, participación y cancelación |
| **Tendencia** | Patrones basados en el tiempo, como ciclos semanales, picos estacionales o reversiones de tendencias |
