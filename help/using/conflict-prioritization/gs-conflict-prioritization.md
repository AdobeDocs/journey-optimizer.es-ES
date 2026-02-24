---
title: Administración de conflictos y priorización
description: Aproveche las herramientas de conflictos y priorización de Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: a0eda2e1d021af37eb54f3ffa5bac0ac6e8ef6ce
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 30%

---

# Administración de conflictos y priorización {#conflict-prioritization}

En Journey Optimizer, administrar el volumen y la cronología de las campañas y los recorridos es esencial para evitar abrumar a los clientes con demasiadas interacciones. Las herramientas de gestión de conflictos y priorización le ayudan a proporcionar comunicaciones reflexivas y oportunas, lo que evita la fatiga de los clientes y garantiza que los mensajes correctos lleguen a su audiencia. Mediante la detección de conflictos, las puntuaciones de prioridad y los conjuntos de reglas, puede optimizar las campañas y los recorridos para evitar superposiciones y equilibrar la frecuencia entre canales.

Estas herramientas están disponibles para campañas y para recorridos de audiencia unitarios, de calificación de audiencias y de lectura. Tanto si establece límites en la frecuencia con la que se envían mensajes como si decide qué campañas tienen prioridad, estas funciones trabajan juntas para simplificar la toma de decisiones y optimizar su estrategia de marketing.

## Por dónde empezar {#where-to-start}

| Su objetivo | Herramienta | Acción |
|-----------|------|--------|
| Ver si los recorridos o las campañas se superponen (cronología, audiencia, canal) | **Detección de conflictos** | [Identificación de posibles conflictos](conflicts.md) |
| Decida qué mensaje gana cuando un perfil cumple los requisitos para varios | **Puntuaciones de prioridad** | [Asignar puntuaciones de prioridad](priority-scores.md) |
| Limitar la frecuencia o la cantidad de mensajes que recibe un perfil | **Conjuntos de reglas** (límite de frecuencia, límite de recorrido, horas de inactividad) | [Establecer reglas de límite de mensajes y recorridos](../../rp_landing_pages/capping-rules-landing-page.md) |

**Flujo típico:** Utilice la detección de conflictos para detectar superposiciones y, a continuación, aplique puntuaciones de prioridad y conjuntos de reglas para controlar qué mensajes se envían y con qué frecuencia.

## Herramientas de priorización y administración de conflictos {#tools}

### Herramienta de detección de conflictos

Con la **herramienta de detección de conflictos**, puede identificar posibles solapamientos en recorridos y campañas. Es crucial, ya que demasiadas comunicaciones simultáneas pueden provocar fatiga en los clientes. Journey Optimizer permite monitorizar elementos como cronologías, solapamiento de público y configuraciones de canal. Al identificar los conflictos con anticipación, puede perfeccionar sus campañas para evitar bombardear a los clientes con múltiples mensajes al mismo tiempo.

[Descubra cómo detectar posibles conflictos en recorridos y campañas](conflicts.md)

### Puntuaciones de prioridad

Las **Puntuaciones de prioridad** le ayudan a controlar qué campañas o recorridos tienen prioridad cuando un cliente cumple los requisitos para recibir varias comunicaciones. Esto resulta especialmente útil en los canales de entrada como web y móviles, donde solo se puede mostrar una campaña a la vez. Al asignar una puntuación de prioridad a cada recorrido o campaña, puede asegurarse de que el mensaje más importante se envíe primero.

[Aprenda a asignar puntuaciones de prioridad a recorridos y campañas](priority-scores.md)

### Conjuntos de reglas

Los conjuntos de reglas permiten **agrupar varias reglas** y aplicarlas a los recorridos y campañas que elija. Esto proporciona una granularidad mejorada para limitar la frecuencia y la cantidad de recorridos que un cliente puede introducir en un lapso de tiempo determinado, o para controlar la frecuencia con la que los usuarios reciben mensajes según el tipo de comunicación.

* **límite y arbitraje de Recorridos**: limita la frecuencia y la cantidad de recorridos que un cliente puede ingresar en un lapso de tiempo determinado. Puede limitar el número de entradas de recorridos de un perfil o el número de recorridos en los que se puede inscribir un cliente al mismo tiempo. Utilice la configuración de arbitraje para decidir qué recorrido debe introducir un cliente si cumple los requisitos para varios recorridos, utilizando puntuaciones de prioridad para determinar el mejor ajuste. [Aprenda a trabajar con la limitación y el arbitraje de recorridos](journey-capping.md)

* **Límite de frecuencia por canal y tipo de comunicación**: establezca un límite de frecuencia por tipo de comunicación (por ejemplo, Ventas, Promocional) para evitar sobrecargar a los clientes con mensajes similares. Controle la frecuencia en varios canales, excluyendo automáticamente los perfiles saturados. [Aprenda a establecer límites de frecuencia por canal y tipo de comunicación](channel-capping.md)

* **Horas tranquilas**: defina exclusiones basadas en el tiempo para que no se envíen mensajes durante períodos específicos (correo electrónico, SMS, push, WhatsApp). [Aprenda a establecer horas de inactividad](quiet-hours.md)

[Aprenda a trabajar con conjuntos de reglas](rule-sets.md)

## Protecciones y limitaciones {#guardrails}

* **Campañas y puntuaciones de prioridad**: en las campañas, la puntuación de prioridad solo está disponible en los canales de entrada **web**, **en la aplicación** y **basados en código**.

* **Latencia de actualización del contador de perfiles**: un cliente puede tardar hasta 10 minutos en actualizar el valor del recorrido de perfiles. Si un perfil inicia dos recorridos en un breve intervalo de tiempo, es posible que el segundo recorrido no reconozca correctamente que ya se ha alcanzado la restricción de frecuencia, lo que podría permitir que el perfil iniciara ambos recorridos.

* **Prioridad de área de nombres para el límite de entrada de recorrido**: el límite de entrada solo se admite si el área de nombres seleccionada en el recorrido es el área de nombres de prioridad más alta definida en la zona protegida. Si la prioridad del espacio de nombres no se ha configurado explícitamente, la prioridad más alta predeterminada es el correo electrónico.

* **Activaciones simultáneas en recorridos de calificación de audiencia**: cuando el mismo evento de calificación de audiencia activa varios recorridos de calificación de audiencia, los recuentos de límite de entrada no serán precisos. Si los recuentos están por debajo del límite, el recorrido seguirá arbitrando, pero no podrá obtener los recuentos más actualizados con activaciones simultáneas.

## Recursos adicionales

* **[Identificar posibles conflictos](conflicts.md)**: aprenda a detectar y resolver conflictos entre campañas y recorridos superpuestos.
* **[Asignar puntuaciones de prioridad](priority-scores.md)**: aprenda a asignar y utilizar puntuaciones de prioridad para controlar la prioridad de entrega de mensajes.
* **[Trabajar con conjuntos de reglas](rule-sets.md)**: aprenda a crear y aplicar conjuntos de reglas para la administración de conflictos y el control de mensajes.
* **[Límite y arbitraje de Recorrido](journey-capping.md)**: configure reglas de límite y arbitraje a nivel de recorrido.
* **[Límite de frecuencia por canal](channel-capping.md)**: establezca límites de frecuencia a nivel de canal para evitar mensajes excesivos.
* **[Establecer horas tranquilas](quiet-hours.md)** - Definir exclusiones basadas en el tiempo para la entrega de mensajes.
* **[Tutoriales de administración de conflictos](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}**: tutoriales de vídeo paso a paso.
