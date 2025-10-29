---
solution: Journey Optimizer
product: journey optimizer
title: Informe de recorrido
description: Aprenda a utilizar los datos del informe de recorrido
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 30a7ebde95f2cb1ddecf3dc48420076914db4b12
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 1%

---

# Monitorización de las acciones personalizadas {#reporting}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_custom_actions_monitor"
>title="Monitorización de las acciones personalizadas"
>abstract="La página de informes **[!UICONTROL Acción personalizada]** le permite rastrear el rendimiento y la confiabilidad de las llamadas de API que sus recorridos realizan a sistemas de terceros."

>[!AVAILABILITY]
>
>Actualmente, los informes de acciones personalizadas solo están disponibles para un conjunto de organizaciones (disponibilidad limitada).

La página de informes **[!UICONTROL Acción personalizada]** le permite supervisar la confiabilidad y el rendimiento de las llamadas API realizadas desde sus recorridos a sistemas de terceros. Estos informes le ayudan a identificar rápidamente los problemas de integración, los cuellos de botella de latencia o los límites de restricción/restricción que pueden afectar a la entrega.

La página Informes de acciones personalizadas funciona como otros informes permanentes en Journey Optimizer. Para obtener detalles sobre las funcionalidades del tablero, consulte [esta documentación](../reports/report-cja-manage.md).

Para obtener acceso a la página de informes **[!UICONTROL Acción personalizada]**, haga clic en ![](assets/do-not-localize/Smock_Monitoring_18_N.svg) desde la página principal de **[!UICONTROL Acciones]**.

![](assets/monitor-1.png)

➡️ [Más información sobre cómo configurar las acciones personalizadas](../action/about-custom-action-configuration.md)

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

+++

## Horas extra de llamadas {#calls}

![](assets/monitor-3.png)

El gráfico **[!UICONTROL Horas extra en llamadas]** muestra la tendencia de KPI de llamadas HTTP a lo largo del período de tiempo seleccionado para el informe. La granularidad de la serie temporal depende del intervalo temporal seleccionado. Por ejemplo:

* Para un informe de 7 días, cada punto de datos mostrará los KPI de un día.
* Si selecciona un intervalo de tiempo de 1 día, el gráfico mostrará los KPI por hora.
* Si selecciona un intervalo de tiempo de 1 hora, el gráfico mostrará los KPI por minuto.

➡️[Consulte la sección KPI para obtener una descripción de las métricas de llamadas HTTP](#kpis)

## Desglose de llamadas {#breakdown}

![](assets/monitor-4.png)

La tabla **[!UICONTROL Desglose de llamadas]** proporciona un desglose jerárquico de las métricas de llamadas HTTP, desde las métricas generales por punto de conexión en el nivel superior hasta las métricas por acción personalizada usando cada punto de conexión y hasta los recorridos que dependen de ellas en el nivel inferior.

➡️[Consulte la sección KPI para obtener una descripción de las métricas de llamadas HTTP](#kpis)


