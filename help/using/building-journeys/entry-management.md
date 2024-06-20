---
solution: Journey Optimizer
product: journey optimizer
title: Administración de entrada de perfil
description: Obtenga información sobre cómo administrar la entrada de perfil
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: reentrada, recorrido, perfil, recurrente
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 5%

---


# Administración de la entrada del perfil {#entry-management}

Existen cuatro tipos de recorridos:

* **Evento unitario** recorridos: estos recorridos comienzan con un evento unitario. Cuando se recibe el evento, el perfil asociado entra en el recorrido. [Más información](#entry-unitary)

* **Evento empresarial** recorridos: estos recorridos comienzan con un evento empresarial inmediatamente seguido de una audiencia de lectura. Cuando se recibe el evento, los perfiles pertenecientes a la audiencia de destino entran en el recorrido. Se creará una instancia de este recorrido para cada perfil. [Más información](#entry-business)

* **Leer audiencia** recorridos: estos recorridos comienzan con una audiencia de lectura. Cuando se ejecuta el recorrido, los perfiles pertenecientes a la audiencia de destino entran en el recorrido. Se creará una instancia de este recorrido para cada perfil. Estos recorridos pueden ser recurrentes o de una sola toma. [Más información](#entry-read-audience)

* **Calificación de audiencia** recorridos: estos recorridos comienzan con un evento de calificación de audiencia. Estos recorridos escuchan las entradas y salidas de perfiles en las audiencias. Cuando esto sucede, el perfil asociado entra en el recorrido. [Más información](#entry-unitary)

En todos los tipos de recorrido, un perfil no puede estar presente varias veces en el mismo recorrido y al mismo tiempo. Para comprobar que una persona está en un recorrido, la identidad del perfil se utiliza como clave. El sistema no permite que la misma clave, por ejemplo la clave CRMID=3224, esté en diferentes lugares del mismo recorrido.

## Recorridos de calificación de eventos unitarios y audiencias{#entry-unitary}

En los recorridos de calificación de eventos unitarios y audiencias, puede habilitar o deshabilitar la reentrada:

* Si la reentrada está habilitada, un perfil puede entrar en un recorrido varias veces, pero no puede hacerlo hasta que salga completamente de la instancia anterior del recorrido.

* Si la reentrada está desactivada, un perfil no puede introducir varias veces el mismo recorrido, dentro del periodo de tiempo de espera de recorrido global. Consulte esta [sección](../building-journeys/journey-properties.md#global_timeout).

De forma predeterminada, los recorridos permiten la reentrada. Si la variable **Permitir la reentrada** está activada, la opción **Período de espera de reentrada** se muestra el campo. Permite definir el tiempo de espera antes de permitir que un perfil vuelva a entrar en el recorrido. Esto evita que los recorridos se activen varias veces por error para el mismo evento. De forma predeterminada, el campo se establece en 5 minutos. La duración máxima es de 91 días ([tiempo de espera global](journey-properties.md#global_timeout)).

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![](assets/journey-re-entrance.png)

Después del periodo de reentrada, los perfiles pueden volver a entrar en el recorrido. Para evitarlo y deshabilitar completamente la reentrada para esos perfiles, puede agregar una condición para comprobar si el perfil introducido ya está o no, utilizando datos de perfil o audiencia.

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## Recorridos empresariales{#entry-business}

<!--
Business events follow re-entrance rules in the same way as for unitary events. If a journey allows re-entrance, the next business event will be processed.
-->

Para permitir varias ejecuciones de eventos empresariales, active la opción correspondiente en la **[!UICONTROL Ejecución]** de las propiedades del recorrido.

![](assets/business-entry.png)

En el caso de los eventos empresariales, para un recorrido determinado, los datos de audiencia recuperados en la primera ejecución se reutilizan durante un intervalo de tiempo de 1 hora.

Un perfil puede estar presente varias veces en el mismo recorrido, al mismo tiempo, pero en el contexto de diferentes eventos empresariales.

Para obtener más información, consulte [sección](../event/about-creating-business.md)

## Leer recorridos de audiencia{#entry-read-audience}

Los recorridos de audiencia de lectura pueden ser recurrentes o de una sola toma:

* Para recorridos no recurrentes: el perfil introduce una vez y solo una vez el recorrido.

* Para recorridos recurrentes: de forma predeterminada, todos los perfiles pertenecientes a la audiencia introducen el recorrido en cada periodicidad. Deben finalizar el recorrido antes de poder volver a entrar en otra ocurrencia.

Hay dos opciones disponibles para los recorridos de lectura de audiencia recurrentes:

* **Lectura incremental** opción: cuando un recorrido con una **Leer audiencia** se ejecuta por primera vez, todos los perfiles de la audiencia entran en el recorrido. Esta opción le permite dirigirse, después de la primera incidencia, solo a las personas que ingresaron a la audiencia desde la última ejecución del recorrido.

  >[!NOTE]
  >
  >Si va a segmentar un [audiencia de carga personalizada](../audience/about-audiences.md#segments-in-journey-optimizer) en el recorrido, los perfiles solo se recuperan en la primera periodicidad si esta opción está habilitada en un recorrido recurrente, ya que estas audiencias son fijas.

* **Forzar reentrada en repetición**: esta opción permite hacer que todos los perfiles que aún están presentes en la recorrido se cierren automáticamente en la siguiente ejecución. Si la duración de los perfiles en este recorrido puede ser mayor que la periodicidad (por ejemplo, si utiliza actividades de espera), no active esta opción para asegurarse de que los perfiles puedan finalizar su recorrido.

![](assets/read-audience-options.png)

Para obtener más información, consulte [sección](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
