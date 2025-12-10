---
solution: Journey Optimizer
product: Journey Optimizer
title: Modelo de optimización personalizado
description: Más información sobre los modelos de optimización personalizados
feature: Ranking, Decisioning
role: User
level: Experienced
exl-id: 1c7bcffe-5a25-444f-8a95-057b7a07f252
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 5%

---

# Modelo de optimización personalizado {#personalized-optimization-model}

## Información general {#overview}

Al aprovechar las tecnologías de vanguardia en cuanto a aprendizaje automático supervisado y aprendizaje profundo, la optimización personalizada permite a un usuario empresarial (experto en marketing) definir objetivos comerciales y utiliza los datos de sus clientes para entrenar modelos orientados a la empresa que proporcionen ofertas personalizadas y maximicen los KPI.

<!--![](../../rn/assets/do-not-localize/ai-ranking.gif)-->

## Requisitos del conjunto de datos

Para entrenar un modelo de optimización personalizado, el conjunto de datos debe cumplir los siguientes requisitos mínimos:

* Al menos 2 ofertas del conjunto de datos deben tener al menos 250 eventos de visualización y 25 eventos de éxito (por ejemplo, clics o conversiones) en los últimos 30 días.
* Las ofertas con menos de 250 visualizaciones o 25 eventos de éxito en los últimos 30 días pueden incluirse en el tráfico personalizado, pero el modelo de personalización trata el rendimiento en el nivel de la oferta con peor puntuación * hasta que superan este umbral.
* Las ofertas con menos de 250 pantallas o 25 eventos de éxito en los últimos 30 días seguirán siendo aptas para su inclusión en el tráfico de exploración.

Hasta la primera vez que se forme un modelo de optimización personalizado, las ofertas dentro de una estrategia de selección que utilice un modelo de optimización personalizado se ofrecerán al azar.

## Suposiciones y limitaciones clave del modelo {#key}

Para maximizar la ventaja de utilizar la optimización personalizada, hay que tener en cuenta algunos supuestos y limitaciones clave.

* **Las ofertas son lo suficientemente diferentes como para que los usuarios tengan preferencias diferentes entre las ofertas consideradas**. Si las ofertas son demasiado similares, un modelo resultante tendrá menos impacto, ya que las respuestas son aparentemente aleatorias.
Por ejemplo, si un banco tiene dos ofertas de tarjetas de crédito y la única diferencia es el color, puede que no importe qué tarjeta se recomiende, pero si cada tarjeta tiene términos diferentes, esto proporciona una justificación de por qué determinados clientes elegirían uno y proporcionaría suficiente diferencia entre ofertas para crear un modelo más impactante.
* **La composición del tráfico del usuario es estable**. Si la composición del tráfico del usuario cambia drásticamente durante el aprendizaje y la predicción del modelo, el rendimiento del modelo podría degradarse. Por ejemplo, supongamos que en la fase de formación del modelo solo están disponibles los datos de los usuarios de la audiencia A, pero el modelo entrenado se utiliza para generar predicciones para los usuarios de la audiencia B y, por lo tanto, el rendimiento del modelo podría verse afectado.
* **El rendimiento de las ofertas no cambia drásticamente en un corto período de tiempo**, ya que este modelo se actualiza semanalmente y los cambios de rendimiento se transmiten como actualizaciones del modelo. Por ejemplo, un producto era muy popular antes, pero un informe público identifica que el producto es perjudicial para nuestra salud, y este producto se vuelve impopular extremadamente rápido. En esta situación, el modelo podría seguir prediciendo este producto hasta que se actualice con cambios en el comportamiento del usuario.

## Cómo funciona {#how}

El modelo aprende interacciones de funciones complejas entre ofertas, información de los usuarios e información contextual para recomendar ofertas personalizadas a los usuarios finales. Las funciones son entradas en el modelo.

Existen tres tipos de funciones:

| Tipos de funciones | Cómo añadir funciones a los modelos |
|--------------|----------------------------|
| Objetos de toma de decisiones (placementID, activityID, decisionScopeID) | Parte de los comentarios de gestión de decisiones Eventos de experiencia enviados a AEP |
| Públicos | Se pueden añadir de 0 a 50 audiencias como funciones al crear el modelo de inteligencia artificial aplicada a la clasificación |
| Datos de contexto | Parte de los comentarios y eventos de experiencia de decisiones enviados a AEP. Datos de contexto disponibles para agregar al esquema: detalles de Commerce, detalles de canal, detalles de aplicación, detalles web, detalles de entorno, detalles de dispositivo, placeContext. |

El modelo tiene dos fases:

* En la fase de **formación de modelos sin conexión**, un modelo se entrena mediante el aprendizaje y la memorización de interacciones de características en datos históricos.
* En la fase de **inferencia en línea**, las ofertas de candidatos se clasifican según las puntuaciones en tiempo real generadas por el modelo. A diferencia de las técnicas de filtrado colaborativas tradicionales, que son difíciles de incluir en funciones para usuarios y ofertas, la optimización personalizada es un método de recomendación basado en el aprendizaje profundo, y es capaz de incluir y aprender patrones de interacción de funciones complejos y no lineales.

A continuación, se muestra un ejemplo simplificado para ilustrar la idea básica detrás de la optimización personalizada. Supongamos que tenemos un conjunto de datos que almacena las interacciones históricas entre usuarios y ofertas, que se muestra en la Figura 1. Existen:

* Dos ofertas, offer_1 y offer_2,
* Dos funciones, feature_1 y feature_2,
* Una columna de respuesta.

El valor de feature_1, feature_2 y response es 0 o 1. Si miramos los cuadros azules y naranjas en la Figura 1, podemos ver que para offer_1, las respuestas tienen más probabilidades de ser 1 cuando feature_1 y feature_2 tienen los mismos valores, mientras que para offer_2, es más probable que las etiquetas sean 1 cuando feature_1 es 0 y feature_2 es 1. También podemos ver que en el cuadro rojo, offer_1 se sirve cuando feature_1 es 0 y feature_2 es 1, y la respuesta es 0. Según el patrón que vemos en los cuadros naranjas, cuando feature_1 es 0 y feature_2 es 1, offer_2 es probablemente una mejor recomendación.

Básicamente, esta es la idea de aprender y memorizar interacciones de características históricas y aplicarlas para generar predicciones personalizadas.

![](../assets/perso-ranking-schema.png)

## Problema de arranque en frío {#cold-start}

El problema de inicio en frío se produce cuando no hay suficientes datos para hacer recomendaciones. Para una optimización personalizada, existen dos tipos de problemas de inicio en frío.

* **Después de crear un nuevo modelo de IA sin datos históricos**, las ofertas se servirán aleatoriamente durante un período de tiempo para recopilar datos y los datos se utilizarán para entrenar el primer modelo.
* **Una vez liberado el primer modelo**, el 10% del tráfico total se asignará a servidores aleatorios, mientras que el 90% del tráfico se utilizará para recomendaciones de modelos. Por lo tanto, si se agregaran nuevas ofertas al modelo de IA, se enviarían como parte del 10 % del tráfico. Los datos recopilados en esas ofertas determinarían la cantidad de veces que se selecciona entre el 90 % del tráfico a medida que el modelo se actualiza.

## Readiestramiento {#re-training}

Los modelos se volverán a entrenar para aprender las últimas interacciones de funciones y mitigar la degradación del rendimiento del modelo semanalmente.
