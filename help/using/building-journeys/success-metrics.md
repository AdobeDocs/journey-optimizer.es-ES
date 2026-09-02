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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1153
ht-degree: 3%

---

# Configuración y seguimiento de la métrica de recorrido {#success-metrics}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a configurar y asignar métricas de recorridos para realizar un seguimiento del rendimiento en relación con los KPI y medir la efectividad de los recorridos de los clientes en tiempo real.

>[!ENDSHADEBOX]

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

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** En esta página se explica cómo configurar y realizar un seguimiento de las métricas de éxito de recorridos en Adobe Journey Optimizer, asignando un KPI a un recorrido y revisando su rendimiento en los informes de recorridos.

**Intenciones:**
* Añada los grupos de campos del conjunto de datos de AEP necesarios (Detalles de Commerce, Web, Móvil) como requisito previo para las métricas de recorrido
* Asignar una métrica de recorridos (KPI) a un recorrido durante la creación o configuración del recorrido
* Comprender qué métricas están disponibles en función de los grupos de campos de conjuntos de datos configurados
* Interprete los modelos de atribución para métricas de recorrido con licencias de Journey Optimizer y Customer Journey Analytics
* Creación de métricas de éxito personalizadas con una licencia de Customer Journey Analytics
* Rastrear el rendimiento del recorrido con el KPI asignado en los informes de recorrido

**Glosario:**
* **métricas de Recorrido**: KPI asignados a un recorrido para medir su efectividad, visibles en informes de recorrido *(específicos del producto)*
* **Atribución de último contacto**: El modelo de atribución predeterminado que acredita la interacción más reciente antes de una conversión
* **Grupo de campos Detalles de Commerce**: grupo de campos XDM que habilita métricas comerciales como Compras, Cierres de compra y Eventos de carro de compras
* **Ventana retrospectiva**: Intervalo de tiempo durante el cual se evalúa la atribución; establecido en un máximo de 7 días solo con licencia de Journey Optimizer

**Protecciones:**
* Solo se permite una métrica de recorridos por recorrido
* Los grupos de campos de conjuntos de datos (detalles de Commerce, web, móvil) deben seleccionarse entre las opciones integradas, no entre los grupos personalizados, y agregarse en Configuración > Informes en Adobe Experience Platform
* Sin un conjunto de datos configurado, solo están disponibles los clics, los clics únicos, la tasa de clics y la tasa de apertura
* La ventana retrospectiva máxima es de 7 días solo con una licencia de Journey Optimizer
* Las métricas personalizadas y la configuración de atribución personalizada requieren una licencia de Customer Journey Analytics

**Terminología:**
* Nombre canónico: métricas de Recorrido — Acrónimo: none — variantes: métricas de éxito, métricas de éxito de recorridos
* Nombre canónico: Tasa de clics — Acrónimo: CTR — variantes: none
* Nombre canónico: Tasa de apertura de clics — Acrónimo: CTOR — variantes: none
* Sinónimos: &quot;métricas de recorrido&quot; = &quot;métricas de éxito&quot; (utilizadas indistintamente en la interfaz de usuario y la documentación de )
* No confunda: &quot;Atribución de licencia de Journey Optimizer&quot; ≠ &quot;Atribución de Customer Journey Analytics&quot;. La licencia de CJA permite modelos de atribución personalizados y ventanas retrospectivas más largas

**PREGUNTAS MÁS FRECUENTES:**
* **Q: ¿Cuántas métricas de recorridos puedo asignar a un solo recorrido?** — Solo se permite una métrica de recorridos por recorrido.
* **Q: ¿Qué métricas están disponibles si no he configurado un conjunto de datos con grupos de campos?** — Solo los clics, los clics únicos, la tasa de clics y la tasa de apertura están disponibles sin necesidad de una configuración de grupo de campos adicional.
* **Q: ¿Qué grupos de campos necesito para habilitar las métricas de compra y comercio?** — Debe añadir el grupo de campos Detalles de Commerce a su conjunto de datos de informes en Adobe Experience Platform.
* **Q: ¿Cuál es el modelo de atribución predeterminado para las métricas de recorrido?** — Último contacto, que acredita la interacción más reciente antes de la conversión, con una ventana retrospectiva de 7 días como máximo con una licencia de Journey Optimizer.
* **Q: ¿Puedo crear métricas de éxito personalizadas?** — Sí, pero solo con una licencia de Customer Journey Analytics.
* **Q: ¿Dónde puedo ver los resultados de las métricas de recorrido después de publicar?** — en la tabla KPI y estadísticas de Recorrido del informe de recorrido.

+++
