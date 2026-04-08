---
solution: Journey Optimizer
product: Journey Optimizer
title: Supervisión del modelo de IA
description: Monitorice el estado, el estado y el rendimiento del modelo de clasificación de IA para modelos de optimización personalizados
feature: Ranking, Decisioning
topic: Artificial Intelligence
role: User
level: Intermediate
version: Journey Orchestration
exl-id: 90e71c42-94f3-4cc5-bd6e-1df29def4d39
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 2%

---

# Monitorización de los modelos de IA {#ai-model-observability}

Tanto si es un experto en marketing, un científico de datos o un administrador de decisiones, comprender cómo funcionan y se comportan los modelos de optimización personalizados le ayuda a seleccionar las mejores ofertas para cada cliente mediante IA.

Para ello, puede supervisar el estado, el estado de formación y la evolución de sus modelos de IA directamente en [!DNL Journey Optimizer].

Esto le proporciona una visión clara de si el modelo funciona, cuándo se entrenó por última vez, qué sucedió durante la formación, cómo está impulsando el resultado de su negocio (por ejemplo, conversiones o ingresos) y cómo solucionar problemas cuando no funciona<!-- (for example, unexpected decision item count, training data date range, or insufficient events)-->.

>[!AVAILABILITY]
>
>Actualmente, esta funcionalidad solo es compatible con [modelos de optimización personalizada](personalized-optimization-model.md).

➡️ [Descubra esta funcionalidad en vídeo](#video)

## Ver el estado de la formación {#from-ai-model-list}

Una vez que un modelo está configurado para funcionar, entra en un ciclo de vida continuo: los datos se recopilan y el modelo se vuelve a entrenar periódicamente para optimizar la clasificación de las ofertas. Puede comprobar el estado de formación de los modelos de optimización personalizados en la lista de modelos de IA.

1. Vaya a **[!UICONTROL Decisiones]** > **[!UICONTROL Configuración de estrategia]** > **[!UICONTROL modelos de IA]** para abrir el inventario de modelos de IA.

1. Puede ver todos los modelos de IA disponibles y su estado.

1. Para cada modelo de IA **[!UICONTROL Live]** del tipo de optimización personalizado, dos columnas le permiten ver:
   * cuando se ejecutó el último trabajo de formación (**[!UICONTROL Último entrenamiento]**), y
   * si cada modelo se ha entrenado correctamente o no (**[!UICONTROL Resultado de la formación]**).

   ![](../assets/ai-model-list-training.png)

   Esto le permite identificar rápidamente los modelos que necesitan más investigación o solución de problemas.

## Acceso a un informe de estado de modelo {#access-ai-model-details}

Haga clic en un modelo de IA de optimización personalizado de la lista. Desde aquí puede ver los elementos que se enumeran a continuación:

* **[!UICONTROL Modelo implementado actualmente]**: esta sección muestra el modelo implementado actualmente, cuándo se implementó, qué intervalo de fechas de datos utiliza, cuántos elementos de decisión (ofertas) se incluyen y personalizan y la asignación de tráfico actual entre submodelos<!-- (random exploration, new offer booster?, contextual bandit, neural network)-->.

  ![](../assets/ai-model-deployed-model.png)

  En este ejemplo, el modelo se entrenó en cinco elementos de decisión y tiene tráfico suficiente para desarrollar predicciones personalizadas para tres de los elementos de decisión. Los dos elementos de decisión restantes se proporcionan de forma aleatoria.

  También se puede ver que el modelo está asignando actualmente el 40% del tráfico a la red neuronal personalizada, el 40% del tráfico al bandido contextual y el 20% del tráfico a la exploración aleatoria.

* **[!UICONTROL Último trabajo de formación]**: en esta sección se muestra el estado del último trabajo de formación, cuándo se ejecutó y los mensajes de error. [Más información sobre los estados de error](#check-for-error-states)

  ![](../assets/ai-model-last-training-job.png)

  En este ejemplo, se puede observar que el modelo implementado coincide con el trabajo de formación según lo esperado.

* **[!UICONTROL Propiedades]**: en esta sección se muestran las propiedades del modelo, como el conjunto de datos utilizado, la métrica de optimización y las audiencias utilizadas para entrenar el modelo de optimización personalizado.

  ![](../assets/ai-model-properties.png)

  Haga clic en **[!UICONTROL Editar propiedades]** para modificar estos elementos. Se le redirigirá a la pantalla Crear modelo de IA. [Más información](create-ai-models.md)

* **[!DNL Model performance]**: esta sección muestra el rendimiento de cada rama del modelo a lo largo del tiempo, como la asignación de tráfico y la tasa de conversión de cada submodelo. Puede alternar entre los **últimos 7 días** y los **últimos 30 días**. El alza y la relevancia estadística son los indicadores clave de si el modelo está mejorando realmente el resultado de marketing.

  ![](../assets/ai-model-performance.png)

  En este ejemplo, puede ver que en los últimos 30 días, los submodelos personalizados han proporcionado más de un 60 % de aumento en la tasa de conversión y este aumento es estadísticamente significativo, lo que significa que este modelo de IA está generando un impacto para su negocio.

* **[!UICONTROL Asignación de tráfico de modelo con el paso del tiempo]**: esta sección muestra cómo ha evolucionado el modelo con el paso del tiempo. Cuando se implementa un modelo por primera vez, el 100 % del tráfico es aleatorio porque aún no se han recopilado datos de ofertas. Después del primer reentrenamiento, el tráfico generalmente se desplaza hacia los brazos personalizados.

  ![](../assets/ai-model-trafic-allocation.png)

  En este ejemplo, se puede ver que la asignación del tráfico ha cambiado de la exploración aleatoria al 100 % al tráfico de red neuronal y de bandido contextual, ya que el modelo se ha vuelto a entrenar con el paso del tiempo.

## Comprender los errores de formación {#check-for-error-states}

Para ver los detalles de error de un modelo de IA de optimización personalizado cuyo último trabajo de formación ha fallado, siga los pasos a continuación.

1. Haga clic en el modelo en la lista. Se muestran los detalles del estado del modelo.

   ![](../assets/ai-model-no-model-deployed.png){width="95%"}

   En este ejemplo, puede ver que no se ha implementado ningún modelo porque se produjo un error en el último trabajo de formación.

   >[!NOTE]
   >
   >Cuando no se implementa ningún modelo, las solicitudes de decisión se atienden mediante una asignación de tráfico aleatorio uniforme.

1. Examine los detalles del error en la sección **[!UICONTROL Último trabajo de formación]**.

   ![](../assets/ai-model-training-job-failed.png){width="70%"}

   Un trabajo de formación suele fallar cuando no hay eventos de comentarios en el conjunto de datos seleccionado para este modelo. Significa que debe rellenar el conjunto de datos o seleccionar uno nuevo con los eventos de conversión adecuados.

1. Puede comprobar qué conjunto de datos está seleccionado en las **[!UICONTROL propiedades]** del modelo. Haga clic en **[!UICONTROL Editar propiedades]** para seleccionar otro conjunto de datos. [Más información](create-ai-models.md)

   ![](../assets/ai-model-properties-edit-dataset.png){align="left" width="45%"}

## Preguntas frecuentes {#faq}

+++ ¿Qué modelos de IA puedo monitorizar?

Actualmente, la monitorización del modelo de IA solo es compatible con [modelos de optimización personalizados](personalized-optimization-model.md). Otros tipos de modelos de clasificación aún no exponen el informe de estado del modelo.
+++

+++ ¿Por qué ha fallado el trabajo de formación de mi modelo?

Los trabajos de formación suelen fallar cuando el conjunto de datos seleccionado para el modelo no tiene eventos de comentarios (conversión) o tiene muy pocos. Consulte la sección **[!UICONTROL Último trabajo de formación]** para ver los detalles del error y, a continuación, revise las **[!UICONTROL propiedades]** del modelo para confirmar el conjunto de datos y la métrica de optimización. Rellene el conjunto de datos con los eventos adecuados o [seleccione un conjunto de datos diferente](create-ai-models.md) con los datos de conversión adecuados.
+++

+++ ¿Cómo se relaciona la monitorización del modelo de IA con los informes de campaña y recorrido?

La monitorización del modelo de IA difiere de la creación de informes de campaña o recorrido. Un solo modelo de IA se puede utilizar en varias campañas o varios recorridos, y los informes de campaña o recorrido no muestran qué modelo se utilizó para una entrega determinada. Utilice la monitorización del estado del modelo de IA para comprender y monitorizar el modelo en sí; use [informes de campaña](../../reports/campaign-global-report-cja.md) e [informes de recorrido](../../reports/journey-global-report-cja.md) para métricas de nivel de entrega.
+++

+++ Mi métrica de optimización es una métrica continua como ingresos o valor de pedido, no una métrica binaria como clics o conversiones. ¿Cómo interpreto los valores de Conversiones y Tasa de conversión notificados?

Cuando se utiliza una métrica continua como ingresos o valor de pedido, el modelo intenta predecir el valor estimado asociado con la presentación de una oferta determinada (no la probabilidad de conversión). El valor &quot;Conversiones&quot; notificado es el ingreso total (o el valor del pedido) asociado con las visualizaciones de ofertas registradas para cada brazo del modelo. La &quot;Tasa de conversión&quot; registrada es el valor de Conversiones dividido por el valor de Pantallas y puede superar el 100 % en el caso de una métrica continua.
+++

+++ ¿Qué es la relevancia del alza?

La relevancia del alza es la relevancia estadística del alza notificada frente a la exploración aleatoria. La significancia se calcula usando una prueba de chi cuadrado de diferencias de proporción, que proporciona un resultado idéntico al cálculo de significancia de una prueba Z para dos proporciones de población.
+++

+++ ¿Cuál es el modelo del índice Gini? ¿Cuál es un valor &quot;bueno&quot; del índice Gini?

El índice de Gini del modelo (también conocido como coeficiente de Gini) es una medida sin conexión del poder predictivo de un modelo. El índice Gini del modelo varía de 0 (sin poder predictivo) a 1 (predice perfectamente la conversión o el valor de métrica de cada oferta para cada cliente). No hay un valor de índice de Gini &quot;bueno&quot; universal, ya que los diferentes casos de uso de decisiones resultan en un comportamiento diferente del usuario y, por lo tanto, en resultados de modelos diferentes. Dentro del mismo caso de uso, los valores más altos del índice de Gini indican un modelo de mayor calidad.
+++

+++ ¿Cómo se calcula el índice de Gini?

El índice Gini de cada grupo de modelos se calcula de forma diferente en función de si la métrica de optimización es binaria o continua:

**Métrica de optimización binaria** (por ejemplo, clics, pedidos): El índice Gini se calcula en función del área bajo la curva (AUC) de la curva de característica de funcionamiento del receptor (ROC), normalmente denominada AUC de ROC o simplemente AUC para abreviar. El AUC de ROC varía de 0,5 (modelo aleatorio con cero poder predictivo) a 1,0 (poder predictivo perfecto). El AUC de ROC se convierte en un índice de Gini usando la fórmula Gini = 2 x (ROC AUC) - 1.

**Métrica de optimización continua** (por ejemplo: ingresos, valor de pedido): El índice Gini se calcula en función del área bajo la curva de Lorenz asociada a los positivos predichos acumulados del modelo frente a los positivos verdaderos acumulados en la población. El área bajo la curva de Lorenz varía de 0,0 (potencia predictiva perfecta) a 0,5 (modelo aleatorio con potencia predictiva cero). El AUC de Lorenz se convierte en un índice de Gini usando la fórmula Gini = 1 - 2 x (AUC de Lorenz).
+++

+++ ¿Cuál es una mejor medida de la calidad del modelo: índice de Gini o relevancia de Alza/Alza?

Normalmente, las medidas en línea de la calidad del modelo, como la relevancia del alza y el alza, se consideran el método &quot;estándar de oro&quot; para medir la calidad del modelo. Los índices Gini proporcionan un punto de datos adicional para los equipos de ciencia de datos de clientes que evalúan modelos de toma de decisiones.
+++

<!--
## Understanding statuses and errors {#statuses-errors}

* **Success** – The latest training job completed successfully. The model is trained and deployed for ranking.
* **Failed** – The latest training job failed (for example, no events in the datasets). The UI shows an error message and a request ID; use these when troubleshooting or contacting support.
* **In progress** – A training job is running. Some metrics may be temporarily unavailable until it finishes.
* **Pending** – No result yet (for example, model recently activated or settings recently changed).

If no model has been successfully deployed yet, the "currently deployed model" section and some performance fields will be empty or show the initial-state messaging.
-->

## Vídeo práctico {#video}

Aprenda a monitorizar los modelos de clasificación de IA e interpretar el estado y el rendimiento de la formación en [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3479852?captions=spa&quality=12)

## Documentación relacionada {#related}

* [Acerca de los modelos de IA](ai-models.md)
* [Modelo de optimización personalizado](personalized-optimization-model.md)
* [Creación de modelos de IA](create-ai-models.md)
* [Crear un conjunto de datos para recopilar eventos](../data-collection/create-dataset.md)
