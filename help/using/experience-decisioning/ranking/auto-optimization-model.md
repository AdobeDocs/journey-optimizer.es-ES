---
solution: Journey Optimizer
product: Journey Optimizer
title: Modelos de optimización automática
description: Más información sobre los modelos de optimización automática
feature: Ranking, Decisioning
role: User
level: Experienced
exl-id: 8a8b66cb-dd96-4373-bbe0-a67e0dc0b2c0
version: Journey Orchestration
source-git-commit: ca31e819b0d120f54adfe2035ecacb21ac4f1f15
workflow-type: tm+mt
source-wordcount: '1675'
ht-degree: 0%

---

# Modelos de optimización automática {#auto-optimization-model}

El modelo de optimización automática de [!DNL Adobe Journey Optimizer] es un modelo de aprendizaje de refuerzo que maximiza la tasa de pulsaciones de oferta (CTR) al explorar todas las ofertas (o contenido) y, a continuación, clasifica los elementos en función del CTR predicho, después de aplicar las reglas de elegibilidad y los límites de frecuencia.

## Casos de uso y ventajas {#use-cases-benefits}

La optimización automática se puede utilizar siempre que desee realizar una configuración rápida y sencilla, buscar ofertas ganadoras generales y maximizar los clics de ofertas dentro de un solo canal. Por ejemplo:

* Elija las mejores ofertas para insertar en una página web para maximizar los clics en las ofertas.
* Elija las mejores ofertas para insertar en un correo electrónico para maximizar los clics en las ofertas.
* Elija las mejores ofertas para insertar en una pantalla de aplicación móvil para maximizar los clics en las ofertas.

La optimización automática es una buena opción cuando:

* Las ofertas cambian con el tiempo o con frecuencia: el modelo de optimización automática se vuelve a entrenar cada seis horas.

## Requisitos y limitaciones {#requirements-limitations}

La optimización automática tiene los siguientes requisitos y límites:

* La optimización automática requiere un conjunto de datos de formación que contenga eventos de visualización de ofertas, eventos de clic de ofertas y el grupo de campos Evento de experiencia: interacciones de propuestas.
* Los modelos de optimización automática no se pueden utilizar en solicitudes a la API de decisiones por lotes.
* La optimización automática siempre se optimiza para los clics en ofertas. Para maximizar para un objetivo que no sean los clics en ofertas, use el modelo [Optimización personalizada](personalized-optimization-model.md).
* La optimización automática intenta encontrar ofertas ganadoras generales y no encuentra una clasificación personalizada para cada cliente. Para encontrar clasificaciones personalizadas para cada cliente, use el modelo [Optimización personalizada](personalized-optimization-model.md).

Para entrenar un modelo de optimización automática, el conjunto de datos debe cumplir los siguientes requisitos mínimos:

* Al menos 2 ofertas del conjunto de datos deben tener al menos 100 eventos de visualización y 5 eventos de clic en los últimos 14 días.
* El modelo tratará las ofertas con menos de 100 visualizaciones o eventos de 5 clics en los últimos 14 días como nuevas ofertas y solo son elegibles para ser servidas por el bandido de exploración.
* El modelo tratará las ofertas con más de 100 visualizaciones y eventos de 5 clics en los últimos 14 días como ofertas existentes y pueden ser servidas por bandidos de exploración y explotación.

Hasta la primera vez que se entrene un modelo de optimización automática, las ofertas dentro de una estrategia de selección que utilice un modelo de optimización automática se servirán al azar.

## Optimización de equilibrio con aprendizaje {#balancing-optimization-learning}

La optimización automática es un modelo de [aprendizaje de refuerzo](https://en.wikipedia.org/wiki/Reinforcement_learning){target="_blank"} que aprende sobre el rendimiento de pulsaciones de ofertas basadas en el comportamiento real de los clientes. Los modelos de aprendizaje de refuerzo buscan maximizar un objetivo mediante la elección de acciones con resultados mejor predichos. Sin embargo, un modelo que siempre presentaba a cada cliente el artículo o artículos con el mejor resultado predicho nunca aprendería sobre el rendimiento de los nuevos artículos introducidos a lo largo del tiempo (el llamado &quot;problema de inicio en frío&quot;), ni sobre los cambios en el rendimiento de otros artículos existentes resultantes de los cambios en el comportamiento de los clientes a lo largo del tiempo. Por lo tanto, los modelos de aprendizaje de refuerzo deben administrar lo que comúnmente se denomina compensación de [explorar-explotar](https://en.wikipedia.org/wiki/Exploration%E2%80%93exploitation_dilemma){target="_blank"}, es decir, la optimización del equilibrio con el aprendizaje.

La optimización automática usa un enfoque común denominado [bandido multibrazo](https://en.wikipedia.org/wiki/Multi-armed_bandit){target="_blank"} para administrar la compensación. El bandido multiarmado toma decisiones de clasificación basadas en:

* la tasa de pulsaciones prevista de cada elemento
* las diferencias en la tasa de pulsaciones prevista de cada elemento
* grado de incertidumbre del modelo sobre sus predicciones para cada ítem.

Los bandidos multiarmados utilizan esta información, junto con la variabilidad aleatoria, para elegir las acciones a tomar. La optimización automática es un [algoritmo de ensamblado](https://en.wikipedia.org/wiki/Ensemble_learning){target="_blank"} que contiene varios bandidos multibrazo para garantizar que todas las ofertas se exploran adecuadamente y, al mismo tiempo, maximizar el rendimiento general.

Al responder a una solicitud de clasificación, un bandido multiarmado &quot;supervisor&quot; primero elige si esta solicitud debe estar sesgada hacia la exploración o sesgada hacia la explotación. Esta decisión se toma con un enfoque &quot;épsilon-codicioso&quot;.

La segunda capa de clasificación la realiza uno de los dos bandidos [Muestreo Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}:

* El 10 % del tráfico se asigna a un método de bandido centrado en la exploración que es más probable que recomiende nuevas ofertas o aquellas con datos limitados, bajo el supuesto de que el modelo se beneficiaría de aprender más sobre el comportamiento de los clientes en respuesta a estas ofertas.
* El 90 % del tráfico se asigna a un método de bandido centrado en la explotación que es más probable que recomiende de forma coherente ofertas de alto rendimiento a lo largo del tiempo, bajo el supuesto de que las ofertas nuevas o de datos bajos tienen más probabilidades de bajo rendimiento hasta que se pruebe lo contrario.

En un sentido técnico, estas suposiciones son parámetros de la distribución de probabilidad anterior, también conocida como [anteriores](https://en.wikipedia.org/wiki/Prior_probability){target="_blank"}. A medida que las ofertas reúnen más datos de visualización y clics, la influencia de los precedentes elegidos disminuye, y las predicciones realizadas por los dos bandidos tienden a converger con el tiempo.

Nuestro enfoque de combinar varios bandidos y asignar algo de tráfico dedicado para la exploración ofrece varios beneficios:

* el modelo obtiene información con mayor rapidez sobre las ofertas más recientes con menos datos
* el modelo sigue conociendo todas las ofertas y responde a los cambios en el comportamiento de los clientes a lo largo del tiempo
* el modelo no se sobreajusta al favorecer agresivamente ofertas con CTR aparente más alto, pero pocas observaciones, o desfavorecer agresivamente ofertas con CTR aparente más bajo, pero pocas observaciones
* el modelo es sólido para administrar las decisiones de asignación de tráfico en cientos de ofertas con datos de clics dispersos y con cantidades muy diferentes de datos históricos

## Muestreo Thompson {#thompson-sampling}

[Muestreo Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}, o bandidos bayesianos, es un enfoque bayesiano del problema de los bandidos multiarmados. El modelo trata la recompensa promedio 𝛍 de cada oferta como una variable aleatoria y usa los datos que hemos recopilado hasta el momento para actualizar nuestra &quot;creencia&quot; sobre la recompensa promedio. Esta &quot;creencia&quot; está representada matemáticamente por una distribución de probabilidad posterior -esencialmente un rango de valores para la recompensa promedio, junto con la plausibilidad (o probabilidad) de que la recompensa tenga ese valor para cada oferta. Luego, para cada decisión, tomaremos una muestra de un punto de cada una de estas distribuciones de recompensa posterior y seleccionaremos la oferta cuya recompensa muestreada tenía el valor más alto.

Este proceso se ilustra en la figura siguiente, donde tenemos 3 ofertas diferentes. Inicialmente no tenemos evidencia de los datos, y asumimos que todas las ofertas tienen una distribución de recompensa posterior uniforme. Tomamos una muestra de la distribución posterior de recompensas de cada oferta. La muestra seleccionada en la distribución de la oferta 2 tiene el valor más alto. Este es un ejemplo de exploración. Después de mostrar la Oferta 2, recopilamos cualquier recompensa potencial (por ejemplo, conversión/no conversión) y actualizamos la distribución posterior de la Oferta 2 usando el Teorema de Bayes como se explica a continuación. Continuamos este proceso y actualizamos las distribuciones posteriores cada vez que se muestra una oferta y se obtiene la recompensa. En la segunda cifra, se selecciona la Oferta 3: a pesar de que la Oferta 1 tiene la recompensa promedio más alta (su distribución de recompensa posterior está más a la derecha), el proceso de muestreo de cada distribución nos ha llevado a elegir una Oferta 3 aparentemente subóptima. Al hacerlo, nos damos la oportunidad de aprender más acerca de la verdadera distribución de recompensas de Offer 3.

A medida que se recogen más muestras, la confianza aumenta y se obtiene una estimación más precisa de la posible recompensa (correspondiente a distribuciones de recompensa más estrechas). Este proceso de actualizar nuestras creencias a medida que se dispone de más evidencia se conoce como **Inferencia bayesiana**.

Finalmente, si una oferta (por ejemplo, la oferta 1) es un claro ganador, su distribución de recompensa posterior se separará de las demás. En este punto, para cada decisión, es probable que la recompensa muestreada de la Oferta 1 sea la más alta y la elegiremos con una mayor probabilidad. Esto es explotación: tenemos la firme convicción de que la Oferta 1 es la mejor, por lo que se elige maximizar las recompensas.

![](../assets/ai-ranking-thompson-sampling.png)

**Figura 1**: *Por cada decisión, tomamos una muestra de un punto de las distribuciones de recompensa posteriores. Se elige la oferta con el valor de muestra más alto (tasa de conversión). En la fase inicial, todas las ofertas tienen una distribución uniforme, ya que no tenemos ninguna evidencia sobre las tasas de conversión de las ofertas a partir de los datos. A medida que recogemos más muestras, las distribuciones posteriores se vuelven más estrechas y precisas. En última instancia, se elegirá siempre la oferta con la tasa de conversión más alta.*

+++ Detalles del cálculo

Para calcular/actualizar distribuciones, usamos el **Teorema de Bayes**. Para cada oferta ***i***, queremos calcular su ***P(𝛍i | datos)***, es decir, para cada oferta ***i***, la probabilidad de que exista un valor de recompensa **𝛍i**, dados los datos que hemos recopilado hasta ahora para esa oferta.

Del Teorema De Bayes:

***Posterior = Probabilidad * Anterior***

La **probabilidad anterior** es la suposición inicial acerca de la probabilidad de producir un resultado. La probabilidad, después de que se hayan recopilado algunas pruebas, se conoce como la **probabilidad posterior**.

La optimización automática está diseñada para tener en cuenta las recompensas binarias (clic/sin clic). En este caso, la probabilidad representa el número de éxitos de los ensayos N y se modela mediante una distribución binomial. Para algunas funciones de probabilidad, si se elige una determinada anterior, la posterior termina estando en la misma distribución que la anterior. A este tipo de prior se le denomina **conjugado prior**. Este tipo de antecedente hace que el cálculo de la distribución posterior sea muy sencillo. La [distribución Beta](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"} es un conjugado anterior a la probabilidad binomial (recompensas binarias), y por lo tanto es una opción conveniente y sensata para las distribuciones de probabilidad anterior y posterior. La distribución de Beta toma dos parámetros, **&#x200B;**&#x200B;**&#x200B; y &#x200B;**&#x200B;**&#x200B;**. Estos parámetros pueden considerarse como el recuento de éxitos y errores y el valor medio dado por:

![](../assets/ai-ranking-beta-distribution.png)

La función de probabilidad, tal como se ha explicado anteriormente, se modela mediante una distribución binomial, con s éxitos (conversiones) y f errores (sin conversiones), y q es una variable aleatoria con una distribución Beta.

La distribución anterior se modela mediante Beta y la posterior toma la siguiente forma:

![](../assets/ai-ranking-posterior-distribution.svg)

+++

### Prejuicio de exploración y prejuicio de explotación {#exploration-exploitation-bias}

Se debe elegir un valor inicial para los parámetros **&#x200B;**&#x200B;**, &#x200B;**&#x200B;**&#x200B;**. La optimización automática incluye un método de muestreo Thompson sesgado por la exploración y un método de muestreo Thompson sesgado por la explotación que utilizan diferentes niveles iniciales de **&#x200B;**&#x200B;**, &#x200B;**&#x200B;**&#x200B;** en sus distribuciones beta.

En un enfoque de muestreo Thompson general, la parte posterior se calcula simplemente añadiendo el número de éxitos y errores a los parámetros existentes **&#x200B;**&#x200B;**, &#x200B;**&#x200B;**&#x200B;**. La optimización automática utiliza diferentes factores de ponderación para nuevos éxitos y errores a la hora de modificar el impacto de los nuevos datos frente a los datos anteriores, tanto en los bandidos basados en la exploración como en los basados en la explotación.

## Referencias {#references}

Para profundizar en el muestreo de bandidos Thompson, consulte los siguientes artículos de investigación:

* [Evaluación empírica del muestreo Thompson](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target="_blank"}
* [Análisis del muestreo Thompson para el problema Multi-armed Bandit](https://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target="_blank"}
