---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor Twilio
description: Aprenda a configurar su entorno para enviar mensajes de texto con Journey Optimizer con Twilio
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: d6f74566-c913-4727-83b9-473a798a0158
source-git-commit: 8f045e1b709c0059ce21cda68c21e8732f58e51e
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---

# Configuración del proveedor Twilio {#sms-configuration-twilio}

Para configurar Twilio con Journey Optimizer, debe crear una nueva credencial de API utilizada para Twilio:

1. En el carril izquierdo, vaya a **[!UICONTROL Administration]** > **[!UICONTROL Canales]** y seleccione la **[!UICONTROL Credenciales de API]** menú. Haga clic en **[!UICONTROL Crear nuevas credenciales de API]** botón.

1. Configure las credenciales de la API de SMS como se detalla a continuación:

   * **[!UICONTROL Proveedor de SMS]**: Twilio.

   * **[!UICONTROL Nombre]**: elija un nombre para la credencial de la API.

   * **[!UICONTROL SID de cuenta]** y **[!UICONTROL Token de autenticación]**: acceda al **Información de cuenta** Panel de control de la consola Twilio para buscar sus credenciales.

   * **[!UICONTROL SID de mensaje]**: introduzca el identificador único asignado a cada mensaje creado por la API de Twilio. Obtenga más información en [Documentación de Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

1. Clic **[!UICONTROL Enviar]** cuando haya terminado de configurar las credenciales de la API.

Después de crear y configurar las credenciales de la API, debe crear una superficie de canal para los mensajes SMS y MMS. [Más información](sms-configuration-surface.md)
