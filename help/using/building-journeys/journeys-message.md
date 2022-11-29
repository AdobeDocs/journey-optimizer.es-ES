---
solution: Journey Optimizer
product: journey optimizer
title: Adición de un mensaje en un recorrido
description: Aprenda a añadir un mensaje en un recorrido
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 20%

---

# Correo electrónico, SMS, push{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] incorpora capacidades de mensajes. Puede simplemente añadir, en su recorrido, una actividad de push, un SMS o un mensaje de correo electrónico y [definir configuración y contenido](../messages/messages-in-journeys.md). A continuación, se ejecuta y envía en el contexto del recorrido.

También puede configurar acciones específicas para enviarle mensajes:

* Si utiliza un sistema de terceros para enviar mensajes, puede crear una acción personalizada. Obtenga más información en esta [sección](../action/action.md).

* Si está trabajando con Campaign y Journey Optimizer, consulte estas secciones:

   * [[!DNL Journey Optimizer] y Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] y Campaign Standard](../action/acs-action.md)

Para añadir un mensaje en un recorrido, siga los pasos a continuación:

1. Inicie el recorrido con un [Evento](general-events.md) o una actividad [Leer segmento](read-segment.md).

1. En la sección **Acciones** de la paleta, arrastre y suelte una actividad de **correo electrónico**, **SMS** o **push** en el lienzo.

   ![](../messages/assets/add-a-message.png)


   Todos los pasos para configurar el mensaje y definir su contenido se detallan en [esta sección](../messages/get-started-content.md).

## Actualizar contenido en directo{#update-live-content}

Puede actualizar el contenido de un mensaje (correo electrónico, sms, push) en un recorrido activo.

Para ello, abra el recorrido activo, seleccione la actividad de mensaje y haga clic en **Editar contenido**.

![](assets/add-a-message2.png)

Sin embargo, no se pueden cambiar los atributos utilizados en la personalización, ya sean atributos de perfil o datos contextuales (a partir de propiedades de evento o recorrido).
