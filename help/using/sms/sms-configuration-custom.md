---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del proveedor personalizado
description: Aprenda a configurar su entorno para enviar mensajes de texto con Journey Optimizer con un proveedor personalizado
feature: SMS, Channel Configuration
badge: label="Beta" type="Informative"
role: Admin
level: Intermediate
exl-id: fd713864-96b9-4687-91bd-84e3533273ff
source-git-commit: 201d7d367540f7b36f27ca4a09b6f0ce12e3e22f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 27%

---

# Configuración de un proveedor personalizado {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="URL del proveedor"
>abstract="Especifique la URL de la API externa a la que desea conectarse. Esta URL sirve como punto final para acceder a las funciones y funcionalidades de la API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Tipo de autenticación"
>abstract="Especifique el método de autenticación necesario para acceder a la API, como OAuth o tokens de portador. Esto garantiza una comunicación segura y autorizada con el servicio externo."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_header_parameters"
>title="Parámetros de encabezado"
>abstract="Especifique la etiqueta, el tipo y el valor de los encabezados adicionales para habilitar la autenticación adecuada, el formato del contenido y la comunicación eficaz de la API. "

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_payload"
>title="Carga útil del proveedor"
>abstract="Proporcione la carga útil de la solicitud para garantizar que se envían los datos correctos para el procesamiento y la generación de respuestas."

>[!AVAILABILITY]
>
>Actualmente, los proveedores personalizados solo están disponibles como una versión beta para los usuarios seleccionados. Póngase en contacto con su representante de Adobe para que se le incluya en el Beta.
>
>Tenga en cuenta que este Beta no admite mensajes entrantes para la administración del consentimiento de inclusión/exclusión ni para los informes de envío.

Para enviar mensajes en Journey Optimizer utilizando un proveedor personalizado no disponible de forma predeterminada por Adobe (por ejemplo, Sinch, Infobip, Twilio), siga estos pasos:

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

1. En el menú **[!UICONTROL Credenciales de API]**, haga clic en el icono bin para eliminar sus credenciales de API.

1. Para modificar las credenciales existentes, busque las credenciales de API que desee y haga clic en la opción **[!UICONTROL Editar]** para realizar los cambios necesarios.

Después de crear y configurar las credenciales de la API, debe crear una superficie de canal para los mensajes SMS. [Más información](sms-configuration-surface.md)

Una vez configuradas, puede aprovechar todas las funcionalidades de canal integradas, como la creación de mensajes, la personalización, el seguimiento de vínculos y la creación de informes.

## Vídeo práctico {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3443609?captions=spa)
