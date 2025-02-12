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
source-git-commit: 56a1ef1ba256d1aac3593d8a61e67bdc42c17d32
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 27%

---

# Uso de acciones de canal integradas {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="Acción de canal integrada"
>abstract="Journey Optimizer incluye funcionalidades de acción de canal integradas. Basta con añadir a su recorrido una actividad saliente (correo electrónico, mensaje de texto SMS/MMS, push) o entrante (aplicación, web, experiencia basada en código, tarjeta de contenido) y definir la configuración y el contenido. A continuación, se ejecuta y envía en el contexto del recorrido."

[!DNL Journey Optimizer] viene con funcionalidades de acción de canal integradas. Basta con añadir a su recorrido una actividad saliente (correo electrónico, mensaje de texto SMS/MMS, push) o entrante (aplicación, web, experiencia basada en código, tarjeta de contenido) y definir la configuración y el contenido. A continuación, se ejecuta y envía en el contexto del recorrido.

>[!NOTE]
>
>También puede configurar acciones específicas para enviarle mensajes. [Más información](#recommendation)

Para añadir una acción de canal integrada a un recorrido, siga los pasos a continuación.

1. Inicie el recorrido con una actividad [Event](general-events.md) o [Read Audience](read-audience.md).

1. En la sección **Acciones** de la paleta, arrastre y suelte una actividad de salida (**correo electrónico**, **push**, **SMS**) o de entrada (**en la aplicación**, **web**, **experiencia basada en código**, **tarjeta de contenido**) en el lienzo.

   ![](assets/journey-web-activity.png)

1. Configure su actividad.

   * Conozca los pasos detallados para crear el contenido del mensaje de la siguiente manera:

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

     >[!NOTE]
     >
     >Para los correos electrónicos y las notificaciones push, puede activar la Optimización del tiempo de envío. [Más información](send-time-optimization.md)

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
     >Cada actividad de mensaje entrante viene con una actividad de **Wait** de 3 días. [Más información](wait-activity.md#auto-wait-node)


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