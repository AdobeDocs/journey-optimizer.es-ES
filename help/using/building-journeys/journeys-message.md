---
title: Añadir un mensaje en un recorrido
description: Añadir un mensaje en un recorrido
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 4%

---

# Añadir un mensaje en un recorrido

![](../assets/do-not-localize/badge.png)

Las funciones de mensajes de Journey Optimizer están integradas, solo tiene que diseñar el contenido y publicar el mensaje. Consulte [esta sección](../get-started-content.md). A continuación, simplemente agregue, en su recorrido, un mensaje push o de correo electrónico diseñado con Journey Optimizer.

Si utiliza un sistema de terceros para enviar mensajes, puede crear una acción personalizada. Obtenga más información en esta [sección](../action/action.md).

## Adición de una actividad de mensaje

1. Como siempre, inicie su recorrido con un evento o una actividad **Read segment**.

   ![](../assets/jo-message0.png)

1. En la sección **Actions** de la paleta, arrastre y suelte una actividad **Message** en el lienzo.

   ![](../assets/jo-message1.png)

1. Añada una etiqueta y una descripción.

   ![](../assets/jo-message2.png)

1. Haga clic dentro del campo **Message**. Se muestra la lista de mensajes disponibles diseñados en Journey Optimizer. Puede filtrar la lista por estado.

   ![](../assets/jo-message3.png)

1. Elija un mensaje y haga clic en **Select**. También puede crear un nuevo mensaje directamente desde esta pantalla haciendo clic en **Create new**.

   ![](../assets/jo-message4-ter.png)

   Si desea comprobar el mensaje, puede hacer clic en el icono **Open the message** en el campo **Message**. El mensaje se abre en una pestaña nueva.

   ![](../assets/jo-message4-bis.png)

1. Añada los siguientes pasos a su recorrido.

## Parámetros de canal

Se muestran los parámetros **Channel**. Estos campos son de solo lectura. Esta configuración se realiza al crear el mensaje. Consulte [esta sección](../get-started-content.md).

![](../assets/jo-message4.png)

Puede utilizar el icono **Enable editing field** en el lado derecho del campo para forzar un valor específico. Esto puede resultar útil para realizar pruebas. Por ejemplo, para un correo electrónico, puede añadir su dirección de correo electrónico. Al publicar el recorrido, se le enviará el correo electrónico.
