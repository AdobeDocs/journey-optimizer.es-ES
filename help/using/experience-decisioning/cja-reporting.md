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
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 270
ht-degree: 4%

---

# Informe sobre la toma de decisiones {#decisioning-report}

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
