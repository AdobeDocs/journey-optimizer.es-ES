---
title: Administración y priorización de conflictos
description: Aproveche las herramientas de conflictos y priorización de Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
TQID: https://experienceleague.adobe.com/vx-CmsYwj7QyN2sVMrpJ9VUNDgnXq8qt1nT9lHOFV3s
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fd59660e-de8a-4bfb-85dc-7fa546030c49
subfeature_v2:
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: f3fe4813-f254-4f8f-99cc-24bd67f119e1
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
source-git-commit: 49542ca70e8899061bc79772cf96069ab2587ab2
workflow-type: ht
source-wordcount: 896
ht-degree: 100%

---

# Administración y priorización de conflictos {#conflict-prioritization}

>[!BEGINSHADEBOX]

**En esta página:** descubra cómo la detección de conflictos, las puntuaciones de prioridad y los conjuntos de reglas funcionan juntos para que pueda evitar comunicaciones superpuestas y controlar la frecuencia con la que se envían mensajes a los clientes.

>[!ENDSHADEBOX]

En Journey Optimizer, administrar el volumen y la cronología de las campañas y los recorridos es esencial para evitar abrumar a los clientes con demasiadas interacciones. Las herramientas de administración de conflictos y la priorización le ayudan a ofrecer comunicaciones reflexivas y oportunas, ya que evitan la fatiga de los clientes y garantizan que los mensajes correctos lleguen a su público. Mediante la detección de conflictos, las puntuaciones de las prioridades y los conjuntos de reglas, puede optimizar las campañas y los recorridos para evitar solapamientos y equilibrar la frecuencia entre canales.

Estas herramientas están disponibles en campañas y recorridos unitarios, de calificación de público y de público de lectura. Tanto si establece límites en la frecuencia con la que se envían mensajes como si decide qué campañas tienen prioridad, estas funciones trabajan conjuntamente para simplificar la toma de decisiones y optimizar su estrategia de marketing.

## Por dónde empezar {#where-to-start}

| Su objetivo | Herramienta | Acción |
|-----------|------|--------|
| Ver si los recorridos o las campañas se superponen (cronología, público, canal) | **Detección de conflictos** | [Identificación de posibles conflictos](conflicts.md) |
| Decida qué mensaje gana cuando un perfil cumple los requisitos para varios | **Puntuaciones de prioridad** | [Asignar puntuaciones de prioridad](priority-scores.md) |
| Limitar la frecuencia o la cantidad de mensajes que recibe un perfil | **Conjuntos de reglas** (restricción de frecuencia, límite de recorrido, horas de inactividad) | [Establecer reglas de límite de mensajes y recorridos](../../rp_landing_pages/capping-rules-landing-page.md) |

**Flujo típico:** utilice la detección de conflictos para detectar superposiciones y, a continuación, aplique puntuaciones de prioridad y conjuntos de reglas para controlar qué mensajes se envían y con qué frecuencia.

## Herramientas de administración de conflictos y priorización {#tools}

### Herramienta de detección de conflictos

Con la **herramienta de detección de conflictos**, puede identificar posibles solapamientos en recorridos y campañas. Es crucial, ya que demasiadas comunicaciones simultáneas pueden provocar fatiga en los clientes. Journey Optimizer permite monitorizar elementos como cronologías, solapamiento de público y configuraciones de canal. Al identificar los conflictos con anticipación, puede perfeccionar sus campañas para evitar bombardear a los clientes con múltiples mensajes al mismo tiempo.

[Aprenda a detectar posibles conflictos en recorridos y campañas](conflicts.md)

### Puntuaciones de prioridad

Las **Puntuaciones de prioridad** le ayudan a controlar qué campañas o recorridos tienen prioridad cuando un cliente cumple los requisitos para recibir varias comunicaciones. Esto resulta especialmente útil en los canales de entrada como web y móviles, donde solo se puede mostrar una campaña a la vez. Al asignar una puntuación de prioridad a cada recorrido o campaña, puede asegurarse de que el mensaje más importante se envíe primero.

[Aprenda a asignar puntuaciones de prioridad a recorridos y campañas](priority-scores.md)

### Conjuntos de reglas

Los conjuntos de reglas permiten **agrupar varias reglas en múltiples reglas** y aplicarlas a los recorridos y campañas que elija. Esto proporciona una mayor granularidad para limitar la frecuencia y la cantidad de recorridos en los que un cliente puede entrar en un lapso de tiempo determinado, o controlar la frecuencia con la que los usuarios reciben mensajes según el tipo de comunicación.

* **Límites de recorrido y arbitraje**: limite la frecuencia y la cantidad de recorridos en los que un cliente puede entrar en un lapso de tiempo determinado. Puede establecer un límite máximo en el número de entradas de recorrido para un perfil o limitar el número de recorridos en los que un cliente puede participar al mismo tiempo. Utilice la configuración de arbitraje para decidir en qué recorrido debe entrar un cliente si cumple los requisitos para varios recorridos, usando puntuaciones de prioridad para determinar cuál es el más adecuado. [Aprenda a trabajar con el límite y arbitraje del recorrido](journey-capping.md)

* **Restricción de frecuencia por canal y tipo de comunicación**: establezca restricciones de frecuencia por tipo de comunicación (por ejemplo, Ventas, Promocional) para evitar sobrecargar a los clientes con mensajes similares. Controle la frecuencia en varios canales, excluyendo automáticamente los perfiles saturados. [Aprenda a establecer restricciones de frecuencia por canal y tipo de comunicación](channel-capping.md)

* **Horas tranquilas**: defina exclusiones basadas en el tiempo para que no se envíen mensajes durante períodos específicos (correo electrónico, SMS, push, WhatsApp). [Aprenda a establecer horas de inactividad](quiet-hours.md)

[Descubra cómo trabajar con conjuntos de reglas](rule-sets.md)

## Mecanismos de protección y limitaciones {#guardrails}

* **Campañas y puntuaciones de prioridad**: en las campañas, la puntuación de prioridad solo está disponible en los canales de entrada **web**, **en la aplicación** y **basados en código**.

* **Latencia de actualización del contador de perfiles:** el valor del contador de perfiles puede tardar hasta 10 minutos en actualizarse después de que un cliente haya entrado en un recorrido. Si un perfil inicia dos recorridos en un breve intervalo de tiempo, es posible que el segundo recorrido no reconozca correctamente que ya se ha alcanzado la restricción de frecuencia, lo que podría permitir que el perfil iniciara ambos recorridos.

* **Prioridad del espacio de nombres para la limitación de entradas de recorrido:** el límite de entradas solo se admite si el espacio de nombres seleccionado en el recorrido es el espacio de nombres de mayor prioridad definido en la zona protegida. Si la prioridad del espacio de nombres no se ha configurado explícitamente, la prioridad más alta predeterminada es el correo electrónico.

* **Activaciones simultáneas en los recorridos de calificación de público:** cuando el mismo evento de calificación de público activa varios recorridos de calificación de público, los recuentos de límite de entradas no son precisos. Si los recuentos están por debajo del límite, el recorrido seguirá arbitrando, pero no podrá obtener los recuentos más actualizados con activaciones simultáneas.

## Recursos adicionales

* **[Identificación de conflictos potenciales:](conflicts.md)** aprenda a identificar y resolver conflictos entre campañas y recorridos superpuestos.
* **[Asignación de puntuaciones de prioridad](priority-scores.md)**: obtenga información sobre cómo asignar y utilizar puntuaciones de prioridad para controlar la prioridad de envío de mensajes.
* **[Trabajar con conjuntos de reglas](rule-sets.md)**: aprenda a crear y aplicar conjuntos de reglas para la administración avanzada de conflictos y el control de mensajes.
* **[Límite y arbitraje de recorridos](journey-capping.md)**: configure las reglas de limitación y el arbitraje a nivel de recorrido.
* **[Restricción de frecuencia por canal](channel-capping.md)**: establezca límites de frecuencia a nivel de canal para evitar mensajes excesivos.
* **[Establecer horas tranquilas](quiet-hours.md)**: defina exclusiones basadas en el tiempo para el envío de mensajes.
* **[Tutoriales de administración de conflictos](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}**: tutoriales de vídeo paso a paso.
* **[Casos de uso de Journey Optimizer](../building-journeys/jo-use-cases.md)**: examine patrones prácticos, como la restricción de frecuencia y la lógica de supresión de recorrido.
