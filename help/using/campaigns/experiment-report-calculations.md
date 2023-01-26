---
title: Cálculos estadísticos utilizados en el informe Experimentación
description: Obtenga más información sobre los cálculos estadísticos utilizados al ejecutar informes de experimento
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Cálculos estadísticos en el informe de experimentación {#experiment-report-calculations}

En esta página se documentan los cálculos estadísticos detallados utilizados en el informe Experimentación para campañas en Adobe Journey Optimizer.

Tenga en cuenta que esta página está diseñada para usuarios técnicos.

## Tasa de conversión

La tasa de conversión o **medium**, μ<sub>ν</sub> para cada tratamiento `ν` en un experimento se define como una proporción de la suma de la métrica con respecto al número de perfiles asignados a esa métrica, N<sub>ν</sub>:

![](assets/statistical_1.png){width="125" align="center"}

Aquí, Y<sub>iν</sub> es el valor de la métrica objetivo para cada perfil `i`, que se ha asignado a una variante determinada *ν*. Cuando la métrica objetivo es una métrica &quot;única&quot;, es decir, un recuento del número de perfiles que realizan una acción en particular, se muestra como una tasa de conversión y con formato de porcentaje. Cuando la métrica es una métrica de &quot;recuento&quot; o &quot;valor total&quot; (por ejemplo, aperturas de correo electrónico, ingresos respectivamente), la estimación media de la métrica se muestra como &quot;Recuento por perfil&quot; o &quot;Valor por perfil&quot;.

Donde sea necesario, se utiliza la desviación estándar de muestra con la expresión:

![](assets/statistical_2.png){width="225" align="center"}

## Alza {#lift}

El alza entre una variante  *ν* y la variante de control  *ν<sub>0</sub>* es el &quot;delta&quot; relativo en las tasas de conversión, definido como el cálculo a continuación donde las tasas de conversión individuales son las definidas anteriormente. Se muestra como porcentaje.

![](assets/statistical_3.png){width="125" align="center"}

</br>

## Intervalos de confianza válidos en cualquier momento para tratamientos individuales

El panel Experimentación con Recorrido muestra intervalos de confianza &quot;en cualquier momento válidos&quot; (secuencias de confianza) para tratamientos individuales en un experimento.

Secuencia de confianza de una variante individual `ν` es fundamental para la metodología estadística utilizada por el Adobe. Puede encontrar su definición en [esta página](https://doi.org/10.48550/arXiv.2103.06476) (reproducido a partir de [Waudby-Smith y otros.]).

Si le interesa calcular un parámetro de destino `ψ` como la tasa de conversión de una variante en un experimento, la dicotomía entre una secuencia de intervalos de confianza (CI) de &quot;tiempo fijo&quot; y una secuencia de confianza (CS) uniforme en el tiempo puede resumirse de la siguiente manera:

![](assets/statistical_4.png){width="500" align="center"}

Para un intervalo de confianza normal, la garantía probabilística de que el parámetro de destino se encuentra dentro del rango de valores Ċ<sub>n</sub> solo es válido con un único valor fijo de `n` (donde `n` es el número de muestras). Por el contrario, para una secuencia de confianza, se garantiza que en todo momento/ todos los valores del tamaño de la muestra `t`, el valor &quot;true&quot; del parámetro de interés se encuentra dentro de los límites.

Esto tiene algunas implicaciones profundas que son muy importantes para las pruebas en línea:

* El CS se puede actualizar de forma opcional cada vez que haya nuevos datos disponibles.
* Los experimentos se pueden supervisar continuamente, detener adaptativamente o continuar.
* El error de tipo I se controla en todo momento de detención, incluidos los tiempos dependientes de los datos.

El Adobe utiliza secuencias de confianza asintóticas, que para una variante individual con estimación media `μ` tiene el formulario:

![](assets/statistical_5.png){width="300" align="center"}

Donde:

* `N` es el número de unidades para esa variante.
* `σ` es una estimación de muestra de la desviación estándar (definida anteriormente).
* `α` es el nivel deseado de error de tipo I (o probabilidad de falta de cobertura). Esto siempre se establece en 0,05.
* ρ<sup>2</sup> es una constante que afina el tamaño de la muestra con el que CS es más ajustado. Adobe ha elegido un valor universal de ρ<sup>2</sup> = 10<sup>-2,8</sup>, que es adecuado para los tipos de tasas de conversión que se ven en los experimentos en línea.

## Confianza {#confidence}

La confianza utilizada por el Adobe es una confianza &quot;válida en cualquier momento&quot;, que se obtiene invirtiendo la secuencia de confianza para el efecto medio del tratamiento.

Para ser precisos, en dos muestras *t* prueba de la diferencia de medios entre dos variantes, hay una asignación 1:1 entre *p*-valor para esta prueba, y el intervalo de confianza para la diferencia de medios. Por analogía, un valor válido en cualquier momento *p*-value puede obtenerse invirtiendo la secuencia de confianza (en cualquier momento válida) para el estimador del efecto de tratamiento medio:

![](assets/statistical_6.png){width="200" align="center"}

Aquí, *E* es una expectativa. El estimador utilizado es un estimador con ponderación de tendencia inversa (IPW). Considere N = N<sub>0</sub> +N<sub>1</sub> unidades, las asignaciones de variante para cada unidad `i` etiquetada por A<sub>i</sub>=0,1 si la unidad se asigna a la variante `ν`=0,1. Si a los usuarios se les asigna una probabilidad fija (propensión) π<sub>0</sub>, (1-π<sub>0</sub>) y su métrica de resultados es Y<sub>i</sub>, el estimador de IPW para el efecto medio del tratamiento es:

![](assets/statistical_12.png){width="400" align="center"}

Observando que *f* es la función de influencia, Waudby-Smith y otros. se ha demostrado que la secuencia de confianza para este estimador es:

![](assets/statistical_7.png){width="500" align="center"}

Sustituir la probabilidad de asignación por sus estimaciones empíricas: π<sub>0</sub> = N<sub>0</sub>/N, el término de variación puede expresarse en términos de estimaciones medias de muestra individuales μ<sub>0,1</sub> y estimaciones de desviaciones estándar, σ<sub>0,1</sub> como:

![](assets/statistical_8.png){width="500" align="center"}

A continuación, recuerde que para una prueba de hipótesis normal con estadística de prueba z = (μ<sub>A</sub>-μ<sub>0</sub>/σ<sub>p</sub>) hay una correspondencia entre `p`-valores e intervalos de confianza:

![](assets/statistical_9.png){width="500" align="center"}

donde `Φ` es la distribución acumulativa de la normalidad estándar. Para cualquier momento válido `p`-valores, dada la secuencia de confianza para el efecto de tratamiento promedio definido anteriormente, podemos invertir esta relación:

![](assets/statistical_10.png){width="600" align="center"}

Por último, la variable **confianza válida en cualquier momento** es:

![](assets/statistical_11.png){width="200" align="center"}

## Declarar un experimento concluyente

Para un experimento con dos brazos, el panel Experimento con Journey Optimizer muestra un mensaje que indica que un experimento es **concluyente** cuando la confianza válida en cualquier momento exceda el 95 % (es decir, el valor válido en cualquier momento `p`-value es inferior al 5 %).

Cuando hay más de dos variantes, la corrección de Bonferonni se aplica para controlar la tasa de error por familia. Para un experimento con `K` tratamientos, y un único tratamiento basal (control), `K-1` pruebas de hipótesis independientes. La corrección de Bonferonni significa que rechazamos la hipótesis nula de que el control y una variante determinada tienen los mismos medios, si el valor es válido en cualquier momento `p`-value (definido anteriormente) está por debajo de un umbral de `α/(K-1)`.

## Mejor rendimiento

Cuando se declara concluyente un experimento, se muestra el brazo de mejor rendimiento. Este es el grupo con el mejor rendimiento (media o tasa de conversión más alta), entre el conjunto que incluye el control y todos los brazos que tienen un `p`-valor que está por debajo del umbral de Bonferonni.
