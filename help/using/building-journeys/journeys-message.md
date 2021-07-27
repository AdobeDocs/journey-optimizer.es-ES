---
title: Adición de un mensaje en un recorrido
description: Adición de un mensaje en un recorrido
feature: Recorridos
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: 7937c3b7c9247868a7a506991850537493a76cf1
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 12%

---

# Adición de un mensaje en un recorrido

[!DNL Journey Optimizer] las funciones de mensajes están integradas, solo tiene que diseñar el contenido y publicar el mensaje. Consulte [esta sección](../get-started-content.md). A continuación, simplemente agregue, en su recorrido, un mensaje push o de correo electrónico diseñado con Journey Optimizer.

Si utiliza un sistema de terceros para enviar mensajes, puede crear una acción personalizada. Obtenga más información en esta [sección](../action/action.md).

## Añadir una actividad Message

1. Como siempre, inicie su recorrido con un evento o una actividad **Leer segmento**.

   ![](../assets/jo-message0.png)

1. En la sección **Actions** de la paleta, arrastre y suelte una actividad **Message** en el lienzo.

   ![](../assets/jo-message1.png)

1. Añada una etiqueta y una descripción.

   ![](../assets/jo-message2.png)

1. Haga clic dentro del campo **Message**. Se muestra la lista de mensajes disponibles diseñados en Journey Optimizer. Puede filtrar la lista por estado.

   ![](../assets/jo-message3.png)

1. Elija un mensaje y haga clic en **Select**. También puede crear un nuevo mensaje directamente desde esta pantalla haciendo clic en **Create message**.

   ![](../assets/jo-message4-ter.png)

   Si desea comprobar el mensaje, puede hacer clic en el icono **Open the message** en el campo **Message**. El mensaje se abre en una pestaña nueva.

   ![](../assets/jo-message4-bis.png)

1. Añada los siguientes pasos a su recorrido.

## Parámetros de correo electrónico y parámetros push

Las secciones **[!UICONTROL Email parameters]** y **[!UICONTROL Push parameters]** muestran campos de solo lectura. Normalmente, se realiza esta configuración al crear el mensaje. Consulte [esta sección](../get-started-content.md).

![](../assets/jo-message4.png)

Para forzar un valor específico, puede utilizar el icono **Enable parameter override** a la derecha del campo. Esta opción puede resultar útil para realizar pruebas. Por ejemplo, para un correo electrónico, puede añadir su dirección de correo electrónico. Después de publicar el recorrido, se le enviará el correo electrónico.
