---
title: Creación de informes en Customer Journey Analytics
description: Obtenga información sobre cómo realizar informes en Customer Journey Analytics
feature: Experience Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="Disponibilidad limitada"
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: 2349145fcf698769d16326a19a48a413a3c1dd95
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 7%

---

# Creación de informes en Customer Journey Analytics {#cja}

Si trabaja con Customer Journey Analytics, puede crear paneles de informes personalizados para sus campañas basadas en código aprovechando Experience Decisioning.

A continuación se enumeran los pasos principales. Encontrará información detallada sobre cómo trabajar con el Customer Journey Analytics en la [documentación del Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Cree y configure una **conexión** en el Customer Journey Analytics. Esto le permite conectarse al conjunto de datos para el que desea crear informes. [Aprenda a crear una conexión](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Cree una **vista de datos** y asóciela a la conexión creada anteriormente. En la ficha **[!UICONTROL Componentes]**, elija los campos de esquema relevantes que desee que aparezcan en los informes. Para Experience Decisioning, asegúrese de incluir los campos **propositioninteraction** y **propositiondisplay**. [Aprenda a crear y configurar vistas de datos](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combine componentes, tablas y visualizaciones de datos en **proyectos del espacio de trabajo** para crear y compartir informes para su campaña basada en código.[Aprenda a crear proyectos del área de trabajo](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
