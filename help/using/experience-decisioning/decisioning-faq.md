---
title: Preguntas más frecuentes sobre decisiones
description: Obtenga respuestas a preguntas comunes sobre las funcionalidades de Decisioning.
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
source-git-commit: 74f8db8f71cbf51260868a93702a563b3c0d4a2d
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 0%

---

# Preguntas más frecuentes sobre decisiones {#decisioning-faq}

Esta página proporciona respuestas a las preguntas frecuentes sobre las capacidades de toma de decisiones en Adobe Journey Optimizer.

## Reglas de límite {#capping-rules}

+++**¿Qué sucede cuando se aplican varias reglas de límite a una sola oferta?**

Una oferta se limita tan pronto como **se cumple cualquier condición individual**. Cuando existen varias reglas de límite, la oferta deja de mostrarse una vez que cualquier regla alcanza su umbral.

**Ejemplo:**
Si define dos reglas de límite para una oferta:
* 5 veces por perfil y por semana
* 100 veces el total entre todos los usuarios

La oferta dejará de mostrarse a un usuario una vez que la haya visto 5 veces en una semana, aunque aún no se haya alcanzado el límite total de 100. Del mismo modo, una vez que se alcanzan las 100 impresiones totales, la oferta deja de mostrarse a todos los usuarios.

Más información sobre [reglas de límite](items.md#capping).

+++

## Fórmulas de clasificación {#ranking-formulas}

+++**¿Cuál es la función de las audiencias en comparación con un conjunto de datos completo en los modelos de IA?**

Al configurar [modelos de IA](ranking/ai-models.md), tanto los conjuntos de datos como las audiencias tienen distintos propósitos.

* **Conjuntos de datos**: capture eventos de conversión (clics, pedidos, ingresos) que sirven como objetivos de optimización para el modelo.
* **Audiencias**: funcionan como variables predictoras que permiten al modelo personalizar las recomendaciones según el abono a segmentos del cliente.

Las audiencias no restringen ni amplían el ámbito del modelo. En su lugar, proporcionan atributos contextuales que mejoran la capacidad del modelo para hacer predicciones personalizadas en diferentes segmentos de clientes.

Ambos componentes son necesarios para obtener [modelos de optimización personalizados](ranking/personalized-optimization-model.md) con rendimiento efectivo.

+++

+++**¿Cómo afectan los cambios en las colecciones de ofertas a la optimización automática o a los modelos de optimización personalizados?**

El modelo de optimización automática proporciona tráfico a la siguiente mejor oferta disponible en función de los datos de tráfico de los últimos 14 días, independientemente de si el modelo de optimización personalizado utiliza datos de tráfico de los últimos 30 días.

Cuando se eliminan varias ofertas simultáneamente y las ofertas restantes tienen datos de tráfico mínimos dentro del intervalo de 14 o 30 días, el modelo puede mostrar un comportamiento subóptimo, incluidos patrones de distribución aleatorios o sesgo hacia ofertas con tasas de conversión más altas basadas en datos de impresión limitados.

**Práctica recomendada**: cuando modifique de forma significativa las colecciones de ofertas, compruebe que las ofertas restantes tengan datos de rendimiento históricos suficientes para mantener la eficacia del modelo.

+++

+++**¿Con qué rapidez los modelos de IA incorporan nuevas ofertas?**

Los modelos de IA identifican y comienzan a probar las ofertas recién disponibles en su próximo ciclo de formación:

* **Optimización automática** identifica y comienza a probar nuevas ofertas en su próximo ciclo de formación. El entrenamiento de optimización automática se realiza de 3 a 4 veces al día, aproximadamente cada 6 horas.
* **Optimización personalizada** identifica y comienza a probar nuevas ofertas a medida que se agregan a la estrategia de ofertas. Se incluirán en el tráfico de exploración aleatorio. A continuación, esas ofertas se personalizarán en el siguiente ciclo de formación del modelo, que se produce semanalmente.

Una vez identificados, ambos modelos empezarán a ofrecer las nuevas ofertas a algunos visitantes inmediatamente para probar su rendimiento y recopilar datos sobre su eficacia.

Obtenga más información sobre [optimización automática](ranking/auto-optimization-model.md) y [modelos de optimización personalizada](ranking/personalized-optimization-model.md).

+++

+++**¿Cómo se optimizan los modelos de IA sin grupos de control?**

Tanto la optimización automática como los modelos de optimización personalizados emplean una estrategia de &quot;explorar y explotar&quot; que elimina la necesidad de grupos de control dedicados.

* **Fase inicial**: los modelos comienzan con una exploración del 100%, probando diferentes ofertas para establecer los datos de rendimiento de línea de base.
* **Optimización adaptable**: a medida que se acumulan eventos de comportamiento y mejora la precisión de predicción, los modelos equilibran automáticamente la exploración y la explotación.
* **Aprendizaje continuo**: El sistema asigna progresivamente más tráfico a ofertas de alto rendimiento mientras continúa probando alternativas.

Esto garantiza un aprendizaje y una optimización continuos en todo el tráfico sin necesidad de grupos de control independientes.

+++

+++**¿Cuáles son los requisitos mínimos de tráfico para un rendimiento óptimo del modelo de IA?**

Adobe recomienda los siguientes umbrales mínimos para garantizar el rendimiento efectivo del modelo:
* 1.000 impresiones por oferta/artículo por semana
* 100 eventos de conversión por oferta/artículo por semana

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

De forma predeterminada, el sistema no intentará crear modelos personalizados para ofertas o elementos con menos de 1000 impresiones o 50 eventos de conversión.

>[!NOTE]
>
>En entornos de producción con catálogos de ofertas grandes (aproximadamente 300 ofertas) y reglas comerciales restrictivas, algunas ofertas pueden acercarse a umbrales absolutos más bajos (250 impresiones y 25 conversiones por 30 días). Estos representan los requisitos mínimos de datos para la formación de modelos, pero es posible que no garanticen un rendimiento óptimo.

Más información sobre [requisitos de recopilación de datos](data-collection/data-collection.md).

+++

+++**¿Cómo afectan las ofertas similares al rendimiento del modelo de IA?**

Los modelos de IA generan mayores beneficios de personalización cuando las ofertas atraen a distintos segmentos de clientes. Cuando las ofertas son muy similares, hay dos resultados típicos:

* **Rendimiento equivalente**: Las ofertas funcionan de manera idéntica y reciben una distribución de tráfico aproximadamente igual.
* **Oferta dominante**: Las diferencias menores hacen que una oferta supere a otras en todos los segmentos, capturando la mayoría del tráfico.

>[!NOTE]
>
>La diferenciación de las ofertas no garantiza una distribución equilibrada del tráfico. Las ofertas con propuestas de valor objetivamente superiores (por ejemplo, descuento de 100 € frente a descuento de 50 €) normalmente predominarán en todos los segmentos de clientes, independientemente de los esfuerzos de personalización.

**Práctica recomendada**: Diseñe ofertas con diferenciación significativa que se alineen con las distintas preferencias de segmentos del cliente para maximizar la eficacia del modelo de IA.

+++

+++**¿Cómo afectan las anomalías de tráfico al rendimiento del modelo de IA?**

Las anomalías de tráfico se incorporan al modelo proporcionalmente dentro de la ventana móvil de 30 días, lo que proporciona estabilidad al modelo durante las fluctuaciones de tráfico temporales. Los picos o caídas a corto plazo no afectan significativamente las predicciones o el rendimiento del modelo.

Un pico de tráfico temporal (por ejemplo, el doble del tráfico diario) tiene un efecto mínimo en el rendimiento general del modelo, ya que el tráfico anómalo representa una pequeña fracción del conjunto de datos de 30 días.

+++
