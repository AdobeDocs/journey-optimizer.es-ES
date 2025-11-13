---
solution: Journey Optimizer
product: journey optimizer
title: Publicación del recorrido
description: Obtenga información sobre cómo informar sobre las métricas de recorridos
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, recorrido, en directo, validez, comprobar
exl-id: 95d0267e-fab4-4057-8ab5-6f7c9c866b0f
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 3%

---

# Configuración y seguimiento de la métrica de recorrido {#success-metrics}

Obtenga una visibilidad clara de la eficacia de los recorridos de sus clientes con las métricas de recorridos. Esta función le permite realizar un seguimiento del rendimiento con respecto a los KPI definidos, descubrir información sobre lo que funciona e identificar áreas para la optimización. Si mide el impacto en tiempo real, puede impulsar una mejora continua y tomar decisiones basadas en datos que aumenten la participación de los clientes.

## Requisitos previos {#prerequisites}

Antes de usar las métricas de recorrido, debe agregar un conjunto de datos que incluya los `Commerce Details`, `Web` y `Mobile` [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target="_blank"} en Configuración > Informes en Adobe Experience Platform.

Estos grupos de campos deben seleccionarse entre las opciones integradas, no entre los grupos personalizados. Consulte la sección [Agregar conjuntos de datos](../reports/reporting-configuration.md#add-datasets).

## Métricas disponibles {#metrics}

La lista de métricas varía según los [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target="_blank"} incluidos en el conjunto de datos.

Si el conjunto de datos no está configurado, solo estarán disponibles las métricas siguientes: **[!UICONTROL Clic]**, **[!UICONTROL Clic único]**, **[!UICONTROL Tasa de clics]** y **[!UICONTROL Tasa de apertura]**.

Tenga en cuenta que con una licencia de Customer Journey Analytics puede crear métricas de éxito personalizadas. [Más información](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/participation-metric)


| Métricas | Grupo de campos relacionado |
|-|-|
| Clics | No se requiere ningún grupo de campos |
| Clics únicos | No se requiere ningún grupo de campos |
| Tasa de clics (CTR) | No se requiere ningún grupo de campos |
| Tasa de apertura de clics (CTOR) | No se requiere ningún grupo de campos |
| Page Views | Grupo de campos web |
| Lanzamientos de aplicaciones | Grupo de campos móviles |
| Primeros inicios de la aplicación | Grupo de campos móviles |
| Instalaciones de aplicación | Grupo de campos móviles |
| Actualizaciones de aplicaciones | Grupo de campos móviles |
| Compras | Grupo de campos Detalles de Commerce |
| Cierres de compra | Grupo de campos Detalles de Commerce |
| Adiciones al carro | Grupo de campos Detalles de Commerce |
| Aperturas de carrito | Grupo de campos Detalles de Commerce |
| Vistas del carro | Grupo de campos Detalles de Commerce |
| Eliminaciones del carro | Grupo de campos Detalles de Commerce |
| Vistas del producto | Grupo de campos Detalles de Commerce |
| Guardar para más tarde | Grupo de campos Detalles de Commerce |

## Atribución {#attribution}

Cada métrica viene con una atribución de conjunto que determina qué puntos de contacto o interacciones contribuyeron a un resultado específico.

* **Atribución de métricas con licencia de Journey Optimizer**:

  Solo con la licencia de Journey Optimizer, la ventana retrospectiva máxima disponible para cualquier métrica seleccionada se establece en 7 días. Para estas métricas, el modelo de atribución se establece de forma predeterminada en **Último contacto**, es decir, la interacción más reciente antes de la conversión.

  Por ejemplo, puede rastrear si una compra se realizó después de que un cliente interactuara con su recorrido en los últimos 7 días.

* **Atribución de métricas con licencia de Customer Journey Analytics**:

  Con las licencias de Journey Optimizer y Customer Journey Analytics, puede crear métricas personalizadas con configuraciones de atribución específicas o cambiar las atribuciones de las métricas integradas.

  Más información sobre [modelos de atribución](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)

## Asignar las métricas de recorrido {#assign}

>[!IMPORTANT]
>
>Solo se permite una métrica de recorridos por recorrido.

Para empezar a rastrear las métricas de recorridos, siga los pasos descritos a continuación:

1. En el menú de **[!UICONTROL Recorridos]**, haz clic en **[!UICONTROL Crear Recorrido]**.

1. Edite el panel de configuración del recorrido para definir el nombre del recorrido y sus propiedades. Aprenda a establecer las propiedades de su recorrido en [esta página](../building-journeys/journey-properties.md).

1. Elija sus **[!UICONTROL métricas de Recorridos]**, que se utilizarán para medir la efectividad de sus recorridos.

   Tenga en cuenta que las métricas se aplican al propio recorrido y se aplican a todos los elementos del recorrido.

   ![Panel de configuración de métricas de éxito en las propiedades del recorrido](assets/success_metric.png)

1. Haga clic en **[!UICONTROL Guardar]**.

1. Diseñe su recorrido con las **[!UICONTROL Actividades]** necesarias.

1. Pruebe y publique el recorrido.

1. Abra el informe de recorridos para realizar un seguimiento del rendimiento de las métricas de éxito asignadas.

   Las métricas seleccionadas se muestran en la tabla KPI y estadísticas de Recorrido del informe.

   ![Menú desplegable de métricas de éxito que muestra los eventos disponibles para el seguimiento de metas](assets/success_metric_2.png)

