---
title: Configuración de SMS
description: Aprenda a configurar su entorno para enviar mensajes SMS con Journey Optimizer
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 8fc470ced790ed65df7e88b861e8b8f7126ace21
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 4%

---

# Configuración del canal de SMS {#sms-configuration}

>[!CAUTION]
>
> Actualmente, el uso del canal SMS está disponible en acceso anticipado solo para usuarios seleccionados. Si desea aprovechar esta función, póngase en contacto con el administrador de cuentas de Adobe.

[!DNL Journey Optimizer] le permite crear sus recorridos y enviar mensajes a la audiencia de destino.

## Crear nueva credencial de API {#create-api}

Para configurar el proveedor de SMS con Journey Optimizer, siga estos pasos:

1. Acceda a la **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL API Credentials]** a continuación, haga clic en **[!UICONTROL Create API credential]**.

   ![](../assets/sms_4.png)

1. Seleccione Sinch como su **[!UICONTROL SMS vendor]**.

1. Escriba un **[!UICONTROL Name]** para su credencial de API.

1. Escriba la **[!UICONTROL Service ID]** y **[!UICONTROL API Token]**.

   >[!NOTE]
   >
   > Sinch requiere credenciales de API especiales. Para encontrar su **[!UICONTROL Service ID]** y **[!UICONTROL API Token]**, acceda al menú SMS > API desde su cuenta de Launch,

   ![](../assets/sms_5.png)

1. Haga clic en **[!UICONTROL Submit]** cuando haya terminado la configuración de sus credenciales de API.

Después de crear y configurar las credenciales de API, debe crear un ajuste preestablecido de mensaje para los mensajes SMS.

## Creación de un ajuste preestablecido de mensaje para mensajes SMS {#message-preset-sms}

Una vez configurado el canal SMS, debe crear un ajuste preestablecido de mensaje para poder enviar mensajes SMS desde **[!DNL Journey Optimizer]**.

Para crear un ajuste preestablecido de mensaje, siga estos pasos:

1. Acceda a la **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** a continuación, haga clic en **[!UICONTROL Create Message preset]**.

   ![](assets/preset-create.png)

1. Introduzca un nombre y una descripción (opcional) para el ajuste preestablecido y, a continuación, seleccione el canal SMS.

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar guiones bajos `_`, punto`.` Guión `-` caracteres.

1. Configure las variables **SMS** configuración.

   ![](assets/preset-sms.png)

   * Seleccione el **[!UICONTROL SMS Type]** que se enviará con el ajuste preestablecido: **[!UICONTROL Transactional]** o **[!UICONTROL Marketing]**.

   * Seleccione el **[!UICONTROL SMS configuration]** para asociarlo al ajuste preestablecido.

      Para obtener más información sobre cómo configurar su entorno para enviar mensajes SMS, consulte [esta sección](sms-configuration.md).

   * Introduzca la variable **[!UICONTROL Sender number]** &#x200B; desea utilizar para sus comunicaciones.

1. Una vez configurados todos los parámetros, haga clic en **[!UICONTROL Submit]** para confirmar. También puede guardar el ajuste preestablecido de mensaje como borrador y reanudar su configuración más adelante.

   ![](assets/sms_preset_2.png)

1. Una vez creado el ajuste preestablecido de mensaje, se muestra en la lista con la variable **[!UICONTROL Processing]** estado.

   >[!NOTE]
   >
   >Si las comprobaciones no son correctas, obtenga más información sobre los posibles motivos de error en [esta sección](#monitor-message-presets).

1. Una vez realizadas las comprobaciones correctamente, el ajuste preestablecido de mensaje obtiene el valor **[!UICONTROL Active]** estado. Está listo para utilizarse para enviar mensajes.

   ![](assets/preset-active.png)

Ya está listo para enviar mensajes SMS con Journey Optimizer.

**Temas relacionados**

* [Creación de un mensaje SMS](../messages/create-sms.md)
* [Adición de un mensaje en un recorrido](../building-journeys/journeys-message.md)
