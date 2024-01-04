---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del canal SMS
description: Aprenda a configurar su entorno para enviar mensajes de texto con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 227cdb77b0db40c59fa089789c444c2364fd062e
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 14%

---

# Configuración del canal de SMS {#sms-configuration}

Antes de enviar SMS o MMS, debe configurar el entorno de Adobe Journey Optimizer. Para realizar esto:

* [Integración de la configuración del proveedor](#create-api) con Journey Optimizer
* [Creación de una superficie SMS](#message-preset-sms) (es decir, ajuste preestablecido de SMS), también se utiliza para MMS

Estos pasos debe realizarlos un Adobe Journey Optimizer [Administrador del sistema](../start/path/administrator.md).

## Requisitos previos{#sms-prerequisites}

Adobe Journey Optimizer se integra actualmente con proveedores externos que ofrecen servicios de mensajería de texto independientes de Adobe Journey Optimizer. Los proveedores admitidos para los mensajes de texto son: **Sinch**, **Twilio** y **Infobip**. MMS solo se admite con **Sinch**.

Antes de configurar el canal SMS, debe crear una cuenta con uno de estos proveedores para obtener su **Token de API** y **ID de servicio**, que es necesario configurar la conexión entre Adobe Journey Optimizer y el proveedor aplicable.

El uso de los servicios de mensajería de texto está sujeto a términos y condiciones adicionales del proveedor correspondiente. Como soluciones de terceros, Sinch, Twilio e Infobip están disponibles para los usuarios de Adobe Journey Optimizer a través de una integración. El Adobe no controla y no es responsable de los productos de terceros. Para cualquier problema o solicitud de asistencia relacionada con los servicios de mensajería de texto (SMS/MMS), póngase en contacto con su proveedor.

>[!CAUTION]
>
>Para acceder y editar subdominios SMS, debe tener los siguientes **[!UICONTROL Administrar subdominios de SMS]** en la zona protegida de producción. Más información sobre los permisos en [esta página](../administration/high-low-permissions.md#administration-permissions).
>

## Creación de nuevas credenciales de API {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurar el proveedor de SMS/MMS con Journey Optimizer"
>abstract="Adobe Journey Optimizer envía mensajes de texto a través de proveedores de servicios de SMS/MMS. Seleccione su proveedor y rellene sus credenciales de API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurar el proveedor de SMS/MMS con Journey Optimizer"
>abstract="Antes de enviar mensajes de texto (SMS/MMS), debe integrar la configuración del proveedor con Journey Optimizer. Una vez finalizado, deberá crear una superficie SMS/MMS. Estos pasos debe realizarlos un administrador del sistema de Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=es#message-preset-sms" text="Crear una superficie de canal SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Seleccione la configuración del proveedor de SMS"
>abstract="Seleccione las credenciales de API configuradas para su proveedor de SMS."

Para configurar su proveedor de SMS/MMS con Journey Optimizer, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administration]** > **[!UICONTROL Canales]** y seleccione la **[!UICONTROL Credenciales de API]** menú. Haga clic en **[!UICONTROL Crear nuevas credenciales de API]** botón.

   ![](assets/sms_6.png)

1. Configure las credenciales de la API de SMS como se detalla a continuación.

   ![](assets/sms_7.png)

   * En el caso de **[!DNL Sinch]**:

      * **[!UICONTROL Nombre]**: elija un nombre para la credencial de la API.

      * **[!UICONTROL ID de servicio]** y **[!UICONTROL Token de API]**: acceda a la página de las API y encontrará sus credenciales en la pestaña SMS. Obtenga más información en [Documentación de Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

      * **[!UICONTROL Mensaje de inclusión]**: introduzca la respuesta personalizada que se envía automáticamente como **[!UICONTROL Mensaje de inclusión]**.

      * **[!UICONTROL Mensaje de ayuda]**: introduzca la respuesta personalizada que se envía automáticamente como **Mensaje de ayuda**.

   * En el caso de **[!DNL Sinch MMS]**:

      * **[!UICONTROL Nombre]**: elija un nombre para la credencial de la API.

      * **[!UICONTROL Identificador de proyecto]**, **[!UICONTROL ID de aplicación]** y **[!UICONTROL Token de API]**: en el menú API de conversación, puede encontrar sus credenciales en el menú Aplicación. Obtenga más información en [Documentación de Sinch](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html){target="_blank"}.

   * En el caso de **[!DNL Twilio]**:

      * **[!UICONTROL Nombre]**: elija un nombre para la credencial de la API.

      * **[!UICONTROL SID de cuenta]** y **[!UICONTROL Token de autenticación]**: acceda al panel Información de cuenta de la página Twilio Console Dashboard para buscar sus credenciales.

      * **[!UICONTROL SID de mensaje]**: introduzca el identificador único asignado a cada mensaje creado por la API de Twilio. Obtenga más información en [Documentación de Twilio](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-){target="_blank"}.

   * En el caso de **[!DNL Infobip]**:

      * **[!UICONTROL Nombre]**: elija un nombre para la credencial de la API.

      * **[!UICONTROL URL base de API]** y **[!UICONTROL Token de API]**: acceda a la página de inicio de la interfaz web o a la página de administración de claves de API para encontrar sus credenciales. Obtenga más información en [Documentación de Infobip](https://www.infobip.com/docs/api){target="_blank"}.


1. Clic **[!UICONTROL Enviar]** cuando haya terminado de configurar las credenciales de la API.

Después de crear y configurar las credenciales de la API, debe crear una superficie de canal (es decir, un ajuste preestablecido de mensaje) para los mensajes SMS.

## Creación de una superficie de SMS {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="Definir la categoría de mensaje"
>abstract="Seleccione el tipo de mensajes de texto con esta superficie: Marketing para mensajes promocionales, que requieren el consentimiento del usuario, o Transaccional para mensajes SMS no comerciales, como el restablecimiento de contraseña."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=es#sms-opt-out-management" text="Exclusión en mensajes de texto de marketing"

Una vez configurado el canal SMS/MMS, debe crear una superficie de canal para poder enviar mensajes SMS desde **[!DNL Journey Optimizer]**.

Para crear una superficie de canal, siga estos pasos:

1. En el carril izquierdo, vaya a **[!UICONTROL Administration]** > **[!UICONTROL Canales]** y seleccione **[!UICONTROL Marca]** > **[!UICONTROL Superficies de canal]**. Haga clic en **[!UICONTROL Crear superficie de canal]** botón.

   ![](assets/preset-create.png)

1. Introduzca un nombre y una descripción (opcional) para la superficie y, a continuación, seleccione el canal SMS.

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > Los nombres deben comenzar por una letra (A-Z). Solo puede contener caracteres alfanuméricos. También puede utilizar guiones bajos `_`, punto`.` y guiones `-` caracteres.

1. Defina el **Configuración de SMS**.

   ![](assets/sms-surface-settings.png)

   Comience por seleccionar la **[!UICONTROL Tipo de SMS]** que se enviarán con la superficie: **[!UICONTROL Transaccional]** o **[!UICONTROL Marketing]**.

   * Elegir **Marketing** para mensajes de texto promocionales: estos mensajes requieren el consentimiento del usuario.
   * Elegir **Transaccional** para mensajes no comerciales, como confirmaciones de pedidos, notificaciones de restablecimiento de contraseña o información de entrega, por ejemplo.

   Al crear un mensaje SMS/MMS, debe elegir una superficie de canal válida que coincida con la categoría seleccionada para el mensaje.

   >[!CAUTION]
   >
   >**Transaccional** los mensajes se pueden enviar a perfiles que cancelaron la suscripción a comunicaciones de marketing. Estos mensajes solo se pueden enviar en contextos específicos.

1. Seleccione el **[!UICONTROL Configuración de SMS]** para asociarlo con la superficie.

   Para obtener más información sobre cómo configurar su entorno para enviar mensajes SMS, consulte [esta sección](#create-api).

1. Introduzca el **[!UICONTROL Número de remitente]** &#x200B;desea utilizar para sus comunicaciones.

1. Seleccione su **[!UICONTROL Campo de ejecución de SMS]** para seleccionar **[!UICONTROL Atributo de perfil]** asociado a los números de teléfono de los perfiles.

1. Si desea utilizar la función de acortamiento de URL en los mensajes SMS, seleccione un elemento del **[!UICONTROL Subdominio]** lista.

   >[!NOTE]
   >
   >Para poder seleccionar un subdominio, asegúrese de haber configurado previamente al menos un subdominio SMS/MMS. [Descubra cómo](sms-subdomains.md)

1. Introduzca el **[!UICONTROL Número de exclusión]** que desee utilizar para esta superficie. Cuando los perfiles se excluyen de este número, aún puede enviarles mensajes de otros números que pueda estar utilizando para enviar mensajes de texto con [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >Entrada [!DNL Journey Optimizer]Por lo tanto, la exclusión de mensajes de texto ya no se administra en el nivel de canal. Ahora es específico de un número.

1. Una vez configurados todos los parámetros, haga clic en **[!UICONTROL Enviar]** para confirmar. También se puede guardar la superficie de canal como inclinación y reanudar su configuración más adelante.

   ![](assets/sms-submit-surface.png)

1. Una vez creada la superficie de canal, esta se muestra en la lista con el **[!UICONTROL Procesando]** estado.

   >[!NOTE]
   >
   >Si las comprobaciones no se realizan correctamente, obtenga más información sobre los posibles motivos de error en [esta sección](#monitor-channel-surfaces).

1. Una vez que las comprobaciones son correctas, la superficie de canal obtiene el **[!UICONTROL Activo]** estado. Está listo para utilizarse para enviar mensajes.

   ![](assets/preset-active.png)

Ya está listo para enviar mensajes de texto con Journey Optimizer.

**Temas relacionados**

* [Creación de un mensaje de texto (SMS/MMS)](create-sms.md)
* [Añadir un mensaje en un recorrido](../building-journeys/journeys-message.md)
* [Añadir un mensaje en una campaña](../campaigns/create-campaign.md)

