---
title: Cálculos estadísticos utilizados por experimentación
description: Obtenga más información sobre los cálculos estadísticos utilizados al ejecutar experimentos
feature: Overview
topic: Content Management
role: User
level: advanced
hide: true
hidefromtoc: true
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 0fb54571ea7620c981e746f8ac240b675e2f0d64
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Comprender los cálculos estadísticos {#experiment-calculations}

>[!AVAILABILITY]
>
>Actualmente, la función de experimento de contenido solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

En este artículo se describen los cálculos estadísticos utilizados al ejecutar Experimentos en Adobe Journey Optimizer. La experimentación utiliza métodos estadísticos avanzados para calcular **Secuencias de confianza** y **Confianza**, que le permiten ejecutar los experimentos durante el tiempo que sea necesario y supervisar los resultados continuamente.

Este artículo describe cómo funciona la experimentación y proporciona una introducción intuitiva al informe de Adobe **Cualquier secuencia de confianza válida por tiempo**.

Para los usuarios expertos, los detalles técnicos y las referencias se detallan en [esta página](https://experienceleague.adobe.com/docs/journey-optimizer/assets/confidence_sequence_technical_details.pdf?lang=en).

## Pruebas estadísticas y control de errores {#statistical-testing}

![](assets/technote_1.png)

Como se ilustra en el cuadro anterior, muchas metodologías de inferenciación estadística están diseñadas para controlar dos tipos de errores:

* **Falsos positivos (errores de tipo I)**: es un rechazo incorrecto de la hipótesis null, cuando en realidad es true. En el contexto de Experimentos en línea, esto significa que concluimos falsamente que la métrica de resultados es diferente entre cada tratamiento, aunque era la misma.
   </br>Antes de ejecutar el experimento, normalmente elegimos un umbral `$\alpha$`. Una vez ejecutado el experimento, la variable `$p$-value` se calcula y rechazamos el `null if $p < \alpha$`. Un umbral comúnmente utilizado es `$\alpha = 0.05$`, lo que significa que a largo plazo, esperamos que 5 de cada 100 experimentos sean falsos positivos.

* **Falsos negativos (errores de tipo II)**: significa que no rechazamos la hipótesis nula aunque sea falsa. En Experimentos, esto significa que no rechazamos la hipótesis nula, cuando de hecho es diferente. Para controlar este tipo de error, generalmente necesitamos tener suficientes usuarios en nuestro experimento para garantizar una cierta Potencia, definida como `$1 - \beta$`(es decir, una menos la probabilidad de un error de tipo II).

La mayoría de las técnicas de inferenciación estadística requieren que fije el tamaño de la muestra con antelación, en función del tamaño del efecto que desee determinar, así como de la tolerancia a errores (`$\alpha$` y `$\beta$`) con antelación. Sin embargo, la metodología de Adobe Journey Optimizer está diseñada para permitirle observar continuamente sus resultados, para cualquier tamaño de muestra.

## Metodología estadística del Adobe: Cualquier secuencia de confianza válida por tiempo

A **Secuencia de confianza** es un analógico secuencial de a **Intervalo de confianza**, por ejemplo, si repite los experimentos cien veces y calcula una estimación de la métrica media y su secuencia de confianza del 95 % asociada para cada nuevo usuario que entre en el experimento. Una secuencia de confianza del 95 % incluirá el valor verdadero de la métrica en 95 de los 100 experimentos que ejecutó. Un intervalo de confianza del 95 % solo se podía calcular una vez por experimento para ofrecer la misma garantía de cobertura del 95 %; no con cada nuevo usuario. Por lo tanto, las secuencias de confianza le permiten supervisar continuamente los experimentos, sin aumentar las tasas de error de False Positive.

La diferencia entre las secuencias de confianza y los intervalos de confianza para un único experimento se muestra en la siguiente animación:

![](assets/technote_2.gif)

**Secuencias de confianza** desplazar el foco de Experimentos a la estimación en lugar de a las pruebas de hipótesis, es decir, centrándose en la estimación precisa de la diferencia de medios entre tratamientos, en lugar de rechazar o no una hipótesis nula basada en un umbral de relevancia estadística.

Sin embargo, de forma similar a la relación entre `$p$-values`o **Confianza** y **Intervalos de confianza**, también hay una relación entre **Secuencias de confianza** y en cualquier momento válido `$p$-values`, o en cualquier momento de Confianza válida. Dada la familiaridad de cantidades como la Confianza, el Adobe proporciona tanto la variable **Secuencias de confianza** y en cualquier momento Confianza válida en sus informes.

Los fundamentos teóricos de **Secuencias de confianza** provienen del estudio de secuencias de variables aleatorias conocidas como martingales. A continuación se incluyen algunos resultados principales para los lectores expertos, pero las opiniones de los profesionales son claras:

    Las secuencias de confianza se pueden interpretar como análisis secuenciales seguros de intervalos de confianza. Puede ver e interpretar los datos de sus experimentos en el momento que desee y detenerlos o continuar con los experimentos de forma segura. La correspondiente Confianza válida por tiempo, o `$p$-value`, también es segura de interpretar.

Es importante señalar que, dado que las secuencias de confianza son &quot;válidas en cualquier momento&quot;, serán más conservadoras que una metodología de horizonte fijo utilizada con el mismo tamaño de muestra. Los límites de la secuencia de confianza son generalmente más anchos que un cálculo de intervalo de confianza, mientras que cualquier confianza válida en cualquier momento será menor que un cálculo de confianza de horizonte fijo. El beneficio de este conservadurismo es que puedes interpretar tus resultados con seguridad en todo momento.

## Declarar un experimento concluyente

![](assets/experimentation_report_2.png)

Cada vez que vea el informe de experimentación, Adobe analiza los datos que se han acumulado en el experimento hasta este punto y declarará que un experimento es &quot;concluyente&quot; cuando la confianza en cualquier momento válido cruce un umbral del 95 % para al menos uno de los tratamientos.

En este punto, el tratamiento que está teniendo el mejor rendimiento (en función de la tasa de conversión o el valor de métrica normalizado por perfil) se resaltará en la parte superior de la pantalla del informe y se indicará con una estrella en el informe tabular. En esta determinación sólo se tienen en cuenta los tratamientos que tienen una confianza buena superior al 95%, junto con el valor basal.

Cuando hay más de dos tratamientos, el enlace de corrección de Bonferroni se utiliza para corregir múltiples problemas de comparación, y controla la tasa de error por familia. En este escenario, también es posible que haya múltiples tratamientos cuya confianza sea buena en más del 95% y cuyos intervalos de confianza se superpongan. En este caso, los Adobes declararán que el que tenga la tasa de conversión más alta (o valor de métrica normalizado por perfil) sea el mejor ejecutante.
