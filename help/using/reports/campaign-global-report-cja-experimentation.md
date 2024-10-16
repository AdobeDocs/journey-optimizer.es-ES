---
solution: Journey Optimizer
product: journey optimizer
title: Informe de campaña
description: Aprenda a utilizar los datos de experimentación del informe de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 10%

---

# Informe de campaña de experimentación {#campaign-global-report-cja-experimentation}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Métrica de éxito"
>abstract="El valor total de la métrica de éxito, previamente seleccionada al crear los experimentos, dividido por el número de perfiles."

## Experimentación {#experimentation}

La ficha **[!UICONTROL Experimentación]** proporciona información clave sobre el rendimiento de cada variante e identifica la que ha tenido más éxito.

Tenga en cuenta que definir el mejor ejecutante puede llevar algún tiempo. Si el experimento no se realiza correctamente, se establecerá en **No concluyente**.

![](assets/cja-experimentation-1.png)

### KPI de experimentación {#experimentation-kpis}

![](assets/cja-experimentation-kpis.png)

Los indicadores clave de rendimiento (KPI) de **[!UICONTROL Experimentación]** funcionan como un tablero que abarca todo, y ofrecen un análisis de las métricas esenciales asociadas con la experimentación.

+++ Más información sobre las métricas de KPI de experimentación

* **[!UICONTROL Alza]**: medición de la mejora porcentual en la tasa de conversión de un tratamiento determinado respecto al valor de referencia.

* **[!UICONTROL Confianza]**: Evidencia de que un tratamiento dado es el mismo que el tratamiento basal. [Más información](../content-management/experiment-calculations.md#understand-confidence)

+++

### Variante por clics entrantes {#variant-inbound}

![](assets/cja-experimentation-variants.png)

El widget **[!UICONTROL Variante por clics entrantes]** detalla el rendimiento de cada variante.
Para profundizar en estos resultados y cómo interpretarlos, consulte [esta página](../content-management/get-started-experiment.md#interpret-results).

+++ Más información sobre las métricas Variante por clics entrantes

* **[!UICONTROL Personas]**: Número de perfiles de usuario que se califican como perfiles de destino para sus mensajes.

* **[!UICONTROL Clics entrantes]**: Recuento total de clics en los canales salientes.

* **[!UICONTROL Tasa de conversión]**: Valor total de la métrica de éxito, seleccionada anteriormente al crear los experimentos, dividido por el número de perfiles.

* **[!UICONTROL Alza]**: medición de la mejora porcentual en la tasa de conversión de un tratamiento determinado respecto al valor de referencia.

* **[!UICONTROL Confianza]**: Evidencia de que un tratamiento dado es el mismo que el tratamiento basal. [Más información](../content-management/experiment-calculations.md#understand-confidence)

<!--
* **[!UICONTROL Confidence Upper bound]**:

* **[!UICONTROL Confidence Lower bound]**:
-->
+++

### Tasa de conversión de clics entrantes {#conversion-rate}

![](assets/cja-experimentation-conversion.png)

El gráfico de **[!UICONTROL intervalo de confianza]** mide la incertidumbre en torno a la mejora. Detalla la diferencia porcentual en el rendimiento entre la línea de base y el tratamiento con mejor rendimiento. [Más información](../content-management/experiment-calculations.md#confidence-intervals).
