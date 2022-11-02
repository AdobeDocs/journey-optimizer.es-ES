---
solution: Journey Optimizer
product: journey optimizer
title: Administración de entradas de perfil
description: Obtenga información sobre cómo administrar la entrada de perfil
feature: Journeys
role: User
level: Intermediate
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Administración de entradas de perfil {#entry-management}

En un recorrido unitario:

* Si la reentrada está activada, un perfil puede introducir un recorrido varias veces, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido.

* Si la reentrada está desactivada, un perfil no puede introducir varias veces el mismo recorrido

Para obtener más información sobre la reentrada de perfiles, consulte esta [sección](../building-journeys/journey-gs.md#change-properties).

En un recorrido de segmento de lectura:

* Para recorridos no recurrentes: el perfil se introduce una vez y solo una vez en el recorrido.
* para recorridos recurrentes: el perfil introduce el recorrido en cada recurrencia, si se encuentra en el estado esperado o del segmento. Si todavía estaba en el recorrido por una recurrencia anterior, lo reiniciará desde el principio.

En los recorridos de evento empresarial que comienzan con un segmento de lectura :

Sabiendo que este recorrido se basa en la recepción de un evento empresarial, si el perfil está cualificado en el segmento esperado, introducirá el recorrido para cada evento comercial recibido, lo que significa que este perfil puede estar varias veces en el mismo recorrido, al mismo tiempo, pero en el contexto de diferentes eventos comerciales.

Los recorridos unitarios (comenzando por un evento o una calificación de segmento) incluyen una protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante 5 minutos. Por ejemplo, si un evento déclencheur un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.
