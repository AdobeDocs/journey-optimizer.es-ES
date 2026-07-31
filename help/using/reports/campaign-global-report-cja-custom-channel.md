---
solution: Journey Optimizer
product: journey optimizer
title: Informe de campaña
description: Aprenda a utilizar los datos de canal personalizados del informe de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: ac64dd4ca2ed5fd1b9d816e19c6726a3ac82d193
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# Informe de campaña de canal personalizado {#campaign-global-report-cja-custom-channel}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a leer el informe de campaña de canal personalizado en Adobe Journey Optimizer para revisar los KPI, los resultados, la latencia y el desglose de resultados de las llamadas de canal personalizado.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Puede acceder a su informe de campaña de canal personalizado si hace clic en el botón **[!UICONTROL Informes]** de su campaña y, a continuación, selecciona **[!UICONTROL Ver informe de todo el tiempo]**. [Más información](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## KPI {#kpis-custom}

![](assets/kpis-custom.png)

La sección **[!UICONTROL KPI]** proporciona una vista consolidada del estado operativo y la fiabilidad de las llamadas de canal personalizadas.

+++ Más información sobre las métricas de KPI

* **[!UICONTROL Llamadas correctas]**: Número total de llamadas HTTP que devolvieron una respuesta válida sin error.

* **[!UICONTROL Errores de 4xx]**: número de llamadas erróneas debido a errores del lado del cliente, que resaltan problemas de configuración o errores de extremo.

* **[!UICONTROL Errores 5xx]**: número de llamadas erróneas debido a errores del lado del servidor, que resaltan problemas de configuración o errores de extremo.

* **[!UICONTROL Llamadas con tiempo de espera]**: número de llamadas que fallaron porque superaron el tiempo de respuesta máximo. Esto ayuda a que aparezcan problemas de latencia o rendimiento con extremos externos.

* **[!UICONTROL Errores previos a la llamada]**: Número de envíos de canal personalizado que fallaron antes de que se realizara la llamada HTTP al extremo externo. Estos errores se producen en la capa de infraestructura propia de [!DNL Journey Optimizer], no en el sistema externo, e incluyen errores de autenticación, errores de generación de solicitudes y errores de análisis HTTP.

* **[!UICONTROL Latencia promedio]**: Tiempo medio de respuesta de un extremo a otro (en milisegundos) para todas las llamadas HTTP, incluidas las llamadas correctas, los errores y los tiempos de espera.

+++

## Resultados de canal personalizado {#outcomes-custom}

![](assets/outcomes-custom.png)

El gráfico **[!UICONTROL Resultados]** muestra la tendencia de KPI de llamadas HTTP durante el período de tiempo seleccionado, con una granularidad que depende del intervalo de tiempo seleccionado (por día para un informe de 7 días, por hora para un intervalo de tiempo de 1 día o por minuto para un intervalo de tiempo de 1 hora), mientras que la tabla **[!UICONTROL Desglose de resultados]** proporciona un desglose jerárquico de estas métricas de llamadas HTTP, desde métricas generales por punto de conexión en el nivel superior, hasta métricas por canal personalizado que utilizan ese punto de conexión, hasta las campañas y recorridos que dependen de ellas en el nivel inferior.

+++ Más información sobre las Métricas de desglose de resultados

* **[!UICONTROL Canal personalizado correcto]**: Número total de llamadas HTTP que devolvieron una respuesta válida sin error.

* **[!UICONTROL Errores de 4xx]**: número de llamadas erróneas debido a errores del lado del cliente, que resaltan problemas de configuración o errores de extremo.

* **[!UICONTROL Errores 5xx]**: número de llamadas erróneas debido a errores del lado del servidor, que resaltan problemas de configuración o errores de extremo.

* **[!UICONTROL Llamadas con tiempo de espera]**: número de llamadas que fallaron porque superaron el tiempo de respuesta máximo. Esto ayuda a que aparezcan problemas de latencia o rendimiento con extremos externos.

* **[!UICONTROL Errores previos a la llamada]**: Número de envíos de canal personalizado que fallaron antes de que se realizara la llamada HTTP al extremo externo. Estos errores se producen en la capa de infraestructura propia de [!DNL Journey Optimizer], no en el sistema externo, e incluyen errores de autenticación, errores de generación de solicitudes y errores de análisis HTTP.

* **[!UICONTROL Llamadas]**: Número total de llamadas HTTP, incluidas las llamadas correctas, los errores y los tiempos de espera.

+++

## Latencia {#latency-custom}

![](assets/latency-custom.png)

El gráfico y las tablas de **[!UICONTROL Latencia]** visualizan la tendencia de las métricas de latencia. Estas vistas le permiten realizar un seguimiento de los patrones de rendimiento, identificar los períodos de latencia máxima y supervisar el impacto de las optimizaciones o los cambios del sistema a lo largo del tiempo.

+++ Más información sobre las Métricas de latencia

* **[!UICONTROL Latencia promedio]**: Tiempo medio de respuesta de un extremo a otro (en milisegundos) para todas las llamadas HTTP, incluidas las llamadas correctas, los errores y los tiempos de espera.

* **[!UICONTROL Promedio de latencia correcta]**: Promedio de tiempo de respuesta de un extremo a otro (en milisegundos) para las llamadas HTTP que devolvieron una respuesta válida sin errores.

+++
