---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor Twilio
description: Aprenda a configurar su entorno para enviar mensajes de texto con Journey Optimizer con Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 4%

---

# Configuración del proveedor Twilio {#sms-configuration-twilio}

Para configurar Twilio con Journey Optimizer, debe crear una nueva credencial de API utilizada para Twilio:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** `>` **[!UICONTROL Configuración de SMS]** y seleccione el menú **[!UICONTROL Credenciales de API]**. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

1. Configure las credenciales de la API de SMS como se detalla a continuación:

   * **[!UICONTROL Proveedor de SMS]**: Twilio.

   * **[!UICONTROL Nombre]**: elige un nombre para tu credencial de API.

   * **[!UICONTROL SID de cuenta]** y **[!UICONTROL token de autenticación]**: acceda al panel **Información de cuenta** de la página del panel de la consola de Twilio para encontrar sus credenciales.

   * **[!UICONTROL SID de mensaje]**: escriba el identificador único asignado a cada mensaje creado por la API de Twilio. Obtenga más información en [Documentación de Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * **[!UICONTROL Número de entrada]**: agrega tu número de entrada único. Esto le permite utilizar las mismas credenciales de API en diferentes zonas protegidas, cada una con su propio número de entrada.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar las credenciales de la API.

Después de crear y configurar las credenciales de la API, debe crear una configuración de canal para los mensajes SMS y MMS. [Más información](sms-configuration-surface.md)
