---
title: Informe sobre la toma de decisiones
description: Obtenga información sobre cómo informar sobre Decisioning.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="Disponibilidad limitada"
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: baf3a8dba9e83e3b82390bd2ab0725b9fc844138
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 5%

---


# Informe sobre la toma de decisiones {#decisioning-report}

## Creación de informes de campañas basadas en código {#campaigns}

Una vez que las experiencias basadas en código estén activas, puede acceder a informes dedicados para monitorizar los indicadores de rendimiento clave (KPI) como un panel que abarca todo, que ofrece un análisis de las métricas esenciales asociadas con su campaña.

Esto incluye detalles relacionados con el rendimiento de los elementos de decisión y la forma en que los usuarios interactuaron con ellos. [Aprenda a trabajar con informes de experiencia basados en código](../reports/campaign-global-report-cja-code.md)

![](../reports/assets/cja-decisioning-item-performance.png)

## Creación de informes en Customer Journey Analytics {#cja}

Si está trabajando con Customer Journey Analytics, puede crear paneles de informes personalizados para sus campañas basadas en código aprovechando Decisioning.

A continuación se enumeran los pasos principales. Encontrará información detallada sobre cómo trabajar con Customer Journey Analytics en la [documentación de Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Cree y configure una **conexión** en Customer Journey Analytics. Esto le permite conectarse al conjunto de datos para el que desea crear informes. [Aprenda a crear una conexión](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Cree una **vista de datos** y asóciela a la conexión creada anteriormente. En la ficha **[!UICONTROL Componentes]**, elija los campos de esquema relevantes que desee que aparezcan en los informes. Para Decisioning, asegúrese de incluir los campos **propositioninteraction** y **propositiondisplay**. [Aprenda a crear y configurar vistas de datos](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combine componentes, tablas y visualizaciones de datos en **proyectos del espacio de trabajo** para crear y compartir informes para su campaña basada en código. [Aprenda a crear proyectos del área de trabajo](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
