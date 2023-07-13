---
solution: Journey Optimizer
product: journey optimizer
title: Administración de entrada de perfil
description: Obtenga información sobre cómo administrar la entrada de perfil
feature: Journeys
role: User
level: Intermediate
keywords: reentrada, recorrido, perfil, recurrente
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 15%

---

# Administración de entrada de perfil {#entry-management}

De forma predeterminada, los nuevos recorridos permiten la reentrada. Puede desmarcar la opción para recorridos de &quot;una sola vez&quot;, por ejemplo, si desea ofrecer un regalo de una sola vez cuando una persona entra en una tienda. En ese caso, no desea que el cliente pueda volver a introducir el recorrido y recibir la oferta de nuevo.

![](assets/journey-re-entrance.png)

Cuando termina un recorrido, su estado es **[!UICONTROL Cerrado]**. Las nuevas personas ya no pueden entrar en el recorrido. Las personas que ya están en el recorrido terminan el recorrido normalmente.

Después del tiempo de espera global predeterminado de 30 días, el recorrido cambia a **Finalizado** estado.  [Más información](journey-gs.md#global_timeout).


## Recorridos unitarios{#entry-unitary}

Los recorridos unitarios (que comienzan con un evento o una calificación de audiencia) incluyen una protección que evita que los recorridos se activen varias veces por error para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante cinco minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.

Además:

* Si la reentrada está habilitada, un perfil puede entrar en un recorrido varias veces, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido.

* Si la reentrada está desactivada, un perfil no puede introducir varias veces el mismo recorrido

## Leer recorridos de audiencia{#entry-read-segment}

En un recorrido de audiencia de lectura:

* Para recorridos no recurrentes: el perfil introduce una vez y solo una vez el recorrido.

* Para recorridos recurrentes: el perfil introduce el recorrido en cada periodicidad, si está en el estado de audiencia/esperado. Si todavía estaba en el recorrido de una repetición anterior, lo reiniciará desde el principio.

En recorridos de eventos empresariales que comienzan por una **Leer audiencia** actividad: sabiendo que este recorrido se basa en la recepción de un evento empresarial, si el perfil está cualificado en la audiencia esperada, introducirá el recorrido para cada evento empresarial recibido, lo que significa que este perfil puede ser varias veces en el mismo recorrido, al mismo tiempo, pero en el contexto de diferentes eventos empresariales.
