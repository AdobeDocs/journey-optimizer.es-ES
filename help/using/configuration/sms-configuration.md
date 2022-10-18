---
solution: Journey Optimizer
product: journey optimizer
title: Configuración de SMS
description: Aprenda a configurar su entorno para enviar SMS con Journey Optimizer
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 2%

---

# Configuración del canal de SMS {#sms-configuration}

[!DNL Journey Optimizer] le permite crear sus recorridos y enviar mensajes a la audiencia de destino.

Antes de enviar SMS, configure su instancia. Debe [integrar la configuración del proveedor](#create-api) con Journey Optimizer y [crear una superficie SMS](#message-preset-sms) (es decir, ajuste preestablecido de SMS). Estos pasos debe realizarlos un [Administrador del sistema de Adobe Journey Optimizer](../start/path/administrator.md).

>[!IMPORTANT]
>
>Actualmente, Adobe Journey Optimizer se integra con proveedores de terceros como Sinch y Twilio, que ofrecen servicios SMS independientes de Adobe Journey Optimizer.  Antes de la configuración de SMS, debe crear una cuenta con uno de estos proveedores de SMS para recibir el token de API y el ID de servicio que le permitan establecer la conexión entre Adobe Journey Optimizer y el proveedor de SMS correspondiente. Su uso de servicios SMS estará sujeto a términos y condiciones adicionales del proveedor de SMS correspondiente. Dado que Sinch y Twilio son productos de terceros disponibles para los usuarios de Adobe Journey Optimizer mediante una integración, para cualquier problema o consulta relacionada con los servicios SMS, los usuarios de Sinch o Twilio deberán ponerse en contacto con el proveedor de SMS correspondiente para obtener ayuda. Adobe no controla ni es responsable de productos de terceros.

## Crear nueva credencial de API {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurar el proveedor de SMS con Journey Optimizer"
>abstract="Seleccione su proveedor y rellene sus credenciales de API de SMS."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurar el proveedor de SMS con Journey Optimizer"
>abstract="Antes de enviar SMS, debe integrar la configuración del proveedor con Journey Optimizer. Una vez finalizado, deberá crear una superficie SMS. Estos pasos debe realizarlos un administrador del sistema de Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/sms-configuration.html#message-preset-sms" text="Creación de una superficie de canal SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Seleccione la configuración del proveedor de SMS"
>abstract="Seleccione las credenciales de API configuradas para su proveedor de SMS."

Para configurar el proveedor de SMS con Journey Optimizer, siga estos pasos:

1. Acceda a la **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Credenciales de API]** a continuación, haga clic en **[!UICONTROL Creación de credenciales de API]**.

   ![](assets/sms_4.png)

1. Seleccione su **[!UICONTROL Proveedor de SMS]**:

   * [!DNL Sinch]. Para encontrar su **[!UICONTROL ID de servicio]** y **[!UICONTROL Token de API]**, acceda al menú SMS > API desde su cuenta de Launch.
   * [!DNL Twilio]. Para encontrar su **[!UICONTROL ID de servicio]** y **[!UICONTROL Token de API]**, acceda al panel Información de la cuenta de la página Tablero de consola .

1. Escriba un **[!UICONTROL Nombre]** para su credencial de API.

1. Escriba la **[!UICONTROL ID de servicio]** y **[!UICONTROL Token de API]**.

   ![](assets/sms_5.png)

1. Haga clic en **[!UICONTROL Submit]** cuando haya terminado la configuración de sus credenciales de API.

Después de crear y configurar las credenciales de API, debe crear una superficie de canal (es decir, un ajuste preestablecido de mensaje) para los mensajes SMS.

## Creación de una superficie de canal para mensajes SMS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Defina la categoría SMS"
>abstract="Seleccione el tipo de mensajes SMS que se enviarán al utilizar esta superficie: Marketing para mensajes SMS promocionales, que requieren el consentimiento del usuario, o transaccional para mensajes SMS no comerciales, que también se pueden enviar a perfiles cancelados de suscripción en contextos específicos."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/create-sms.html#sms-opt-in-out" text="Exclusión en mensajes SMS de marketing"

Una vez configurado el canal SMS, debe crear una superficie de canal para poder enviar mensajes SMS desde **[!DNL Journey Optimizer]**.

Para crear una superficie de canal, siga estos pasos:

1. Acceda a la **[!UICONTROL Canales]** > **[!UICONTROL Marcas]** > **[!UICONTROL Superficies de canal]** a continuación, haga clic en **[!UICONTROL Crear superficie de canal]**.

   ![](assets/preset-create.png)

1. Introduzca un nombre y una descripción (opcional) para la superficie y, a continuación, seleccione el canal SMS.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar guiones bajos `_`, punto`.` Guión `-` caracteres.

1. Configure las variables **SMS** configuración.

   ![](assets/preset-sms.png)

   * Seleccione el **[!UICONTROL Tipo de SMS]** que se enviará con la superficie: **[!UICONTROL Transaccional]** o **[!UICONTROL Marketing]**.

   * Seleccione el **[!UICONTROL Configuración de SMS]** para asociarlo a la superficie.

      Para obtener más información sobre cómo configurar su entorno para enviar mensajes SMS, consulte [esta sección](#create-api).

   * Introduzca la variable **[!UICONTROL Número de remitente]** &#x200B; desea utilizar para sus comunicaciones.

   * Seleccione su **[!UICONTROL Campo de ejecución de SMS]** para seleccionar el **[!UICONTROL Atributo de perfil]** asociado a los números de teléfono de los perfiles.

1. Una vez configurados todos los parámetros, haga clic en **[!UICONTROL Submit]** para confirmar. También puede guardar la superficie del canal como borrador y reanudar su configuración más adelante.

   ![](assets/sms_preset_2.png)

1. Una vez creada la superficie del canal, se muestra en la lista con la variable **[!UICONTROL Procesamiento]** estado.

   >[!NOTE]
   >
   >Si las comprobaciones no son correctas, obtenga más información sobre los posibles motivos de error en [esta sección](#monitor-channel-surfaces).

1. Una vez realizadas las comprobaciones, la superficie del canal recibe el **[!UICONTROL Activo]** estado. Está listo para utilizarse para enviar mensajes.

   ![](assets/preset-active.png)

Ya está listo para enviar mensajes SMS con Journey Optimizer.

**Temas relacionados**

* [Creación de un mensaje SMS](../messages/create-sms.md)
* [Adición de un mensaje en un recorrido](../building-journeys/journeys-message.md)
