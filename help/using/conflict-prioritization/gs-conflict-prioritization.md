---
title: Administración de conflictos y priorización
description: Aprenda a aprovechar las herramientas de conflictos y priorización de Journey Optimizer.
role: User
level: Beginner
badge: label="Disponibilidad limitada"
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: dbe312f332031391c49a973f323994f860e354e3
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 10%

---

# Administración de conflictos y priorización {#conflict-prioritization}

>[!AVAILABILITY]
>
>Actualmente, las funciones de conflicto y priorización están disponibles en Disponibilidad limitada para un grupo selecto de clientes. Tenga en cuenta que estas funciones se implementarán gradualmente para más usuarios en el futuro. Póngase en contacto con el equipo de la cuenta si está interesado en que se le añada a la lista de espera de estas funciones.

En Journey Optimizer, administrar el volumen y la cronología de las campañas y los recorridos es esencial para evitar abrumar a los clientes con demasiadas interacciones. Journey Optimizer ofrece varias herramientas para la administración de conflictos y la priorización.

## Herramientas de administración de conflictos y priorización {#tools}

Con la **herramienta de detección de conflictos**, puede identificar posibles superposiciones en recorridos y campañas. Esto es crucial, ya que demasiadas comunicaciones simultáneas pueden provocar fatiga en los clientes. Journey Optimizer permite monitorizar elementos como líneas de tiempo, superposición de audiencias y configuraciones de canal. Al identificar los conflictos de forma temprana, puede refinar sus campañas para evitar bombardear a los clientes con varios mensajes al mismo tiempo. [Aprenda a detectar posibles conflictos en recorridos y campañas](conflicts.md)

Además, **las puntuaciones de prioridad** le ayudan a controlar qué campañas o recorridos tienen prioridad cuando un cliente califica para varias comunicaciones. Esto resulta especialmente útil en canales entrantes como web y móvil, donde solo se puede mostrar una campaña a la vez. Al asignar una puntuación de prioridad a cada recorrido o campaña, puede asegurarse de que el mensaje más importante se envíe primero. [Aprenda a asignar puntuaciones de prioridad a recorridos y campañas](priority-scores.md)

**límite y arbitraje de Recorridos** le permite limitar la frecuencia y la cantidad de recorridos que un cliente puede ingresar en un lapso de tiempo determinado. Puede configurar reglas para limitar el número de entradas de recorrido de un perfil o el número de recorridos en los que se puede inscribir un cliente al mismo tiempo. Además, puede usar la configuración de arbitraje para decidir qué recorrido debe ingresar un cliente si cumple los requisitos para varios recorridos, usando puntuaciones de prioridad para determinar el mejor ajuste. [Aprenda a trabajar con la restricción y el arbitraje de recorridos](journey-capping.md)

Por último, también puede usar conjuntos de reglas para establecer un límite de **frecuencia por tipo de comunicación** (por ejemplo, Ventas, Promocional) a fin de evitar sobrecargar a los clientes con mensajes similares. Puede controlar la frecuencia en varios canales, excluyendo automáticamente los perfiles saturados para garantizar una mejor experiencia del cliente. [Aprenda a trabajar con conjuntos de reglas](../configuration/rule-sets.md)</li></ul>

Al aprovechar estas funciones, puede garantizar esfuerzos de marketing más fluidos y orientados, enviando el mensaje correcto en el momento adecuado y evitando conflictos y sobrecargas.

## Mecanismos de protección y limitaciones

**Límite de frecuencia y audiencias por lotes**

Para la restricción de frecuencia, tanto de canal como de recorrido, si la audiencia utilizada es una audiencia por lotes, el valor del contador de perfiles al que se hace referencia en el momento de la entrada en la recorrido o el tiempo de ejecución del mensaje para una comunicación de canal procederá de la instantánea diaria tomada.

Esto puede suponer un problema, ya que los clientes pueden superar el límite de frecuencia si han entrado en otro recorrido o si han recibido otra comunicación entre la hora de la instantánea diaria y la hora de entrada del recorrido (o del mensaje que se está enviando).

**Límite de frecuencia y audiencias de streaming**

Para las audiencias de streaming, el sistema puede tardar hasta dos horas en reconocer un valor de contador actualizado y, como tal, recomendamos espaciar las comunicaciones y los recorridos al menos dos horas entre sí si es posible para mitigar este riesgo.

**hora de inicio de Recorridos**

Para garantizar que las funciones de priorización y administración de conflictos funcionen correctamente, se recomienda configurar la hora de inicio de su recorrido al menos 10 minutos en el futuro, para permitir que el sistema actualice el contador en consecuencia.

Si los clientes ya han alcanzado su límite al introducir un recorrido, aún no se les permitirá entrar, pero si no han alcanzado su límite, el contador de entradas no se incrementará.

**arbitraje de Recorrido**

Por ahora, solo se admiten recorridos de lectura-audiencia para la mediación de recorrido. La configuración de mediación no se puede aprovechar para recorridos de cualificación unitarios o de audiencia.
