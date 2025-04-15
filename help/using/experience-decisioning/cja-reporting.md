---
title: Informe sobre la toma de decisiones
description: Aprenda a informar sobre la toma de decisiones.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: 4c0605d6ccff5cd62ef7aeb04e0610342d7cc3d5
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 5%

---


# Informe sobre la toma de decisiones {#decisioning-report}

## sistema de informes de campañas basadas en Code {#campaigns}

Una vez que las experiencias basadas en código están activas, puede acceder a informes dedicados a monitor indicadores clave de rendimiento (KPI) como un panel integral que ofrece una análisis de métricas esenciales asociadas con su campaña.

Esto engloba detalles relacionados con el rendimiento de los elementos de decisión y la forma en que los usuarios interactuaban con ellos. [Aprenda a trabajar con informes de experiencia basados en Code](../reports/campaign-global-report-cja-code.md)

![](../reports/assets/cja-decisioning-item-performance.png)

## Creación de informes en Customer Journey Analytics {#cja}

Si trabaja con Customer Journey Analytics, puede crear paneles de sistema de informes personalizados para sus campañas basadas en código aprovechando Decisioning.

A continuación se enumeran los pasos principales. En la [documentación](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"} del Customer Journey Analytics encontrará información detallada sobre cómo trabajar con Customer Journey Analytics.

1. Crear y configurar una **conexión** en Customer Journey Analytics. Esto le permite conectarse con la conjunto de datos para la que desea informes. [Aprenda a crear una conexión](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Crear un **vista** de datos y asociarlo a la conexión creada anteriormente. En el **[!UICONTROL pestaña Componentes]** , elija los campos de esquema relevantes que desea mostrar en sistema de informes. Para la toma de decisiones, asegúrese de incluir los **campos propositioninteract** y **propositiondisplay** . [Aprenda a crear y configurar vistas de datos](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combine componentes de datos, tablas y visualizaciones en proyectos **de espacio de trabajo para crear y compartir informes para sus campaña basados en** código. [Aprende a crear proyectos espacio de trabajo](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
