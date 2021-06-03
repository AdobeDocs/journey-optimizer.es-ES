---
title: Crear ajustes preestablecidos de mensaje
description: Descubra cómo crear ajustes preestablecidos de mensajes de correo electrónico y notificaciones push
source-git-commit: 4353b8f01bb4e47f6f2384e464341c0ee80ecaf2
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Crear ajustes preestablecidos de mensaje

Con [!DNL Journey Optimizer], puede configurar ajustes preestablecidos de mensaje que definan todos los parámetros técnicos necesarios para los mensajes de correo electrónico y notificaciones push (tipo de correo electrónico, correo electrónico y nombre del remitente, aplicaciones móviles, etc.).

Puede configurar tantos ajustes preestablecidos de mensaje como desee según las diferentes marcas para las que necesite comunicarse.

Una vez configurados los ajustes preestablecidos de mensaje, puede seleccionarlos al crear mensajes desde la lista **[!UICONTROL Presets]**.

## Crear un ajuste preestablecido de mensaje {#create-message-preset}

Para crear un ajuste preestablecido de mensaje, siga estos pasos:

1. Acceda al menú **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** y haga clic en **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. Proporcione un nombre y una descripción (opcional) para el ajuste preestablecido y, a continuación, especifique los canales que desea configurar.

   ![](../assets/preset-general.png)

1. Configure los ajustes de correo electrónico y notificaciones push:

   Para el canal de correo electrónico, especifique:

   * El tipo de comunicaciones que se envían con el ajuste preestablecido (mensajes transaccionales o de marketing),
   * El [subdominio](about-subdomain-delegation.md) que se utilizará para enviar los correos electrónicos,
   * El [grupo IP](ip-pools.md) que se va a asociar al ajuste preestablecido,
   * Parámetros de encabezado que se utilizarán para los correos electrónicos enviados con el ajuste preestablecido.

   ![](../assets/preset-email.png)

   Para el canal de notificaciones push, especifique las aplicaciones móviles de IOS o Android que desea utilizar para sus mensajes. Para obtener más información sobre cómo configurar el entorno para enviar notificaciones push, consulte [esta sección](../push-configuration.md).

   ![](../assets/preset-push.png)

1. Una vez configurados todos los parámetros, haga clic en **[!UICONTROL Submit]** para confirmar. También puede guardar el ajuste preestablecido de mensaje como borrador y reanudar su configuración más adelante.

   ![](../assets/preset-submit.png)

1. Una vez creado el ajuste preestablecido de mensaje, aparece en la lista con el estado **[!UICONTROL Processing]**.

   Durante este paso, se realizarán varias comprobaciones para verificar que se ha configurado correctamente. El tiempo de procesamiento es de aproximadamente 48 horas a 72 horas y puede tardar entre 7 y 10 días.

   Estas comprobaciones incluyen pruebas de capacidad de envío que realiza el equipo de entrega de Adobes:

   * validación de SPF,
   * Validación de DKIM,
   * Validación de registros MX,
   * Comprobar las listas negras de direcciones IP,
   * Comprobación de host de Helo,
   * Verificación del grupo IP,
   * Registro A/PTR, verificación del subdominio t/m/res.

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