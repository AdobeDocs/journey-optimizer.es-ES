---
solution: Journey Optimizer
product: journey optimizer
title: Informe de campaña
description: Aprenda a utilizar los datos de actividad en directo desde el informe de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 58034ec4-62dc-406c-99c4-d6b7aa107140
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 2%

---

# Informe de campaña de actividad en directo {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

Puede acceder a su informe de campaña de Actividad en directo haciendo clic en el botón **[!UICONTROL Informes]** de su campaña y después seleccionando **[!UICONTROL Ver informe de todo el tiempo]**. [Más información](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Envío de estadísticas {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

La tabla **[!UICONTROL Estadísticas de envío]** proporciona una descripción detallada de las métricas clave relacionadas con sus campañas de Actividad en directo. Muestra información esencial, como el tamaño de la audiencia objetivo y la cantidad de notificaciones push enviadas correctamente, lo que le ayuda a evaluar el alcance y el rendimiento generales de sus notificaciones push activas.

+++ Más información sobre el envío de métricas de estadísticas

* **[!UICONTROL Segmentado]**: número de perfiles aptos para la audiencia antes de aplicar las exclusiones, las supresiones o las eliminaciones de consentimiento.

* **[!UICONTROL Envíos]**: Número total de notificaciones push que se intentaron enviar a perfiles de destino.

* **[!UICONTROL Entregado]**: Número de notificaciones push entregadas correctamente a los dispositivos, en relación con el número total de envíos intentados.

* **[!UICONTROL Enviar errores]**: Número total de notificaciones push que no se pudieron enviar debido a errores (por ejemplo, tokens no válidos o problemas de conectividad).

* **[!UICONTROL Enviar exclusiones]**: Número de perfiles excluidos del envío por Adobe Journey Optimizer (por ejemplo, debido al estado de exclusión o a las reglas de idoneidad).

+++

## Ciclo de actividad activo {#lifecycle}

La tabla **[!UICONTROL Ciclo de vida de la actividad en directo]** ofrece una vista completa de cómo progresan sus actividades en directo a lo largo del tiempo. Proporciona visibilidad de los eventos clave, como cuándo se inician, actualizan o finalizan las actividades, lo que le ayuda a comprender mejor la participación del usuario y el ciclo de vida general de las campañas de Actividad en directo.

Los informes difieren según si utiliza campañas transaccionales o de marketing.

### Actividades transaccionales activas

![](assets/activity-lifecycle.png)

Para la campaña transaccional, el informe de campaña de actividades en directo muestra todos los eventos del ciclo vital, incluidos los inicios remotos, los inicios locales, las actualizaciones y los finales.

+++ Obtenga más información acerca de las métricas del ciclo vital de la actividad con campañas transaccionales

* **[!UICONTROL Inicios remotos]**: Número total de eventos de inicio de actividades activas iniciados de forma remota, normalmente desencadenados por el servidor o los sistemas back-end.

* **[!UICONTROL Inicios locales]**: Número total de eventos de inicio de actividades activas iniciados localmente en el dispositivo de un usuario, a menudo como resultado de la interacción del usuario o de déclencheur del lado del cliente.

* **[!UICONTROL Actualizaciones]**: Número total de actualizaciones de actividades activas enviadas a dispositivos. Las actualizaciones pueden incluir cambios de estado, nuevo contenido o notificaciones de progreso.

* **[!UICONTROL Finalizaciones]**: Número total de eventos de finalización de actividades en curso enviados a dispositivos.

* **[!UICONTROL Recuento total]**: Total general de todos los eventos del ciclo vital de la actividad en directo, incluidos los inicios, las actualizaciones y los fines, que proporcionan una medida completa del volumen de la actividad en directo.

+++

### Marketing Live activities

![](assets/activity-lifecycle-broadcast.png)

Las campañas de marketing utilizan actividades en directo para casos de uso de difusión, y envían actualizaciones a varios dispositivos simultáneamente.

Para las actividades de iOS Live en campañas de marketing, el informe muestra solo **[!UICONTROL Inicios remotos]** eventos y **[!UICONTROL errores de inicios remotos]** al inicio. Los eventos **[!UICONTROL Updates]** y **[!UICONTROL Ends]** no se rastrean porque APNS distribuye actualizaciones a todos los dispositivos sin proporcionar comentarios. Para ver los eventos **[!UICONTROL Updates]** y **[!UICONTROL Ends]**, usa [la consola de notificaciones push de Apple](https://developer.apple.com/notifications/push-notifications-console/).

+++ Obtenga más información sobre las métricas del ciclo vital de la actividad con campañas de marketing

* **[!UICONTROL Inicios remotos]**: Número total de eventos de inicio de actividades activas iniciados de forma remota, normalmente desencadenados por el servidor o los sistemas back-end.

* **[!UICONTROL Errores de inicios remotos]**: Número total de errores que se produjeron al intentar iniciar actividades Live de forma remota (por ejemplo, tokens no válidos o problemas de conectividad).

+++

## Motivos de error {#error-reasons}

![](assets/error-reasons-activity.png)

La tabla **[!UICONTROL Motivos del error]** le permite identificar los errores específicos que se produjeron durante el proceso de envío de sus actividades en directo, lo que facilita un análisis exhaustivo de cualquier problema encontrado.

## Motivos excluidos {#excluded-reasons}

![](assets/excluded-activity.png)

La tabla **[!UICONTROL Razones de exclusión]** muestra visualmente los diversos factores que llevaron a la exclusión de perfiles de usuarios de la audiencia de destino, lo que les impidió recibir su actividad en vivo.
