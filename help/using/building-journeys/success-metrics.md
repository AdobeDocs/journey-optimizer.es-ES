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
TQID: https://experienceleague.adobe.com/iHr0CFVSDz-4tOxNKyCyPZdwva3nfDyuU0Y5XHZEdjk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44feid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 595
ht-degree: 6%

---

# Configuración y seguimiento de la métrica de recorrido {#success-metrics}

Obtenga una visibilidad clara de la eficacia de los recorridos de sus clientes con las métricas de recorridos. Esta función le permite realizar un seguimiento del rendimiento con respecto a los KPI definidos, descubrir información sobre lo que funciona e identificar áreas para la optimización. Si mide el impacto en tiempo real, puede impulsar una mejora continua y tomar decisiones basadas en datos que aumenten la participación de los clientes.

## Requisitos previos {#prerequisites}

Antes de usar las métricas de recorrido, debe agregar un conjunto de datos que incluya los `Commerce Details`, `Web` y `Mobile` [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target="_blank"} en Configuración > Informes en [!DNL Adobe Experience Platform].

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

