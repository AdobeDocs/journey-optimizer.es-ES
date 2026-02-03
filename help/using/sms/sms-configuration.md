---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del canal SMS
description: Aprenda a configurar su entorno para enviar mensajes de texto con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 4278d8c8294b1413788402cd8eac5959996ad3f5
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 42%

---

# Introducción a la configuración de SMS/MMS/RCS {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configuración del proveedor de SMS con Journey Optimizer"
>abstract="Adobe Journey Optimizer envía mensajes de texto a través de proveedores de servicios de SMS. Seleccione su proveedor y cumplimente sus credenciales de API."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Configurar el proveedor de MMS con Journey Optimizer"
>abstract="Adobe Journey Optimizer envía contenido de medios a través de proveedores de servicios de MMS. Seleccione su proveedor y cumplimente sus credenciales de API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurar el proveedor de SMS/MMS con Journey Optimizer"
>abstract="Antes de enviar mensajes de texto (SMS/MMS), debe integrar la configuración del proveedor con Journey Optimizer. Una vez finalizada, deberá crear una configuración de SMS/MMS. Estos pasos debe realizarlos un administrador del sistema de Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Crear una configuración de canal de SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Seleccione la configuración del proveedor de SMS"
>abstract="Seleccione las credenciales de API configuradas para su proveedor de SMS."

>[!CONTEXTUALHELP]
>id="ajo_admin_fuzzy_opt_out"
>title="Exclusión aproximada"
>abstract="Cuando está habilitada, la exclusión aproximada detecta mensajes entrantes que se parecen mucho a las palabras clave de exclusión definidas (por ejemplo, Cancilar) y envía automáticamente una respuesta de confirmación para comprobar la intención del usuario de cancelar su suscripción. Si el usuario confirma esta decisión a través de la indicación definida, se cancela su suscripción."

Antes de enviar SMS, MMS o RCS, debe configurar su entorno de Adobe Journey Optimizer. Para realizar esto:

1. Integre la configuración del proveedor con Journey Optimizer.
Los pasos dependen del proveedor de SMS. Examine los vínculos siguientes para acceder a la documentación detallada:
   * [Infobip](sms-configuration-infobip.md)
   * [Sinch](sms-configuration-sinch.md)
   * [Twilio](sms-configuration-twilio.md)
   * [Proveedor personalizado](sms-configuration-custom.md)
1. [Crear webhook](sms-webhook.md)
1. [Creación de una configuración de SMS](sms-configuration-surface.md)

Estos pasos debe realizarlos un administrador del sistema [de Adobe Journey Optimizer](../start/path/administrator.md).

## Requisitos previos{#sms-prerequisites}

Adobe Journey Optimizer se integra actualmente con proveedores externos que ofrecen servicios de mensajería de texto independientes de Adobe Journey Optimizer. Los proveedores compatibles con los mensajes de texto y MMS son: **Sinch**, **Twilio** y **Infobip**. Tenga en cuenta que puede configurar proveedores de mensajería adicionales mediante la [configuración de proveedor personalizado](sms-configuration-custom.md).

Antes de configurar el canal SMS, debe crear una cuenta con uno de estos proveedores para obtener el **token de API** y el **ID de servicio**, que necesita para configurar la conexión entre Adobe Journey Optimizer y el proveedor correspondiente.

El uso de los servicios de mensajería de texto y MMS está sujeto a términos y condiciones adicionales del proveedor correspondiente. Como soluciones de terceros, Sinch, Twilio e Infobip están disponibles para los usuarios de Adobe Journey Optimizer a través de una integración. Adobe no controla y no es responsable de los productos de terceros. Para cualquier problema o solicitud de asistencia relacionada con los servicios de mensajería de texto (SMS/MMS), póngase en contacto con su proveedor.

>[!CAUTION]
>
>Para acceder y editar subdominios SMS, debe tener el permiso **[!UICONTROL Administrar subdominios SMS]** en la zona protegida de producción. Más información sobre los permisos de [esta página](../administration/high-low-permissions.md#administration-permissions).
>

