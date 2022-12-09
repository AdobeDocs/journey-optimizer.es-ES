---
solution: Journey Optimizer
product: journey optimizer
title: Añadir un mensaje en un recorrido
description: Aprenda a añadir un mensaje en un recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# Correo electrónico, SMS, push{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] incorpora capacidades de mensajes. Puede simplemente añadir, en su recorrido, una actividad de push, SMS o mensaje de correo electrónico y definir la configuración y el contenido. A continuación, se ejecuta y envía en el contexto del recorrido.

También puede configurar acciones específicas para enviarle mensajes:

* Si utiliza un sistema de terceros para enviar mensajes, puede crear una acción personalizada. Obtenga más información en esta [sección](../action/action.md).

* Si está trabajando con Campaign y Journey Optimizer, consulte estas secciones:

   * [[!DNL Journey Optimizer] y Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] y Campaign Standard](../action/acs-action.md)

Para añadir un mensaje en un recorrido, siga los pasos a continuación:

1. Inicie el recorrido con un [Evento](general-events.md) o [Leer segmento](read-segment.md) actividad.

1. En el **Acciones** de la paleta, arrastre y suelte una **email**, un **SMS** o **Push** actividad en el lienzo.

1. Configure la actividad . Conozca los pasos detallados para crear el contenido del mensaje en las páginas siguientes:

   <table style="table-layout:fixed">
   <tr style="border: 0;">
   <td>
   <a href="../email/create-email.md">
   <img alt="Posible cliente" src="../assets/do-not-localize/email.jpg">
   </a>
   <div><a href="../email/create-email.md"><strong>Creación de correos electrónicos</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../push/create-push.md">
   <img alt="Poco frecuente" src="../assets/do-not-localize/push.jpg">
   </a>
   <div>
   <a href="../push/create-push.md"><strong>Creación de notificaciones push<strong></a>
   </div>
   <p>
   </td>
   <td>
   <a href="../sms/create-sms.md">
   <img alt="Validación" src="../assets/do-not-localize/sms.jpg">
   </a>
   <div>
   <a href="../sms/create-sms.md"><strong>Creación de mensajes SMS</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## Actualizar contenido en directo{#update-live-content}

Puede actualizar el contenido de un mensaje (correo electrónico, sms, push) en un recorrido en directo.

Para ello, abra el recorrido en directo, seleccione la actividad de mensaje y haga clic en **Editar contenido**.

![](assets/add-a-message2.png)

Sin embargo, no se pueden cambiar los atributos utilizados en la personalización, ya sean atributos de perfil o datos contextuales (desde propiedades de evento o recorrido).

## Optimización del tiempo de envío{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="Acerca de la optimización del tiempo de envío"
>abstract="La función de optimización del tiempo de envío de Adobe Journey Optimizer, con tecnología de los servicios de IA de Adobe, puede predecir el mejor momento para enviar un mensaje push o de correo electrónico para maximizar la participación en función de las tasas históricas de apertura y clics."

### Acerca de la optimización del tiempo de envío {#about-send-time}

La función de optimización del tiempo de envío de Adobe Journey Optimizer, con tecnología de los servicios de IA de Adobe, puede predecir el mejor momento para enviar un mensaje push o de correo electrónico para maximizar la participación en función de las tasas históricas de apertura y clics. Utilice nuestro modelo de aprendizaje automático para programar tiempos de envío personalizados para que cada usuario aumente las tasas de apertura y clics de sus mensajes.

El modelo de optimización del tiempo de envío incorpora los datos de Adobe Journey Optimizer y observa las tasas de apertura a nivel de usuario (para correo electrónico y push) y de clics (para correo electrónico) para determinar cuándo es más probable que los clientes interactúen con la mensajería. La optimización del tiempo de envío requiere un mínimo de un mes de datos de seguimiento de mensajes para realizar recomendaciones informadas. Para cada usuario, el sistema selecciona automáticamente el mejor momento utilizando las siguientes puntuaciones:

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

También puede optar por cortejar los tiempos de envío utilizados por el sistema introduciendo un valor para la variable **Envíe dentro del siguiente** . Si elige &quot;seis horas&quot; como valor, [!DNL Journey Optimizer] comprobará cada perfil de usuario y elegirá el tiempo de envío óptimo en un plazo de seis horas a partir del tiempo de ejecución del recorrido.
