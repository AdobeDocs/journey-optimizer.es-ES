---
solution: Journey Optimizer
product: journey optimizer
title: Alertas
description: Obtenga información sobre cómo administrar alertas
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 78085934a00f4e365b49012b426e57a218bf48ba
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 1%

---

# Introducción a las alertas {#alerts}

## Funcionalidades de alerta {#alerting-capabilities}

Puede acceder a las alertas del sistema a través de la interfaz de usuario o recibir un correo electrónico cuando se produce un error. Desde el **Alertas** , puede ver las alertas disponibles y suscribirse a ellas. Cuando se alcanza un determinado conjunto de condiciones en las operaciones (como un problema potencial cuando el sistema incumple un umbral), los mensajes de alerta se envían a cualquier usuario de la organización que se haya suscrito a ellos.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Obtenga más información sobre las alertas en Adobe Experience Platform en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=es){target="_blank"}.

En el menú de la izquierda, debajo de **Administration**, haga clic en **Alertas**. Hay dos alertas preconfiguradas para Journey Optimizer disponibles: la [Error de acción personalizada de recorrido](#alert-custom-actions) alerta y el [Déclencheur de segmentos leído incorrecto](#alert-read-audiences) alerta. Estas alertas se detallan a continuación.

Puede suscribirse a cada alerta individualmente desde la interfaz de usuario, seleccionando la **Suscribirse** de la opción **Alertas** panel. Utilice el mismo método para cancelar la suscripción.

![](assets/alert-subscribe.png)

También puede suscribirse a alertas mediante [Notificaciones de eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html){target="_blank"}. Las reglas de alerta se organizan en diferentes paquetes de suscripción. A continuación, se detallan las suscripciones a eventos correspondientes a las alertas de Journey Optimizer específicas.

Si se produce un comportamiento inesperado, se envía una notificación de alerta a los suscriptores. En función de las preferencias del usuario, las alertas se envían por correo electrónico, o directamente en el centro de notificaciones de Journey Optimizer, en la esquina superior derecha de la interfaz de usuario.

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

## Déclencheur de segmentos leído incorrecto {#alert-read-audiences}

Esta alerta le advierte si **Leer audiencia** la actividad no ha procesado ningún perfil 10 minutos después de la hora programada de ejecución. Este error puede deberse a problemas técnicos o a que la audiencia está vacía.

![](assets/alerts1.png)

Alertas el **Leer audiencia** Las actividades de solo se aplican a recorridos recurrentes. **Leer audiencia** actividades en recorridos activos que tienen una programación para ejecutarse **Una** o **Lo antes posible** se ignoran.

Alertas el **Leer audiencia** se resuelven cuando un perfil introduce en **Leer audiencia** nodo.

El nombre de la suscripción del evento de E/S correspondiente a **Déclencheur de segmentos leído incorrecto** la alerta es **Retrasos, errores y errores del segmento de lectura de recorrido**.
