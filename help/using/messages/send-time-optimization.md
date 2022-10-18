---
solution: Journey Optimizer
product: journey optimizer
title: Optimización del tiempo de envío
description: Aprenda a configurar la optimización del tiempo de envío en los mensajes
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 1%

---

## Optimización del tiempo de envío{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Acerca de la optimización del tiempo de envío"
>abstract="La función de optimización del tiempo de envío de Adobe Journey Optimizer, con tecnología de los servicios de IA de Adobe, puede predecir el mejor momento para enviar un mensaje push o de correo electrónico para maximizar la participación en función de las tasas de apertura y clics históricas."

La función de optimización del tiempo de envío de Adobe Journey Optimizer, con tecnología de los servicios de IA de Adobe, puede predecir el mejor momento para enviar un mensaje push o de correo electrónico para maximizar la participación en función de las tasas de apertura y clics históricas. Utilice nuestro modelo de aprendizaje automático para programar tiempos de envío personalizados para que cada usuario aumente las tasas de apertura y clics de sus mensajes.

El modelo de optimización del tiempo de envío incorpora los datos de Adobe Journey Optimizer y observa las tasas de apertura a nivel de usuario (para correo electrónico y push) y de clics (para correo electrónico) para determinar cuándo es más probable que sus clientes interactúen con sus mensajes. La optimización del tiempo de envío requiere un mínimo de un mes de datos de seguimiento de mensajes para realizar recomendaciones informadas. Para cada usuario, el sistema selecciona automáticamente el mejor momento utilizando las siguientes puntuaciones:

* La mejor hora de cada día de la semana para maximizar la participación
* El mejor día de la semana para maximizar la participación
* La mejor hora del mejor día de la semana para maximizar la participación

El modelo varía si se habla de puntuación o de entrenamiento. La formación se imparte semanalmente y posteriormente trimestralmente. La puntuación es semanal inicialmente y, a continuación, mensual.

* Formación: el desarrollo del algoritmo utilizado para obtener la puntuación.
* Puntuación: la aplicación de una puntuación a perfiles individuales en función del modelo entrenado

Esta información se almacena con el perfil del usuario y se hace referencia a ella en la ejecución del recorrido para indicar a Adobe Journey Optimizer cuándo enviar el mensaje.

>[!CAUTION]
>
>Esta función no es compatible con el modo de ráfaga.

### Activación de la optimización del tiempo de envío{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Activación de la optimización del tiempo de envío"
>abstract="Seleccione si desea optimizar las aperturas de correo electrónico o las pulsaciones de correo electrónico seleccionando el botón de radio adecuado. También puede optar por cortejar los tiempos de envío utilizados por el sistema introduciendo un valor para la opción Send in the next ."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Activación de la optimización del tiempo de envío"
>abstract="Los mensajes push toman el valor predeterminado de la opción de aperturas, ya que los clics no son aplicables a la mensajería push. También puede optar por cortejar los tiempos de envío utilizados por el sistema introduciendo un valor para la opción Send in the next ."

Habilite la optimización del tiempo de envío en un mensaje push o de correo electrónico seleccionando la opción **Optimización del tiempo de envío** desde los parámetros de actividad.

![](../building-journeys/assets/jo-message5.png)

En el caso de los mensajes de correo electrónico, seleccione si desea optimizar las aperturas de correo electrónico o las pulsaciones de correo electrónico seleccionando el botón de opción adecuado. Los mensajes push toman el valor predeterminado de la opción de aperturas, ya que los clics no son aplicables a la mensajería push.

También puede optar por cortejar los tiempos de envío utilizados por el sistema introduciendo un valor para la variable **Envíe dentro del siguiente** . Si elige &quot;seis horas&quot; como valor, [!DNL Journey Optimizer] comprobará cada perfil de usuario y elegirá el tiempo de envío óptimo dentro de las seis horas siguientes al tiempo de ejecución del recorrido.
