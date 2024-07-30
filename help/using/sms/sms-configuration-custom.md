---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor personalizado
description: Aprenda a configurar su entorno para enviar mensajes de texto con Journey Optimizer con un proveedor personalizado
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: af03ad62c2c7b29d695670f083e0dfb6d0c71b93
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 1%

---

# Configuración de un proveedor personalizado (Beta) {#sms-configuration-custom}

>[!AVAILABILITY]
>
>Actualmente, los proveedores personalizados solo están disponibles como una versión beta para los usuarios seleccionados. Póngase en contacto con el representante del Adobe para que se le incluya en el Beta.
>
>Tenga en cuenta que este Beta no admite mensajes entrantes para la administración del consentimiento de inclusión/exclusión ni para los informes de envío.

Para enviar mensajes en Journey Optimizer mediante un proveedor personalizado no disponible de forma predeterminada por Adobe (por ejemplo, Sinch, Infobip, Twilio), siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** y seleccione el menú **[!UICONTROL Credenciales de API]**.

1. Haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

   ![](assets/sms_byo_1.png)

1. Configure las credenciales de la API de SMS como se detalla a continuación:

   * **[!UICONTROL Proveedor de SMS]**: personalizado.

   * **[!UICONTROL Nombre]**: escriba un nombre para su credencial de API.

   * **[!UICONTROL Id. de aplicación de proveedor]**: escriba el identificador de aplicación proporcionado por su proveedor de SMS.

   * **[!UICONTROL Nombre de proveedor]**: escriba el nombre de su proveedor de SMS.

   * **[!UICONTROL URL de proveedor]**: escribe la URL de tu proveedor de SMS.

   * **[!UICONTROL Tipo de autenticación&#x200B;]**: seleccione su tipo de autorización. Los tipos de autorización admitidos son **Bearer App** o **Basic**.

   * **[!UICONTROL Token de API]**: escriba el token de API proporcionado por su proveedor de SMS.

   * **[!UICONTROL Carga útil del proveedor]**: agregue la carga útil del proveedor, por ejemplo: `{"from": "+1234XXXXXX", "to": "+1374XXXXXX", "content": "This is a test message", "contentType": "TEXT"}`.

     Asegúrese de que la carga útil incluya `{{toNumber}}`, `{{fromNumber}}`, `{{message}}`.

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar las credenciales de la API.

Después de crear y configurar las credenciales de la API, debe crear una superficie de canal para los mensajes SMS. [Más información](sms-configuration-surface.md)

Una vez configuradas, puede aprovechar todas las funcionalidades de canal integradas, como la creación de mensajes, la personalización, el seguimiento de vínculos y la creación de informes.

## Vídeo explicativo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3431625)
