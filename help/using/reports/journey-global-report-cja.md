---
solution: Journey Optimizer
product: journey optimizer
title: Informe global de recorrido
description: Aprenda a utilizar los datos del informe de recorrido
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="Disponibilidad limitada" type="Informative"
exl-id: d43ae701-6e3b-4dcf-8da1-11c07be10fcf
source-git-commit: b80d794f3782056a10310c65144a8eecbddaaf3e
workflow-type: tm+mt
source-wordcount: '4176'
ht-degree: 2%

---

# Informe de recorrido {#journey-global-report}

El **informe de recorrido** funciona como un tablero completo, que ofrece un análisis de las métricas esenciales asociadas con el recorrido. Esto incluye detalles como el recuento de perfiles introducidos y los casos de recorridos individuales fallidos, lo que ofrece una perspectiva completa de la eficacia y el nivel de participación de su recorrido.

**informe de recorrido** se puede acceder directamente desde su recorrido con el **[!UICONTROL Ver informe]** botón.

![](assets/gs-cja-report-3.png)

El **[!UICONTROL informe de recorrido]** se mostrará con las siguientes pestañas según las actividades de mensajes del recorrido:

* [ Recorrido ](#journey-global)
* [Correo electrónico](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [En la aplicación](#in-app-global)
* [Web](#web-cja)
* [Correo directo](#direct-mail-cja)

Para obtener más información sobre Customer Journey Analytics Workspace y cómo filtrar y analizar datos, consulte [esta página](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home).

## Información general del recorrido {#journey-global}

El **[!UICONTROL Recorrido]** le ofrece una visión clara de los datos de seguimiento más importantes sobre su recorrido.

### KPI de recorrido {#journey-perfomance}

![](assets/cja-journey-kpis.png)

El **[!UICONTROL Recorrido]** Los indicadores clave de rendimiento (KPI) funcionan como un panel que abarca todo, lo que ofrece un análisis de las métricas esenciales asociadas con el recorrido. Esto incluye detalles como el recuento de perfiles introducidos y los casos de recorridos individuales fallidos, lo que ofrece una perspectiva completa de la eficacia y el nivel de participación de su recorrido.

+++ Más información sobre las métricas de KPI de Recorrido

* **[!UICONTROL participación de recorrido]**: Número total de personas que interactuaron con los mensajes enviados desde el recorrido

* **[!UICONTROL el recorrido entra]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL salidas de recorrido]**: Número total de personas que salieron del recorrido.

* **[!UICONTROL errores de recorrido]**: Número total de recorridos individuales que no se ejecutaron correctamente.

+++

### estadísticas de recorrido {#journey-stats}

![](assets/cja-journey-stats.png)

El **[!UICONTROL Estadísticas de recorrido]** ofrece un resumen detallado de los datos cruciales sobre sus recorridos. Incluye métricas clave como el número de errores y las entradas exitosas, lo que proporciona una valiosa perspectiva del rendimiento y el alcance de sus correos electrónicos y recorridos.

+++ Más información sobre las métricas de Estadísticas de Recorrido

* **[!UICONTROL participación de recorrido]**: Número total de personas que interactuaron con los mensajes enviados desde el recorrido.

* **[!UICONTROL el recorrido entra]**: Número total de personas que llegaron al evento de entrada del recorrido.

* **[!UICONTROL salidas de recorrido]**: Número total de personas que salieron del recorrido.

* **[!UICONTROL errores de recorrido]**: Número total de recorridos individuales que no se ejecutaron correctamente.

* **[!UICONTROL Ingresa un Recorrido único]**: Número total de individuos que llegaron al evento de entrada del recorrido, no se tienen en cuenta las interacciones múltiples de un perfil.

* **[!UICONTROL Salidas de Recorrido únicas]**: Número total de individuos que salieron del recorrido, no se tienen en cuenta las interacciones múltiples de un perfil.

* **[!UICONTROL Errores de Recorrido único]**: Número total de recorridos individuales que no se ejecutaron correctamente, no se tienen en cuenta las interacciones múltiples de un perfil.

+++

## lienzo de recorrido {#journey-canvas}

![](assets/cja-journey-canvas.png)

El **[!UICONTROL Lienzo de recorrido]** Este widget permite rastrear visualmente la trayectoria de los perfiles de destino a medida que navegan por el recorrido.

Mejore la personalización del lienzo con las siguientes opciones:

* Añada o quite el tipo de actividad deseado, como mensajes o condiciones, de la **[!UICONTROL Tipo de nodo]** menú desplegable.
* Ajuste de **[!UICONTROL Valor porcentual]** para determinar la distribución del flujo entre las diferentes rutas de recorrido.
* Personalice su **[!UICONTROL Configuración de flecha]** para incluir etiquetas, condiciones u optar por una visualización limpia.
* Habilite la **[!UICONTROL Mostrar visitas en orden previsto]** para visualizar perfiles que salieron del recorrido directamente en el lienzo.

## Rendimiento de las acciones {#action-performance}

### Rendimiento con el tiempo {#action-overtime}

![](assets/cja-journey-action-performance.png)

El **[!UICONTROL Rendimiento con el tiempo]** Este gráfico le permite identificar y analizar el número de perfiles que cumplen los criterios para ser considerados perfiles objetivo para las acciones. Esta visualización proporciona información valiosa sobre la eficacia de sus estrategias y le ayuda a tomar decisiones basadas en datos para optimizar su rendimiento.

### Resumen de acción {#action-overview}

![](assets/cja-journey-action-overview.png)

El **[!UICONTROL Resumen de acción]** La tabla de sirve como un tablero completo, que ofrece un análisis de las métricas clave relacionadas con las acciones del recorrido. Esto incluye detalles cruciales como el número de interacciones y la tasa de clics

+++ Más información sobre las Métricas de resumen de la acción

* **[!UICONTROL People]**: Número de perfiles de usuario que se califican como perfiles de destinatario para sus acciones.

* **[!UICONTROL Tasa de pulsaciones]**: porcentaje de usuarios que interactuaron con la acción.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en sus acciones.

* **[!UICONTROL Entregado]**: Número de acciones enviadas correctamente, en relación con el número total de acciones enviadas.

+++

## Rendimiento de eventos {#events-performance}

### Rendimiento con el tiempo {#event-overtime}

![](assets/cja-journey-performance-event.png)

El **[!UICONTROL Rendimiento con el tiempo]** Este gráfico permite identificar y analizar el número de perfiles que cumplen los requisitos de perfiles de destinatario para los eventos. Esta potente herramienta le ayuda a seguir las tendencias y los patrones a lo largo del tiempo, proporcionando valiosas perspectivas para optimizar las estrategias de eventos.

### Resumen del evento {#event-overview}

![](assets/cja-journey-events-overview.png)

El **[!UICONTROL Resumen del evento]** La tabla muestra cuántos perfiles cumplen los criterios de evento a lo largo del tiempo. Esta herramienta le ayuda a identificar patrones en las tasas de calificación para refinar su estrategia de eventos.

+++ Más información sobre las métricas de Estadísticas de Recorrido

* **[!UICONTROL People]**: Número de perfiles de usuario que se califican como perfiles de destinatario para los eventos.

+++

## Detalles de correo electrónico {#email-global}

A partir del informe de recorrido, la variable **[!UICONTROL Correo electrónico]** Esta pestaña detalla la información principal relativa a los correos electrónicos enviados en el recorrido.

### Tendencia de envíos frente a clics {#delivered-click}

![](assets/cja-journey-email-delivered.png)

El **[!UICONTROL Tendencia de envíos frente a clics]** El gráfico presenta un análisis detallado de la participación de sus perfiles con sus correos electrónicos, lo que ofrece información valiosa sobre cómo varios dominios interactúan con el contenido.

+++ Obtenga más información sobre las métricas de tendencias de Entregado frente a Clic

* **[!UICONTROL Entregado]**: Número de correos electrónicos enviados correctamente, en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los correos electrónicos.

+++

### Estado del envío {#delivery-status}

![](assets/cja-journey-email-delivery-stat.png)

El **[!UICONTROL Estado del envío]** Este gráfico le permite ver el rendimiento de sus correos electrónicos de un vistazo. Rastree métricas clave como envíos y devoluciones, lo que le permitirá comprender rápidamente la eficacia de su recorrido de correo electrónico.

+++ Más información sobre las Métricas de estado de entrega

* **[!UICONTROL Entregado]**: Número de correos electrónicos enviados correctamente, en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Devoluciones para canales salientes]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores salientes]**: Número total de errores que se produjeron durante un proceso de envío que impidieron que se enviara a los perfiles.

* **[!UICONTROL Excluido]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

### Estadísticas de envío {#email-sending-statistics}

![](assets/cja-journey-email-sending-stat.png)

El **[!UICONTROL Envío de estadísticas]** proporciona una visión clara del rendimiento de los correos electrónicos en sus recorridos. Rastrea métricas clave como tasas de entrega e interacciones, lo que le proporciona información valiosa para optimizar su estrategia de correo electrónico y mejorar el alcance y la participación.

+++ Más información sobre el envío de métricas de estadísticas

* **[!UICONTROL People]**: Número de perfiles de usuario que se califican como perfiles de destinatario para los mensajes.

* **[!UICONTROL Objetivos]**: Número total de correos electrónicos procesados durante el proceso de envío.

* **[!UICONTROL Envíos]**: Número total de envíos del correo electrónico.

* **[!UICONTROL Entregado]**: Número de correos electrónicos enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Devoluciones]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores de salida]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.

* **[!UICONTROL Exclusiones de salida]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++


### Correo electrónico: Estadísticas de seguimiento {#email-tracking}

![](assets/cja-journey-email-track-stat.png)

El **[!UICONTROL Correo electrónico: estadísticas de seguimiento]** La tabla de ofrece una descripción detallada de la actividad de perfil relacionada con los correos electrónicos incluidos en el recorrido. Esto incluye métricas sobre aperturas, clics y otros indicadores de participación relevantes, lo que ofrece una vista completa de cómo los perfiles interactúan con el contenido del correo electrónico.

+++ Más información sobre las Métricas de estadísticas de seguimiento

* **[!UICONTROL Tasa de pulsaciones (CTR)]**: porcentaje de usuarios que interactuaron con el correo electrónico.

* **[!UICONTROL Tasa de apertura de pulsaciones (CTOR)]**: Número de veces que se abrió el correo electrónico.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los correos electrónicos.

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de un correo electrónico.

* **[!UICONTROL Aperturas de correo electrónico]**: Número de veces que los correos electrónicos se abrieron en un recorrido.

* **[!UICONTROL Aperturas de correo electrónico únicas]**: porcentaje de correos electrónicos abiertos.

* **[!UICONTROL Quejas de spam]**: Número de veces que un mensaje se declaró como correo no deseado.

* **[!UICONTROL Cancela la suscripción]**: Número de clics en el vínculo de baja de suscripción.

+++

### Dominios de correo electrónico {#email-domains}

![](assets/cja-journey-email-domain.png)

El **[!UICONTROL Dominios de correo electrónico]** ofrece un desglose detallado de los correos electrónicos clasificados por dominio, lo que proporciona una amplia perspectiva de las métricas de rendimiento de sus recorridos de correo electrónico. Este análisis completo le permite comprender el comportamiento de los distintos dominios en respuesta al contenido del correo electrónico.

+++ Más información sobre las métricas de Dominios de correo electrónico

* **[!UICONTROL Envíos]**: Número total de envíos del correo electrónico.

* **[!UICONTROL Entregado]**: Número de correos electrónicos enviados correctamente, en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Aperturas de correo electrónico]**: Número de veces que los correos electrónicos se abrieron en un recorrido.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los correos electrónicos.

* **[!UICONTROL Devoluciones para canales salientes]**: Número total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de correos electrónicos enviados.

* **[!UICONTROL Errores de salida]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.
+++

### Etiquetas de vínculos rastreados {#track-link-label}

![](assets/cja-journey-tracked-link-labels.png)

El **[!UICONTROL Etiquetas de vínculos rastreados]** ofrece una amplia descripción general de las etiquetas de vínculo de los correos electrónicos, destacando las que generan el mayor tráfico de visitantes. Esta función le permite identificar y priorizar los vínculos más populares.

+++ Obtenga más información sobre las métricas de etiquetas de vínculos rastreados

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de un correo electrónico.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los correos electrónicos.

+++

### URL de vínculos rastreados {#track-link-url}

![](assets/cja-journey-tracked-link-urls.png)

El **[!UICONTROL URL de vínculos rastreados]** proporciona una visión general de las direcciones URL del correo electrónico que atraen el mayor tráfico de visitantes. Esto le permite identificar y priorizar los vínculos más populares, lo que mejora su comprensión de la participación del perfil con contenido específico en los correos electrónicos.

+++ Más información sobre las métricas de URL de vínculos rastreados

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de un correo electrónico.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los correos electrónicos.

* **[!UICONTROL Visualizaciones]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Visualizaciones únicas]**: Número de veces que se abrió el mensaje, no se tienen en cuenta varias interacciones de un perfil.

+++

### Asuntos de correo electrónico {#email-subject}

![](assets/cja-journey-email-subjects.png)

El **[!UICONTROL Temas de correo electrónico]**  presenta una descripción general detallada de los temas de correo electrónico que han atraído el mayor tráfico de visitantes. Este recurso ofrece información valiosa sobre la dinámica de participación de la audiencia.

+++ Más información sobre las métricas de Temas de correo electrónico

* **[!UICONTROL People]**: Número de perfiles de usuario que se califican como perfiles de destinatario para los correos electrónicos.

+++

### Motivos de rechazo {#email-bounce-reasons}

El **[!UICONTROL Motivos del rechazo]** Esta tabla compila los datos disponibles relacionados con los mensajes rechazados, y proporciona una perspectiva detallada de los motivos específicos detrás de los rechazos de correo electrónico.

Para obtener más información sobre las devoluciones, consulte [Lista de supresión](../reports/suppression-list.md) página.

### Motivos excluidos {#email-excluded}

El **[!UICONTROL Razones de exclusión]** La tabla presenta una vista completa de los diferentes factores que resultaron en la exclusión de perfiles de usuario de la audiencia de destino, lo que da como resultado que el mensaje no se reciba.

Consulte [esta página](exclusion-list.md) para obtener la lista completa de motivos de exclusión.

### Motivos de error {#email-errors}

El **[!UICONTROL Motivos del error]** La tabla ofrece visibilidad de los errores específicos que se produjeron durante el proceso de envío y proporciona información valiosa sobre la naturaleza y la incidencia de los errores.

## Pestaña de notificación push {#push-global}

A partir del informe de recorrido, la variable **[!UICONTROL Notificación push]** Esta pestaña detalla la información principal relativa a las notificaciones push enviadas en el recorrido.

## Notificación push {#push-notification}

### Estadísticas de envío {#sending-statistics-push}

![](assets/cja-campaign-push-sending-stat.png)

El **[!UICONTROL Envío de estadísticas]** le ayuda a comprender el rendimiento de las notificaciones push. Incluye métricas clave como la tasa de entrega y el tamaño de la audiencia, lo que le ofrece información valiosa sobre la eficacia y el alcance de sus recorridos.

+++ Más información sobre el envío de métricas de estadísticas

* **[!UICONTROL People]**: Número de perfiles de usuario que se califican como perfiles de destinatario para sus mensajes SMS.

* **[!UICONTROL Objetivos]**: Número total de notificaciones push procesadas durante el análisis.

* **[!UICONTROL Envíos]**: Número total de envíos para la notificación push.

* **[!UICONTROL Entregado]**: Número de notificaciones push enviadas correctamente, en relación con el número total de notificaciones push enviadas.

* **[!UICONTROL Devoluciones para canales salientes]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de notificaciones push.

* **[!UICONTROL Errores salientes]**: Número total de errores que han impedido su envío a los perfiles.

* **[!UICONTROL Exclusiones salientes]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

### Estadísticas de seguimiento {#tracking-statistics-push}

![](assets/cja-campaign-push-track-stat.png)

El **[!UICONTROL Estadísticas de seguimiento]** ofrece una instantánea detallada de la actividad del perfil vinculada a sus notificaciones push, lo que proporciona perspectivas esenciales sobre la participación y la eficacia de las notificaciones push.

+++ Más información sobre las Métricas de estadísticas de seguimiento

* **[!UICONTROL Tasa de pulsaciones (CTR)]**: porcentaje de usuarios que interactuaron con la notificación push.

* **[!UICONTROL Tasa de apertura de clics (CTOR)]**: Número de veces que se abrió la notificación push.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en la notificación push.

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de la notificación push.

<!--
* **[!UICONTROL Push custom actions]**: 
-->
+++

### Etiquetas de vínculos rastreados {#track-link-label-push}

![](assets/cja-campaign-push-link-labels.png)

El **[!UICONTROL Etiquetas de vínculos rastreados]** ofrece una descripción general completa de las etiquetas de vínculo de las notificaciones push, destacando las que generan el mayor tráfico de visitantes. Esta función le permite identificar y priorizar los vínculos más populares.

+++ Obtenga más información sobre las métricas de etiquetas de vínculos rastreados

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido en las notificaciones push.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en las notificaciones push.

+++

### URL de vínculos rastreados {#track-link-url-push}

![](assets/cja-campaign-push-link-urls.png)

El **[!UICONTROL URL de vínculos rastreados]** proporciona una visión general de las direcciones URL dentro de las notificaciones push que atraen el mayor tráfico de visitantes. Esto le permite identificar y priorizar los vínculos más populares, lo que le permite comprender mejor la participación del perfil con contenido específico en las notificaciones push.

+++ Más información sobre las métricas de URL de vínculos rastreados

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido en las notificaciones push.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en las notificaciones push.

+++

### Motivos de rechazo {#bounce-reasons-push}

El **[!UICONTROL Razones de rechazos]** proporciona una amplia descripción general de los datos relacionados con las notificaciones push devueltas, lo que proporciona una valiosa perspectiva de los motivos específicos detrás de las instancias de devoluciones de notificaciones push.

### Motivos de error {#error-reasons-push}

El **[!UICONTROL Motivos del error]** La tabla de permite identificar los errores específicos que se produjeron durante el proceso de envío de las notificaciones push, lo que facilita un análisis exhaustivo de cualquier problema encontrado.

### Motivos excluidos {#exclude-reasons-push}

![](assets/cja-campaign-push-excluded.png)

El **[!UICONTROL Razones de exclusión]** Esta tabla muestra visualmente los diversos factores que llevaron a la exclusión de perfiles de usuario de la audiencia de destino, lo que les impidió recibir las notificaciones push.

Consulte [esta página](exclusion-list.md) para obtener la lista completa de motivos de exclusión.

## SMS {#sms}

### Tendencia de envíos frente a clics {#delivered-click-sms}

El **[!UICONTROL Tendencia de envíos frente a clics]** Este gráfico presenta un análisis detallado de la participación de sus perfiles con sus mensajes SMS, lo que ofrece información valiosa sobre cómo varios dominios interactúan con el contenido.

+++ Obtenga más información sobre las métricas de tendencias de Entregado frente a Clic

* **[!UICONTROL Entregado]**: Número de mensajes SMS enviados correctamente en relación con el número total de mensajes SMS.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en sus mensajes SMS.

+++

### Estado del envío {#delivery-status-sms}

El **[!UICONTROL Estado del envío]** ofrece una cuenta detallada de la actividad de perfil relacionada con sus mensajes SMS. Esto incluye métricas sobre mensajes enviados, clics y otros indicadores de participación relevantes, lo que ofrece una vista completa de cómo los perfiles interactúan con el contenido del SMS.

+++ Más información sobre las Métricas de estado de entrega

* **[!UICONTROL Entregado]**: Número de mensajes SMS enviados correctamente en relación con el número total de mensajes SMS.

* **[!UICONTROL Devoluciones para canales salientes]**: Total de errores acumulados durante el proceso de envío y el procesamiento automático de devoluciones en relación con el número total de mensajes SMS enviados.

* **[!UICONTROL Errores salientes]**: Número total de errores que han impedido su envío a los perfiles.

* **[!UICONTROL Exclusiones salientes]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

### Etiquetas de vínculos rastreados {#track-link-label-sms}

El **[!UICONTROL Etiquetas de vínculos rastreados]** ofrece una visión general completa de las etiquetas de vínculo dentro de los mensajes SMS, destacando las que generan el mayor tráfico de visitantes. Esta función le permite identificar y priorizar los vínculos más populares.

+++ Obtenga más información sobre las métricas de etiquetas de vínculos rastreados

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido del mensaje SMS.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en sus mensajes SMS.

+++

### URL de vínculos rastreados {#track-link-url-sms}

El **[!UICONTROL URL de vínculos rastreados]** Esta tabla proporciona una visión general de las direcciones URL de los mensajes SMS que atraen el mayor tráfico de visitantes. Esto le permite identificar y priorizar los vínculos más populares, lo que mejora su comprensión de la participación del perfil con contenido específico en los mensajes SMS.

+++ Más información sobre las métricas de URL de vínculos rastreados

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido del mensaje SMS.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en sus mensajes SMS.

* **[!UICONTROL Visualizaciones]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Visualizaciones únicas]**: Número de veces que se abrió el mensaje, no se tienen en cuenta varias interacciones de un perfil.

+++

### Mensaje entrante SMS {#sms-inbound}

El **[!UICONTROL Mensaje entrante de SMS]** La tabla presenta una descripción detallada de los mensajes SMS que han atraído el mayor tráfico de visitantes. Este recurso ofrece información valiosa sobre la dinámica de participación de la audiencia.

+++ Más información sobre las métricas de mensajes entrantes de SMS

* **[!UICONTROL People]**: Número de perfiles de usuario que se califican como perfiles de destinatario para sus mensajes SMS.

+++

### Tipo de mensaje SMS {#sms-message-type}

El **[!UICONTROL Tipo de mensaje SMS]** La tabla presenta una descripción detallada de los tipos de mensajes SMS que han atraído el mayor tráfico de visitantes. Este recurso ofrece información valiosa sobre la dinámica de participación de la audiencia.

+++ Más información sobre las métricas de tipo Mensaje SMS

* **[!UICONTROL People]**: Número de perfiles de usuario que se califican como perfiles de destinatario para sus mensajes SMS.

+++

### Proveedores de SMS {#sms-providers}

El **[!UICONTROL Proveedores de SMS]** La tabla presenta una descripción detallada de los proveedores de SMS que han atraído el mayor tráfico de visitantes. Este recurso ofrece información valiosa sobre la dinámica de participación de la audiencia.

+++ Más información sobre las métricas de proveedores de SMS

* **[!UICONTROL People]**: Número de perfiles de usuario que se califican como perfiles de destinatario para sus mensajes SMS.

+++

### Motivos de rechazo {#bounce-reasons-sms}

El **[!UICONTROL Razones de rechazos]** Esta tabla proporciona una visión general completa de los datos relacionados con los mensajes SMS devueltos, lo que ofrece una valiosa perspectiva de las razones específicas detrás de las instancias de devoluciones de mensajes SMS.

### Motivos de error {#error-reasons-sms}

El **[!UICONTROL Motivos del error]** Esta tabla le permite identificar los errores específicos que se produjeron durante el proceso de envío de sus mensajes SMS, lo que facilita un análisis exhaustivo de cualquier problema encontrado.

### Motivos excluidos {#excluded-reasons-sms}

El **[!UICONTROL Razones de exclusión]** Esta tabla muestra visualmente los diversos factores que llevaron a la exclusión de perfiles de usuario de la audiencia de destino, lo que les impidió recibir sus mensajes SMS.

Consulte [esta página](exclusion-list.md) para obtener la lista completa de motivos de exclusión.

## En la aplicación

### Tendencia de impresión y clics {#impression-click-trend}

![](assets/cja-inapp-impressions-click.png)

El **[!UICONTROL Tendencia de impresión y clics]** Este gráfico presenta un análisis detallado de la participación de sus perfiles con los mensajes en la aplicación, lo que ofrece información valiosa sobre cómo los perfiles interactúan con el contenido.

+++ Obtenga más información sobre las métricas de tendencias de impresión y clics

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los mensajes en la aplicación.

* **[!UICONTROL Visualizaciones]**: Número de veces que se abrió el mensaje.

+++

### Clics {#clicks-inapp}

El **[!UICONTROL Clics]** El gráfico muestra las métricas de clics en la aplicación, e ilustra tanto la cantidad total de clics en el contenido como la cantidad de perfiles únicos que hicieron clic en el contenido.

+++ Más información sobre las métricas de Clics

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de los mensajes en la aplicación

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los mensajes en la aplicación.

+++

### Mostrar {#display-inapp}

El **[!UICONTROL Visualizaciones]** Este gráfico le ayuda a comprender el alcance general del mensaje y la cantidad de perfiles únicos que interactúan con él.

+++ Más información sobre las Métricas de visualización

* **[!UICONTROL Visualizaciones]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Visualizaciones únicas]**: Número de veces que se abrió el mensaje, no se tienen en cuenta varias interacciones de un perfil.

+++

### Datos de seguimiento {#tracking-data-inapp}

El **[!UICONTROL Datos de seguimiento]** ofrece una instantánea detallada de la actividad del perfil vinculada a sus mensajes en la aplicación, lo que proporciona perspectivas esenciales sobre la participación y la eficacia de los mensajes en la aplicación.

+++ Más información sobre el Seguimiento de métricas de datos

* **[!UICONTROL People]**: Número de perfiles de usuario que se califican como perfiles de destino para los mensajes en la aplicación.

* **[!UICONTROL Tasa de pulsaciones (CTR)]**: porcentaje de usuarios que interactuaron con los mensajes en la aplicación.

* **[!UICONTROL Tasa de apertura de pulsaciones (CTOR)]**: Número de veces que se abrieron los mensajes en la aplicación.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los mensajes en la aplicación.

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de los mensajes en la aplicación.

* **[!UICONTROL Visualizaciones]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Visualizaciones únicas]**: Número de veces que se abrió el mensaje, no se tienen en cuenta varias interacciones de un perfil.

* **[!UICONTROL Envíos]**: Número total de envíos para los mensajes en la aplicación.

<!--
* **[!UICONTROL Inbound triggered]**: 

* **[!UICONTROL Inbound dismisses]**: 
-->
+++

### Etiquetas de vínculos rastreados {#track-link-label-inapp}

![](assets/cja-inapp-tracked-link-labels.png)

El **[!UICONTROL Etiquetas de vínculos rastreados]** ofrece una descripción general completa de las etiquetas de los vínculos de los mensajes en la aplicación, en los que se destacan los que generan el mayor tráfico de visitantes. Esta función le permite identificar y priorizar los vínculos más populares.

+++ Obtenga más información sobre las métricas de etiquetas de vínculos rastreados

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de los mensajes en la aplicación.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los mensajes en la aplicación.

* **[!UICONTROL Visualizaciones]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Visualizaciones únicas]**: Número de veces que se abrió el mensaje, no se tienen en cuenta varias interacciones de un perfil.

+++

### URL de vínculos rastreados {#track-link-url-inapp}

![](assets/cja-inapp-tracked-link-urls.png)

El **[!UICONTROL URL de vínculos rastreados]** proporciona una visión general de las direcciones URL de los mensajes en la aplicación que atraen el mayor tráfico de visitantes. Esto le permite identificar y priorizar los vínculos más populares, lo que le permite comprender mejor la participación del perfil con contenido específico en los mensajes en la aplicación.

+++ Más información sobre las métricas de URL de vínculos rastreados

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de los mensajes en la aplicación

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en los mensajes en la aplicación.

+++

## Web {#web-cja}

### Tendencia de impresión y clics {#impressions-web}

![](assets/cja-web-impression.png)

El **[!UICONTROL Tendencia de impresión y clics]** Este gráfico presenta un análisis detallado de la participación de sus perfiles con sus páginas web, lo que ofrece información valiosa sobre cómo los perfiles interactúan con el contenido.

+++ Obtenga más información sobre las métricas de tendencias de impresión y clics

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en las páginas web.

* **[!UICONTROL Visualizaciones]**: Número de veces que se abrió el mensaje.

+++

### Clics {#clicks-web}

![](assets/cja-web-clicks.png)

El **[!UICONTROL Clics]** Este gráfico muestra las métricas de clics en páginas web, ilustrando tanto el número total de clics en contenido como el número de perfiles únicos que hicieron clic en el contenido.

+++ Más información sobre las métricas de Clics

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de sus páginas web.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en las páginas web.

+++

### Visualizaciones {#displays-web}

![](assets/cja-web-displays.png)

El **[!UICONTROL Visualizaciones]** Este gráfico le ayuda a comprender el alcance general del mensaje y la cantidad de perfiles únicos que interactúan con él.

+++ Más información sobre las Métricas de visualización

* **[!UICONTROL Visualizaciones]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Visualizaciones únicas]**: Número de veces que se abrió el mensaje, no se tienen en cuenta varias interacciones de un perfil.

+++


### Datos de seguimiento {#track-data-web}

![](assets/cja-web-tracking-data.png)

El **[!UICONTROL Datos de seguimiento]** ofrece una instantánea detallada de la actividad del perfil vinculada a sus páginas web, proporcionando información esencial sobre la participación y la eficacia de las páginas web.

+++ Más información sobre el Seguimiento de métricas de datos

* **[!UICONTROL People]**: Número de perfiles de usuario que se califican como perfiles de destino para las páginas web.

* **[!UICONTROL Tasa de pulsaciones (CTR)]**: porcentaje de usuarios que interactuaron con las páginas web.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en las páginas web.

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de sus páginas web.

* **[!UICONTROL Visualizaciones]**: Número de veces que se abrió la página web.

* **[!UICONTROL Visualizaciones únicas]**: Número de veces que se abrió la página web, no se tienen en cuenta las interacciones múltiples de un perfil.

+++

### Etiquetas de vínculos rastreados {#track-link-web}

![](assets/cja-web-tracked-link-labels.png)

El **[!UICONTROL Etiquetas de vínculos rastreados]** ofrece una descripción general completa de las etiquetas de vínculo de las páginas web, destacando las que generan el mayor tráfico de visitantes. Esta función le permite identificar y priorizar los vínculos más populares.

+++ Obtenga más información sobre las métricas de etiquetas de vínculos rastreados

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de sus páginas web.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en las páginas web.

* **[!UICONTROL Visualizaciones]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Visualizaciones únicas]**: Número de veces que se abrió el mensaje, no se tienen en cuenta varias interacciones de un perfil.

+++

### URL de vínculos rastreados {#track-url-web}

![](assets/cja-web-tracked-link-urls.png)

El **[!UICONTROL URL de vínculos rastreados]** proporciona una visión general completa de las direcciones URL de las páginas web que atraen el mayor tráfico de visitantes. Esto le permite identificar y priorizar los vínculos más populares, lo que le permite comprender mejor la participación de perfiles con contenido específico en las páginas web.

+++ Más información sobre las métricas de URL de vínculos rastreados

* **[!UICONTROL Clics únicos]**: Número de perfiles que hicieron clic en un contenido de sus páginas web.

* **[!UICONTROL Clics]**: Número de veces que se hizo clic en un contenido en las páginas web.

* **[!UICONTROL Visualizaciones]**: Número de veces que se abrió el mensaje.

* **[!UICONTROL Visualizaciones únicas]**: Número de veces que se abrió el mensaje, no se tienen en cuenta varias interacciones de un perfil.

+++

## Correo directo {#direct-mail-cja}

### Estadísticas de envío {#sending-statistics-directmail}

![](assets/cja-direct-sending-stat.png)

El **[!UICONTROL Envío de estadísticas]** le ofrece una perspectiva del rendimiento de sus recorridos de correo postal. Consulte métricas clave como la cantidad de destinatarios objetivo y las piezas enviadas correctamente, lo que le ayuda a medir el alcance y la eficacia de sus envíos de correo.

+++ Más información sobre el envío de métricas de estadísticas

* **[!UICONTROL People]**: Número de perfiles de usuario que se califican como perfiles de destinatario para los mensajes.

* **[!UICONTROL Objetivos]**: Número total de mensajes de correo postal procesados durante el proceso de envío.

* **[!UICONTROL Envíos]**: Número total de envíos para los mensajes de correo postal.

* **[!UICONTROL Entregado]**: Número de mensajes de correo postal enviados correctamente, en relación con el número total de mensajes enviados.

* **[!UICONTROL Errores de salida]**: Número total de errores que se produjeron durante el proceso de envío y que impiden su envío a los perfiles.

* **[!UICONTROL Exclusiones de salida]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

### Estado del envío {#delivery-status-directmail}

![](assets/cja-direct-delivery-status.png)

El **[!UICONTROL Estado del envío]** El gráfico proporciona una vista completa de los datos relacionados con los mensajes de correo postal enviados en el recorrido, y ofrece información sobre las métricas clave como errores y envíos. Esto permite un análisis detallado del proceso de envío de mensajes de correo postal, proporcionando información valiosa sobre la eficacia y el rendimiento de sus recorridos.

+++ Más información sobre las Métricas de estado de entrega

* **[!UICONTROL Entregado]**: Número de mensajes de correo postal enviados correctamente, en relación con el número total de mensajes de correo postal enviados.

* **[!UICONTROL Errores salientes]**: Número total de errores que se produjeron durante un proceso de envío que impiden que se envíen los mensajes de correo postal a los perfiles.

* **[!UICONTROL Exclusiones salientes]**: Número de perfiles que han sido excluidos por Adobe Journey Optimizer.

+++

### Motivos de error {#error-reasons-directmail}

El **[!UICONTROL Motivos del error]** Esta tabla le permite identificar los errores específicos que se han producido durante el proceso de envío de sus mensajes de correo postal, lo que facilita un análisis exhaustivo de los problemas encontrados.

### Motivos excluidos {#exclude-reasons-directmail}

[](assets/cja-direct-excluded.png)

El **[!UICONTROL Razones de exclusión]** Esta tabla muestra visualmente los diversos factores que llevaron a la exclusión de perfiles de usuario de la audiencia de destino, lo que les impidió recibir sus mensajes de correo postal.

Consulte [esta página](exclusion-list.md) para obtener la lista completa de motivos de exclusión.
