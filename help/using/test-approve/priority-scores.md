---
title: Asignar puntuaciones de prioridad a recorridos y campañas
description: Aprenda a asignar puntuaciones de prioridad a recorridos y campañas.
role: User
level: Beginner
badge: label="Disponibilidad limitada"
hide: true
hidefromtoc: true
source-git-commit: e1121d998711ea4751da5293efdd7c1578ee44a2
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 6%

---


# Asignar puntuaciones de prioridad a recorridos y campañas {#priority}

>[!BEGINSHADEBOX]

Lo que encontrará en esta guía de documentación:

* [Introducción a la administración y priorización de conflictos](gs-conflict-prioritization.md)
* [Detección de posibles conflictos en recorridos y campañas](conflicts.md)
* **[Asignar puntuaciones de prioridad a recorridos y campañas](priority-scores.md)**
* [límite y arbitraje de recorridos](journey-capping.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Actualmente, las herramientas de priorización y administración de conflictos están disponibles como disponibilidad limitada solo para usuarios seleccionados.

Journey Optimizer le permite asignar una puntuación de prioridad a un recorrido o campaña. La prioridad es esencial para priorizar un recorrido, una campaña o una acción cuando hay una restricción impuesta (como un límite de frecuencia). En situaciones en las que un cliente cumple los requisitos para muchos recorridos, campañas o comunicaciones y desea ser selectivo sobre qué debe introducir y recibir, debe utilizar este campo.

>[!NOTE]
>
>La puntuación de prioridad está disponible para canales entrantes: canales web, en la aplicación y basados en código. En recorrido, la puntuación de prioridad solo está disponible para los canales **en la aplicación** y **basados en código**.

Asignar una puntuación de prioridad es crucial para la comunicación entrante, como web, móvil y en la aplicación. Si tiene varias campañas con la misma configuración de canal (por ejemplo, un banner en la parte superior de la página web), esto podría resultar problemático, ya que solo se puede mostrar contenido de una campaña de forma factible. La puntuación de prioridad es donde insertará su preferencia para la campaña que debe mostrarse cuando el destinatario pueda cumplir los requisitos para más de una campaña.

Para asignar una puntuación de prioridad a un recorrido o campaña, escriba un valor numérico (de 0 a 100) en el campo **[!UICONTROL Puntuación de prioridad]** ubicado en las propiedades de recorrido o campaña. Tenga en cuenta que, cuanto mayor sea el número, mayor será la prioridad. Si fuera el autor de esta campaña y quisiera asegurarse de que se muestra su contenido, le daría una puntuación de 100.

![](assets/priority-score.png)

En situaciones en las que dos campañas tienen la misma puntuación de prioridad, se muestra la campaña que se activó primero.
