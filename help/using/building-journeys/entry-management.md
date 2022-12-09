---
solution: Journey Optimizer
product: journey optimizer
title: Administración de entradas de perfil
description: Obtenga información sobre cómo administrar la entrada de perfil
feature: Journeys
role: User
level: Intermediate
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Administración de entradas de perfil {#entry-management}

De forma predeterminada, los nuevos recorridos permiten volver a entrar. Puede desmarcar la opción de recorridos de &quot;una toma&quot;, por ejemplo, si desea ofrecer un regalo único cuando una persona entra en una tienda. En ese caso, no desea que el cliente pueda volver a entrar en el recorrido y recibir la oferta de nuevo.

![](assets/journey-re-entrance.png)

Cuando finaliza un recorrido, su estado es **[!UICONTROL Closed]**. Nuevos individuos ya no pueden entrar en el recorrido. Las personas que ya están en el recorrido terminan normalmente el viaje.

Después del tiempo de espera global predeterminado de 30 días, el recorrido cambia a la **Finalizado** estado.  [Más información](journey-gs.md#global_timeout).


## Recorridos unitarios{#entry-unitary}

Los recorridos unitarios (comenzando por un evento o una calificación de segmento) incluyen una protección que evita que los recorridos se activen varias veces por error para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante 5 minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no volverá a comenzar para este perfil.

Además:

* Si la reentrada está activada, un perfil puede introducir un recorrido varias veces, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido.

* Si la reentrada está deshabilitada, un perfil no puede entrar varias veces el mismo recorrido

## Leer recorridos de segmentos{#entry-read-segment}

En un recorrido de segmento de lectura:

* Para recorridos no recurrentes: el perfil introduce una vez y solo una vez el recorrido.

* Para recorridos recurrentes: el perfil entra en el recorrido de cada recurrencia, si está en el estado esperado/del segmento. Si todavía estaba en el viaje desde una recurrencia anterior, lo reiniciará desde el principio.

En los recorridos de evento empresarial que comiencen por una **Leer segmento** actividad: sabiendo que este recorrido se basa en la recepción de un evento empresarial, si el perfil está cualificado en el segmento esperado, entrará en el recorrido de cada evento comercial recibido, lo que significa que este perfil puede estar varias veces en el mismo recorrido, al mismo tiempo, pero en el contexto de diferentes eventos comerciales.
