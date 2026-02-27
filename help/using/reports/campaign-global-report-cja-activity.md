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
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 1%

---

# Informe de campaña de actividad en directo {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

Puede acceder a su informe de campaña de Actividad en directo haciendo clic en el botón **[!UICONTROL Informes]** de su campaña y después seleccionando **[!UICONTROL Ver informe de todo el tiempo]**. [Más información](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Envío de estadísticas {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

La tabla **[!UICONTROL Estadísticas de envío]** proporciona una descripción detallada de las métricas clave relacionadas con su campaña de Actividad en vivo. Muestra información esencial, como el tamaño de la audiencia objetivo y la cantidad de actividad en directo que se entregó correctamente, lo que le ayuda a evaluar el alcance y el rendimiento generales de su actividad en directo.

+++ Más información sobre el envío de métricas de estadísticas

* **[!UICONTROL Segmentado]**: número de perfiles aptos para la audiencia antes de aplicar las exclusiones, las supresiones o las eliminaciones de consentimiento.

* **[!UICONTROL Envíos]**: Número total de actividades activas que se intentó enviar a perfiles de destino.

* **[!UICONTROL Entregado]**: Número de actividades activas entregadas correctamente a los dispositivos, en relación con el número total de envíos intentados.

* **[!UICONTROL Errores de envío]**: Número total de actividades activas que no se pudieron enviar debido a errores (por ejemplo, tokens no válidos o problemas de conectividad).

* **[!UICONTROL Enviar exclusiones]**: Número de perfiles excluidos del envío por Adobe Journey Optimizer (por ejemplo, debido al estado de exclusión o a las reglas de idoneidad).

+++

## Ciclo de actividad activo {#lifecycle}

La tabla **[!UICONTROL Ciclo de vida de la actividad en directo]** ofrece una vista completa de cómo progresa su actividad en directo a lo largo del tiempo. Proporciona visibilidad de los eventos clave, como cuándo se inicia, actualiza o finaliza la actividad, lo que le ayuda a comprender mejor la participación del usuario y el ciclo de vida general de la campaña de la actividad en directo.

Los informes difieren según si utiliza campañas transaccionales o de marketing.

### Actividad transaccional en directo

![](assets/activity-lifecycle.png)

Para la campaña transaccional, el informe Campaña de actividades en directo muestra todos los eventos del ciclo vital, incluidos los inicios remotos, los inicios locales, las actualizaciones y los finales.

+++ Obtenga más información acerca de las métricas del ciclo vital de la actividad con campañas transaccionales

* **[!UICONTROL Inicios remotos]**: Número total de eventos de inicio de actividades activas iniciados de forma remota, que suelen desencadenarse mediante el servidor o los sistemas back-end.

* **[!UICONTROL Inicios locales]**: Número total de eventos de inicio de actividades activas iniciados localmente en el dispositivo de un usuario, a menudo como resultado de la interacción del usuario o de déclencheur del lado del cliente.

* **[!UICONTROL Actualizaciones]**: Número total de actualizaciones de actividades activas enviadas a dispositivos. Las actualizaciones pueden incluir cambios de estado, nuevo contenido o notificaciones de progreso.

* **[!UICONTROL Finalizaciones]**: Número total de eventos de finalización de actividad en directo enviados a dispositivos.

* **[!UICONTROL Recuento total]**: Total general de todos los eventos del ciclo vital de la actividad en directo, incluidos los inicios, las actualizaciones y los fines, que proporcionan una medida completa del volumen de la actividad en directo.

+++

### Actividad de Marketing Live

![](assets/activity-lifecycle-broadcast.png)

Las campañas de marketing utilizan la actividad en directo para casos de uso de difusión, y envían actualizaciones a varios dispositivos simultáneamente.

Para la actividad de iOS Live en campañas de marketing, el informe muestra solo **[!UICONTROL Inicios remotos]** eventos y **[!UICONTROL errores de inicios remotos]** al inicio. Los eventos **[!UICONTROL Updates]** y **[!UICONTROL Ends]** no se rastrean porque APNS distribuye actualizaciones a todos los dispositivos sin proporcionar comentarios. Para ver los eventos **[!UICONTROL Updates]** y **[!UICONTROL Ends]**, usa [la consola de notificaciones push de Apple](https://developer.apple.com/notifications/push-notifications-console/).

+++ Obtenga más información sobre las métricas del ciclo vital de la actividad con campañas de marketing

* **[!UICONTROL Inicios remotos]**: Número total de eventos de inicio de actividades activas iniciados de forma remota, que suelen desencadenarse mediante el servidor o los sistemas back-end.

* **[!UICONTROL Errores de inicios remotos]**: Número total de errores que se produjeron al intentar iniciar la actividad en directo de forma remota (por ejemplo, tokens no válidos o problemas de conectividad).

+++

#### Recuperación de actualizaciones y recuentos finales mediante API {#retrieving-updates-end-api}

Como alternativa al uso de la consola de notificaciones push de Apple, las actualizaciones y los recuentos finales se pueden obtener a través de llamadas de API sin encabezado.

Al ejecutar las llamadas de actualización o finalización de API para casos de uso de difusión, la respuesta incluye una sección `controlBreakdown` que proporciona contadores que indican cuántas llamadas de actualización y finalización se ejecutaron para la ejecución de la actividad en directo. Este bloque está ausente para ejecuciones heredadas sin datos del ciclo vital. El estado de ejecución también se puede recuperar explícitamente mediante el punto de conexión de GET cuando sea necesario.

**ACTUALIZACIÓN/RESPUESTA FINAL (200 OK)**

```json
{
  "executionId": "HA-exec-abc",
  "campaignId": "campaign-abc-123",
  "campaignVersionId": "v1",
  "audienceId": "audience-segment-id",
  "status": "processing",
  "targetedProfileCount": 150000,
  "createdAt": "2026-02-27T10:00:00Z",
  "executionLifecycle": {
    "lastControlAt": "2026-02-27T10:45:00Z",
    "controlBreakdown": {
      "update": 5,
      "end": 1
    }
  }
}
```

**Estado de ejecución (GET)**

```
GET /im/executions/audience/{executionId}
```

## Motivos de error {#error-reasons}

![](assets/error-reasons-activity.png)

La tabla **[!UICONTROL Motivos del error]** le permite identificar los errores específicos que se produjeron durante el proceso de envío de su actividad en directo, lo que facilita un análisis exhaustivo de los problemas encontrados.

## Motivos excluidos {#excluded-reasons}

![](assets/excluded-activity.png)

La tabla **[!UICONTROL Razones de exclusión]** muestra visualmente los diversos factores que llevaron a la exclusión de perfiles de usuarios de la audiencia de destino, lo que les impidió recibir su actividad en vivo.
