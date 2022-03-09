---
product: experience platform
solution: Experience Platform
title: Acerca de los modelos de IA
description: Obtenga información sobre los modelos de IA que permiten clasificar ofertas
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: a7483965e3154d0ad34cfb56b6458bb63b46a26c
workflow-type: tm+mt
source-wordcount: '1530'
ht-degree: 0%

---

# Modelos de IA {#ai-models}

## Introducción a los modelos de IA {#get-started-with-ai-rankings}

Puede utilizar un sistema de modelos entrenado que clasifique las ofertas para mostrarlas en un perfil determinado.

>[!CAUTION]
>
>Actualmente, el uso de modelos de IA está disponible en acceso anticipado solo para usuarios seleccionados.

Esta función le permite crear diferentes **Modelos de IA** en función de sus objetivos comerciales. Utilizando estas diferentes estrategias basadas en objetivos en una decisión, el sistema de modelos entrenado le ayudará a comprender cómo los diferentes modelos de IA están afectando a sus objetivos.

Por ejemplo, puede seleccionar un modelo de IA para el canal de correo electrónico y otro para el canal push. Para cada canal, el sistema de modelos entrenado utilizará múltiples puntos de datos para determinar qué oferta debe presentarse primero para una ubicación determinada, en lugar de tener en cuenta las puntuaciones de prioridad de las ofertas o una [fórmula de clasificación](create-ranking-formulas.md).

Una vez creado un modelo de IA, asígnelo a una colocación en una decisión. Obtenga más información en [Configurar la selección de ofertas en decisiones](../offer-activities/configure-offer-selection.md).

>[!NOTE]
>
>Actualmente en [!DNL Journey Optimizer] el único tipo de modelo admitido para la clasificación AI es **optimización automática**.

## Modelo de optimización automática {#auto-optimization}

Un modelo de optimización automática tiene como objetivo ofrecer ofertas que maximicen el rendimiento (KPI) establecido por los clientes empresariales. Estos KPI podrían presentar tasas de conversión, ingresos, etc. En este punto, la optimización automática se centra en optimizar los clics de ofertas con la conversión de ofertas como nuestro objetivo. La optimización automática no está personalizada y se optimiza según el rendimiento &quot;global&quot; de las ofertas.

### Terminología

Los siguientes términos son útiles al tratar el tema de la optimización automática:

* **Multi-armed bandit**: A [multi-armed bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit)El método de optimización {target=&quot;_blank&quot;} equilibra el aprendizaje de exploración y la explotación de dicho aprendizaje.

* **Muestreo Thomson**: El muestreo Thompson es un algoritmo para problemas de decisión en línea en el que las acciones se toman secuencialmente de manera que se debe equilibrar entre explotar lo que se sabe que maximiza el rendimiento inmediato y la inversión para acumular nueva información que puede mejorar el rendimiento futuro. [Más información](#thompson-sampling)

* [**Distribución beta**](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}: Conjunto continuo [distribuciones de probabilidad](https://en.wikipedia.org/wiki/Probability_distribution){target=&quot;_blank&quot;} definido en el intervalo [0, 1] [parametrizado](https://en.wikipedia.org/wiki/Statistical_parameter){target=&quot;_blank&quot;} por dos positivos [parámetros de forma](https://en.wikipedia.org/wiki/Shape_parameter){target=&quot;_blank&quot;}.

### Muestreo Thompson {#thompson-sampling}

El algoritmo que subyace a la optimización automática es **Muestreo Thompson**. En esta sección, discutimos la intuición detrás del muestreo Thompson.

[Muestreo Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target=&quot;_blank&quot;}, o bandidos bayesianos, es un enfoque bayesiano del problema multi-armed bandit.  La idea básica es tratar la recompensa promedio ?? de cada oferta como **variable aleatoria** y usar los datos que hemos recopilado hasta ahora, para actualizar nuestra &quot;creencia&quot; sobre la recompensa promedio. Esta &quot;creencia&quot; se representa matemáticamente mediante una **distribución posterior de la probabilidad** - básicamente, un rango de valores para la recompensa promedio, junto con la plausibilidad (o probabilidad) de que la recompensa tenga ese valor para cada oferta. Entonces, para cada decisión, **muestra un punto de cada una de estas distribuciones de recompensa posteriores** y seleccione la oferta cuya recompensa de muestra tenía el valor más alto.

Este proceso se ilustra en la figura siguiente, donde tenemos 3 ofertas diferentes. Inicialmente no tenemos evidencia de los datos y asumimos que todas las ofertas tienen una distribución posterior uniforme. Obtenemos una muestra de la distribución de recompensas posterior de cada oferta. El ejemplo seleccionado de la distribución de la oferta 2 tiene el valor más alto. Este es un ejemplo de **exploración**. Después de mostrar la Oferta 2, recopilamos cualquier recompensa potencial (por ejemplo, conversión/no conversión) y actualizamos la distribución posterior de la Oferta 2 usando Bayes Theorem como se explica más abajo.  Continuamos con este proceso y actualizamos las distribuciones posteriores cada vez que se muestra una oferta y se recopila la recompensa. En la segunda figura, se selecciona la Oferta 3 - a pesar de que la Oferta 1 tiene la recompensa promedio más alta (su distribución de recompensa posterior está más lejos a la derecha), el proceso de muestreo de cada distribución nos ha llevado a elegir una Oferta 3 aparentemente subóptima. Al hacerlo, nos damos la oportunidad de aprender más sobre la verdadera distribución de recompensas de la Oferta 3.

A medida que se recogen más muestras, aumenta la confianza y se obtiene una estimación más precisa de la posible recompensa (correspondiente a distribuciones de recompensa más estrechas). Este proceso de actualización de nuestras creencias a medida que más evidencia está disponible se conoce como **Inferencia bayesiana**.

Al final, si una oferta (por ejemplo, la oferta 1) es una clara ganadora, la distribución posterior de la recompensa se separará de otras. En este punto, para cada decisión, es probable que la recompensa de la oferta 1 muestreada sea la más alta y la elegiremos con una probabilidad mayor. Esto es **explotación** - tenemos la firme convicción de que la Oferta 1 es la mejor, por lo que se está eligiendo para maximizar las recompensas.

![](../assets/ai-ranking-thompson-sampling.png)

**Figura 1**: *Por cada decisión, mostramos un punto de las distribuciones de recompensa posteriores. Se elige la oferta con el valor de muestra más alto (tasa de conversión). En la fase inicial, todas las ofertas tienen una distribución uniforme, ya que no tenemos ninguna evidencia de las tasas de conversión de las ofertas a partir de los datos. A medida que recolectamos más muestras, las distribuciones posteriores se vuelven más estrechas y precisas. Finalmente, la oferta con la tasa de conversión más alta se elige cada vez.*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**Detalles técnicos**

Para calcular/actualizar distribuciones, utilizamos **Teorema de Bayes**. Para cada oferta ***i***, queremos calcular su ***P(??i | data)***, es decir, para cada oferta ***i***, qué probabilidad tiene un valor de recompensa **??i** es, dados los datos que hemos recopilado hasta ahora para esa oferta.

De Bayes Theorem:

***Posterior = Probabilidad * Anterior***

La variable **probabilidad previa** es la suposición inicial sobre la probabilidad de producir una salida. La probabilidad, después de que se hayan recopilado algunas pruebas, se conoce como **probabilidad posterior**. 

La optimización automática está diseñada para considerar recompensas binarias (clic/sin clic). En este caso, la probabilidad representa el número de éxitos de N ensayos y está modelado por un **Distribución binomial**. Para algunas funciones de probabilidad, si elige un antes determinado, el posterior termina en la misma distribución que el anterior. Un entonces anterior se denomina **conjugado anterior**. Este tipo de anteriores hace que el cálculo de la distribución posterior sea muy simple. La variable **Distribución beta** es un conjugado previo a la probabilidad binomial (recompensas binarias), por lo que es una opción conveniente y sensata para las distribuciones de probabilidad anteriores y posteriores.La distribución beta emplea dos parámetros, ***α*** y ***β***. Estos parámetros se pueden considerar como el recuento de éxitos y fracasos y el valor medio dado por:

![](../assets/ai-ranking-beta-distribution.png)

La función Probabilidad, como hemos explicado anteriormente, está modelada por una distribución binomial, con éxitos de s (conversiones) y de errores (no conversiones) y q es una [variable aleatoria](https://en.wikipedia.org/wiki/Random_variable){target=&quot;_blank&quot;} con un [distribución beta](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}.

El anterior está modelado por la distribución beta y la distribución posterior adopta la siguiente forma:

![](../assets/ai-ranking-posterior-distribution.svg)

El posterior se calcula simplemente añadiendo el número de éxitos y errores a los parámetros existentes ***α***, ***β***.

Para la optimización automática, como se muestra en el ejemplo anterior, comenzamos con una distribución anterior ***Beta(1, 1)*** (distribución uniforme) para todas las ofertas y después de obtener los éxitos y los errores de una oferta determinada, el posterior se convierte en una distribución beta con parámetros ***(s+α, f+β)*** para esa oferta.
+++

**Temas relacionados**:

Para profundizar en el muestreo Thompson, lea los siguientes artículos de investigación:
* [Evaluación empírica del muestreo Thompson](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target=&quot;_blank&quot;}
* [Análisis del Muestreo Thompson para el Problema de Multi-armed Bandit](http://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target=&quot;_blank&quot;}

### Problema de arranque en frío

El problema de &quot;inicio en frío&quot; se produce cuando se agrega una oferta nueva a una campaña y no hay datos disponibles sobre la tasa de conversión de la oferta nueva. Durante este periodo, tenemos que idear una estrategia sobre la frecuencia con la que se elige esta nueva oferta para minimizar la caída del rendimiento, mientras recopilamos información sobre la tasa de conversión de esta nueva oferta. Hay múltiples soluciones disponibles para enfrentar este problema. La clave es encontrar un equilibrio entre la exploración de esta nueva oferta mientras que no sacrificamos la explotación mucho. Actualmente utilizamos &quot;distribución uniforme&quot; como nuestra estimación inicial sobre la tasa de conversión de la nueva oferta (distribución previa). Básicamente, damos a todos los valores de tasa de conversión la misma probabilidad de ocurrencia.


![](../assets/ai-ranking-cold-start-strategies.png)

**Figura 2**: *Considere una campaña con 3 ofertas. Mientras la campaña está activa, la oferta 4 se agrega a la campaña. Inicialmente no tenemos datos sobre la tasa de conversión de la oferta 4 y tenemos que lidiar con el problema de arranque en frío. Utilizamos la distribución uniforme como nuestra estimación inicial sobre la tasa de conversión de la oferta 4, mientras recopilamos datos para esta nueva oferta. Como se explica en la sección [Muestreo Thompson](#thompson-sampling) , para elegir qué oferta se mostrará a un usuario, tomamos muestras de los puntos de las distribuciones de recompensas posteriores de las ofertas y seleccionamos la oferta con el valor de muestra más alto. En el ejemplo anterior, se elige la oferta 4 y más tarde, según la recompensa recopilada, la distribución posterior de esta oferta se actualiza como se explica en la [Muestreo Thompson](#thompson-sampling) para obtener más información.*

### Medición del alza

&quot;Alza&quot; es la métrica utilizada para medir el rendimiento de cualquier estrategia implementada en el servicio de clasificación, en comparación con la estrategia de línea de base (sirve ofertas de forma aleatoria).

Por ejemplo, si estamos interesados en medir el rendimiento de una estrategia de muestreo Thompson (TS) utilizada en la clasificación del servicio, y el KPI es la tasa de conversión (CVR), el &quot;alza&quot; de la estrategia de TS frente a la estrategia de línea de base se define de la siguiente manera:

![](../assets/ai-ranking-lift.png)
