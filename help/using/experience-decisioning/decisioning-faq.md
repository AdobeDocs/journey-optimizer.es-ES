---
title: Preguntas más frecuentes sobre decisiones
description: Obtenga respuestas a preguntas comunes sobre las funcionalidades de Decisioning.
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: 59e85eb7a14f88d95b2ef97e3ace11a65f115b75
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 1%

---

# Preguntas más frecuentes sobre decisiones {#decisioning-faq}

Esta página proporciona respuestas a las preguntas frecuentes sobre las capacidades de toma de decisiones en Adobe Journey Optimizer.

## Reglas de límite {#capping-rules}

+++**¿Qué sucede cuando crea más de una regla de límite para una oferta? ¿Dejaremos de mostrar la oferta cuando coincidamos con alguna de las reglas de límite o con todas ellas?**

La oferta se limita tan pronto como **se cumple una condición**. Esto significa que cualquiera de las reglas de límite evitará que la oferta se muestre una vez alcanzado su umbral.

Por ejemplo, si tiene dos reglas de límite:
* 5 veces por perfil y por semana
* 100 veces el total entre todos los usuarios

La oferta dejará de mostrarse a un usuario una vez que la haya visto 5 veces en una semana, aunque aún no se haya alcanzado el límite total de 100. Del mismo modo, una vez que se alcanzan las 100 impresiones totales, la oferta deja de mostrarse a todos los usuarios.

Más información sobre [reglas de límite](items.md#capping).

+++

## Fórmulas de clasificación {#ranking-formulas}

+++**¿Por qué debería agregar una audiencia a un modelo de IA? ¿Cuál es la ventaja de añadir audiencias en lugar de un conjunto de datos completo? ¿Restringirá el modelo o expandirá el modelo?**

Al trabajar con modelos de IA (específicamente [modelos de optimización personalizados](ranking/personalized-optimization-model.md)):

* Se han agregado **conjuntos de datos** para recopilar sus eventos de conversión (clics, pedidos, ingresos). Estos son los resultados para los que el modelo intenta optimizar.
* Se agregaron **audiencias** para usarlas como variables predictoras en el modelo. Ayudan a personalizar las predicciones para intentar predecir clics, pedidos o ingresos para diferentes segmentos de clientes.

Tanto los conjuntos de datos como las audiencias son necesarios para que el modelo de optimización personalizado funcione correctamente. Las audiencias **no restringen ni amplían** el modelo; en su lugar, proporcionan contexto adicional que ayuda al modelo a tomar mejores decisiones personalizadas.

Más información sobre [modelos de IA](ranking/ai-models.md).

+++

+++**¿Agregar o quitar ofertas a una colección tendrá algún impacto en el modelo si utilizo modelos de optimización automática o personalizados?**

Ambos modelos proporcionarán tráfico a la siguiente mejor oferta disponible según los datos de tráfico de los últimos 30 días.

Si se eliminan varias ofertas al mismo tiempo y las ofertas restantes recibieron muy poco tráfico en los últimos 30 días, la distribución de la oferta puede comportarse de forma inesperada. Esto podría dar como resultado una distribución aleatoria o un sesgo hacia determinadas ofertas que tienen una tasa de conversión más alta basada en solo unas pocas impresiones.

**Práctica recomendada**: Cuando realice cambios significativos en las colecciones de ofertas, asegúrese de que las ofertas restantes tengan datos de rendimiento históricos suficientes para mantener el rendimiento óptimo del modelo.

+++

+++**¿Cuánto tiempo tardan los modelos de IA en comprender que se ha agregado contenido nuevo y empezar a agregarlo a la mezcla?**

Ambos modelos de IA identificarán las ofertas recién disponibles en la próxima ejecución de formación:

* **Optimización automática**: ejecuciones de formación diarias
* **Optimización personalizada**: ejecuciones de formación semanales

Una vez identificados, ambos modelos empezarán a ofrecer las nuevas ofertas a algunos visitantes inmediatamente para probar su rendimiento y recopilar datos sobre su eficacia.

Obtenga más información sobre [optimización automática](ranking/auto-optimization-model.md) y [modelos de optimización personalizada](ranking/personalized-optimization-model.md).

+++

+++**Si no tenemos grupos de control en los modelos de IA, ¿estamos aprendiendo y optimizando todo el tráfico al mismo tiempo?**

Sí. Ambos modelos de IA (optimización automática y optimización personalizada) utilizan un enfoque de &quot;explorar y explotar&quot;:

* Inicialmente, ambos modelos son de **100% exploración**, lo que significa que prueban distintas ofertas para recopilar datos de rendimiento.
* Con el tiempo, los modelos **administran automáticamente el equilibrio entre explorar y explotar** a medida que se recopilan eventos de comportamiento y mejoran las predicciones.
* Los modelos cambian gradualmente más tráfico a ofertas de mejor rendimiento, al tiempo que siguen explorando y probando otras opciones.

Esto garantiza un aprendizaje y una optimización continuos en todo el tráfico sin necesidad de grupos de control independientes.

+++

+++**¿Cuántos eventos de optimización necesitamos para ser estadísticamente significativos? ¿Hay un umbral mínimo de tráfico para una superficie?**

Para garantizar un rendimiento óptimo del modelo, Adobe recomienda los siguientes mínimos:

**Mínimos recomendados (por semana):**
* Al menos **1.000 impresiones** por oferta/elemento
* Al menos **100 eventos de conversión** por oferta/artículo

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

De forma predeterminada, el sistema no intentará crear modelos personalizados para ofertas o elementos con menos de 1000 impresiones o 50 eventos de conversión.

**Importante**: En la práctica, algunos clientes tienen muchas ofertas (~300) en un solo modelo, y algunas ofertas pueden tener reglas comerciales muy restrictivas. Los mínimos absolutos (250 impresiones / 25 conversiones por 30 días) representan el umbral más bajo que el sistema puede admitir para los modelos de construcción.

Más información sobre [requisitos de recopilación de datos](data-collection/data-collection.md).

+++

+++**¿Es necesario diferenciar claramente el contenido de las ofertas para que los modelos de IA funcionen bien? ¿Qué sucede si tengo varias ofertas demasiado similares entre sí?**

En términos generales, es más probable que el modelo de IA genere beneficios de la personalización cuando las **ofertas se adapten a diferentes tipos de clientes**.

Cuando las ofertas son muy similares, es probable que se produzca una de estas dos situaciones:

* **Rendimiento similar**: las ofertas funcionarán de manera idéntica y recibirán una parte relativamente uniforme del tráfico.
* **Dominio**: Las pequeñas diferencias pueden hacer que una oferta domine a las demás en todos los tipos de clientes y reciba la mayor parte del tráfico.

>[!NOTE]
>
>Las diferencias en las ofertas no garantizan que una oferta no domine a las demás. Por ejemplo, una oferta de descuento de 100 € casi siempre superará a una oferta de descuento de 50 € en todos los tipos de clientes, independientemente de la personalización.

**Práctica recomendada**: Asegúrese de que sus ofertas proporcionen una diferenciación significativa que pueda atraer a diferentes segmentos de clientes para obtener un rendimiento óptimo del modelo de IA.

+++

+++**¿Qué le sucede al modelo si hay una anomalía de tráfico, como un pico de tráfico enorme? ¿Causará problemas o elevará la rareza?**

Un pico de tráfico se incluiría en el modelado de forma proporcional a otro tráfico en los últimos 30 días.

Por ejemplo, un pico de tráfico dos veces al día tendrá un efecto relativamente modesto en el modelo general, ya que hay 29 días de tráfico normal que representan significativamente más de los datos de comportamiento generales.

**Punto clave**: la ventana móvil de 30 días ayuda al modelo a mantener la estabilidad durante las anomalías de tráfico temporales. Los picos o caídas a corto plazo no afectarán significativamente el rendimiento del modelo.

+++

## Temas relacionados {#related-topics}

<!--* [Get started with Decisioning](gs-experience-decisioning.md)-->
* [Creación de elementos de decisión](items.md)
* [Información general sobre modelos de IA](ranking/ai-models.md)
* [Limitaciones y protecciones de decisiones](decisioning-guardrails.md)

