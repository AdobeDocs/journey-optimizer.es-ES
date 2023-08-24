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
source-git-commit: 6386a5ee5a0d1f221beab67f43636c599531736a
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 4%

---

# Introducción a las alertas {#alerts}

Journey Optimizer aprovecha las funcionalidades de alerta de Adobe Experience Platform. Esto le permite acceder a las alertas del sistema a través de la interfaz de usuario. Puede ver las alertas disponibles y suscribirse a ellas.

Cuando se alcanza un determinado conjunto de condiciones en las operaciones (como un problema potencial cuando el sistema incumple un umbral), los mensajes de alerta se envían a cualquier usuario de la organización que se haya suscrito a ellos.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

Más información sobre las alertas en Adobe Experience Platform [documentación](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=es).

Para obtener información sobre cómo suscribirse a alertas y configurarlas, consulte esta sección [página](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

>[!AVAILABILITY]
>
>Algunos cambios de diseño están en curso para la alerta &#39;Leer Déclencheur de audiencia no ha tenido éxito&#39;, por lo que esta alerta está en pausa por ahora y se ha eliminado temporalmente de la interfaz de usuario. Una vez lanzados estos cambios, la alerta vuelve a aparecer y usted puede suscribirse a ella.

En el menú de la izquierda, debajo de **Administration**, haga clic en **Alertas**. Hay disponible una alerta preconfigurada para Journey Optimizer. Esta alerta le advierte si falla una acción personalizada. Consideramos que hay un error en el que ha habido más del 1 % de errores en una acción personalizada específica en los últimos 5 minutos. Esto se evalúa cada 30 segundos.

![](assets/alerts-custom-action.png)


<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

Si se produce un comportamiento inesperado, se envía una notificación de alerta a los suscriptores por correo electrónico o directamente en Journey Optimizer, en la esquina superior derecha de la interfaz, según las preferencias del usuario.

Cuando se resuelve una alerta, recibe una notificación &quot;Resuelto&quot;. Para la alerta de acción personalizada, esto puede ocurrir por dos motivos:
* En los últimos 5 minutos, no ha habido ningún error en esa acción personalizada (o errores por debajo del umbral del 1 %).
* Ningún perfil ha alcanzado esa acción personalizada.

Cuándo [ver las reglas de alerta en la IU de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), puede suscribirse a cada regla individualmente. Al suscribirse a alertas mediante [Notificaciones de eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)Sin embargo, las reglas de alerta están organizadas en diferentes paquetes de suscripción. El nombre de suscripción de evento de E/S correspondiente a la alerta de acción personalizada es: &quot;Error de acción personalizada de Recorrido&quot;.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".-->

>[!WARNING]
>
>Estas alertas solo se aplican a los recorridos activos. Las alertas no se activarán para los recorridos en modo de prueba.

