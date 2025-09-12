---
solution: Journey Optimizer
product: journey optimizer
title: Experimentation Accelerator
description: Uso de datos en IA con Experimentation Accelerator
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: contenido, experimento, múltiple, audiencia, tratamiento
hide: true
hidefromtoc: true
source-git-commit: 50dcdd30e21fe1b12d502a2b9c478f4ceb546c49
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Uso de datos en IA con Experimentation Accelerator{#experiment-accelerator-security}

>[!BEGINSHADEBOX]

* [Introducción a Experimentation Accelerator](experiment-accelerator.md)
* [Uso de datos en IA con Experimentation Accelerator](experiment-accelerator-security.md)
* [Prácticas recomendadas de Experimentation Accelerator](experiment-accelerator-best-practices.md)
* [Monitorización de experimentos](experiment-accelerator-monitor.md)
* [Métricas de experimentación](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

**Adobe Journey Optimizer Experimentation Accelerator** le permite descubrir automáticamente información y recomendar oportunidades para mejorar sus experimentos y programas de experimentación. La solución aprovecha la IA y el aprendizaje automático para ofrecer estas recomendaciones. Esta instrucción aclara cómo se usan los datos de los clientes en **Experimentation Accelerator**.

## ¿Qué datos utiliza el acelerador de experimentación?

Actualmente hay tres tipos de datos usados por **acelerador de experimentación**:

* **Metadatos del experimento**: nombre del experimento, definición de la audiencia utilizada en el experimento y tratamientos en el experimento, por ejemplo: nombre, porcentajes de división, ubicación o superficie en la que se proporcionó el experimento.

* **Rendimiento de los tratamientos**: número de personas, media de la métrica de éxito y desviación estándar de cada tratamiento.

* **Contenido del tratamiento**: el HTML procesado y la captura de pantalla del tratamiento tal como lo vería un usuario en su sitio web.

## ¿Qué hace el acelerador de experimentación con estos datos?

**El acelerador de experimentación** toma el contenido de cada tratamiento y crea una incrustación, es decir, una representación matemática del contenido, y luego correlaciona esas incrustaciones con el rendimiento de los tratamientos. Este proceso permite extraer los atributos de contenido que tienen el mejor rendimiento para un uso futuro. Estos atributos se incorporan a un modelo de lenguaje grande alojado en Adobe, que los convierte en declaraciones legibles por humanos utilizadas para generar perspectivas y sugerir oportunidades.

## ¿Qué restricciones tiene Experimentation Accelerator sobre los datos utilizados?

Cada cliente se asigna a una organización y zona protegida específicas. Se entrena un modelo dedicado para cada zona protegida. Al eliminar una zona protegida, todos los datos, señales y modelos relacionados se eliminan de forma permanente.

* Solo utilizamos los datos del cliente para entrenar o ajustar el modelo de ese cliente.

* Nunca mezclamos clientes para entrenar o afinar un modelo.

## ¿Cambiarán los modelos de Adobe o la IA la experiencia de usuario de una marca automáticamente?

No. **Experimentation Accelerator** solo hace recomendaciones sobre qué se puede cambiar y cómo se puede cambiar. Solo los usuarios que tengan permisos para cambiar la experiencia con Journey Optimizer o Target podrán seguir estas recomendaciones. Todas las recomendaciones se pueden revisar y editar antes de ser eliminadas.

## ¿Existe algún riesgo para la estabilidad de sus datos o del sistema?

**Experimentation Accelerator** solo ingiere y analiza datos, produciendo información y recomendaciones para futuras pruebas. No tiene acceso para modificar ninguna configuración de prueba. Todas las sugerencias generadas dentro de la herramienta se envían a Target y Journey Optimizer para su implementación, lo que garantiza que no afecten a las actividades actuales de los clientes.
