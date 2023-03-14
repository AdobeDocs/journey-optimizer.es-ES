---
title: Cálculos estadísticos Utilizados en el Informe de Experimentación
description: Obtenga más información acerca de los cálculos estadísticos utilizados al ejecutar informes de experimentos
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 3%

---

# Cálculos estadísticos en el informe de experimentación {#experiment-report-calculations}

>[!BEGINSHADEBOX]

Lo que encontrará en esta documentación:

* [Introducción al experimento de contenido](get-started-experiment.md)
* [Creación de un experimento de contenido](content-experiment.md)
* [Comprensión de los cálculos estadísticos](experiment-calculations.md)
* [Configurar informes de experimentación](reporting-configuration.md)
* **[Cálculos estadísticos en el informe de experimentación](experiment-report-calculations.md)**

>[!ENDSHADEBOX]

Esta página documenta los cálculos estadísticos detallados utilizados en el Informe de experimentación para campañas en Adobe Journey Optimizer.

Tenga en cuenta que esta página está destinada a usuarios técnicos.

## Tasa de conversión

La tasa de conversión o **malo**,<sub></sub> para cada tratamiento `ν` en un experimento se define como una proporción de la suma de la métrica respecto al número de perfiles asignados a esa métrica, N<sub></sub>:

![](assets/statistical_1.png){width="125" align="center"}

Aquí, Y<sub>ibIoIoIoIo</sub> es el valor de la métrica objetivo para cada perfil `i`, que se ha asignado a una variante determinada **. Cuando la métrica del objetivo es una métrica &quot;única&quot;, es decir, es un recuento del número de perfiles que realizan una acción concreta, se muestra como una tasa de conversión y se le aplica un formato de porcentaje. Cuando la métrica es una métrica de &quot;recuento&quot; o &quot;valor total&quot; (por ejemplo, aperturas de correo electrónico, ingresos respectivamente), la estimación media de la métrica se muestra como &quot;Recuento por perfil&quot; o &quot;Valor por perfil&quot;.

Siempre que sea necesario, la desviación estándar de la muestra se utiliza con la expresión:

![](assets/statistical_2.png){width="225" align="center"}

## Alza {#lift}

El alza entre una variante  ** y la variante de control  *<sub>0</sub>* es el &quot;delta&quot; relativo en tasas de conversión, definido como el cálculo debajo de donde las tasas de conversión individuales son como se definen arriba. Esto se muestra como un porcentaje.

![](assets/statistical_3.png){width="125" align="center"}

</br>

## Intervalos de confianza válidos en cualquier momento para tratamientos individuales

El panel Experimentación con Recorridos muestra intervalos de confianza &quot;válidos en cualquier momento&quot; (secuencias de confianza) para tratamientos individuales en un experimento.

La secuencia de confianza para una variante individual `ν` es fundamental para la metodología estadística utilizada por el Adobe. Puede encontrar su definición en [esta página](https://doi.org/10.48550/arXiv.2103.06476) (reproducido desde [Waudby-Smith y otros.]).

Si le interesa calcular un parámetro de destinatario `ψ` como la tasa de conversión de una variante en un experimento, la dicotomía entre una secuencia de intervalos de confianza (IC) de tiempo fijo y una secuencia de confianza uniforme en el tiempo puede resumirse de la siguiente manera:

![](assets/statistical_4.png){width="500" align="center"}

Para un intervalo de confianza normal, la garantía probabilística de que el parámetro de destinatario se encuentra dentro del intervalo de valores se encuentra en el intervalo de valores que se ha establecido en el valor de la propiedad de la variable<sub>n</sub> solo es válido en un único valor fijo de `n` (donde `n` es el número de muestras). Por el contrario, para una secuencia de confianza, se garantiza que en todo momento/ todos los valores del tamaño de la muestra `t`, el valor &quot;true&quot; del parámetro de interés se encuentra dentro de los límites.

Esto tiene algunas implicaciones profundas que son muy importantes para las pruebas en línea:

* El CSS se puede actualizar de forma opcional cada vez que haya nuevos datos disponibles.
* Los experimentos pueden monitorizarse continuamente, detenerse de forma adaptativa o continuar.
* El error de tipo I se controla en todos los momentos de detención, incluidos los tiempos que dependen de los datos.

El Adobe utiliza secuencias de confianza asintóticas, que para una variante individual con estimación media `μ` tiene el siguiente formulario:

![](assets/statistical_5.png){width="300" align="center"}

Donde:

* `N` es el número de unidades de esa variante.
* `σ` es una estimación de muestra de la desviación estándar (definida anteriormente).
* `α` es el nivel deseado de error de tipo I (o probabilidad de cobertura incorrecta). Siempre se establece en 0,05.
* <sup>2</sup> es una constante que ajusta el tamaño de muestra con el que el CS es más ajustado. El Adobe ha elegido un valor universal de la<sup>2</sup> = 10<sup>-2,8</sup>, que es adecuada para los tipos de tasas de conversión de los experimentos en línea.

## Confianza {#confidence}

La confianza utilizada por el Adobe es una confianza &quot;válida en cualquier momento&quot;, que se obtiene invirtiendo la secuencia de confianza para el efecto medio del tratamiento.

Para ser precisos, en una muestra de dos *t* para comprobar la diferencia de medias entre dos variantes, existe una asignación 1:1 entre las variables *p*-valor para esta prueba, y el intervalo de confianza para la diferencia de medias. Por analogía, un en cualquier momento válido *p* El valor de -puede obtenerse invirtiendo la secuencia de confianza (válida en cualquier momento) para el estimador del efecto de tratamiento promedio:

![](assets/statistical_6.png){width="200" align="center"}

Aquí, *E* es una expectativa. El estimador utilizado es un estimador de tendencia inversa ponderada (PPI). Considerar N = N<sub>0</sub> +N<sub>1</sub> unidades, las asignaciones de variante para cada unidad `i` etiquetado por A<sub>i</sub>=0,1 si la unidad está asignada a una variante `ν`=0,1. Si los usuarios tienen asignada una probabilidad fija (tendencia), se debe realizar una prueba con la siguiente<sub>0</sub>, (1-<sub>0</sub>) y su métrica de resultados es Y<sub>i</sub>, entonces el estimador IPW para el efecto de tratamiento promedio es:

![](assets/statistical_12.png){width="400" align="center"}

Observando que *f* es la función de influencia, Waudby-Smith et al. mostró que la Secuencia de confianza para este estimador es:

![](assets/statistical_7.png){width="500" align="center"}

Sustituir la probabilidad de asignación por sus estimaciones empíricas:<sub>0</sub> = N<sub>0</sub>/N, el término de varianza puede expresarse en términos de estimaciones medias individuales de la muestra, en términos de valores estimados de la media de la muestra<sub>0,1</sub> y estimaciones de la desviación estándar,<sub>0,1</sub> como:

![](assets/statistical_8.png){width="500" align="center"}

A continuación, recuerde que para una prueba de hipótesis regular con la estadística de prueba z = (<sub>A</sub>-<sub>0</sub>/<sub>p</sub>) existe una correspondencia entre `p`-valores e intervalos de confianza:

![](assets/statistical_9.png){width="500" align="center"}

donde `Φ` es la distribución acumulada de la normalidad estándar. Para cualquier momento válido `p`-valores, dada la secuencia de confianza para el efecto de tratamiento promedio definido anteriormente, podemos invertir esta relación:

![](assets/statistical_10.png){width="600" align="center"}

Por último, el **confianza válida en cualquier momento** es:

![](assets/statistical_11.png){width="200" align="center"}

## Declarar un experimento como concluyente

Para un experimento con dos brazos, el panel Experimentación con Journey Optimizer muestra un mensaje que indica que un experimento es **concluyente** cuando la confianza válida en cualquier momento supere el 95 % (es decir, la confianza válida en cualquier momento) `p`-value está por debajo del 5 %).

Cuando hay más de dos variantes, se aplica la corrección de Bonferroni para controlar la tasa de error en el sentido familiar. Para experimentar con `K` tratamientos, y un único tratamiento basal (control), hay `K-1` pruebas de hipótesis independientes. La corrección de Bonferroni significa que rechazamos la hipótesis nula de que el control y una variante determinada tienen los mismos medios, si el en cualquier momento válido `p`-value (definido arriba) está por debajo de un umbral de `α/(K-1)`.

## Brazo con mejor rendimiento

Cuando se declara que un experimento es concluyente, se muestra el brazo con mejor rendimiento. Este es el brazo con el mejor rendimiento (media o tasa de conversión más alta), entre el Conjunto que incluye el control y todos los brazos que tienen un `p`-valor que está por debajo del umbral de Bonferroni.
