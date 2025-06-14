---
title: Administración y priorización de conflictos
description: Aproveche las herramientas de conflictos y priorización de Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: 9d84a319497e833aa77416479dd019bab59aab55
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 28%

---

# Administración de conflictos y priorización {#conflict-prioritization}

## Herramientas de administración y priorización de conflictos {#tools}

En Journey Optimizer, administrar el volumen y la cronología de las campañas y los recorridos es esencial para evitar abrumar a los clientes con demasiadas interacciones. Journey Optimizer ahora ofrece varias herramientas para la administración y priorización de conflictos.

Estas herramientas están disponibles en campañas y recorridos unitarios, de calificación de público y de público de lectura.

Aprovechando estas herramientas, puede garantizar unos esfuerzos de marketing más fluidos y específicos, enviando el mensaje correcto en el momento adecuado y evitando conflictos y sobrecargas.

### Herramienta de detección de conflictos

Con la **herramienta de detección de conflictos**, puede identificar posibles solapamientos en recorridos y campañas. Es crucial, ya que demasiadas comunicaciones simultáneas pueden provocar fatiga en los clientes. Journey Optimizer permite monitorizar elementos como cronologías, solapamiento de público y configuraciones de canal. Al identificar los conflictos de forma temprana, puede refinar sus campañas para evitar bombardear a los clientes con varios mensajes al mismo tiempo.

➡️ [Aprenda a detectar posibles conflictos en recorridos y campañas](conflicts.md)

### Puntuaciones de prioridad

**Las puntuaciones de prioridad** le ayudan a controlar qué campañas o recorridos tienen prioridad cuando un cliente califica para varias comunicaciones. Esto resulta especialmente útil en los canales de entrada como web y móviles, donde solo se puede mostrar una campaña a la vez. Al asignar una puntuación de prioridad a cada recorrido o campaña, puede asegurarse de que el mensaje más importante se envíe primero.

➡️ [Aprenda a asignar puntuaciones de prioridad a recorridos y campañas](priority-scores.md)

### Conjuntos de reglas

Los conjuntos de reglas permiten **agrupar varias reglas en conjuntos de reglas** y aplicarlas a los recorridos y campañas que elija. Esto proporciona una granularidad mejorada para limitar la frecuencia y la cantidad de recorridos que un cliente puede introducir en un lapso de tiempo determinado o controlar la frecuencia con la que los usuarios recibirán un mensaje según el tipo de comunicación.

* **límite y arbitraje de Recorridos**

  Los conjuntos de reglas permiten limitar la frecuencia y la cantidad de recorridos que un cliente puede introducir en un lapso de tiempo determinado. También puede configurar reglas para limitar el número de entradas de recorridos de un perfil o el número de recorridos en los que se puede inscribir un cliente al mismo tiempo.

  Además, puede usar la configuración de arbitraje para decidir qué recorrido debe ingresar un cliente si cumple los requisitos para varios recorridos, usando puntuaciones de prioridad para determinar el mejor ajuste.

  ➡️ [Aprenda a trabajar con la restricción y el arbitraje de recorridos](journey-capping.md)

* **Límite de frecuencia por canal y tipo de comunicación**

  También puede utilizar conjuntos de reglas para establecer límites de frecuencia por tipo de comunicación (por ejemplo, Ventas, Promocional) para evitar sobrecargar a los clientes con mensajes similares. Puede controlar la frecuencia en varios canales, excluyendo automáticamente los perfiles saturados para garantizar una mejor experiencia del cliente.

  ➡️ [Aprenda a establecer límites de frecuencia por canal y tipo de comunicación](../conflict-prioritization/channel-capping.md)

## Mecanismos de protección y limitaciones

* **Campañas y puntuaciones de prioridad**: en las campañas, la puntuación de prioridad solo está disponible para los canales entrantes **web**, **en la aplicación** y **basado en código**.

* **Latencia de actualización del contador de perfiles**

  El valor del contador de perfiles puede tardar hasta 20 minutos en actualizarse después de que un cliente haya introducido un recorrido.

  Si un perfil introduce dos recorridos en un breve intervalo, es posible que el segundo recorrido no reconozca correctamente que ya se ha alcanzado el límite de frecuencia, lo que podría permitir que el perfil introduzca ambos recorridos.

* **Prioridad de área de nombres para límite de entrada de recorrido**

  El límite de entrada solo se admite si el área de nombres seleccionada en el recorrido es la área de nombres de mayor prioridad definida en la zona protegida. Si la prioridad del área de nombres no se ha configurado explícitamente, la prioridad más alta predeterminada es el correo electrónico.

* **Activaciones simultáneas en recorridos de calificación de audiencia**

  Cuando el mismo evento de calificación de audiencia activa varios recorridos de cualificación de audiencia, los recuentos de límite de entrada no son precisos. Si los recuentos están por debajo del límite, recorrido seguirá arbitrando, pero no podrá obtener los recuentos más actualizados con activaciones simultáneas.
