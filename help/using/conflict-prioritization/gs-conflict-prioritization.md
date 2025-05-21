---
title: Administración y priorización de conflictos
description: Aproveche las herramientas de conflictos y priorización de Journey Optimizer.
role: User
level: Beginner
badge: label="Disponibilidad limitada"
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: f55f985375cf360ce55074cb227b6c424db05b5c
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 94%

---

# Administración y priorización de conflictos {#conflict-prioritization}

>[!AVAILABILITY]
>
>Las funciones de conflictos y priorización están disponibles en Disponibilidad limitada para un grupo selecto de clientes. Tenga en cuenta que estas funciones se implementarán gradualmente para más usuarios en el futuro. Póngase en contacto con el equipo de la cuenta si está interesado en que se le añada a la lista de espera de estas funciones.

En Journey Optimizer, la administración del volumen y la sincronización de las campañas y los recorridos tiene vital importancia, ya que reducen las interacciones para los clientes. Journey Optimizer ahora ofrece varias herramientas para la administración y priorización de conflictos.

Estas herramientas están disponibles para campañas y recorridos unitarios, de calificación de audiencias y de lectura de audiencias.

Al aprovechar estas herramientas, puede garantizar esfuerzos de marketing más fluidos y orientados, enviando el mensaje correcto en el momento adecuado y evitando conflictos y sobrecargas.

## Herramientas de administración y priorización de conflictos {#tools}

Con la **herramienta de detección de conflictos**, puede identificar posibles solapamientos en recorridos y campañas. Es crucial, ya que demasiadas comunicaciones simultáneas pueden provocar fatiga en los clientes. Journey Optimizer permite monitorizar elementos como cronologías, solapamiento de público y configuraciones de canal. Al identificar los conflictos con anticipación, puede perfeccionar sus campañas para evitar bombardear a los clientes con varios mensajes al mismo tiempo. [Aprenda a detectar posibles conflictos en recorridos y campañas](conflicts.md)

Además, **las puntuaciones de prioridad** le ayudan a controlar qué campañas o recorridos tienen prioridad cuando un cliente cumple los requisitos para recibir varias comunicaciones. Esto resulta especialmente útil en los canales de entrada como web y móviles, donde solo se puede mostrar una campaña a la vez. Al asignar una puntuación de prioridad a cada recorrido o campaña, puede asegurarse de que el mensaje más importante se envíe primero. [Aprenda a asignar puntuaciones de prioridad a recorridos y campañas](priority-scores.md)

**Límite y arbitraje de recorridos** le permite limitar la frecuencia y la cantidad de recorridos en los que un cliente puede entrar en un lapso de tiempo determinado. Puede configurar reglas para limitar el número de entradas de recorrido de un perfil o el número de recorridos en los que un cliente se puede inscribir al mismo tiempo. Además, puede usar la configuración de arbitraje para decidir en qué recorrido debe entrar un cliente si cumple los requisitos para varios recorridos, usando puntuaciones de prioridad para determinar cuál es el más adecuado. [Aprenda a trabajar con la limitación y el arbitraje de recorridos](journey-capping.md)

Por último, también puede usar conjuntos de reglas para establecer **restricciones de frecuencia por tipo de comunicación** (por ejemplo, ventas, promociones), a fin de evitar sobrecargar a los clientes con mensajes similares. Puede controlar la frecuencia en varios canales, excluyendo automáticamente los perfiles con exceso de solicitudes para garantizar una mejor experiencia del cliente. [Descubra cómo trabajar con conjuntos de reglas](../configuration/rule-sets.md)</li></ul>

Al aprovechar estas funciones, puede garantizar esfuerzos de marketing más fluidos y orientados, enviando el mensaje correcto en el momento adecuado y evitando conflictos y sobrecargas.

## Mecanismos de protección y limitaciones

**Restricción de frecuencia y públicos por lotes**

Para la restricción de frecuencia, tanto de canal como de recorrido, si el público utilizado es un público por lotes, el valor del contador de perfiles al que se hace referencia en el momento de la entrada en la recorrido o el tiempo de ejecución del mensaje para una comunicación de canal procederá de la instantánea diaria tomada.

Esto puede suponer un problema, ya que los clientes pueden superar la restricción de frecuencia si han entrado en otro recorrido o si han recibido otra comunicación entre la hora de la instantánea diaria y la hora de entrada del recorrido (o del mensaje que se está enviando).

**Restriccón de frecuencia y públicos de streaming**

Para los públicos de streaming, el sistema puede tardar hasta dos horas en reconocer un valor de contador actualizado y, como tal, recomendamos espaciar las comunicaciones y los recorridos al menos dos horas entre sí si es posible para mitigar este riesgo.

**Hora de inicio de los recorridos**

Para garantizar que las funciones de administración y priorización de conflictos funcionen correctamente, se recomienda configurar la hora de inicio de su recorrido al menos 10 minutos en el futuro, para permitir que el sistema actualice el contador en consecuencia.

Si los clientes ya han alcanzado su límite al entrar en un recorrido, aún no se les permitirá entrar, pero si no han alcanzado su límite, el contador de entradas no se incrementará.

**Arbitraje de recorridos**

Por ahora, solo se admiten los recorridos de público de lectura para el arbitraje de recorridos. La configuración del arbitraje no se puede aprovechar para recorridos de calificación unitarios o de público.
