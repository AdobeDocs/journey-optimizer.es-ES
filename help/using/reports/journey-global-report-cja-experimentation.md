---
solution: Journey Optimizer
product: journey optimizer
title: Informe de experimento de recorrido
description: Aprenda a utilizar los datos de experimentación del informe de Recorrido
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a2b4ef74-96a9-4907-ba70-7aee69e45f20
TQID: https://experienceleague.adobe.com/oN7VFQvhQlwNa2U5CmcAYkGbKb0Vnxc7yA5rCLDjQw4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 407
ht-degree: 2%

---

# Informe de recorrido de experimentación {#campaign-global-report-cja-experimentation}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a leer las métricas de experimentación en el informe de recorrido, incluidos los KPI de experimento, el alza y la confianza y la métrica de rendimiento de variante por éxito para sus experimentos de contenido y ruta.

>[!ENDSHADEBOX]

El informe de Recorrido le ofrece una vista completa del rendimiento de su experimento, junto con las métricas clave que necesita para comprender su impacto.

En Journey Optimizer, la experimentación con recorridos se divide en dos tipos:

* [Experimentos de contenido](../content-management/content-experiment.md)

  Tenga en cuenta que las tablas y los KPI detallados para el experimento de contenido son los mismos que para un experimento de ruta. Consulte la [documentación siguiente](#experimentation) si ha configurado un experimento de contenido.

* [Experimentos de ruta](../building-journeys/optimize.md)

## Experimento de ruta {#experimentation}

### KPI de experimentación {#experimentation-kpis}

![](assets/journey-report-experiment-1.png)

**Resumen de experimentación** proporciona información clave sobre el rendimiento de tu experimento e identifica el más exitoso. Tenga en cuenta que definir el mejor ejecutante puede llevar algún tiempo. Si el experimento no se realiza correctamente, se establecerá en **No concluyente**.

Los **Indicadores clave de rendimiento (KPI) de experimentación** funcionan como un tablero que abarca todo, y ofrecen un análisis de las métricas esenciales asociadas con la experimentación.

+++ Más información sobre las métricas de KPI de experimentación

* **[!UICONTROL Alza]**: medición de la mejora porcentual en la tasa de conversión de un tratamiento determinado respecto al valor de referencia.

* **[!UICONTROL Confianza]**: Evidencia de que un tratamiento dado es el mismo que el tratamiento basal. [Más información](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

+++



### Variante por métricas de éxito {#variant-inbound}

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
