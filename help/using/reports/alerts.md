---
solution: Journey Optimizer
product: journey optimizer
title: Alertas
description: Obtenga información sobre cómo administrar alertas
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: d5be5ba43351e3143fce7f64878baceb8507d7f8
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 6%

---

# Introducción a las alertas {#alerts}

Journey Optimizer aprovecha las funciones de alerta de Adobe Experience Platform. Esto le permite acceder a las alertas del sistema a través de la interfaz de usuario. Puede ver las alertas disponibles y suscribirse a ellas. Cuando se alcanza un determinado conjunto de condiciones en sus operaciones (por ejemplo, un problema potencial cuando el sistema supera un umbral), los mensajes de alerta se envían a cualquier usuario de su organización que se haya suscrito a ellos. Estos mensajes se pueden repetir durante un intervalo de tiempo predefinido hasta que se haya resuelto la alerta.

Obtenga más información sobre las alertas en Adobe Experience Platform [documentación](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=es).
Para obtener información sobre cómo suscribirse a las alertas y configurarlas, consulte esta [página](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html).

En el menú de la izquierda, debajo de **Administración**, haga clic en **Alertas**. Hay disponible una alerta preconfigurada para Journey Optimizer. Esta alerta le avisará si un nodo de segmento de lectura no ha procesado ningún perfil durante el lapso de tiempo definido.

![](assets/alerts1.png)

Si se produce este comportamiento inesperado, se envía una notificación de alerta a los suscriptores de la alerta por correo electrónico, en la esquina superior derecha de la interfaz.

![](assets/alerts2.png)

When [visualización de reglas de alerta en la interfaz de usuario de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), puede suscribirse a cada regla individualmente. Al suscribirse a alertas mediante [Notificaciones de eventos de E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html)sin embargo, las reglas de alerta están organizadas en diferentes paquetes de suscripción. El nombre de suscripción del evento de E/S correspondiente a la alerta Leer segmento es: &quot;Recorrido leer retrasos, errores y errores del segmento&quot;.

>[!WARNING]
>
>Estas alertas se aplican únicamente a los recorridos activos. Las alertas no se activan para los recorridos en el modo de prueba.
