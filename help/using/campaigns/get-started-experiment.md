---
solution: Journey Optimizer
product: journey optimizer
title: Introducción al experimento de contenido
description: Obtenga más información sobre el experimento de contenido en Journey Optimizer
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: introducción, inicio, contenido, experimento
hide: true
hidefromtoc: true
exl-id: 7fe4b24e-f60a-4107-a064-00010b0cbbfc
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '2013'
ht-degree: 2%

---

# Introducción a los experimentos de contenido {#get-started-experiment}

>[!BEGINSHADEBOX]

Lo que encontrará en esta documentación:

* **[Introducción al experimento de contenido](get-started-experiment.md)**
* [Creación de un experimento de contenido](content-experiment.md)
* [Comprensión de los cálculos estadísticos](experiment-calculations.md)
* [Configurar informes de experimentación](reporting-configuration.md)
* [Cálculos estadísticos en el informe de experimentación](experiment-report-calculations.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Actualmente, la función Experimento de contenido solo está disponible para un conjunto de organizaciones (disponibilidad limitada). Para obtener más información, contacte con su representante de Adobe.

## ¿Qué es un experimento de contenido?

Los experimentos de contenido le permiten optimizar el contenido para las acciones de sus campañas.

Los experimentos son un conjunto de ensayos aleatorios que, en el contexto de las pruebas en línea, significa que algunos usuarios seleccionados aleatoriamente están expuestos a una variación determinada de un mensaje y otro conjunto de usuarios seleccionados aleatoriamente a otro tratamiento. Después de enviar el mensaje, puede medir las métricas de resultado que le interesan, por ejemplo, las aperturas de correos electrónicos o los clics.

## ¿Por qué ejecutar experimentos?

![](assets/content_experiment_schema.png)

Los experimentos le permiten aislar los cambios que conducen a mejoras en las métricas. Como se ilustra en la imagen anterior: algunos usuarios seleccionados al azar están expuestos a cada grupo de tratamiento, lo que significa que, en promedio, los grupos compartirán las mismas características. Por lo tanto, cualquier diferencia en los resultados puede interpretarse como debida a las diferencias en los tratamientos recibidos, es decir, usted es capaz de establecer un vínculo causal entre los cambios que hizo, y los resultados que le interesan.

Esto le permite tomar decisiones basadas en datos para optimizar sus objetivos comerciales.

Para Experimentos de contenido en Adobe Journey Optimizer, puede probar ideas como:

* **Línea de asunto**: ¿Cuál podría ser el impacto de un cambio en el tono o en el grado de personalización de una línea de asunto?
* **Contenido del mensaje**: ¿Cambiar el diseño visual de un correo electrónico resultará en más clics en el correo electrónico?

## ¿Cómo funciona el experimento de contenido? {#content-experiment-work}

### Asignación aleatoria

La experimentación de contenido en Adobe Journey Optimizer utiliza un hash seudoaleatorio de la identidad del visitante para realizar una asignación aleatoria de usuarios en la audiencia de destino a uno de los tratamientos que haya definido. El mecanismo de hash garantiza que, en los escenarios en los que el visitante entra en una campaña varias veces, reciba el mismo tratamiento de forma determinista.

En detalle, el algoritmo MumurHash3 de 32 bits se utiliza para hash la cadena de identidad del usuario en uno de los 10 000 buckets. En un experimento de contenido con el 50 % del tráfico asignado a cada tratamiento, los usuarios que se encuentren en bloques del 1 al 5 000 recibirán el primer tratamiento, mientras que los usuarios de los bloques del 5 001 al 10 000 recibirán el segundo tratamiento. Dado que se utiliza un hash seudoaleatorio, las divisiones de visitante que observe pueden no ser exactamente 50-50; sin embargo, la división será estadísticamente equivalente al porcentaje de división objetivo.

Tenga en cuenta que, como parte de la configuración de cada campaña con un experimento de contenido, debe elegir un área de nombres de identidad desde la que se seleccionará userId para el algoritmo de aleatorización. Esto es independiente de la variable [direcciones de ejecución](../configuration/primary-email-addresses.md).

### Recopilación y análisis de datos

En el momento de la asignación, es decir, cuando el mensaje se envía en canales salientes o cuando el usuario introduce la campaña en canales entrantes, se registra un &quot;registro de asignación&quot; en el conjunto de datos del sistema correspondiente. Registrará a qué tratamiento se asignó el usuario, junto con los identificadores de experimento y campaña.

Las métricas objetivas se pueden agrupar en dos clases principales:

* Métricas directas, en las que el usuario reacciona directamente al tratamiento, por ejemplo, abriendo un correo electrónico o haciendo clic en un vínculo.
* Métricas indirectas o &quot;en la parte inferior del canal&quot;, que ocurren después de que el usuario haya estado expuesto al tratamiento.

En el caso de las métricas objetivas directas en las que Adobe Journey Optimizer realiza un seguimiento de los mensajes, los eventos de respuesta de los usuarios finales se etiquetan automáticamente con los identificadores de campaña y tratamiento, lo que permite la asociación directa de la métrica de respuesta con un tratamiento. [Más información sobre el seguimiento](../email/message-tracking.md).

![](assets/technote_2.png)

En el caso de objetivos indirectos o &quot;al final del canal&quot;, como las compras, los eventos de respuesta de los usuarios finales no se etiquetan con los identificadores de campaña y tratamiento, es decir, un evento de compra se produce después de la exposición a un tratamiento y no hay una asociación directa de esa compra con una asignación de tratamiento previa. Para estas métricas, los Adobes asociarán el tratamiento con la parte inferior del evento de conversión de canal si:

* La identidad del usuario es la misma en el momento del evento de asignación y conversión.
* La conversión se produce en un plazo de siete días tras la asignación del tratamiento.

![](assets/technote_3.png)

A continuación, Adobe Journey Optimizer utiliza métodos estadísticos avanzados &quot;válidos en cualquier momento&quot; para interpretar estos datos de informes sin procesar, lo que le permite interpretar sus informes de experimentación. Para obtener más información, consulte [esta página](../campaigns/experiment-calculations.md).

## Sugerencias para ejecutar experimentos

Al ejecutar experimentos, es importante seguir ciertas prácticas recomendadas. A continuación se ofrecen algunas sugerencias para ejecutar estos experimentos:

+++Aisle las variables que está intentando probar

Formule alguna hipótesis que pretenda probar y restrinja esta hipótesis al menor número posible de cambios para determinar qué ha influido en su envío.

Por ejemplo, una buena hipótesis puede ser si la personalización en las líneas de asunto del correo electrónico genera mejores tasas de apertura. Sin embargo, también añadir un cambio en el contenido del mensaje o en las imágenes puede dar como resultado una conclusión confusa.
+++

+++Asegúrese de que está utilizando la métrica correcta

Determine la métrica a la que desea dirigirse y si los cambios que está realizando pueden tener algún impacto directo en esta métrica.

Por ejemplo, es poco probable que el cambio del contenido del cuerpo del mensaje afecte a las tasas de apertura de los correos electrónicos.
+++

+++Ejecute la prueba en el tamaño de audiencia correcto o durante el tiempo suficiente

Si ejecuta las pruebas durante más tiempo, podrá detectar diferencias menores en la métrica de objetivo entre tratamientos. Sin embargo, si el valor de línea de base de la métrica de objetivo es pequeño, necesitará tamaños de muestra más grandes.
El número de usuarios que se debe incluir en el experimento depende del tamaño del efecto que desee detectar, la variación o propagación de la métrica de objetivo, así como la tolerancia para errores de falsos positivos y falsos negativos. En Experimentos clásicos, puede utilizar un [calculadora de tamaño de muestra](https://experienceleague.adobe.com/tools/calculator/testcalculator.html?lang=es){_blank} para determinar durante cuánto tiempo debe ejecutar la prueba.
+++

+++Comprender la incertidumbre estadística

Si está ejecutando un experimento en el que 1000 usuarios han visto un tratamiento y la tasa de conversión se establece en 5 %. ¿Sería esta la tasa de conversión real si se incluyeran todos los usuarios? ¿Cuál sería la tasa de conversión real?
Los métodos estadísticos nos dan una forma de formalizar esa incertidumbre. Uno de los conceptos más importantes que hay que entender al realizar experimentos en línea es que las tasas de conversión observadas son coherentes con una serie de tasas de conversión reales subyacentes, lo que significa que debe esperar hasta que esas estimaciones sean lo suficientemente precisas antes de intentar sacar una conclusión. Los intervalos de confianza y la confianza nos ayudan a cuantificar esta incertidumbre.
+++

+++Forme nuevas hipótesis y realice pruebas continuamente

Para obtener verdaderas perspectivas comerciales, debe ceñirse a un solo Experimento. En su lugar, realice un seguimiento de los experimentos formulando nuevas hipótesis y ejecutando nuevas pruebas con diferentes cambios en diferentes segmentos, y examinando el impacto en las distintas métricas.
+++

## Interprete los resultados de sus experimentos {#interpret-results}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_summary"
>title="Widget de resumen"
>abstract="El widget Resumen proporciona una descripción general de los resultados del experimento, incluido si son concluyentes o no. Ofrece una forma rápida y sencilla de comprender el resultado de su experimento."

![](assets/experimentation_report_3.png)

En esta sección se describen los informes de experimento y cómo comprender las distintas cantidades estadísticas que se presentan.

Estas son algunas directrices para interpretar los resultados de su experimento de contenido.

Tenga en cuenta que una descripción completa de los resultados debe tener en cuenta todas las pruebas disponibles (es decir, los tamaños de las muestras, las tasas de conversión, los intervalos de confianza, etc.), y no solo la declaración de concluyente o no. Incluso cuando un resultado aún no es concluyente, puede haber pruebas convincentes de que un tratamiento es diferente de otro.

Para comprender los cálculos estadísticos, consulte [página](../campaigns/experiment-calculations.md).

### 1. Comparar métricas normalizadas {#normalized-metrics}

Al comparar el rendimiento de dos tratamientos, siempre debe comparar las métricas normalizadas para tener en cuenta cualquier diferencia en el número de perfiles expuestos a cada tratamiento.

Por ejemplo, si el objetivo del experimento se establece en **[!UICONTROL Aperturas únicas]**, y se mostró un tratamiento determinado para 10 000 perfiles con 200 aperturas únicas registradas, lo que representa un **[!UICONTROL Tasa de conversión]** del 2 %. En el caso de métricas no únicas, como la métrica Abrir, la métrica normalizada se muestra como un **[!UICONTROL Recuento por perfil]**, mientras que para métricas continuas como Precio total, la métrica normalizada se muestra como un **[!UICONTROL Total por perfil]**.

### 2. Centrarse en los intervalos de confianza {#confidence-intervals}

Cuando se ejecutan experimentos con muestras de los perfiles, la tasa de conversión observada para un tratamiento determinado representa una estimación de la tasa de conversión subyacente real.

Por ejemplo, si el tratamiento A tiene un **[!UICONTROL Tasa de conversión]** del 3 %, mientras que el Tratamiento B tiene un **[!UICONTROL Tasa de conversión]** del 2%, ¿es el tratamiento A mejor ejecutor que el tratamiento B? Para responder a esta pregunta, primero debemos cuantificar la incertidumbre en las tasas de conversión observadas.

Los intervalos de confianza ayudan a cuantificar la incertidumbre en las tasas de conversión estimadas, pero unos intervalos de confianza más amplios implican más incertidumbre. A medida que se añadan más perfiles al experimento, los intervalos se reducirán, lo que representa una estimación más precisa. El intervalo de confianza representa una serie de tasas de conversión que son compatibles con los datos observados.

Si los intervalos de confianza para dos tratamientos apenas se superponen, significa que los dos tratamientos tienen tasas de conversión diferentes. Sin embargo, si existe mucha superposición entre los intervalos de confianza para dos tratamientos, es más probable que los dos tratamientos tengan la misma tasa de conversión.

El Adobe utiliza intervalos de confianza válidos en cualquier momento del 95 % o secuencias de confianza, lo que significa que los resultados se pueden ver de forma segura en cualquier momento durante el experimento.

### 3. Comprender el alza {#understand-lift}

El resumen del informe de experimento muestra la **[!UICONTROL Alza sobre línea base]**, que es una medida de la mejora porcentual en la tasa de conversión de un tratamiento determinado respecto al valor de referencia. Definida con precisión, es la diferencia de rendimiento entre un tratamiento determinado y la línea de base, dividida por el rendimiento de la línea de base, expresada como porcentaje.

### 3. Comprender la confianza {#understand-confidence}

Aunque debe centrarse principalmente en la **[!UICONTROL Intervalo de confianza]** para la realización de cada tratamiento, el Adobe también muestra la Confianza, que es una medida probabilística de cuánta evidencia existe de que un tratamiento dado es el mismo que el tratamiento de base. Una mayor confianza indica menos evidencia para el supuesto de que los tratamientos basales y no basales tienen un rendimiento igual. Más precisamente, la confianza que se muestra es una probabilidad (expresada como porcentaje) de que habríamos observado una diferencia menor en las tasas de conversión entre un tratamiento determinado y la línea de base, si en realidad no hay diferencia en las tasas de conversión subyacentes reales. En términos de valores p, la confianza mostrada es 1 - valor p.

El Adobe utiliza la confianza &quot;válida en cualquier momento&quot; y los valores P &quot;válida en cualquier momento&quot; que son coherentes con las secuencias de confianza descritas anteriormente.

### 4. Relevancia estadística

Al ejecutar experimentos, un resultado se considera estadísticamente significativo si era muy poco probable que se hubiera observado, dada una hipótesis nula de que un tratamiento determinado y la línea de base tienen tasas de conversión/rendimiento subyacentes reales idénticas.

El Adobe declara que un experimento es concluyente cuando la confianza está por encima del 95 %.

## Qué hacer después de ejecutar un experimento

Después de ejecutar el experimento, hay varias acciones de seguimiento posibles:

* **Implementar ideas ganadoras**

   Con un resultado inequívoco, puede implementar esta idea ganadora, ya sea aplicando el tratamiento con mejor rendimiento a todos sus clientes o creando nuevas campañas en las que se duplique la estructura del tratamiento con mejor rendimiento.
   </br>Tenga en cuenta que en un entorno dinámico, lo que funciona bien en un momento dado, puede no funcionar bien más adelante.

* **Ejecutar pruebas de seguimiento**

   A veces, los resultados de sus experimentos pueden ser inconclusos, ya sea porque no había suficientes perfiles incluidos para detectar cualquier diferencia en los tratamientos, o porque los tratamientos que definió no eran suficientemente diferentes.

   Si la hipótesis que estaba probando sigue siendo relevante, ejecutar una prueba de seguimiento en una audiencia mayor o diferente, o modificar los tratamientos para que haya diferencias más claras puede ser la mejor acción de seguimiento.

* **Realizar análisis en profundidad**

   El tratamiento que funciona bien para una audiencia a veces puede no ser el mejor tratamiento para otra audiencia. Realizar análisis más profundos sobre cómo se comportaron los tratamientos para diferentes segmentos ayuda a generar ideas para nuevas pruebas.

   Del mismo modo, estudiar el rendimiento de cada tratamiento con diferentes métricas también puede proporcionar una vista más completa de sus Experimentos.

   >[!CAUTION]
   >
   >Un mayor número de análisis implica una mayor probabilidad de detectar un efecto falso o un falso positivo.
