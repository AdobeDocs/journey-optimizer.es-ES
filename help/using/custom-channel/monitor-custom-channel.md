---
title: Administrar y supervisar canales personalizados
description: Obtenga información sobre cómo administrar el ciclo de vida de los canales personalizados y las configuraciones de canal, y monitorizar el rendimiento de entrega a través de los informes de Adobe Journey Optimizer.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 1%

---


# Monitorización de canales personalizados {#monitor-custom-channel}

Una vez que se haya creado y activado un canal personalizado, puede [administrar su ciclo de vida](create-custom-channel.md#access-channel-builder) y supervisar el rendimiento de la entrega a través de la interfaz [!DNL Journey Optimizer].

## Aprovechamiento de informes de campaña y recorrido {#reporting}

[!DNL Journey Optimizer] proporciona informes predeterminados para los canales personalizados.

Las siguientes métricas están disponibles para canales personalizados en informes en vivo (24h) y globales (CJA).<!--TBC and add or replace with CJA link when available-->

| Métrica | Descripción |
|--------|-------------|
| **Envíos intentados** | Número total de mensajes enviados al extremo externo. |
| **Envíos correctos** | Mensajes para los que el extremo devolvió una respuesta HTTP 2xx. |
| **Perfiles segmentados** | Número de perfiles únicos alcanzados. |
| **Clics** | Número de clics en vínculos rastreados en la carga útil. Requiere un subdominio delegado para canales personalizados. |
| **Errores / Errores** | Número de intentos de envío fallidos, con desglose por motivo del error. |

Obtenga más información sobre [informes en vivo](../reports/live-report.md) y [informes globales](../reports/report-gs-cja.md). Para obtener detalles sobre las funcionalidades de informes, consulte [esta documentación](../reports/report-cja-manage.md).

<!--
### Journey reports {#journey-reports}

To view delivery data for a custom channel action in a journey:

1. Open the journey from the **[!UICONTROL Journeys]** list.
1. Click **[!UICONTROL View report]** in the top-right area.
   * **[!UICONTROL Live report]** – Data for the last 24 hours.
   * **[!UICONTROL All time]** – Full lifetime data via Customer Journey Analytics (CJA).

### Campaign reports {#campaign-reports}

To view delivery data for a custom channel campaign:

1. Open the campaign from the **[!UICONTROL Campaigns]** list.
1. Click **[!UICONTROL Reports]** in the top-right area.

The campaign report includes execution count, successful deliveries, errors, and click data (if link tracking is enabled).
-->

## Monitorización del rendimiento de la entrega {#monitoring}

Además de los informes de campaña y recorrido, [!DNL Journey Optimizer] proporciona un panel de supervisión de canal personalizado. Acceda a él desde **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Generador de canales]** > **[!UICONTROL Supervisión de canales personalizados]**.

![Panel de supervisión de canal personalizado](assets/custom_channel_monitoring_dashboard.png){width="100%"}

Este panel le permite supervisar la fiabilidad y el rendimiento de las llamadas de API que [!DNL Journey Optimizer] realiza a sus extremos externos al enviar mensajes de canal personalizados. Utilícela para identificar rápidamente los problemas de integración, la latencia y los límites de restricción.

El panel **[!UICONTROL Supervisión de canales personalizados]** funciona como otros informes permanentes en [!DNL Journey Optimizer]. Puede seleccionar un intervalo de tiempo, filtrar por canal o extremo, y explorar en profundidad las campañas y recorridos que dependen de cada canal personalizado. [Más información](../reports/report-cja-manage.md)

### Métricas de canal personalizadas {#monitoring-kpis}

La sección **[!UICONTROL Métricas de canal personalizadas]** proporciona una vista consolidada del estado operativo y la confiabilidad de sus llamadas de canal personalizadas.

![Métricas de canal personalizado](assets/custom_channel_metrics.png){width="100%"}

+++ Más información sobre las métricas de canal personalizadas

* **[!UICONTROL Llamadas correctas]**: Número total de llamadas HTTP que devolvieron una respuesta válida sin error.

* **[!UICONTROL Errores de 4xx/5xx]**: número de llamadas erróneas debido a errores del lado del cliente (4xx) o del lado del servidor (5xx), que resaltan problemas de configuración o errores de extremo.

* **[!UICONTROL Llamadas con tiempo de espera]**: número de llamadas que fallaron porque superaron el tiempo de respuesta máximo. Esto ayuda a que aparezcan problemas de latencia o rendimiento con extremos externos.

* **[!UICONTROL Errores previos a la llamada]**: Número de envíos de canal personalizado que fallaron antes de que se realizara la llamada HTTP al extremo externo. Estos errores se producen en la capa de infraestructura propia de [!DNL Journey Optimizer], no en el sistema externo. Hay tres categorías:

  | Categoría | Descripción |
  |----------|-------------|
  | **Errores de autenticación** (`AUTH_*`) | [!DNL Journey Optimizer] no pudo obtener o actualizar el token de OAuth o las credenciales necesarias para llamar al extremo. Compruebe que las credenciales de la API vinculadas a la configuración del canal sean válidas y no hayan caducado. |
  | **Errores de generación de solicitudes** (`REQUEST_GENERATION_ERROR`) | [!DNL Journey Optimizer] no pudo construir una solicitud HTTP válida; por ejemplo, porque no se pudo resolver una plantilla URL o faltaba un campo de personalización requerido. |
  | **Errores de análisis HTTP** (`HTTP_PARSE_ERROR`) | [!DNL Journey Optimizer] recibió una respuesta del extremo, pero no pudo analizarla en una estructura utilizable. |

  >[!TIP]
  >
  >Los errores previos a la llamada indican un problema en el lado [!DNL Journey Optimizer] o en la configuración del canal, en lugar de un problema con el extremo externo. Empiece a solucionar problemas revisando las credenciales de la API y los campos de carga útil requeridos.

* **[!UICONTROL Latencia promedio]**: Tiempo medio de respuesta de un extremo a otro (en milisegundos) para todas las llamadas HTTP, incluidas las llamadas correctas, los errores y los tiempos de espera.

<!--
* **[!UICONTROL Capped calls]**: Number of calls that were blocked due to capping limits, ensuring downstream systems are not overloaded.

* **[!UICONTROL Average RPS]**: Number of requests per second processed by the custom channel over the selected time range.

* **[!UICONTROL Average successful latency]**: Average end-to-end response time (in milliseconds) for successful calls only, excluding failed requests and timeouts.

* **[!UICONTROL Average queue time]**: Average time (in milliseconds) calls spent waiting in the execution queue before being sent. This only applies to throttled endpoints, where [!DNL Journey Optimizer] queues calls when the throughput limit is reached.
-->

+++

### Resultados de canales personalizados con el tiempo {#outcomes-overtime}

![Resultados de canal personalizado con el tiempo](assets/custom_channel_metrics.png){width="100%"}

El gráfico **[!UICONTROL Resultados de canales personalizados a lo largo del tiempo]** muestra la tendencia de KPI de llamadas HTTP durante el período de tiempo seleccionado. La granularidad de la serie temporal depende del intervalo temporal seleccionado:

* Para un informe de 7 días, cada punto de datos muestra los KPI de un día.
* Para un intervalo de tiempo de 1 día, el gráfico muestra los KPI por hora.
* Para un intervalo de tiempo de 1 hora, el gráfico muestra los KPI por minuto.

### Latencia con el tiempo {#latency-overtime}

![Latencia de canal personalizado con el tiempo](assets/custom_channel_latency.png){width="100%"}

El gráfico **[!UICONTROL Latencia en el tiempo]** visualiza la tendencia de las métricas de latencia en el período de tiempo seleccionado. Esta vista de serie temporal le permite realizar un seguimiento de los patrones de rendimiento, identificar los períodos de latencia máxima y supervisar el impacto de las optimizaciones o los cambios del sistema a lo largo del tiempo.

### Desglose de resultados de canal personalizado {#outcome-breakdown}

![Desglose de resultados de canal personalizado](assets/custom_channel_latency.png){width="100%"}

La tabla **[!UICONTROL Desglose de resultados de canal personalizado]** proporciona un desglose jerárquico de las métricas de llamada HTTP: desde métricas generales por punto de conexión en el nivel superior hasta métricas por canal personalizado que usa ese punto de conexión y hasta campañas y recorridos que dependen de ellas en el nivel inferior.

### Desglose de latencia {#latency-breakdown}

La tabla **[!UICONTROL desglose de latencia]** proporciona un desglose detallado de las métricas de latencia en los canales personalizados. Esta vista le ayuda a identificar qué extremos o canales específicos están experimentando problemas de rendimiento, lo que le permite identificar y abordar los cuellos de botella de latencia de forma eficaz.

### Insight Builder {#insight-builder}

Use **[!UICONTROL Insight Builder]** para crear visualizaciones y paneles personalizados basados en las métricas de canal personalizadas. Esta herramienta le permite combinar varios KPI, aplicar filtros y crear vistas adaptadas que se ajusten a sus necesidades de monitorización e informes. [Más información](../reports/report-cja-manage.md#insight-builder)

## Resolución de problemas {#troubleshooting}

Si tiene problemas con el canal personalizado, en la tabla siguiente se enumeran los síntomas comunes, las posibles causas y las resoluciones recomendadas.

| Síntoma | Posible causa | Resolución |
|---------|----------------|------------|
| **Errores HTTP 401 / 403** | Error de autenticación: credenciales caducadas o incorrectas. | Actualice las credenciales en **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL credenciales de API]**. |
| **Errores HTTP 429** | El extremo externo está limitando las solicitudes de [!DNL Journey Optimizer]. | Revise los límites de velocidad del punto final. Reduzca la configuración de restricción en la configuración de la directiva de Channel Builder. |
| **Errores HTTP 5xx** | El sistema externo está inactivo o devuelve errores del servidor. | Compruebe el panel de estado del sistema externo. Configure las rutas de error en la actividad de acción de recorrido para gestionar correctamente los errores transitorios. |
| **Tokens de personalización sin resolver** | La expresión hace referencia a un atributo que no está presente en el perfil. | Compruebe que la ruta del atributo XDM sea correcta. Agregar una reserva de valor predeterminado: `{{profile.person.name.firstName \| default("Valued Customer")}}`. |
| **Error de validación de campo obligatorio** | Un campo de carga útil requerido no tiene valor en el momento de la creación. | Asegúrese de que todos los campos obligatorios se rellenen en el editor de contenido. Como alternativa, elimine la restricción requerida en el Generador de canales si el campo es realmente opcional. |

<!--
## Related resources {#related}

* [Get started with custom channels](get-started-custom-channel.md)
* [Configure a custom channel](custom-channel-configuration.md)
* [Global report overview](../reports/report-gs-cja.md)
* [Journey live report](../reports/live-report.md
-->