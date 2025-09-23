---
title: Cálculos estadísticos Utilizados en el Informe de Experimentación
description: Más información sobre las Pruebas A/B frente a bandidos multiarmados
feature: A/B Testing, Experimentation
role: User
level: Experienced
source-git-commit: 397fad9c95e0c11c0496ab5c9adfb6f8169de4f6
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 2%

---

# Experimentos de bandidos A/B vs Multi-armed {#mab-vs-ab}

<!--
>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Experiment type"
>abstract="Experiment type determines how traffic is allocated between treatments during your test. Choose the method that best aligns with your goals:</br>
>
>* **A/B Experiment**: Splits traffic as you define between treatments and measures performance until results are statistically significant. Best for learning which treatment performs better in a controlled comparison.
>
>* **Multi-armed Bandit**: Shifts traffic toward higher-performing treatments as data is collected, balancing speed and optimization. Useful when you want to maximize conversions during the experiment.
>
>* **Bring your own Multi-armed Bandit**: Use your own algorithm to decide traffic allocation, giving you flexibility if you have a custom model or strategy."
-->

Esta página proporciona una comparación detallada de los experimentos de **A/B** y **Multi-armed bandit**, explicando sus respectivas fortalezas, limitaciones y los escenarios en los que cada enfoque es más eficaz.

## A/B {#ab-test}

El experimento A/B tradicional implica dividir el tráfico de forma equitativa entre tratamientos y mantener esta asignación hasta que finalice el experimento. Una vez alcanzada la relevancia estadística, se identifica el tratamiento ganador y posteriormente se escala.

### Ventajas

Los puntos fuertes clave de los experimentos A/B tradicionales son:

* **Rigor estadístico**

  El diseño fijo proporciona tasas de error e intervalos de confianza bien definidos.

  Los marcos de prueba de hipótesis, por ejemplo, una confianza del 95 %, son más fáciles de aplicar e interpretar.

  Los experimentos con la potencia adecuada reducen la probabilidad de falsos positivos.

* **Simplicidad**

  La metodología es sencilla de diseñar y ejecutar.

  Los resultados se pueden comunicar claramente a las partes interesadas no técnicas.

* **Recopilación de datos completa**

  Cada tratamiento recibe una exposición adecuada, lo que permite el análisis no solo de la variante ganadora, sino también de alternativas de bajo rendimiento.

  Esta información adicional puede servir de base para las decisiones estratégicas a largo plazo.

* **Control de sesgo**

  La asignación fija reduce la susceptibilidad a sesgos como la &quot;maldición del ganador&quot; o la regresión a la media.

### Limitaciones

Las principales limitaciones de los experimentos A/B tradicionales son las siguientes:

* **Costo de oportunidad**

  Una proporción sustancial del tráfico se dirige a tratamientos inferiores, lo que puede reducir las conversiones o los ingresos durante la prueba.

  El tratamiento ganador no puede implementarse hasta que el experimento finalice.

* **Requisito De Duración Fija**

  Por lo general, las pruebas deben realizarse en el horizonte previamente establecido, incluso si las condiciones externas, por ejemplo, la estacionalidad, los cambios de mercado, cambian a mitad de camino.

  La adaptación durante el experimento es limitada.

## Bandido multiarmado {#mab-experiment}

Los algoritmos de bandidos multiarmados utilizan la asignación adaptativa: a medida que se acumula evidencia, más tráfico se dirige hacia tratamientos de mejor rendimiento. El objetivo es maximizar la recompensa acumulada durante el experimento en lugar de centrarse únicamente en el resultado final.

### Ventajas

Los puntos fuertes de los métodos multi-armed bandit son:

* **Optimización más rápida**

  Los tratamientos prometedores se priorizan antes, mejorando el rendimiento general durante la prueba.

* **Adaptación**

  Las asignaciones se actualizan continuamente a medida que se recopilan los datos, lo que hace que Multi-armed bandit sea adecuado para entornos dinámicos.

* **Costo de oportunidad reducido**

  Los tratamientos deficientes se eliminan rápidamente, minimizando el tráfico desperdiciado.

* **Idoneidad para pruebas continuas**

  Eficaz para la experimentación continua o en contextos en los que el tráfico es costoso.

### Limitaciones

Las principales limitaciones de los métodos multi-armed bandit son:

* **Garantías estadísticas más débiles**

  Las pruebas de hipótesis tradicionales son más difíciles de aplicar y las reglas de detención son menos claras.

* **Transparencia reducida**

  La asignación adaptable puede ser difícil de explicar a las partes interesadas.

* **Información limitada sobre tratamientos de bajo rendimiento**

  Los tratamientos débiles reciben poca exposición, lo que limita el diagnóstico de insight.

* **Complejidad de implementación**

  Requiere algoritmos e infraestructura avanzados, con mayor potencial de errores de configuración.

## Cuándo usar A/B o multi-armed bandit

| Escenario | Método recomendado |
|-|-|
| Está ejecutando pruebas exploratorias o basadas en investigación | A/B |
| Está ejecutando campañas siempre activas, por ejemplo, anuncios o recomendaciones | Multi-armed bandit |
| Desea maximizar las conversiones durante la prueba | Multi-armed bandit |
| Desea información clara y fiable | A/B |
| Debe adaptarse rápidamente, por ejemplo, con los turnos de temporada | Multi-armed bandit |
| Tiene tráfico limitado y desea optimizar el retorno de la inversión rápidamente | Multi-armed bandit |
| Tiene mucho tráfico y puede permitirse un aprendizaje más lento | A/B |
| Las partes interesadas necesitan puntos de decisión claros | A/B |

