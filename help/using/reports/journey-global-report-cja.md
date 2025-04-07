---
solution: Journey Optimizer
product: journey optimizer
title: Informe de recorrido
description: Aprenda a utilizar los datos del informe de recorrido
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 30d4f967-e085-44f1-973d-11e79f693e6e
source-git-commit: 1af75a0e6bfc2c3b9c565c3190f46d137a68d32e
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 1%

---

# Informe de recorrido {#journey-global-report}

El **informe de Recorrido** funciona como un tablero que abarca todo, y ofrece un análisis de las métricas esenciales asociadas con el recorrido. Esto incluye detalles como el recuento de perfiles introducidos y los casos de recorridos individuales fallidos, lo que ofrece un insight completo de la eficacia y el nivel de participación de su recorrido.

Se puede acceder directamente al **informe de Recorrido** desde su recorrido con el botón **[!UICONTROL Ver informe]**.

![](assets/gs-cja-report-3.png)

Para obtener más información sobre Customer Journey Analytics Workspace y cómo filtrar y analizar datos, consulte [esta página](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home).

## Información general del recorrido {#journey-global}

El informe **[!UICONTROL Recorrido]** le ofrece una visión clara de los datos de seguimiento más importantes sobre su recorrido.

### KPI de recorrido {#journey-perfomance}

![](assets/cja-journey-kpis.png)

Los indicadores clave de rendimiento (KPI) **[!UICONTROL Recorrido]** funcionan como un tablero que abarca todo, y ofrecen un análisis de las métricas esenciales asociadas con el recorrido. Esto incluye detalles como el recuento de perfiles introducidos y los casos de recorridos individuales fallidos, lo que ofrece un insight completo de la eficacia y el nivel de participación de su recorrido.

+++ Más información sobre las métricas de KPI de Recorrido

* **[!UICONTROL Participación en el Recorrido]**: Número total de individuos únicos que recibieron mensajes enviados a través del recorrido, que representan perfiles distintos que alcanzaron un punto de acción designado en el recorrido.

* **[!UICONTROL Entradas de Recorrido]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Salidas de Recorrido]**: Número total de personas que salieron del recorrido.

+++

### estadísticas de recorrido {#journey-stats}

![](assets/cja-journey-stats.png)

La tabla **[!UICONTROL Estadísticas de Recorrido]** ofrece un resumen detallado de datos cruciales sobre tus recorridos. Incluye métricas clave como el número de errores y las entradas exitosas, lo que proporciona una valiosa perspectiva del rendimiento y el alcance de sus correos electrónicos y recorridos.

+++ Más información sobre las métricas de Estadísticas de Recorrido

* **[!UICONTROL Exclusión de Recorridos]**: Número total de personas que se excluyeron del recorrido debido a criterios predefinidos o reglas de supresión.

* **[!UICONTROL Participación en el Recorrido]**: Número total de individuos únicos que recibieron mensajes enviados a través del recorrido, que representan perfiles distintos que alcanzaron un punto de acción designado en el recorrido.

* **[!UICONTROL Entradas de Recorrido]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL Salidas de Recorrido]**: Número total de personas que salieron del recorrido.

* **[!UICONTROL Errores de Recorrido]**: Número total de recorridos individuales que no se ejecutaron correctamente.

* **[!UICONTROL Entradas de Recorridos únicos]**: Número total de individuos que llegaron al evento de entrada del recorrido; no se tienen en cuenta las interacciones múltiples de un perfil.

* **[!UICONTROL Salidas de Recorrido únicas]**: Número total de individuos que salieron del recorrido, no se tienen en cuenta las interacciones múltiples de un perfil.

* **[!UICONTROL Errores de Recorridos únicos]**: Número total de recorridos individuales que no se ejecutaron correctamente, no se tienen en cuenta las interacciones múltiples de un perfil.

+++

## exclusión de recorrido {#journey-exclusion}

La tabla **[!UICONTROL exclusión de Recorrido]** presenta una vista completa de los diferentes factores que resultaron en la exclusión de perfiles de usuario.

## Error de acción {#action-error}

![](assets/cja-journey-action-error.png)

El widget **[!UICONTROL Errores de acción]** detalla los diferentes errores que se produjeron para las acciones de su recorrido.

## Lienzo del recorrido  {#journey-canvas}

![](assets/cja-journey-canvas.png)

El widget **[!UICONTROL Lienzo de Recorrido]** le permite rastrear visualmente la trayectoria de sus perfiles de destino a medida que navegan por su recorrido. [Obtenga más información en la documentación de Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/journey-canvas/journey-canvas)

Mejore la personalización del lienzo con las siguientes opciones:

* Agregue o quite el tipo de actividad deseado, como mensajes o condiciones, del menú desplegable **[!UICONTROL Tipo de nodo]**.
* Ajuste el **[!UICONTROL valor de porcentaje]** para determinar la distribución del flujo entre las diferentes rutas de recorrido.
* Personaliza tu **[!UICONTROL configuración de flechas]** para incluir etiquetas, condiciones u optar por una pantalla limpia.
* Habilite la opción **[!UICONTROL Mostrar visitas en el orden previsto]** para visualizar los perfiles que salieron del recorrido directamente en el lienzo.

Al usar el filtrado **[!UICONTROL Tipo de nodo]**, se aplican las siguientes reglas:

* Al crear un segmento en un nodo, seguirá incluyendo nodos de etapas anteriores del recorrido, incluso si esos nodos se han excluido a través del filtro **[!UICONTROL Node type]**.

* No se pueden crear segmentos formados a partir de una flecha si los nodos de etapas anteriores del recorrido se han excluido mediante el filtro **[!UICONTROL Node type]**. En este caso, la funcionalidad del botón derecho se desactiva en esas flechas.

## Rendimiento de las acciones {#action-performance}

### Rendimiento con el tiempo {#action-overtime}

![](assets/cja-journey-action-performance.png)

El gráfico **[!UICONTROL Rendimiento con el tiempo]** le permite identificar y analizar el número de perfiles que cumplen los criterios para ser considerados perfiles objetivo para sus acciones. Esta visualización proporciona información valiosa sobre la eficacia de sus estrategias y le ayuda a tomar decisiones basadas en datos para optimizar su rendimiento.

### Resumen de acción {#action-overview}

![](assets/cja-journey-action-overview.png)

La tabla **[!UICONTROL Descripción general de la acción]** sirve como un panel completo, que ofrece un análisis de las métricas clave relacionadas con las acciones del recorrido. Esto incluye detalles cruciales como el número de interacciones y la tasa de clics

+++ Más información sobre las métricas de resumen de acción

* **[!UICONTROL El nodo ingresa]**: Número total de individuos que han ingresado un nodo específico dentro del recorrido.

* **[!UICONTROL Error de Recorrido]**: Número total de recorridos individuales que no se ejecutaron correctamente.

* **[!UICONTROL Tasa de pulsaciones]**: Porcentaje de usuarios que interactuaron con la acción.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en sus acciones.

* **[!UICONTROL Entregado]**: número de acciones enviadas correctamente, en relación con el número total de acciones enviadas.

+++

## Rendimiento de eventos {#events-performance}

### Rendimiento con el tiempo {#event-overtime}

![](assets/cja-journey-performance-event.png)

El gráfico **[!UICONTROL Rendimiento con el tiempo]** le permite identificar y analizar el número de perfiles que cumplen los requisitos como perfiles de destino para sus eventos. Esta potente herramienta le ayuda a seguir las tendencias y los patrones a lo largo del tiempo, proporcionando valiosas perspectivas para optimizar las estrategias de eventos.

### Resumen del evento {#event-overview}

![](assets/cja-journey-events-overview.png)

La tabla **[!UICONTROL Información general del evento]** muestra cuántos perfiles cumplen los criterios del evento a lo largo del tiempo. Esta herramienta le ayuda a identificar patrones en las tasas de calificación para refinar su estrategia de eventos.

+++ Más información sobre las métricas de Estadísticas de Recorrido

* **[!UICONTROL Personas]**: Número de perfiles de usuario que se califican como perfiles de destino para sus eventos.

+++
