---
title: Añadir mensajes en campañas
description: Aprenda a añadir mensajes en una campaña
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 87f9a4661b64cf24a8cd62bb9c70d5f1c9fcaddf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 80%

---


# Añadir mensajes en campañas{#messages-in- campaigns}

En sus campañas, seleccione el canal para diseñar y personalizar el mensaje que desea enviar a su audiencia. Al añadir un correo electrónico, un SMS o una notificación push a la campaña, puede enviarlo inmediatamente o programar el mensaje.

>[!NOTE]
>También puede crear recorridos para enviar mensajes activados. Obtenga más información [en esta sección](messages-in-journeys.md).

Obtenga información sobre cómo añadir y configurar mensajes en una campaña [en esta sección](../campaigns/create-campaign.md)

Conozca los pasos detallados para crear el contenido del mensaje en la siguiente página:

* [Crear un correo electrónico](create-email.md)
* [Crear notificaciones push](create-push.md)
* [Creación de un mensaje SMS](create-sms.md)

## Habilitación de la optimización del tiempo de envío{#sto-in-journeys}

Para las notificaciones push y de correo electrónico, puede activar la **[!UICONTROL Send-time optimization]**.

Use la **[!UICONTROL Send-time optimization]** para programar tiempos de envío personalizados para cada usuario y, así, aumentar las tasas de apertura y de clics de sus mensajes. [Más información](../messages/send-time-optimization.md).

## Parámetros avanzados{#adv-settings}

Los parámetros avanzados son de solo lectura y están ocultos de forma predeterminada.

Para acceder a los parámetros avanzados, haga clic en el icono **[!UICONTROL Show read-only fields]** en la parte superior del panel de mensajes.

![](assets/show-read-only.png)

Los parámetros avanzados se muestran en la parte inferior del panel de mensajes. Estos parámetros los define el [administrador del sistema](../start/path/administrator.md) en la [superficie del canal](../configuration/channel-surfaces.md) (es decir, el ajuste preestablecido de mensaje) asociado al mensaje.

Para las notificaciones push, puede mostrar los siguientes parámetros: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Para el correo electrónico, puede mostrar la dirección de correo electrónico principal.

Para un uso específico, puede anular estos valores en contextos concretos. Para forzar un valor, haga clic en el icono **Habilitar la sustitución de parámetros** a la derecha del campo. Esta opción puede resultar útil, por ejemplo, para lo siguiente:

* Pruebe un correo electrónico, puede añadir su dirección de correo electrónico. Después de publicar el recorrido, se le enviará el correo electrónico.
* Consulte la dirección de correo electrónico de los suscriptores de una lista. Obtenga más información en [este caso de uso](../building-journeys/message-to-subscribers-uc.md).

Haga clic en el mismo icono para ocultar la configuración avanzada.

## Examen de mensajes{#browse-message}

Cuando se utilizan varios mensajes en un recorrido, puede cambiar de uno a otro desde la pantalla **Editar contenido**.

![](assets/inline-messages-multi-content.png)

Entonces, puede [comprobar las alertas](alerts.md) y [simular](../design/preview.md) cada contenido en una sola vista.

## Duplicar un mensaje {#duplicate-message}

Puede copiar un mensaje existente del lienzo de recorrido.

Para ello, siga los pasos a continuación:

1. Seleccione el mensaje que desea copiar.

1. Utilice el botón **[!UICONTROL Copy]** del panel **[!UICONTROL Action]**.

   ![](assets/message-duplicate.png)

1. Presione **ctrl+V** para pegar el mensaje.

   El mensaje se añade a los lienzos de recorrido. Todos los ajustes y configuraciones se copiarán en el nuevo mensaje.

   ![](assets/message-duplicated.png)

1. Cambie el nombre del mensaje para poder diferenciar el mensaje inicial de la copia, por ejemplo, al editar mensajes, como se muestra a continuación:

   ![](assets/multi-message.png)


>[!NOTE]
>
>En el caso de los correos electrónicos, también puede convertir un mensaje existente en una plantilla. [Más información](../design/email-templates.md).

## Eliminación de un mensaje{#delete-message}

Para eliminar un mensaje, utilice el icono de papelera en la parte superior del panel de actividad de acción del canal.

![](assets/delete-message.png)

Utilice el botón **[!UICONTROL Confirm]** para validarlo.
