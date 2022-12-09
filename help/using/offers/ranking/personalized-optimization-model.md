---
product: experience platform
solution: Experience Platform
title: Modelo de optimización personalizado
description: Obtenga más información sobre los modelos de optimización personalizados
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: c73b3092-e96d-4957-88e6-500e99542782
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Modelo de optimización personalizado {#personalized-optimization-model}

>[!CAUTION]
>
>Actualmente, el uso de modelos de Optimización personalizada está disponible en el acceso anticipado solo para usuarios seleccionados.

## Información general {#overview}

Al aprovechar las tecnologías más avanzadas en aprendizaje automático supervisado y aprendizaje profundo, la personalización automática permite que un usuario empresarial (especialista en marketing) defina los objetivos del negocio y utilice sus datos de clientes para formar modelos orientados al negocio con el fin de ofrecer ofertas personalizadas y maximizar los KPI.

## Suposiciones y limitaciones del modelo clave {#key}

Para maximizar la ventaja de utilizar la personalización automática, hay que tener en cuenta algunas suposiciones y limitaciones clave.

* **Las ofertas son lo suficientemente diferentes como para que los usuarios tengan diferentes preferencias entre las ofertas en consideración**. Si las ofertas son demasiado similares, un modelo resultante tendrá menos impacto, ya que las respuestas parecen aleatorias.
Por ejemplo, si un banco tiene dos ofertas de tarjetas de crédito con la única diferencia de color, puede que no importe qué tarjeta se recomiende, pero si cada tarjeta tiene términos diferentes, esto justifica por qué determinados clientes elegirían una y proporciona la diferencia suficiente entre ofertas para crear un modelo más impactante.
* **La composición del tráfico del usuario es estable**. Si la composición del tráfico del usuario cambia drásticamente durante la formación y predicción de modelos, el rendimiento del modelo podría degradarse. Por ejemplo, supongamos que en la fase de formación de modelos solo están disponibles los datos para los usuarios del segmento A, pero el modelo entrenado se utiliza para generar predicciones para los usuarios del segmento B, por lo que el rendimiento del modelo podría verse afectado.
* **El rendimiento de las ofertas no cambia drásticamente en un corto período de tiempo** a medida que este modelo se actualiza semanalmente y los cambios en el rendimiento se transmiten como actualizaciones del modelo. Por ejemplo, un producto era muy popular antes, pero un informe público identifica que es dañino para nuestra salud, y este producto se vuelve impopular extremadamente rápido. En este escenario, el modelo podría seguir prediciendo este producto hasta que el modelo se actualice con cambios en el comportamiento del usuario.

## Cómo funciona {#how}

La personalización automática aprende interacciones complejas entre las características de las ofertas, la información de los usuarios y la información contextual para recomendar ofertas personalizadas a los usuarios finales. Las funciones son entradas en el modelo.

Existen tres tipos de funciones:

| Tipos de funciones | Adición de funciones a modelos |
|--------------|----------------------------|
| Decidir objetos (placementID, activityID, decisionScopeID) | Parte de los comentarios de la administración de decisiones Eventos de experiencias enviados a AEP |
| Segmentos | Se pueden añadir de 0 a 50 segmentos como funciones al crear el modelo de IA de clasificación |
| Datos de contexto | Parte de los comentarios de decisión sobre los eventos de experiencia enviados a AEP. Datos de contexto disponibles para agregar al esquema: Detalles de comercio, Detalles de canal, Detalles de aplicación, Detalles de web, Detalles de entorno, Detalles del dispositivo, placeContext |

El modelo tiene dos fases:

* En el **formación del modelo sin conexión** , un modelo se forma aprendiendo y memorizando interacciones de características en datos históricos.
* En el **inferencia en línea** , las ofertas de los candidatos se clasifican en función de puntuaciones en tiempo real generadas por el modelo. A diferencia de las técnicas de filtrado colaborativas tradicionales, que son difíciles de incluir para usuarios y ofertas, la personalización automática es un método de recomendación basado en el aprendizaje profundo, y es capaz de incluir y aprender patrones de interacción de características complejas y no lineales.

A continuación se muestra un ejemplo simplificado para ilustrar la idea básica de la personalización automática. Supongamos que tenemos un conjunto de datos que almacena interacciones históricas entre usuarios y ofertas, que se muestra en la Figura 1. Hay:
* Dos ofertas, offer_1 y offer_2,
* Dos funciones, feature_1 y feature_2,
* Una columna de respuesta.

El valor de feature_1, feature_2 y response es 0 o 1. Cuando miramos los cuadros azules y los cuadros naranjas de la Figura 1, podemos encontrar que para offer_1, las respuestas tienen más probabilidades de ser 1 cuando feature_1 y feature_2 tienen los mismos valores, mientras que para offer_2, las etiquetas tienen más probabilidades de ser 1 cuando feature_1 es 0 y feature_2 es 1. También podemos ver que en el cuadro rojo, offer_1 se suministra cuando feature_1 es 0 y feature_2 es 1, y la respuesta es 0. Basándonos en el patrón que vemos en los cuadros naranja, cuando feature_1 es 0 y feature_2 es 1, offer_2 es probablemente una mejor recomendación.

Básicamente, esta es la idea de aprender y memorizar las interacciones históricas de características y aplicarlas para generar predicciones personalizadas.

![](../assets/perso-ranking-schema.png)

## Problema de arranque en frío {#cold-start}

El problema del arranque en frío se produce cuando no hay datos suficientes para hacer recomendaciones. Para la personalización automática, existen dos tipos de problemas de arranque en frío.

* **Después de crear una nueva estrategia de clasificación sin datos históricos**, las ofertas se servirán aleatoriamente durante un periodo de tiempo para recopilar datos y los datos se utilizarán para entrenar el primer modelo.
* A **Después de lanzar el primer modelo**, el 10 % del tráfico total se asignará a la entrega aleatoria, mientras que el 90 % del tráfico se utilizará para recomendaciones de modelos. Por lo tanto, si se añaden nuevas ofertas a la estrategia de clasificación, se entregarán como parte del 10 % del tráfico. Los datos recopilados en esas ofertas determinarían el número de veces que se selecciona entre el 90 % del tráfico a medida que el modelo se actualiza.

## Nuevo entrenamiento {#re-training}

Los modelos se volverán a capacitar para aprender las interacciones más recientes entre las funciones y mitigar la degradación semanal del rendimiento del modelo.
