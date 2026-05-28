---
title: Cálculos estadísticos Utilizados en el Informe de Experimentación
description: Más información sobre las Pruebas A/B frente a bandidos multiarmados
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 1f7b74d2-77c3-4113-8e6a-1e2a95117748
TQID: https://experienceleague.adobe.com/47tFiWTUUsGUMeWhuJVQnakAIrgz1Ax1mO-u8pf27uc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: []
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d3cdead0-685a-4489-9250-4bb709942f66id: e1e0219c-f879-479f-8427-888ed2a6e9c2
subfeature_v2: id: f29a52db-c90c-4345-902e-b586d1406d8d
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 629
ht-degree: 19%

---

# Experimentos A/B frente a de bandido multibrazo {#mab-vs-ab}

>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Tipo de experimento"
>abstract="El tipo de experimento determina cómo se asigna el tráfico entre los tratamientos durante la prueba. Elija el método que mejor se ajuste a sus objetivos:</br><b>Experimento A/B</b>: divide el tráfico a medida que usted define entre tratamientos y mide el rendimiento hasta que los resultados son estadísticamente significativos. Lo mejor para saber qué tratamiento funciona mejor en una comparación controlada.</br><b>Multi-armed Bandit</b>: desplaza el tráfico hacia tratamientos de mayor rendimiento a medida que se recopilan los datos, equilibrando la velocidad y la optimización. Es útil cuando desea maximizar las conversiones durante el experimento.</br><b>Traiga su propio bandido multibrazo</b>: use su propio algoritmo para decidir la asignación del tráfico, lo que le proporciona flexibilidad si tiene un modelo o una estrategia personalizados."

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

## Multi-armed bandit {#mab-experiment}

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

| Situación | Método recomendado |
|-|-|
| Está ejecutando pruebas exploratorias o basadas en investigación | A/B |
| Está ejecutando campañas siempre activas, por ejemplo, anuncios o recomendaciones | Multi-armed bandit |
| Desea maximizar las conversiones durante la prueba | Multi-armed bandit |
| Desea información clara y fiable | A/B |
| Debe adaptarse rápidamente, por ejemplo, con los turnos de temporada | Multi-armed bandit |
| Tiene tráfico limitado y desea optimizar el retorno de la inversión rápidamente | Multi-armed bandit |
| Tiene mucho tráfico y puede permitirse un aprendizaje más lento | A/B |
| Las partes interesadas necesitan puntos de decisión claros | A/B |
