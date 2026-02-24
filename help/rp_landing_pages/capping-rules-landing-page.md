---
solution: Journey Optimizer
product: Journey Optimizer
title: Establecimiento de reglas de límite de mensajes y recorridos
description: Establecimiento de reglas de límite de mensajes y recorridos
redpen-status: CREATED_||_2025-08-11_20-28-34
exl-id: 630e252a-aab2-4a27-ad46-d4dbfbc3f3a4
source-git-commit: 9e23162373564e7866af115ee2cd706527336e4a
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 38%

---

# Establecimiento de reglas de límite de mensajes y recorridos{#section-overview}

Las reglas de límite son parte de la [administración y priorización de conflictos](../using/conflict-prioritization/gs-conflict-prioritization.md), y ayudan a garantizar que los clientes reciban la cantidad correcta de comunicación sin sentirse abrumados. Antes de aplicar las reglas, use la [herramienta de detección de conflictos](../using/conflict-prioritization/conflicts.md) para identificar recorridos y campañas que se superponen. Cuando varias comunicaciones cumplen los requisitos para el mismo perfil, [las puntuaciones de prioridad](../using/conflict-prioritization/priority-scores.md) determinan qué mensaje se envía primero.

Puede establecer límites en la frecuencia con la que se envían los mensajes (restricción de recorrido), la cantidad de recorridos que puede introducir un perfil (restricción de frecuencia) y el momento en el que se bloquean los mensajes (horas de silencio). Las reglas se agrupan en **conjuntos de reglas** y se aplican a campañas o recorridos. Para el control mediante programación desde sistemas externos, consulte [API de límite](../using/configuration/capping.md).

## Establecer reglas de límite de mensajes y recorridos

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=es)

Trabajar con conjuntos de reglas

Obtenga información sobre cómo crear, administrar y activar conjuntos de reglas para controlar la frecuencia de los mensajes y las reglas de entrada de recorrido en Adobe Journey Optimizer.

[Explorar conjuntos de reglas](../using/conflict-prioritization/rule-sets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=es)

Límite y arbitraje del recorrido

Descubra cómo establecer límites de entrada y simultaneidad de recorridos, priorizar los recorridos y monitorizar exclusiones para evitar una sobrecarga en la comunicación.

[Información sobre el límite de recorrido](../using/conflict-prioritization/journey-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=es)

Restricción de frecuencia por canal

Obtenga información sobre cómo crear y aplicar reglas de restricción de frecuencia específicas del canal para optimizar el envío de mensajes y evitar una sobrecarga en la comunicación.

[Establecer restricción de frecuencia](../using/conflict-prioritization/channel-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=es)

Establecer horas tranquilas

Defina exclusiones basadas en el tiempo para Correo electrónico, SMS, Push y WhatsApp de modo que no se envíen mensajes durante períodos específicos, respetando las preferencias y el cumplimiento de los clientes.

[Establecimiento de horas tranquilas](../using/conflict-prioritization/quiet-hours.md)
:::

::::

## Recursos adicionales

- **[Introducción a la administración y priorización de conflictos](../using/conflict-prioritization/gs-conflict-prioritization.md)**: Información general sobre la detección de conflictos, las puntuaciones de prioridad y los conjuntos de reglas.
- **[Identificar posibles conflictos](../using/conflict-prioritization/conflicts.md)**: detecte recorridos y campañas superpuestos antes de aplicar reglas de límite.
- **[Asignar puntuaciones de prioridad](../using/conflict-prioritization/priority-scores.md)**: controla qué recorrido o campaña tiene prioridad cuando un perfil cumple los requisitos para varias comunicaciones.
