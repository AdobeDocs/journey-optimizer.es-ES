---
title: Administración de conflictos y priorización
description: Aproveche las herramientas de conflictos y priorización de Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: 8146221975b7460bf1deaca9363d1624b719b480
workflow-type: ht
source-wordcount: '629'
ht-degree: 100%

---

# Administración de conflictos y priorización {#conflict-prioritization}

## Herramientas de administración y priorización de conflictos {#tools}

En Journey Optimizer, administrar el volumen y la cronología de las campañas y los recorridos es esencial para evitar abrumar a los clientes con demasiadas interacciones. Journey Optimizer ahora ofrece varias herramientas para la administración y priorización de conflictos.

Estas herramientas están disponibles en campañas y recorridos unitarios, de calificación de público y de público de lectura.

Aprovechando estas herramientas, puede garantizar unos esfuerzos de marketing más fluidos y específicos, enviando el mensaje correcto en el momento adecuado y evitando conflictos y sobrecargas.

### Herramienta de detección de conflictos

Con la **herramienta de detección de conflictos**, puede identificar posibles solapamientos en recorridos y campañas. Es crucial, ya que demasiadas comunicaciones simultáneas pueden provocar fatiga en los clientes. Journey Optimizer permite monitorizar elementos como cronologías, solapamiento de público y configuraciones de canal. Al identificar los conflictos con anticipación, puede perfeccionar sus campañas para evitar bombardear a los clientes con múltiples mensajes al mismo tiempo.

➡️ [Aprenda a detectar posibles conflictos en recorridos y campañas](conflicts.md)

### Puntuaciones de prioridad

Las **Puntuaciones de prioridad** le ayudan a controlar qué campañas o recorridos tienen prioridad cuando un cliente cumple los requisitos para recibir varias comunicaciones. Esto resulta especialmente útil en los canales de entrada como web y móviles, donde solo se puede mostrar una campaña a la vez. Al asignar una puntuación de prioridad a cada recorrido o campaña, puede asegurarse de que el mensaje más importante se envíe primero.

➡️ [Aprenda a asignar puntuaciones de prioridad a recorridos y campañas](priority-scores.md)

### Conjuntos de reglas

Los conjuntos de reglas permiten **agrupar varias reglas en conjuntos de reglas** y aplicarlas a los recorridos y campañas que elija. Esto proporciona una mayor granularidad para limitar la frecuencia y la cantidad de recorridos en los que un cliente puede entrar en un lapso de tiempo determinado o controlar la frecuencia con la que los usuarios recibirán un mensaje según el tipo de comunicación. [Descubra cómo trabajar con conjuntos de reglas](../conflict-prioritization/rule-sets.md)

* **Límite y arbitraje del recorrido**

  Los conjuntos de reglas le permiten limitar la frecuencia y la cantidad de recorridos en los que un cliente puede entrar en un lapso de tiempo determinado. Puede configurar reglas para limitar el número de entradas de recorrido de un perfil o el número de recorridos en los que un cliente se puede inscribir al mismo tiempo.

  Además, puede usar la configuración de arbitraje para decidir en qué recorrido debe entrar un cliente si cumple los requisitos para varios recorridos, usando puntuaciones de prioridad para determinar cuál es el más adecuado.

  ➡️ [Aprenda a trabajar con el límite y arbitraje del recorrido](journey-capping.md)

* **Restricción de frecuencia por canal y tipo de comunicación**

  También puede utilizar los conjuntos de reglas para establecer restricciones de frecuencia por tipo de comunicación (por ejemplo, ventas, promociones), a fin de evitar sobrecargar a los clientes con mensajes similares. Puede controlar la frecuencia en varios canales, excluyendo automáticamente los perfiles saturados para garantizar una mejor experiencia del cliente.

  ➡️ [Aprenda a establecer restricciones de frecuencia por tipo de canal y comunicación](../conflict-prioritization/channel-capping.md)

## Mecanismos de protección y limitaciones

* **Campañas y puntuaciones de prioridad**: en las campañas, la puntuación de prioridad solo está disponible en los canales de entrada **web**, **en la aplicación** y **basados en código**.

* **Latencia de actualización del contador de perfiles**

  El valor del contador de perfiles puede tardar hasta 10 minutos en actualizarse después de que un cliente haya entrado en un recorrido.

  Si un perfil inicia dos recorridos en un breve intervalo de tiempo, es posible que el segundo recorrido no reconozca correctamente que ya se ha alcanzado la restricción de frecuencia, lo que podría permitir que el perfil iniciara ambos recorridos.

* **Prioridad del espacio de nombres para el límite de entradas a recorridos**

  El límite de entradas solo se admite si el espacio de nombres seleccionado en el recorrido es el espacio de nombres de mayor prioridad definido en la zona protegida. Si la prioridad del espacio de nombres no se ha configurado explícitamente, la prioridad más alta predeterminada es el correo electrónico.

* **Activaciones simultáneas en recorridos de calificación de público**

  Cuando el mismo evento de calificación de público activa varios recorridos de calificación de público, los recuentos de límite de entradas no son precisos. Si los recuentos están por debajo del límite, el recorrido seguirá arbitrando, pero no podrá obtener los recuentos más actualizados con activaciones simultáneas.
