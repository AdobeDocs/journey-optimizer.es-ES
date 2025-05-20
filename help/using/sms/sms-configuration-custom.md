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
source-git-commit: fc78fcfb0f2ce3616cb8b1df44dda2cfd66262fe
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 13%

---

# Configuración de un proveedor de SMS personalizado {#sms-configuration-custom}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_provider_url"
>title="URL del proveedor"
>abstract="Especifique la URL de la API externa a la que desea conectarse. Esta URL sirve como punto final para acceder a las funciones y funcionalidades de la API."

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
>Tenga en cuenta que este Beta no admite mensajes entrantes para la administración del consentimiento de inclusión/exclusión ni para los informes de envío.


Esta función le permite integrar y configurar sus propios proveedores de SMS, lo que ofrece flexibilidad más allá de los proveedores predeterminados (Sinch, Twilio e Infobip). Esto permite la creación, entrega, creación de informes y administración de consentimiento de SMS sin problemas.

Con la configuración de proveedor personalizada para SMS, puede:

* Configure proveedores de SMS personalizados directamente en Journey Optimizer.
* Utilice la personalización avanzada de la carga útil para la mensajería dinámica.
* Administre las preferencias de consentimiento (inclusión/exclusión) para garantizar el cumplimiento.

## Cree sus credenciales de API {#api-credential}

Para enviar mensajes en Journey Optimizer utilizando un proveedor personalizado no disponible de forma predeterminada por Adobe (por ejemplo, Sinch, Infobip, Twilio), siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administración]** `>` **[!UICONTROL Canales]**, seleccione el menú **[!UICONTROL Credenciales de API]** y haga clic en el botón **[!UICONTROL Crear nuevas credenciales de API]**.

   ![](assets/sms_byo_1.png)

1. Configure las credenciales de la API de SMS como se detalla a continuación:

   * **[!UICONTROL Proveedor de SMS]**: personalizado.

   * **[!UICONTROL Nombre]**: escriba un nombre para su credencial de API.

   * **[!UICONTROL Id. de aplicación de proveedor]**: escriba el identificador de aplicación proporcionado por su proveedor de SMS.

   * **[!UICONTROL Nombre de proveedor]**: Escriba el nombre de su proveedor de SMS.

   * **[!UICONTROL URL de proveedor]**: escribe la URL de tu proveedor de SMS.

   * **[!UICONTROL Tipo de autenticación&#x200B;]**: seleccione el tipo de autorización y [complete los campos correspondientes](#auth-options) según el método de autenticación elegido.

     ![](assets/sms-byop.png)

1. En la sección **[!UICONTROL Encabezados]**, haga clic en **[!UICONTROL Agregar nuevo parámetro]** para especificar los encabezados HTTP para el mensaje de solicitud que se enviará al servicio externo.

   Los campos de encabezado **Content-Type** y **Charset** están establecidos de forma predeterminada y no se pueden eliminar.

   ![](assets/sms_byo_2.png)

1. Agregue su **[!UICONTROL carga útil del proveedor]** para validar y personalizar las cargas útiles de solicitud.

   Puede personalizar dinámicamente la carga útil mediante atributos de perfil y garantizar que se envíen datos precisos para el procesamiento y la generación de respuestas con la ayuda de funciones de ayuda integradas.
<!--
1. Add your **Inbound settings** to determine how your system handles incoming messages and subscriber preferences: 

    * **[!UICONTROL Inbound Webhook URL]**: Specify the endpoint URL where inbound messages (e.g. replies or new messages from users) are sent.
    * **[!UICONTROL Opt-in Keywords]**: Enter the default or custom keywords that will automatically trigger your Opt-In Message. For multiple keywords, use comma-separated values.
    * **[!UICONTROL Opt-in Message]**: Enter the custom response that is automatically sent as your Opt-In Message.
    * **[!UICONTROL Opt-out Keywords]**: Enter the default or custom keywords that will automatically trigger your Opt-Out Message. For multiple keywords, use comma-separated values.
    * **[!UICONTROL Opt-out Message]**: Enter the custom response that is automatically sent as your Opt-Out Message.
-->

1. Haga clic en **[!UICONTROL Enviar]** cuando termine de configurar las credenciales de la API.

1. En el menú **[!UICONTROL Credenciales de API]**, haga clic en el icono bin para eliminar sus credenciales de API.

   ![](assets/sms_byo_3.png)

1. Para modificar las credenciales existentes, busque las credenciales de API que desee y haga clic en la opción **[!UICONTROL Editar]** para realizar los cambios necesarios.

   ![](assets/sms_byo_4.png)

Después de crear y configurar las credenciales de la API, debe crear una superficie de canal para los mensajes SMS. [Más información](sms-configuration-surface.md)

Una vez configuradas, puede aprovechar todas las funcionalidades de canal integradas, como la creación de mensajes, la personalización, el seguimiento de vínculos y la creación de informes.

### Opciones de autenticación para proveedores de SMS personalizados {#auth-options}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_byop_auth_type"
>title="Tipo de autenticación"
>abstract="Especifique el método de autenticación necesario para acceder a la API: esto garantiza una comunicación segura y autorizada con el servicio externo."

>[!BEGINTABS]

>[!TAB Clave de API]

Una vez creadas las credenciales de la API, complete los campos necesarios para la autenticación de claves de API:

* **[!UICONTROL Nombre]**&#x200B;: escriba un nombre para la configuración de la clave de API.
* **[!UICONTROL Token de API]**&#x200B;: escriba el token de API proporcionado por su proveedor de SMS.

![](assets/sms-byop-api-key.png)

>[!TAB Autenticación de MAC]

Una vez creadas las credenciales de la API, complete los campos necesarios para la autenticación de MAC:

* **[!UICONTROL Nombre]**&#x200B;: escriba un nombre para la configuración de autenticación de MAC.
* **[!UICONTROL Token de API]**&#x200B;: escriba el token de API proporcionado por su proveedor de SMS.
* **[!UICONTROL Clave secreta de API]**: escriba la clave secreta de API proporcionada por su proveedor de SMS. Esta clave se utiliza para generar el MAC (código de autenticación de mensaje) para una comunicación segura.
* **[!UICONTROL Formato hash de autorización de Mac]**: elija el formato hash para la autenticación de MAC.

![](assets/sms-byop-mac.png)

>[!TAB Autenticación OAuth]

Una vez creadas las credenciales de la API, complete los campos necesarios para la autenticación OAuth:

* **[!UICONTROL Nombre]**&#x200B;: escriba un nombre para la configuración de autenticación de OAuth.

* **[!UICONTROL Token de API]**&#x200B;: escriba el token de API proporcionado por su proveedor de SMS.

* **[!UICONTROL URL de OAuth]**&#x200B;: introduzca la URL para obtener el token de OAuth.

* **[!UICONTROL Cuerpo de OAuth]**&#x200B;: proporcione el cuerpo de la solicitud de OAuth en formato JSON, incluidos parámetros como `grant_type`, `client_id` y `client_secret`.

![](assets/sms-byop-oauth.png)

>[!TAB Autenticación JWT]

Una vez creadas las credenciales de la API, complete los campos necesarios para la autenticación JWT:

* **[!UICONTROL Nombre]**&#x200B;: escriba un nombre para la configuración de autenticación JWT.

* **[!UICONTROL Token de API]**&#x200B;: escriba el token de API proporcionado por su proveedor de SMS.

* **[!UICONTROL Carga útil JWT]**&#x200B;: introduzca la carga útil JSON que contiene las notificaciones necesarias para JWT, como el emisor, el asunto, la audiencia y la caducidad.

![](assets/sms-byop-jwt.png)

>[!ENDTABS]

## Vídeo práctico {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3443609?captions=spa)
