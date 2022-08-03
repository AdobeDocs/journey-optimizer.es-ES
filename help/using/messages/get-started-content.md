---
title: Introducción a los mensajes
description: Obtenga información sobre cómo crear y enviar mensajes personalizados en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 8%

---

# Introducción a los mensajes {#get-started-messages}

>[!CONTEXTUALHELP]
>id="ajo_journey_message"
>title="Acciones de canal"
>abstract="Utilice acciones del canal para enviar un mensaje push, SMS o de correo electrónico."

Uso [!DNL Journey Optimizer] para crear y enviar notificaciones push personalizadas, SMS y mensajes de correo electrónico. Todos los mensajes se pueden editar en línea como parte de una acción en el lienzo del Recorrido.  Utilice la función Guardar como plantilla para reutilizar el contenido fácilmente. Puede:

* Uso [!DNL Journey Optimizer] **capacidades de diseño de correo electrónico** para crear o importar correos electrónicos interactivos.

* Aprovechar **Adobe Experience Manager Assets Essentials** para enriquecer los correos electrónicos, cree y administre su propia base de datos de recursos.

* Buscar **Fotos de Adobe Stock** para crear su contenido y mejorar su diseño de correo electrónico.

* Mejorar la experiencia de los clientes creando **notificaciones push, SMS y correos electrónicos** en función de sus atributos de perfil.

* **Envío de envíos** en función de estos contenidos y realice un seguimiento del comportamiento de los clientes.

>[!NOTE]
>
>Los usuarios pueden acceder, crear, editar o publicar recorridos en función de su perfil de producto. Obtenga más información sobre los permisos de usuario [en esta sección](../administration/permissions.md).


## Añadir mensajes en los recorridos{#messages-in-journeys}

>[!CONTEXTUALHELP]
>id="ajo_message_category"
>title="Categoría del mensaje"
>abstract="Seleccione Marketing para mensajes comerciales o Transaccional para mensajes no comerciales, como confirmación de pedido, notificaciones de restablecimiento de contraseña o información de envío"

>[!CONTEXTUALHELP]
>id="ajo_message_surface"
>title="Superficie de canal"
>abstract="Una superficie de canal es una instancia de ese canal que tiene toda la configuración para enviar una acción correctamente a través de una campaña o un recorrido. Se define mediante un administrador del sistema."

Para añadir mensajes en los recorridos, simplemente añada una actividad push, SMS o de correo electrónico en los lienzos de recorrido.

1. Inicie el recorrido con un [Evento](../building-journeys/general-events.md) o [Leer segmento](../building-journeys/read-segment.md) actividad.

1. En el **Acciones** de la paleta, arrastre y suelte una **email**, un **SMS** o **Push** actividad en el lienzo.

   ![](assets/add-a-message.png)

1. Introduzca una etiqueta y una descripción.

1. Seleccione el mensaje **[!UICONTROL Category]**: elija **Marketing** para mensajes comerciales, o **Transaccional** para mensajes no comerciales como confirmación de pedido, notificaciones de restablecimiento de contraseña o información de entrega.

   >[!CAUTION]
   >
   >Si ha definido [reglas de frecuencia](../configuration/frequency-rules.md) para un canal y categoría específicos, se aplican automáticamente al mensaje al seleccionar ese canal y categoría. Actualmente solo el **[!UICONTROL Marketing]** está disponible para reglas de frecuencia.

   ![](assets/inline-message-category.png)

   >[!CAUTION]
   >
   >Los mensajes de tipo de marketing deben incluir un [vínculo de no participación](../messages/consent.md#opt-out-management). Esto no es necesario para los mensajes transaccionales, ya que estos mensajes se pueden enviar a perfiles que cancelaron la suscripción a comunicaciones de marketing.

1. Seleccione el canal **[!UICONTROL Surface]** (es decir, el ajuste preestablecido de mensaje) que se utiliza para enviar el mensaje.

   Una superficie es una configuración que se ha definido mediante una [Administrador del sistema](../start/path/administrator.md). Contiene todos los parámetros técnicos para enviar el mensaje, como parámetros de encabezado, subdominio, aplicaciones móviles, etc. [Más información](../configuration/channel-surfaces.md).

   >[!CAUTION]
   >
   >Debe elegir una superficie de canal válida para la categoría de mensaje y el canal seleccionados.

   Puede acceder a la etiqueta, la descripción y la superficie del mensaje y modificarlas en cualquier momento utilizando la variable **[!UICONTROL Properties]** en la interfaz de mensajes.

1. Creación del contenido del mensaje.

   Conozca los pasos detallados para crear el contenido del mensaje en la siguiente página:

   * [Crear un correo electrónico](create-email.md)
   * [Crear notificaciones push](create-push.md)
   * [Creación de un mensaje SMS](create-sms.md)

## Habilitar la optimización del tiempo de envío{#sto-in-journeys}

Para las notificaciones push y por correo electrónico, puede activar **[!UICONTROL Send-time optimization]**.

Uso **[!UICONTROL Send-time optimization]** para programar tiempos de envío personalizados para que cada usuario aumente las tasas de apertura y de clics de sus mensajes. [Más información](../messages/send-time-optimization.md).


## Parámetros avanzados{#adv-settings}

Los parámetros avanzados son de solo lectura y están ocultos de forma predeterminada.

Para acceder a los parámetros avanzados, haga clic en el botón **[!UICONTROL Show read-only fields]** en la parte superior del panel de mensajes.

![](assets/show-read-only.png)

Los parámetros avanzados se muestran en la parte inferior del panel de mensajes. Estos parámetros se definen mediante la variable [administrador del sistema](../start/path/administrator.md) en el [superficie del canal](../configuration/channel-surfaces.md) (es decir, el ajuste preestablecido de mensaje) asociado al mensaje.

Para las notificaciones push, puede mostrar los siguientes parámetros: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Para el correo electrónico, puede mostrar la dirección de correo electrónico principal.

Para un uso específico, puede anular estos valores en contextos específicos. Para forzar un valor, haga clic en el botón **Habilitar anulación de parámetros** a la derecha del campo . Esta opción puede resultar útil, por ejemplo:

* Pruebe un correo electrónico, puede añadir su dirección de correo electrónico. Después de publicar el recorrido, se le enviará el correo electrónico.
* Consulte la dirección de correo electrónico de los suscriptores de una lista. Obtenga más información en [este caso de uso](../building-journeys/message-to-subscribers-uc.md).

Haga clic en el mismo icono para restablecer al parámetro predeterminado.


## Examinar mensajes{#browse-message}

Cuando se utilizan varios mensajes en un recorrido, puede cambiar de uno a otro desde el **Editar contenido** en el Navegador.

![](assets/inline-messages-multi-content.png)

Entonces puede [comprobar alertas](alerts.md) y [simulate](../design/preview.md) cada contenido de una sola vista.

## Duplicar un mensaje {#duplicate-message}

Puede copiar un mensaje existente del lienzo de recorrido.

Para ello, siga los pasos a continuación:

1. Seleccione el mensaje que desee copiar.

1. Utilice la variable **[!UICONTROL Copy]** del **[!UICONTROL Action]** panel.

   ![](assets/message-duplicate.png)

1. Entrar **crtl+V** para pegar el mensaje.

   El mensaje se añade a los lienzos de recorrido. Todos los ajustes y configuraciones se copiarán en el nuevo mensaje.

   ![](assets/message-duplicated.png)

1. Cambie el nombre del mensaje para poder diferenciar el mensaje inicial de la copia, por ejemplo al editar mensajes, como se muestra a continuación:

   ![](assets/multi-message.png)


>[!NOTE]
>
>En el caso de los correos electrónicos, también puede convertir un mensaje existente en una plantilla. [Más información](../design/email-templates.md).

## Eliminar un mensaje{#delete-message}

Para eliminar un mensaje, utilice el icono de papelera en la parte superior del panel de actividad de acción del canal.

![](assets/delete-message.png)

Utilice la variable **[!UICONTROL Confirm]** para validar.
