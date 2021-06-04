---
title: Crear ajustes preestablecidos de mensaje
description: Obtenga información sobre cómo configurar y supervisar los ajustes preestablecidos de mensajes
source-git-commit: 68716d6520848f4825e90106ea1cd76185ae0f87
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---


# Crear ajustes preestablecidos de mensaje

Con [!DNL Journey Optimizer], puede configurar ajustes preestablecidos de mensaje que definan todos los parámetros técnicos necesarios para el mensaje de correo electrónico y los mensajes de notificaciones push: tipo de correo electrónico, correo electrónico y nombre del remitente, aplicaciones móviles, etc.

>[!CAUTION]
>
> La configuración de los ajustes preestablecidos de mensaje está restringida a los administradores de Recorrido. [Más información](../administration/ootb-product-profiles.md#journey-administrator)


Una vez configurados los ajustes preestablecidos de mensaje, puede seleccionarlos al crear mensajes desde la lista **[!UICONTROL Presets]**.

## Crear un ajuste preestablecido de mensaje {#create-message-preset}

Para crear un ajuste preestablecido de mensaje, siga estos pasos:

1. Acceda al menú **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** y haga clic en **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. Introduzca un nombre y una descripción (opcional) para el ajuste preestablecido y, a continuación, seleccione los canales que desea configurar.

   ![](../assets/preset-general.png)


   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos y `_` `.` `-` caracteres.

1. Configure la configuración **email**.

   ![](../assets/preset-email.png)

   * Seleccione el tipo de mensaje que se enviará con el ajuste preestablecido: **Transactional** o **Marketing**

      >[!CAUTION]
      >
      > **** Los mensajes de transacción se pueden enviar a perfiles que cancelan la suscripción a comunicaciones de marketing. Estos mensajes solo se pueden enviar en contextos específicos, como restablecimiento de contraseña, estado de pedido o notificación de envío, por ejemplo.

   * Seleccione el subdominio que desea utilizar para enviar los correos electrónicos. [Más información](about-subdomain-delegation.md)
   * Seleccione el grupo de IP que desea asociar al ajuste preestablecido. [Más información](ip-pools.md)
   * Introduzca los parámetros de encabezado para los correos electrónicos enviados mediante el ajuste preestablecido.

      >[!NOTE]
      >
      > * Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos y caracteres `_`, `.`, `-`.
         > 
         > 
      * Excepto para **Responder a (enviar correo electrónico)**, el dominio de direcciones de correo electrónico debe utilizar el subdominio seleccionado actual.



1. Configure la **notificación push** configuración.

   ![](../assets/preset-push.png)

   * Seleccione al menos una plataforma: **iOS** o **Android**

   * Seleccione las aplicaciones móviles que desea utilizar para cada plataforma.

      Para obtener más información sobre cómo configurar el entorno para enviar notificaciones push, consulte [esta sección](../push-configuration.md).

1. Una vez configurados todos los parámetros, haga clic en **[!UICONTROL Submit]** para confirmar. También puede guardar el ajuste preestablecido de mensaje como borrador y reanudar su configuración más adelante.

   ![](../assets/preset-submit.png)

1. Una vez creado el ajuste preestablecido de mensaje, aparece en la lista con el estado **[!UICONTROL Processing]**.

   Durante este paso, se realizarán varias comprobaciones para verificar que se ha configurado correctamente. El tiempo de procesamiento es de aproximadamente **48h-72h** y puede tardar **7-10 días**.

   Estas comprobaciones incluyen pruebas de capacidad de envío que realiza el equipo de entrega de Adobes:

   * Validación de SPF
   * Validación de DKIM
   * Validación de registros MX
   * Comprobación de IP inclusión en la lista de bloqueados
   * Comprobación de host de Helo
   * Verificación del grupo IP
   * Registro A/PTR, verificación del subdominio t/m/res

1. Una vez realizadas las comprobaciones correctamente, el ajuste preestablecido de mensaje obtiene el estado **[!UICONTROL Active]**. Está listo para utilizarse para enviar mensajes.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Monitorización de mensajes preestablecidos

Todos los ajustes preestablecidos de mensajes se muestran en el menú **[!UICONTROL Channels]** / **[!UICONTROL Message presets]**. Los filtros están disponibles para ayudarle a navegar por la lista (tipo de canal, usuario, estado).

![](../assets/preset-filters.png)

Los ajustes preestablecidos de mensaje pueden tener los siguientes estados:

* **[!UICONTROL Draft]**: El ajuste preestablecido de mensaje se ha guardado como borrador y aún no se ha enviado. Ábrala para reanudar la configuración.
* **[!UICONTROL Processing]**: El ajuste preestablecido de mensaje se ha enviado y se está realizando en varios pasos de verificación.
* **[!UICONTROL Active]**: El ajuste preestablecido de mensaje se ha verificado y se puede seleccionar para crear mensajes.
* **[!UICONTROL Failed]**: Se han producido errores en una o varias comprobaciones durante la verificación del ajuste preestablecido de mensaje.
* **[!UICONTROL De-activated]**: El ajuste preestablecido de mensaje se desactiva. No se puede usar para crear nuevos mensajes.

## Editar ajustes preestablecidos de mensaje

Para editar un ajuste preestablecido de mensaje, primero debe desactivarlo para que no esté disponible para crear nuevos mensajes (los mensajes publicados con este ajuste preestablecido no se verán afectados y seguirán funcionando). A continuación, debe duplicar el ajuste preestablecido de mensaje para crear una nueva versión que utilizará para crear nuevos mensajes:

1. Acceda a la lista de ajustes preestablecidos de mensaje y, a continuación, desactive el ajuste preestablecido de mensaje que desee editar.

   ![](../assets/preset-deactivate.png)

1. Duplique el ajuste preestablecido de mensaje desactivado. Se añade automáticamente a la lista una copia con el estado **[!UICONTROL Draft]**.

   ![](../assets/preset-duplicated.png)

1. Abra el mensaje preestablecido duplicado, modifíquelo según sus necesidades y, a continuación, envíe los cambios. El ajuste preestablecido de mensaje atravesará el mismo ciclo de validación que durante el [paso de creación](#create-message-preset).

1. Una vez validado, obtiene el estado **[!UICONTROL Active]** y está listo para utilizarse para crear nuevos mensajes.

   >[!NOTE]
   >
   >Los ajustes preestablecidos de mensajes desactivados no se pueden eliminar para evitar problemas en los recorridos que utilizan estos ajustes preestablecidos para enviar mensajes.

