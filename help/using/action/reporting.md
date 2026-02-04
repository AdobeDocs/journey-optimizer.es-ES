---
solution: Journey Optimizer
product: journey optimizer
title: Monitorización de acciones personalizadas
description: Aprenda a utilizar los datos del informe de recorrido
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 97464b7afa07199792bd4311d0477b5bcb140d8e
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 2%

---

# Monitorización de acciones personalizadas {#reporting}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_custom_actions_monitor"
>title="Monitorización de acciones personalizadas"
>abstract="La página de informes **[!UICONTROL Acción personalizada]** le permite rastrear el rendimiento y la confiabilidad de las llamadas de API que sus recorridos realizan a sistemas de terceros."

La página de informes **[!UICONTROL Acción personalizada]** le permite supervisar la confiabilidad y el rendimiento de las llamadas API realizadas desde sus recorridos a sistemas de terceros. Estos informes le ayudan a identificar rápidamente los problemas de integración, los cuellos de botella de latencia o los límites de restricción/restricción que pueden afectar a la entrega.

La página Informes de acciones personalizadas funciona como otros informes permanentes en Journey Optimizer. Para obtener detalles sobre las funcionalidades del tablero, consulte [esta documentación](../reports/report-cja-manage.md).

Para obtener acceso a la página de informes **[!UICONTROL Acción personalizada]**, haga clic en ![](assets/do-not-localize/Smock_Monitoring_18_N.svg) desde la página principal de **[!UICONTROL Acciones]**.

![](assets/monitor-1.png)

➡️ [Más información acerca de la configuración de acciones personalizadas](../action/about-custom-action-configuration.md)

Además de la página de informes **[!UICONTROL Acción personalizada]**, puede usar **[!DNL Adobe Experience Platform Query Service]** para generar consultas con el fin de informar sobre métricas de rendimiento de acciones personalizadas. Hay ejemplos de consultas disponibles en [esta sección](../reports/query-examples.md).

## KPI {#kpis}

![](assets/monitor-2.png)

Los indicadores clave de rendimiento (KPI) de **[!UICONTROL acción personalizada]** actúan como un panel centralizado que proporciona una vista consolidada del estado operativo y la confiabilidad de las llamadas de acción personalizadas. Estas métricas le permiten evaluar el rendimiento, identificar cuellos de botella y garantizar integraciones estables con sistemas externos.

+++ Más información sobre los KPI de acción personalizada

* **[!UICONTROL Llamadas correctas]**: Número total de llamadas HTTP que devolvieron una respuesta válida sin error.

* **[!UICONTROL Errores de 4xx/5xx]**: número de llamadas erróneas debido a errores del lado del cliente (4xx) o del lado del servidor (5xx), que resaltan problemas de configuración o errores de extremo.

* **[!UICONTROL Tiempos de espera]**: Número de llamadas que fallaron porque excedieron el tiempo de respuesta máximo. Esto ayuda a que aparezcan problemas de latencia o rendimiento con extremos externos.

* **[!UICONTROL Llamadas restringidas]**: Número de llamadas que se bloquearon debido a los límites de límite, lo que garantiza que los sistemas descendentes no se sobrecarguen.

* **[!UICONTROL Promedio de RPS]**: número de solicitudes por segundo procesadas por la acción personalizada en el intervalo de tiempo seleccionado.

* **[!UICONTROL Latencia promedio]**: Tiempo medio de respuesta de un extremo a otro (en milisegundos) para todas las llamadas HTTP, incluidas las llamadas correctas, los errores y los tiempos de espera.

* **[!UICONTROL Promedio de latencia correcta]**: Promedio de tiempo de respuesta de un extremo a otro (en milisegundos) solo para las llamadas correctas, excluyendo las solicitudes con errores y los tiempos de espera.

* **[!UICONTROL Tiempo promedio en cola]**: Tiempo promedio (en milisegundos) que las llamadas han estado esperando en la cola de ejecución antes de enviarse. Esto solo se aplica a los extremos restringidos, donde Journey Optimizer pone en cola las llamadas cuando se alcanza el límite de rendimiento.

+++

## Llamadas con el tiempo {#calls}

![](assets/monitor-3.png)

El gráfico **[!UICONTROL Llamadas en el tiempo]** muestra la tendencia del KPI de llamadas HTTP en el período de tiempo seleccionado para el informe. La granularidad de la serie temporal depende del intervalo temporal seleccionado. Por ejemplo:

* Para un informe de 7 días, cada punto de datos mostrará los KPI de un día.
* Si selecciona un intervalo de tiempo de 1 día, el gráfico mostrará los KPI por hora.
* Si selecciona un intervalo de tiempo de 1 hora, el gráfico mostrará los KPI por minuto.

➡️[Consulte la sección KPI para obtener una descripción de las métricas de llamadas HTTP](#kpis)

## Latencia con el tiempo {#latency-overtime}

![](assets/monitor-6.png)

El gráfico **[!UICONTROL Latencia en el tiempo]** visualiza la tendencia de las métricas de latencia en el período de tiempo seleccionado. Esta vista de serie temporal le permite realizar un seguimiento de los patrones de rendimiento, identificar los períodos de latencia máxima y supervisar el impacto de las optimizaciones o los cambios del sistema a lo largo del tiempo.

➡️[Consulte la sección KPI para obtener una descripción de las métricas de latencia](#kpis)


## Desglose de llamadas {#breakdown}

![](assets/monitor-4.png)

La tabla **[!UICONTROL Desglose de llamadas]** proporciona un desglose jerárquico de las métricas de llamadas HTTP, desde las métricas generales por punto de conexión en el nivel superior hasta las métricas por acción personalizada usando cada punto de conexión y hasta los recorridos que dependen de ellas en el nivel inferior.

➡️[Consulte la sección KPI para obtener una descripción de las métricas de llamadas HTTP](#kpis)

## Desglose de latencia {#latency-breakdown}

![](assets/monitor-5.png)

La tabla **[!UICONTROL desglose de latencia]** proporciona un desglose detallado de las métricas de latencia en las acciones personalizadas. Esta vista le ayuda a identificar qué extremos o acciones específicos están experimentando problemas de rendimiento, lo que le permite identificar y abordar los cuellos de botella de latencia de forma eficaz.

➡️[Consulte la sección KPI para obtener una descripción de las métricas de latencia](#kpis)

## Vídeo práctico {#video}

El siguiente vídeo muestra cómo monitorizar la fiabilidad y el rendimiento de las llamadas de API realizadas desde sus recorridos a sistemas de terceros.

+++Vea el vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3479544?captions=spa&quality=12&learn=on)

+++
