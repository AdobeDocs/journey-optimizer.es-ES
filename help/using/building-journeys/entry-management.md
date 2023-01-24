---
solution: Journey Optimizer
product: journey optimizer
title: Administración de entradas de perfil
description: Obtenga información sobre cómo administrar la entrada de perfil
feature: Journeys
role: User
level: Intermediate
keywords: reentrada, recorrido, perfil, recurrente
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 22%

---

# Administración de entradas de perfil {#entry-management}

De forma predeterminada, los nuevos recorridos permiten volver a entrar. Puede desmarcar la opción de recorridos de &quot;una toma&quot;, por ejemplo, si desea ofrecer un regalo único cuando una persona entra en una tienda. En ese caso, no desea que el cliente pueda volver a entrar en el recorrido y recibir la oferta de nuevo.

![](assets/journey-re-entrance.png)

Cuando finaliza un recorrido, su estado es **[!UICONTROL Cerrado]**. Las personas nuevas ya no pueden entrar en el recorrido. Las personas que ya están en el recorrido terminan normalmente el recorrido.

Después del tiempo de espera global predeterminado de 30 días, el recorrido cambia a la variable **Finalizado** estado.  [Más información](journey-gs.md#global_timeout).


## Recorridos unitarios{#entry-unitary}

Los recorridos unitarios (que se inician con un evento o una calificación de segmentos) incluyen una protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante cinco minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.

Además:

* Si la reentrada está activada, un perfil puede introducir un recorrido varias veces, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido.

* Si la reentrada está desactivada, un perfil no puede introducir varias veces el mismo recorrido

## Leer recorridos de segmentos{#entry-read-segment}

En un recorrido de segmento de lectura:

* Para recorridos no recurrentes: el perfil se introduce una vez y solo una vez en el recorrido.

* Para recorridos recurrentes: el perfil introduce el recorrido en cada recurrencia, si se encuentra en el estado esperado o del segmento. Si todavía estaba en el recorrido por una recurrencia anterior, lo reiniciará desde el principio.

En recorridos de eventos empresariales que empiecen por un **Leer segmento** actividad: sabiendo que este recorrido se basa en la recepción de un evento comercial, si el perfil está cualificado en el segmento esperado, introducirá el recorrido para cada evento comercial recibido, lo que significa que este perfil puede estar varias veces en el mismo recorrido, al mismo tiempo, pero en el contexto de diferentes eventos comerciales.
