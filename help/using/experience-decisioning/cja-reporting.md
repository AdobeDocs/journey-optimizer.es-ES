---
title: Informe sobre la toma de decisiones
description: Obtenga información sobre cómo informar sobre Decisioning.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/jbakmb7S9cFitmpa7ypVe8YrYvbZh0E0VogYi3KpNbo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee394c77b226dd35a9c27f4a02e3b8d7a997ccbd
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 3%

---

# Informe sobre la toma de decisiones {#decisioning-report}

>[!BEGINSHADEBOX]

**En esta página:** Acceda a informes específicos de decisiones y cree paneles de Customer Journey Analytics para poder supervisar los indicadores clave de rendimiento y analizar cómo los clientes interactúan con los elementos de decisión.

>[!ENDSHADEBOX]

## Informes de decisiones {#campaigns}

Una vez que los recorridos o las campañas con estrategias de selección están activos, puede acceder a informes específicos para monitorizar los Indicadores clave de rendimiento (KPI) de decisiones.

<!--
Once code-based experiences are live, you can access dedicated reports to monitor Key Performance Indicators (KPIs) as an all-encompassing dashboard, delivering an analysis of essential metrics associated with your campaign.

This encompasses details related to the decision items performances and how users interacted with them. [Learn how to work with Code-based experience reports](../reports/campaign-global-report-cja-code.md)
-->

![](../reports/assets/cja-decisioning-kpis.png)

También puede acceder a los detalles relacionados con el rendimiento de los elementos de decisión y cómo interactuaron los usuarios con ellos, lo que ofrece un análisis de las métricas esenciales asociadas con la campaña.

![](../reports/assets/cja-decisioning-item-performance.png)

Aprenda a trabajar con los informes de experiencias basadas en código sobre Decisioning en [esta sección](../reports/campaign-global-report-cja-code.md#decisioning-reporting).

## Creación de informes en Customer Journey Analytics {#cja}

Si está trabajando con Customer Journey Analytics, puede crear paneles de informes personalizados para sus campañas basadas en código aprovechando Decisioning.

A continuación se enumeran los pasos principales. Encontrará información detallada sobre cómo trabajar con Customer Journey Analytics en la [documentación de Customer Journey Analytics](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Cree y configure una **conexión** en Customer Journey Analytics. Esto le permite conectarse al conjunto de datos para el que desea crear informes. [Aprenda a crear una conexión](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Cree una **vista de datos** y asóciela a la conexión creada anteriormente. En la ficha **[!UICONTROL Componentes]**, elija los campos de esquema relevantes que desee que aparezcan en los informes. Para Decisioning, asegúrese de incluir los campos **propositioninteraction** y **propositiondisplay**. [Aprenda a crear y configurar vistas de datos](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combine componentes, tablas y visualizaciones de datos en **proyectos del espacio de trabajo** para crear y compartir informes para su campaña basada en código. [Aprenda a crear proyectos de Workspace](https://experienceleague.adobe.com/es/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
