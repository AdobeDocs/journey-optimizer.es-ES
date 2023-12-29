---
solution: Journey Optimizer
product: journey optimizer
title: Cálculos estadísticos Utilizados por Experimentación con Adobe Journey Optimizer
description: Obtenga más información acerca de los cálculos estadísticos utilizados al ejecutar experimentos
feature: Experimentation
topic: Content Management
role: User
level: Experienced
keywords: contenido, experimento, estadística, cálculo
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 1490ac2efd39c6bf9b6ca97e682750463e9f054d
workflow-type: tm+mt
source-wordcount: '1067'
ht-degree: 0%

---

# Comprensión de los cálculos estadísticos {#experiment-calculations}

En este artículo se describen los cálculos estadísticos utilizados al ejecutar Experimentos en Adobe Journey Optimizer.

La experimentación utiliza [métodos estadísticos avanzados](../campaigns/assets/confidence_sequence_technical_details.pdf) para calcular **Secuencias de confianza** y **Confianza**, que le permiten ejecutar los experimentos durante el tiempo que sea necesario y supervisar los resultados continuamente.

En este artículo se describe cómo funciona Experimentación y se ofrece una introducción intuitiva a la de Adobe **Secuencias de confianza válidas en cualquier momento**.

Para usuarios expertos, los detalles técnicos y las referencias se detallan en [esta página](../campaigns/assets/confidence_sequence_technical_details.pdf).

## Pruebas estadísticas y control de errores {#statistical-testing}

Cuando ejecuta un experimento intenta determinar si hay una diferencia entre dos poblaciones y la probabilidad de que esa diferencia se deba al azar.

Generalmente hay dos hipótesis:

* el **Hipótesis nula** lo que significa que el tratamiento no tiene ningún efecto.
* el **Hipótesis alternativa** significa que el tratamiento tiene un efecto.

En la significancia estadística, el objetivo es tratar de evaluar la fuerza de la evidencia para rechazar la hipótesis nula. Un punto importante a tener en cuenta es que se utiliza la relevancia estadística para juzgar la probabilidad de que los tratamientos sean diferentes, no la probabilidad de que tengan éxito. Por este motivo, la relevancia estadística se utiliza en combinación con **Alza**.

La experimentación efectiva requiere tener en cuenta diferentes tipos de errores que podrían causar inferencias incorrectas.

![](assets/technote_1.png)

La tabla anterior ilustra los diferentes tipos de errores:

* **Falsos positivos (errores de tipo I)**: son un rechazo incorrecto de la hipótesis nula, cuando en realidad es verdadera. En el contexto de los experimentos en línea, esto significa que concluimos erróneamente que la métrica de resultados es diferente entre cada tratamiento, aunque era la misma.
  </br>Antes de ejecutar el experimento, generalmente elegimos un umbral `\alpha`. Una vez ejecutado el experimento, la variable `p-value` se calcula y rechazamos la variable `null if p < \alpha`.Elegir un `/alpha` se basa en las consecuencias de obtener una respuesta incorrecta, por ejemplo, en un ensayo clínico en el que la vida de una persona podría verse afectada. `\alpha = 0.005`. Un umbral comúnmente utilizado en la experimentación en línea es `\alpha = 0.05`, lo que significa que a largo plazo, esperamos que 5 de cada 100 experimentos sean falsos positivos.

* **Falsos negativos (errores de tipo II)**: significa que no rechazamos la hipótesis nula aunque sea falsa. Para Experimentos, esto significa que no rechazamos la hipótesis nula, cuando en realidad es diferente. Para controlar este tipo de error, generalmente necesitamos tener suficientes usuarios en nuestro experimento para garantizar un determinado poder, definido como `1 - \beta`(es decir, uno menos la probabilidad de un error de tipo II).

La mayoría de las técnicas de inferencia estadística requieren que arregle el tamaño de la muestra con antelación, según el tamaño del efecto que desee determinar, así como su tolerancia a errores (`\alpha` y `\beta`) con antelación. Sin embargo, la metodología de Adobe Journey Optimizer está diseñada para permitirle observar continuamente sus resultados, para cualquier tamaño de muestra.

## Metodología Estadística Del Adobe: Secuencias De Confianza Válidas En Cualquier Momento

A **Secuencia de confianza** es un análogo secuencial de un **Intervalo de confianza**, por ejemplo, si repite los experimentos cien veces y calcula una estimación de la métrica media y su secuencia de confianza del 95 % asociada para cada nuevo usuario que entra en el experimento. Una secuencia de confianza del 95 % incluirá el valor verdadero de la métrica en 95 de los 100 experimentos que ejecutó. Un intervalo de confianza del 95 % solo se podía calcular una vez por experimento para ofrecer la misma garantía de cobertura del 95 %; no con cada nuevo usuario. Por lo tanto, las secuencias de confianza le permiten monitorizar continuamente los experimentos, sin aumentar las tasas de error de los falsos positivos.

La diferencia entre las secuencias de confianza y los intervalos de confianza para un único experimento se muestra en la siguiente animación:

![](assets/technote_2.gif)

**Secuencias de confianza** desplazar el enfoque de Experimentos a la estimación en lugar de a las pruebas de hipótesis, es decir, centrarse en la estimación precisa de la diferencia en las medias entre tratamientos, en lugar de rechazar o no una hipótesis nula basada en un umbral de relevancia estadística.

Sin embargo, de manera similar a la relación entre `p-values`, o **Confianza**, y **Intervalos de confianza**, también existe una relación entre **Secuencias de confianza** y en cualquier momento válido `p-values`, o en cualquier momento de confianza válida. Dada la familiaridad de cantidades como la Confianza, el Adobe proporciona tanto la **Secuencias de confianza** y en cualquier momento Confianza válida en sus informes.

Los fundamentos teóricos de **Secuencias de confianza** provienen del estudio de secuencias de variables aleatorias conocidas como martingales. A continuación se incluyen algunos resultados principales para lectores expertos, pero las conclusiones de los profesionales son claras:

>[!NOTE]
>
>Las secuencias de confianza se pueden interpretar como análogos secuenciales seguros de los intervalos de confianza. Con intervalos de confianza solo puede interpretar el experimento una vez que haya alcanzado el tamaño de muestra predeterminado. Sin embargo, con las secuencias de confianza puede ver e interpretar los datos de los experimentos siempre que lo desee y detener o continuar los experimentos de forma segura. La confianza válida en cualquier momento correspondiente, o `p-value`, también es seguro de interpretar en cualquier momento.

Es importante señalar que, dado que las secuencias de confianza son &quot;válidas en cualquier momento&quot;, serán más conservadoras que una metodología de horizonte fijo utilizada con el mismo tamaño de muestra. Los límites de la secuencia de confianza son generalmente más anchos que el cálculo del intervalo de confianza, mientras que la confianza válida en cualquier momento será menor que el cálculo de confianza del horizonte fijo. El beneficio de este conservadurismo es que puedes interpretar tus resultados de forma segura en todo momento.

## Declarar un experimento como concluyente

![](assets/experimentation_report_2.png)

Cada vez que visualiza el informe de experimentación, Adobe analiza los datos que se hayan acumulado en el experimento hasta este momento. Luego declara que un experimento es &quot;concluyente&quot; cuando la confianza válida en cualquier momento supere el umbral del 95 % para al menos uno de los tratamientos.

En este punto, el tratamiento que funcione mejor (según la tasa de conversión o el valor de métrica normalizado por perfiles) se resaltará en la parte superior de la pantalla del informe y se indicará con una estrella en el informe tabular. En esta determinación solo se tienen en cuenta los tratamientos que tienen una confianza superior al 95 %, junto con la línea de base.

Cuando hay más de dos tratamientos, se utiliza el enlace de corrección de Bonferroni para corregir los problemas de comparación múltiple y controla la tasa de error familiar. En este escenario, también es posible que haya varios tratamientos cuya confianza sea superior al 95 % y cuyos intervalos de confianza se superpongan. En este caso, Adobe Journey Optimizer declarará que el que tenga la tasa de conversión más alta (o el valor de métrica normalizado por perfiles) es el que tiene el mejor rendimiento.
