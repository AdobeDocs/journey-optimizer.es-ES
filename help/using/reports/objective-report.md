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
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 4%

---

# Informe global de la campaña {#objective-report}

Se puede acceder al informe global de Campaign directamente desde la campaña con la variable **[!UICONTROL Ver informe]** botón.

La campaña **[!UICONTROL Informe global]** se divide en diferentes widgets que detallan el éxito y los errores de la campaña. Se puede cambiar el tamaño de cada widget y eliminarlo si es necesario. Para obtener más información, consulte [sección](../reports/global-report.md#modify-dashboard).

Para obtener una lista detallada de todas las métricas disponibles en Adobe Journey Optimizer, consulte [esta página](global-report.md#list-of-components-global.md)

## Pestaña Campaña {#campaign-global-objectives}

### envío {#delivery-global-objectives}

![](assets/campaign_report_global_1.png)

El **[!UICONTROL Estadísticas de la campaña]** El widget detalla la información principal relativa a la campaña:

* **[!UICONTROL Perfiles introducidos]**: Número de perfiles que iniciaron el recorrido.

* **[!UICONTROL Acciones entregadas]**: Número total de veces que se ha entregado una acción en el recorrido.

* **[!UICONTROL Acciones con errores en %]**: Número total de veces únicas que una acción ha fallado en el recorrido comparado con el número total de veces únicas que se ha entregado una acción.

### Informe Objetivos {#objective-global}

>[!AVAILABILITY]
>
>El **Informe Objetivos** Actualmente, esta función solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

![](assets/performance_report.gif)

El **[!UICONTROL Objetivos]** Esta pestaña le permite ajustar mejor los informes de las entregas dirigiéndose a una métrica específica.

El **[!UICONTROL Objetivos]** los elementos enumerados están vinculados a **[!UICONTROL Conjuntos de datos]** que definen una conexión a un sistema para recuperar información adicional. Una lista de componentes integrados **[!UICONTROL Objetivos]** está disponible, pero puede agregar los suyos propios agregando nuevos **[!UICONTROL Conjunto de datos]**. Para ver el procedimiento detallado, consulte [sección](../content-management/reporting-configuration.md).

Después de seleccionar los Objetivos en los que desea centrarse, se muestran los dos **[!UICONTROL Resumen de rendimiento]** y **[!UICONTROL Objetivo de campaña]** los widgets proporcionan un resumen detallado del rendimiento de su envío.

Con el **[!UICONTROL Objetivo de campaña]** , también puede optar por comparar su objetivo principal con otra métrica.

### Informe de experimentación {#experimentation-global-objectives}

![](assets/experimentation_report_3.png)

El **[!UICONTROL Experimentación]** proporciona perspectivas clave sobre el rendimiento de cada variante e identifica la que tiene más éxito.

Tenga en cuenta que la definición del mejor ejecutante puede llevar algún tiempo y se representará mediante este icono ![](assets/experimentation_report_1.png).

+++Obtenga más información sobre las distintas métricas y widgets disponibles para el informe Experimentación.

El **[!UICONTROL Resultado del experimento]** widget detalla el rendimiento de cada variante. Puede cambiar la línea de base seleccionando uno de los tratamientos en la **[!UICONTROL Línea base]** la lista desplegable. El mejor tratamiento se representará con un icono de estrella.

La tabla presenta las siguientes métricas:

* **[!UICONTROL Alza sobre la línea base]**: Medida de la mejora porcentual en la tasa de conversión de un tratamiento determinado respecto al valor basal.

* **[!UICONTROL Confianza]**: Evidencia de que un tratamiento dado es el mismo que el tratamiento basal. [Más información](../content-management/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Clics salientes únicos]**: Recuento total de clics en los canales salientes.

* **[!UICONTROL Perfiles]**: Número de perfiles objetivo para este tratamiento.

* **[!UICONTROL Clics/perfiles salientes únicos]**: Valor total de la métrica de éxito, seleccionada anteriormente al crear los experimentos, dividido por el número de perfiles.

El **[!UICONTROL Intervalo de confianza]** el gráfico mide la incertidumbre en torno a la mejora. Detalla la diferencia porcentual en el rendimiento entre la línea de base y el tratamiento con mejor rendimiento. [Más información](../content-management/experiment-calculations.md#confidence-intervals).
+++

Para profundizar en estos resultados y en cómo interpretarlos, consulte [esta página](../content-management/get-started-experiment.md#interpret-results).
