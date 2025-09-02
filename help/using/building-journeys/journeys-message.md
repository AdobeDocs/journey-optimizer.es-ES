---
solution: Journey Optimizer
product: journey optimizer
title: Añadir una acción de canal integrada a un recorrido
description: Aprenda a añadir una acción de canal integrada a un recorrido
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: recorrido, mensaje, push, sms, correo electrónico, en la aplicación, web, tarjeta de contenido, experiencia basada en código
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: c39a71da901b888ff440a1488658b577ff72cc32
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 17%

---

# Uso de acciones de canal integradas {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Acción de canal integrada"
>abstract="Journey Optimizer incluye funcionalidades de acción de canal integradas. Basta con añadir a su recorrido una actividad de mensaje (correo electrónico, mensaje de texto SMS/MMS, push) o de experiencia entrante (in-app, web, experiencia basada en código, tarjeta de contenido) y definir la configuración y el contenido. A continuación, se ejecuta y envía en el contexto del recorrido."

[!DNL Journey Optimizer] viene con funcionalidades de acción de canal integradas que se utilizan para enviar mensajes: cuando un perfil entra en esta actividad, se les envía un mensaje.

Para agregar una acción de canal integrada al recorrido, arrastre y suelte una actividad de canal y defina su configuración y contenido. A continuación, se ejecuta y envía en el contexto del recorrido.

>[!NOTE]
>
>También puede configurar acciones personalizadas para enviar los mensajes en [!DNL Journey Optimizer] [Más información](#recommendation)

## Añadir un mensaje en un recorrido  {#add-msg-in-journey}

Con las acciones de canal integradas, puede configurar los mensajes salientes o entrantes. Los canales entrantes admitidos son el correo electrónico, los mensajes de texto (SMS/MMS) y las notificaciones push. Los canales salientes admitidos son la experiencia en la aplicación, la web, basada en código y la tarjeta de contenido.

Para añadir una acción de canal integrada a un recorrido, siga los pasos a continuación.

1. Inicie el recorrido con una actividad [Event](general-events.md) o [Read Audience](read-audience.md).

1. En la sección **Acciones** de la paleta, arrastre y suelte una actividad de canal en el lienzo.

   ![](assets/journey-web-activity.png)

1. También puede seleccionar la actividad **[!UICONTROL Action]**, que le permite seleccionar varias acciones entrantes. [Más información](journey-action.md)

1. Configure su actividad. Encontrará instrucciones de configuración detalladas en los vínculos siguientes.

   * Conozca los pasos detallados para crear su acción saliente de la siguiente manera:

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
      <a href="../sms/create-sms.md"><strong>Crear mensajes de texto (SMS/MMS)</strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

   * Conozca los pasos detallados para crear su acción entrante de la siguiente manera:

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../in-app/create-in-app.md">
      <img alt="Posible cliente" src="../assets/do-not-localize/in-app.jpg">
      </a>
      <div><a href="../in-app/create-in-app.md"><strong>Crear mensajes en la aplicación</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../web/create-web.md">
      <img alt="Posible cliente" src="../assets/do-not-localize/web-create.jpg">
      </a>
      <div><a href="../web/create-web.md"><strong>Crear experiencias web</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../content-card/create-content-card.md">
      <img alt="Posible cliente" src="../assets/do-not-localize/sms-config.jpg">
      </a>
      <div><a href="../content-card/create-content-card.md"><strong>Creación de tarjetas de contenido</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../code-based/create-code-based.md">
      <img alt="Poco frecuente" src="../assets/do-not-localize/web-design.jpg">
      </a>
      <div>
      <a href="../code-based/create-code-based.md"><strong>Crear experiencias basadas en código<strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

   >[!NOTE]
   >
   >* Cada actividad de experiencia entrante viene con una actividad de **Espera** de 3 días. [Más información](wait-activity.md#auto-wait-node)
   >
   >* Para los correos electrónicos y las notificaciones push, puede activar la Optimización del tiempo de envío. [Más información](send-time-optimization.md)

1. Según la actividad, puede mostrar parámetros avanzados específicos del canal seleccionado y anular algunos valores predeterminados como la dirección de ejecución. [Más información](../about-journey-activities.md#advanced-parameters)

   >[!NOTE]
   >
   >Si los parámetros avanzados están ocultos, haga clic en el botón **[!UICONTROL Mostrar campos de solo lectura]** situado en la parte superior del panel derecho.

## Actualización de contenido en directo {#update-live-content}

Puede actualizar el contenido de una acción de canal integrada en un recorrido en directo.

Para ello, abre el recorrido en vivo, selecciona la actividad del canal y haz clic en **Editar contenido**.

![](assets/add-a-message2.png)

Sin embargo, no se pueden cambiar los atributos utilizados en la personalización, ya sean atributos de perfil o datos contextuales (de propiedades de evento o recorrido).

Si ha modificado datos contextuales, se mostrará el siguiente mensaje de error: `ERR_AUTHORING_JOURNEYVERSION_201`

Si ha modificado los atributos de perfil, se mostrará el siguiente mensaje de error: `ERR_AUTHORING_JOURNEYVERSION_202`

Tenga en cuenta que para la actividad en la aplicación, cualquier cambio se puede realizar en el contenido mientras el recorrido está activo, pero los déclencheur en la aplicación no se pueden modificar.

## Enviar con acciones personalizadas {#recommendation}

En lugar de utilizar las funciones de mensajes integradas, puede utilizar acciones personalizadas para configurar la conexión de un sistema de terceros para enviar mensajes o llamadas API.

* Si utiliza un sistema de terceros para enviar mensajes, puede crear una acción personalizada. [Más información](../action/action.md)

* Si está trabajando con Adobe Campaign, consulte estas secciones:

   * [[!DNL Journey Optimizer] y Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] y Campaign Standard](../action/acs-action.md)