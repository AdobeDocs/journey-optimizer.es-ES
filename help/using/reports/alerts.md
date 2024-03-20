---
solution: Journey Optimizer
product: journey optimizer
title: Alertas
description: Obtenga información sobre cómo administrar alertas
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# Introducción a las alertas {#alerts}

## Alertas de acceso y suscripción {#alerting-capabilities}

Cuando se produce un error, puede recibir alertas del sistema en el centro de notificaciones de Journey Optimizer (alertas en la aplicación) o un correo electrónico.

Desde el **Alertas** , puede ver las alertas disponibles y suscribirse a ellas. Cuando se alcanza un determinado conjunto de condiciones en las operaciones (como un problema potencial cuando el sistema incumple un umbral), los mensajes de alerta se envían a cualquier usuario de la organización que se haya suscrito a ellos.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Obtenga más información sobre las alertas en Adobe Experience Platform en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=es){target="_blank"}.

En el menú de la izquierda, debajo de **Administration**, haga clic en **Alertas**. Hay dos alertas preconfiguradas para Journey Optimizer disponibles: la [Error de acción personalizada de recorrido](#alert-custom-actions) alerta y el [Déclencheur de segmentos leído incorrecto](#alert-read-audiences) alerta. Estas alertas se detallan a continuación.

Puede suscribirse a cada alerta individualmente desde la interfaz de usuario, seleccionando la **Suscribirse** de la opción **Alertas** panel. Utilice el mismo método para cancelar la suscripción.

![](assets/alert-subscribe.png)

También puede suscribirse a alertas mediante [Notificaciones de eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}. Las reglas de alerta se organizan en diferentes paquetes de suscripción. A continuación, se detallan las suscripciones a eventos correspondientes a las alertas de Journey Optimizer específicas.

Si se produce un comportamiento inesperado, se envía una notificación de alerta a los suscriptores. En función de las preferencias del usuario, las alertas se envían por correo electrónico o directamente en el centro de notificaciones de Journey Optimizer, en la esquina superior derecha de la interfaz de usuario. De forma predeterminada, solo están habilitadas las alertas en la aplicación. Para activar las alertas por correo electrónico, consulte [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.

Cuando se resuelve una alerta, los suscriptores reciben una notificación &quot;Resuelto&quot;.

>[!CAUTION]
>
>Las alertas específicas de Adobe Journey Optimizer solo se aplican a **live** recorridos. Las alertas no se activan para los recorridos en el modo de prueba.

## Error de acción personalizada de recorrido {#alert-custom-actions}

Esta alerta le advierte si falla una acción personalizada. Consideramos que hay un error en el que ha habido más del 1 % de errores en una acción personalizada específica en los últimos 5 minutos. Esto se evalúa cada 30 segundos.

![](assets/alerts-custom-action.png)

Las alertas de acciones personalizadas se resuelven cuando, en los últimos 5 minutos:

* no se ha producido ningún error en esa acción personalizada (o errores por debajo del umbral del 1 %),

* o bien, ningún perfil ha alcanzado esa acción personalizada.

El nombre de suscripción de evento de E/S correspondiente a la alerta de acción personalizada es **Error de acción personalizada de recorrido**.

## Error al leer Déclencheur de audiencia {#alert-read-audiences}

Esta alerta le advierte si **Leer audiencia** la actividad no ha procesado ningún perfil 10 minutos después de la hora programada de ejecución. Este error puede deberse a problemas técnicos o a que la audiencia está vacía.

![](assets/alerts1.png)

Alertas el **Leer audiencia** Las actividades de solo se aplican a recorridos recurrentes. **Leer audiencia** actividades en recorridos activos que tienen una programación para ejecutarse **Una** o **Lo antes posible** se ignoran.

Alertas el **Leer audiencia** se resuelven cuando un perfil introduce en **Leer audiencia** nodo.

El nombre de la suscripción del evento de E/S correspondiente a **Déclencheur de segmentos leído incorrecto** la alerta es **Retrasos, errores y errores del segmento de lectura de recorrido**.

## Resolución de problemas {#alert-troubleshooting}

Para solucionar problemas **Leer audiencia** alertas, compruebe el recuento de audiencias en la interfaz del Experience Platform.

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

Para solucionar problemas **Acción personalizada** alertas:

* Compruebe la acción personalizada mediante el modo de prueba en otro recorrido:

  ![](assets/alert-troubleshooting-2.png)

* Consulte el informe de recorridos para ver los motivos de error al realizar la acción.

  ![](assets/alert-troubleshooting-3.png)

* Compruebe los stepEvents de recorrido para buscar más información sobre &quot;failureReason&quot;.
* Compruebe la configuración de la acción personalizada y compruebe que la autenticación sigue siendo correcta. Realice una comprobación manual con Postman, por ejemplo.
