---
solution: Journey Optimizer
product: journey optimizer
title: Optimización del tiempo de envío
description: Obtenga información sobre cómo parametrizar la optimización del tiempo de envío en los mensajes
feature: Journeys, Activities, Email, Push, Send Time Optimization
topic: Content Management
role: User
level: Intermediate
keywords: tiempo de envío, envío, mensaje, optimización, recorrido, IA, inteligente
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 26%

---

# Optimización del tiempo de envío{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Acerca de la optimización del tiempo de envío"
>abstract="La función de optimización del tiempo de envío de Adobe Journey Optimizer, con tecnología de los servicios de IA de Adobe, puede predecir el mejor momento para enviar un mensaje push o de correo electrónico para maximizar la participación en función de las tasas históricas de apertura y clics."

La función de optimización del tiempo de envío de Adobe Journey Optimizer, con tecnología de los servicios de IA de Adobe, puede predecir el mejor momento para enviar un mensaje push o de correo electrónico para maximizar la participación en función de la apertura histórica y las tasas de clics. Utilice nuestro modelo de aprendizaje automático para programar tiempos de envío personalizados para cada usuario y, así, aumentar las tasas de apertura y de clics de sus mensajes.

El modelo de optimización del tiempo de envío ingiere los datos de Adobe Journey Optimizer y observa las tasas de apertura a nivel de usuario (para correo electrónico y push) y clics (para correo electrónico) para determinar cuándo es más probable que los clientes interactúen con los mensajes. La optimización del tiempo de envío requiere un mínimo de un mes de datos de seguimiento de mensajes para hacer recomendaciones informadas. Para cada usuario, el sistema seleccionará automáticamente el mejor momento con las siguientes puntuaciones:

* La mejor hora de cada día de la semana para maximizar la participación
* El mejor día de la semana para maximizar la participación
* La mejor hora del mejor día de la semana para maximizar la participación

El modelo varía si se habla de puntuación o de formación. La capacitación se imparte semanalmente inicialmente y luego trimestralmente. La puntuación inicial es semanal y, a continuación, mensual.

* Formación: el desarrollo del algoritmo utilizado para obtener la puntuación
* Puntuación: la aplicación de una puntuación a perfiles individuales en función del modelo entrenado

Esta información se almacena con el perfil del usuario y se hace referencia a ella en la ejecución del recorrido para indicar a Adobe Journey Optimizer cuándo enviar el mensaje.

## Activación de la optimización del tiempo de envío{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="Activación de la optimización del tiempo de envío"
>abstract="Elija si desea optimizar las aperturas de correo electrónico o los clics de correo electrónico seleccionando el botón de radio adecuado. También puede optar por poner entre paréntesis los tiempos de envío utilizados por el sistema introduciendo un valor para la opción Enviar dentro de los próximos."

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="Activación de la optimización del tiempo de envío"
>abstract="Los mensajes push tienen por defecto la opción de apertura, ya que los clics no se aplican a la mensajería push. También puede optar por poner entre paréntesis los tiempos de envío utilizados por el sistema introduciendo un valor para la opción Enviar dentro de los próximos."

Habilite la optimización del tiempo de envío en un mensaje push o de correo electrónico seleccionando la variable **Optimización del tiempo de envío** cambie de los parámetros de actividad.

![](../building-journeys/assets/jo-message5.png)

Para los mensajes de correo electrónico, seleccione si desea optimizar las aperturas de correo electrónico o las pulsaciones de correo electrónico seleccionando el botón de opción adecuado. Los mensajes push usan de forma predeterminada la opción de aperturas, ya que los clics no son aplicables a los mensajes push.

También puede elegir entre corchetes los tiempos de envío utilizados por el sistema introduciendo un valor para **Enviar en el siguiente** opción. Si elige &quot;seis horas&quot; como valor, [!DNL Journey Optimizer] comprobará cada perfil de usuario y elegirá el tiempo de envío óptimo en un plazo de seis horas desde el momento en que se ejecuta el recorrido.
