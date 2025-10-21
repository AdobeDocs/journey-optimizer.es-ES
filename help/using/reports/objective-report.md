---
solution: Journey Optimizer
product: journey optimizer
title: Informe global de la campaña
description: Aprenda a utilizar los datos del informe global de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: ec1af88c-7b0a-4eaf-97e1-0d9676268fed
badge: label="Beta" type="Informative"
source-git-commit: 722d37dc4bcb9ab7983ea336aa0b12a6a09e01dc
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 4%

---

# Informe global de la campaña {#objective-report}

Se puede acceder directamente al informe global de Campaign desde la campaña con el botón **[!UICONTROL Ver informe]**.

El **[!UICONTROL informe global]** de la campaña está dividido en diferentes widgets que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte <!--[section](../reports/global-report.md#modify-dashboard)-->.

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte <!--[this page](global-report.md#list-of-components-global.md)-->

## Pestaña Campaña {#campaign-global-objectives}

### envío {#delivery-global-objectives}

<!--
![](assets/campaign_report_global_1.png)
-->

El widget **[!UICONTROL Estadísticas de campaña]** detalla la información principal relativa a su campaña:

* **[!UICONTROL Perfiles introducidos]**: Número de perfiles que iniciaron el recorrido.

* **[!UICONTROL Acciones entregadas]**: Número total de veces únicas que se ha entregado una acción en el recorrido.

* **[!UICONTROL Acciones con errores en %]**: Número total de veces únicas que una acción ha fallado en el recorrido comparado con el número total de veces únicas que se ha entregado una acción.

### Informe Objetivos {#objective-global}

>[!AVAILABILITY]
>
>Actualmente, la característica **Informe de objetivos** solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

![](assets/performance_report.gif)

La ficha **[!UICONTROL Objetivos]** le permite ajustar mejor los informes de las entregas dirigiéndose a una métrica específica.

Los **[!UICONTROL Objetivos]** enumerados están vinculados a **[!UICONTROL Conjuntos de datos]** que definen una conexión con un sistema para recuperar información adicional. Hay disponible una lista de **[!UICONTROL Objetivos]** integrados, pero puede agregar los suyos propios agregando un nuevo **[!UICONTROL conjunto de datos]**. Para ver el procedimiento detallado, consulte esta [sección](../reports/reporting-configuration.md).

Después de seleccionar los objetivos con los que se quiere dirigir, los dos widgets de **[!UICONTROL Información general sobre el rendimiento]** y **[!UICONTROL Objetivo de la campaña]** proporcionarán un resumen detallado del rendimiento de su envío.

Con el widget **[!UICONTROL Objetivo de campaña]**, también puedes elegir comparar tu objetivo principal con otra métrica.

### Informe de experimentación {#experimentation-global-objectives}

<!--
![](assets/experimentation_report_3.png)
-->

La ficha **[!UICONTROL Experimentación]** proporciona información clave sobre el rendimiento de cada variante e identifica la que ha tenido más éxito.

Tenga en cuenta que la definición del mejor ejecutante puede tardar algún tiempo, se representará mediante este icono ![](assets/experimentation_report_1.png).

+++Obtenga más información acerca de las distintas métricas y widgets disponibles para el informe Experimentación.

El widget **[!UICONTROL Resultado del experimento]** detalla el rendimiento de cada variante. Puede cambiar la línea de base seleccionando uno de los tratamientos en la lista desplegable **[!UICONTROL Línea de base]**. El mejor tratamiento se representará con un icono de estrella.

La tabla presenta las siguientes métricas:

* **[!UICONTROL Alza sobre el nivel basal]**: medición de la mejora porcentual en la tasa de conversión de un tratamiento determinado sobre el nivel basal.

* **[!UICONTROL Confianza]**: Evidencia de que un tratamiento dado es el mismo que el tratamiento basal. [Más información](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Clics salientes únicos]**: Recuento total de clics en los canales salientes.

* **[!UICONTROL Perfiles]**: número de perfiles segmentados para este tratamiento.

* **[!UICONTROL Clics/perfiles salientes únicos]**: Valor total de la métrica de éxito, seleccionada anteriormente al crear los experimentos, dividido por el número de perfiles.

El gráfico de **[!UICONTROL intervalo de confianza]** mide la incertidumbre en torno a la mejora. Detalla la diferencia porcentual en el rendimiento entre la línea de base y el tratamiento con mejor rendimiento. [Más información](../content-management/experiment-calculations.md#confidence-intervals).
+++

Para profundizar en estos resultados y cómo interpretarlos, consulte [esta página](../content-management/get-started-experiment.md#interpret-results).
