---
solution: Journey Optimizer
product: journey optimizer
title: Informe de campaña
description: Aprenda a utilizar los datos de actividad en directo desde el informe de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '400'
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

* **[!UICONTROL Segmentación]**: Número total de perfiles segmentados durante la actividad en directo.

* **[!UICONTROL Envíos]**: Número total de notificaciones push que se intentaron enviar a perfiles de destino.

* **[!UICONTROL Entregado]**: Número de notificaciones push entregadas correctamente a los dispositivos, en relación con el número total de envíos intentados.

* **[!UICONTROL Enviar errores]**: Número total de notificaciones push que no se pudieron enviar debido a errores (por ejemplo, tokens no válidos o problemas de conectividad).

* **[!UICONTROL Enviar exclusiones]**: Número de perfiles excluidos del envío por Adobe Journey Optimizer (por ejemplo, debido al estado de exclusión o a las reglas de idoneidad).

+++

## Ciclo de actividad activo {#lifecycle}

![](assets/activity-lifecycle.png)

La tabla **[!UICONTROL Ciclo de vida de la actividad en directo]** ofrece una vista completa de cómo progresan sus actividades en directo a lo largo del tiempo. Proporciona visibilidad de los eventos clave, como cuándo se inician, actualizan o finalizan las actividades, lo que le ayuda a comprender mejor la participación del usuario y el ciclo de vida general de las campañas de Actividad en directo.

+++ Más información sobre las Métricas del ciclo vital de actividades activas

* **[!UICONTROL Inicios remotos]**: Número de actividades activas iniciadas de forma remota, normalmente desencadenadas por el servidor o el sistema back-end.

* **[!UICONTROL Inicios locales]**: número de actividades activas iniciadas localmente en el dispositivo de un usuario, a menudo como resultado de la interacción del usuario o de déclencheur del lado del cliente.

**[!UICONTROL Actualizaciones]**: Número total de actualizaciones de actividades activas enviadas a dispositivos. Las actualizaciones pueden incluir cambios de estado, nuevo contenido o notificaciones de progreso.

**[!UICONTROL Ends]**: número de actividades activas que se han finalizado, ya sea automáticamente al finalizar o manualmente tras un déclencheur o tiempo de espera definido.

**[!UICONTROL Recuento total]**: Total general de todos los eventos del ciclo vital de la actividad en directo, incluidos los inicios, las actualizaciones y los fines, que proporcionan una medida completa del volumen de la actividad en directo.

+++

## Motivos de error {#error-reasons}

![](assets/error-reasons-activity.png)

La tabla **[!UICONTROL Motivos del error]** le permite identificar los errores específicos que se produjeron durante el proceso de envío de sus actividades en directo, lo que facilita un análisis exhaustivo de cualquier problema encontrado.

## Motivos excluidos {#excluded-reasons}

![](assets/excluded-activity.png)

La tabla **[!UICONTROL Razones de exclusión]** muestra visualmente los diversos factores que llevaron a la exclusión de perfiles de usuarios de la audiencia de destino, lo que les impidió recibir su actividad en vivo.
