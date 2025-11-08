---
solution: Journey Optimizer
product: journey optimizer
title: Informe de campaña
description: Aprenda a utilizar los datos de experimentación del informe de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 69742163-7378-49ab-929e-86213d6e65e3
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 9%

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

* **[!UICONTROL Confianza]**: Evidencia de que un tratamiento dado es el mismo que el tratamiento basal. [Más información](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

+++

### Variante por métrica de éxito {#variant-inbound}

![](assets/cja-experimentation-variants.png)

La tabla **Variante según métricas de éxito** muestra el rendimiento de cada variante en función de la métrica de éxito seleccionada al configurar el experimento.
Para profundizar en estos resultados y cómo interpretarlos, consulte [esta página](../content-management/get-started-experiment.md#interpret-results).

+++ Más información sobre la Variante por métrica de éxito

* **[!UICONTROL Personas]**: Número de perfiles de usuario que se califican como perfiles de destino para sus mensajes.

* **[!UICONTROL Clics entrantes]**: Valor total de la métrica de éxito, seleccionada anteriormente al crear los experimentos.

* **[!UICONTROL Tasa de conversión]**: Valor total de la métrica de éxito, seleccionada anteriormente al crear los experimentos, dividido por el número de perfiles.

* **[!UICONTROL Alza]**: medición de la mejora porcentual en la tasa de conversión de un tratamiento determinado respecto al valor de referencia.

* **[!UICONTROL Límite inferior de confianza]**: Valor estimado más bajo de la diferencia de tasa de conversión entre el tratamiento y la línea de base, dentro del intervalo de confianza elegido.

* **[!UICONTROL Confianza]**: Evidencia de que un tratamiento dado es el mismo que el tratamiento basal. [Más información](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

* **[!UICONTROL Límite superior de confianza]**: Valor estimado más alto de la diferencia de tasa de conversión entre el tratamiento y la línea de base, dentro del intervalo de confianza elegido.

+++

### Tasa de conversión para la métrica de éxito {#conversion-rate}

![](assets/cja-experimentation-conversion.png)


El gráfico de **[!UICONTROL Intervalo de confianza]** muestra el rango de posibles mejoras, comparando la línea de base con el tratamiento de mejor rendimiento para la métrica de éxito elegida. [Más información](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences).