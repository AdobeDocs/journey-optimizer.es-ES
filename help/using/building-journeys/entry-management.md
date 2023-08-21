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
source-git-commit: b3a047977fc4ffcab6674b573ef50018076d156a
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 14%

---


# Administración de entrada de perfil {#entry-management}

Existen dos tipos principales de recorridos:

* recorridos basados en eventos: a partir de un evento, estos recorridos son unitarios y se asocian a un individuo. Cuando se recibe el evento, el individuo entra en el recorrido. [Más información](#entry-unitary)
* leer recorridos de audiencia: empezando por una audiencia de lectura, son recorridos por lotes. Los individuos que pertenecen a la audiencia entran en el mismo recorrido. Estos recorridos pueden ser recurrentes o de una sola toma. [Más información](#entry-read-segment)

En ambos tipos de recorrido, un perfil no puede estar presente varias veces en el mismo recorrido y al mismo tiempo.

## Recorridos unitarios{#entry-unitary}

En los recorridos unitarios, puede habilitar o deshabilitar la reentrada:

* Si la reentrada está habilitada, un perfil puede entrar en un recorrido varias veces, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido.

* Si la reentrada está desactivada, un perfil no puede introducir varias veces el mismo recorrido.

De forma predeterminada, los nuevos recorridos permiten la reentrada. Puede desactivar la opción para recorridos de &quot;una sola vez&quot;, por ejemplo, si desea ofrecer un regalo de una sola vez cuando una persona visita una tienda. En ese caso, el cliente no debe poder volver a introducir el recorrido y recibir la oferta de nuevo. Cuando termina un recorrido, su estado es **[!UICONTROL Cerrado]**. Las nuevas personas ya no pueden entrar en el recorrido. Las personas que ya están en el recorrido terminan el recorrido normalmente. [Más información](journey-gs.md#entrance)

![](assets/journey-re-entrance.png)

Después del tiempo de espera global predeterminado de 30 días, el recorrido cambia a **Finalizado** estado. Los perfiles que ya están en el recorrido finalizan el recorrido normalmente. Los nuevos perfiles ya no pueden entrar en el recorrido. Este comportamiento solo se establece para 30 días (valor predeterminado de tiempo de espera de recorrido). Después de ese periodo, los perfiles pueden volver a entrar en el recorrido. Para evitarlo, añada una condición para comprobar si el perfil ya se ha introducido o no. Obtenga más información acerca del tiempo de espera de recorrido en [esta sección](journey-gs.md#global_timeout).

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 30 days. Indeed, as we remove all information about persons who entered the journey 30 days after they enter, we cannot know the person entered previously, more than 30 days ago. -->

Los recorridos unitarios (que se inician con un evento o una calificación de audiencia) incluyen un mecanismo de protección que evita que los recorridos se activen varias veces de forma errónea para el mismo evento. La reentrada del perfil está bloqueada temporalmente de forma predeterminada durante cinco minutos. Por ejemplo, si un evento activa un recorrido a las 12:01 para un perfil específico y otro llega a las 12:03 (ya sea el mismo evento o uno diferente que active el mismo recorrido), ese recorrido no se iniciará de nuevo para este perfil.

La clave también se utiliza para comprobar que una persona está en un recorrido. De hecho, una persona no puede estar en dos lugares diferentes en el mismo recorrido. Como resultado, el sistema no permite que la misma clave, por ejemplo la clave CRMID=3224, esté en diferentes lugares del mismo recorrido.

## Leer recorridos de audiencia{#entry-read-segment}

En un recorrido de audiencia de lectura:

* Para recorridos no recurrentes: el perfil introduce una vez y solo una vez el recorrido.

* Para recorridos recurrentes: de forma predeterminada, todos los perfiles pertenecientes a la audiencia introducen el recorrido en cada periodicidad. Deben finalizar el recorrido antes de poder volver a entrar en otra ocurrencia.

>[!NOTE]
>
>Hay dos opciones disponibles para recorridos de audiencia de lectura recurrentes. El **Forzar reentrada en repetición** hace que todos los perfiles que aún están presentes en la recorrido se cierren automáticamente en la siguiente ejecución. El **Lectura incremental** solo se dirige a las personas que ingresaron a la audiencia desde la última ejecución del recorrido. Consulte esta [sección](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

En recorridos de eventos empresariales que comienzan por una **Leer audiencia** actividad: sabiendo que este recorrido se basa en la recepción de un evento empresarial, si el perfil está cualificado en la audiencia esperada, introducirán el recorrido para cada evento empresarial recibido, lo que significa que este perfil puede ser varias veces en el mismo recorrido, al mismo tiempo, pero en el contexto de diferentes eventos empresariales.