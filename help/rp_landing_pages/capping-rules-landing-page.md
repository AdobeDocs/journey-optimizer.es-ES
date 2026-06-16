---
solution: Journey Optimizer
product: Journey Optimizer
title: Establecimiento de reglas de límite de mensajes y recorridos
description: Establecimiento de reglas de límite de mensajes y recorridos
redpen-status: CREATED_||_2025-08-11_20-28-34
exl-id: 630e252a-aab2-4a27-ad46-d4dbfbc3f3a4
source-git-commit: 0a2c384faea70dcbc9b99596740e375d85b2bc64
workflow-type: ht
source-wordcount: '292'
ht-degree: 100%

---

# Establecimiento de reglas de límite de mensajes y recorridos{#section-overview}

Las reglas de límite forman parte de la [administración y priorización de conflictos](../using/conflict-prioritization/gs-conflict-prioritization.md): ayudan a garantizar que los clientes reciban la cantidad adecuada de comunicación sin sentirse abrumados. Antes de aplicar las reglas, use la [herramienta de detección de conflictos](../using/conflict-prioritization/conflicts.md) para identificar recorridos y campañas que se superponen. Cuando varias comunicaciones cumplen los requisitos para el mismo perfil, [las puntuaciones de prioridad](../using/conflict-prioritization/priority-scores.md) determinan qué mensaje se envía primero.

Puede establecer límites en cuanto a la frecuencia con la que se envían los mensajes (restricción de frecuencia), en cuanto a la cantidad de recorridos que puede introducir un perfil (restricción de recorrido) y en qué momento se bloquean los mensajes (horas de inactividad). Las reglas se agrupan en **conjuntos de reglas** y se aplican a campañas o recorridos. Para el control mediante programación desde sistemas externos, consulte [API de límite](../using/configuration/capping.md).

## Establecer reglas de límite de mensajes y recorridos

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

Trabajar con conjuntos de reglas

Obtenga información sobre cómo crear, administrar y activar conjuntos de reglas para controlar la frecuencia de los mensajes y las reglas de entrada de recorrido en Adobe Journey Optimizer.

[Explorar conjuntos de reglas](../using/conflict-prioritization/rule-sets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Límite y arbitraje del recorrido

Descubra cómo establecer límites de entrada y simultaneidad de recorridos, priorizar los recorridos y monitorizar exclusiones para evitar una sobrecarga en la comunicación.

[Información sobre el límite de recorrido](../using/conflict-prioritization/journey-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Restricción de frecuencia por canal

Obtenga información sobre cómo crear y aplicar reglas de restricción de frecuencia específicas del canal para optimizar el envío de mensajes y evitar una sobrecarga en la comunicación.

[Establecer restricción de frecuencia](../using/conflict-prioritization/channel-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

Establecer horas de inactividad

Defina exclusiones basadas en el tiempo para Correo electrónico, SMS, Notificaciones push y WhatsApp para que no se envíen mensajes durante períodos específicos, respetando las preferencias y el cumplimiento de los clientes.

[Establecer horas de inactividad](../using/conflict-prioritization/quiet-hours.md)
:::

::::

## Recursos adicionales

- **[Introducción a la administración de conflictos y priorización](../using/conflict-prioritization/gs-conflict-prioritization.md)**: información general sobre la detección de conflictos, las puntuaciones de prioridad y los conjuntos de reglas.
- **[Identificar posibles conflictos](../using/conflict-prioritization/conflicts.md)**: detecte recorridos y campañas superpuestos antes de aplicar reglas de límite.
- **[Asignar puntuaciones de prioridad](../using/conflict-prioritization/priority-scores.md)**: controle qué recorrido o campaña tiene prioridad cuando un perfil cumple los requisitos para varias comunicaciones.
