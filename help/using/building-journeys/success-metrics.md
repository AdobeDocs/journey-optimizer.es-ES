---
solution: Journey Optimizer
product: journey optimizer
title: Publicar el recorrido
description: Obtenga información sobre cómo informar sobre la métrica de recorridos elegida
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publicar, recorrido, en directo, validez, comprobar
hide: true
hidefromtoc: true
exl-id: 95d0267e-fab4-4057-8ab5-6f7c9c866b0f
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 5%

---

# Configuración y seguimiento de la métrica de recorridos {#success-metrics}

Con las métricas de recorridos, puede medir de manera eficaz el impacto de sus actividades realizando un seguimiento de su rendimiento con respecto a las métricas predefinidas.
Al rastrear estas métricas, puede ver el rendimiento de su recorrido, identificar áreas que se pueden mejorar y tomar decisiones informadas para mejorar la participación de los clientes.

## Requisitos previos {#prerequisites}

Antes de usar la métrica de recorridos, debe agregar un conjunto de datos que incluya los `Commerce Details`, `Web`y `Mobile` [grupos de campos](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=es#field-group){target="_blank"}.

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
| Lanzamientos de la aplicación | Grupo de campos móviles |
| Primeros lanzamientos de la aplicación | Grupo de campos móviles |
| Instalaciones de la aplicación | Grupo de campos móviles |
| Actualizaciones de aplicaciones | Grupo de campos móviles |
| Compras | Grupo de campos Detalles de Commerce |
| Cierres de compra | Grupo de campos Detalles de Commerce |
| Adiciones al carro | Grupo de campos Detalles de Commerce |
| Aperturas de carrito | Grupo de campos Detalles de Commerce |
| Vistas del carro | Grupo de campos Detalles de Commerce |
| Eliminaciones del carro | Grupo de campos Detalles de Commerce |
| Vistas del producto | Grupo de campos Detalles de Commerce |
| Guardados para después | Grupo de campos Detalles de Commerce |

## Atribución {#attribution}

Cada métrica viene con una atribución de conjunto que determina qué puntos de contacto o interacciones contribuyeron a un resultado específico.

* **Atribución de métricas con licencia de Journey Optimizer**:

  Solo con la licencia de Journey Optimizer, la ventana retrospectiva máxima disponible para cualquier métrica seleccionada se establece en 7 días. Para estas métricas, el modelo de atribución se establece de forma predeterminada en **Último contacto**, es decir, la interacción más reciente antes de la conversión.

  Por ejemplo, puede rastrear si una compra se realizó después de que un cliente interactuara con su recorrido en los últimos 7 días.

* **Atribución de métricas con licencia de Customer Journey Analytics**:

  Con las licencias de Journey Optimizer y Customer Journey Analytics, puede crear métricas personalizadas con configuraciones de atribución específicas o cambiar las atribuciones de las métricas integradas.

  Más información sobre [modelos de atribución](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)

## Asignar la métrica de Recorridos {#assign}

Para empezar a rastrear la métrica de recorridos, siga los pasos descritos a continuación:

1. En el menú de **[!UICONTROL Recorridos]**, haz clic en **[!UICONTROL Crear Recorrido]**.

1. Edite el panel de configuración del recorrido para definir el nombre del recorrido y sus propiedades. Aprenda a establecer las propiedades de su recorrido en [esta página](../building-journeys/journey-properties.md).

1. Elija sus **[!UICONTROL métricas de Recorridos]**, que se utilizarán para medir la efectividad de sus recorridos.

   Tenga en cuenta que las métricas se aplican al propio recorrido y se aplican a todos los elementos del recorrido.

   ![](assets/success_metric.png)

1. Haga clic en **[!UICONTROL Guardar]**.

1. Diseñe su recorrido con las **[!UICONTROL Actividades]** necesarias.

1. Pruebe y publique el recorrido.

1. Abra el informe de recorridos para rastrear el rendimiento de la métrica de éxito asignada.

   La métrica que haya elegido se mostrará en la tabla KPI y estadísticas de Recorrido del informe.

   ![](assets/success_metric_2.png)
