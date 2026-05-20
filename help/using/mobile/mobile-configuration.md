---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del canal SMS
description: Aprenda a configurar su entorno para enviar mensajes móviles con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
TQID: https://experienceleague.adobe.com/dO8HoRdGLuYVFN2YVjRCiFJQHmWHApROU8qz2-hKmTs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0201927f8d9260e8ba1d0db7014d6a7b30d09062
workflow-type: tm+mt
source-wordcount: 432
ht-degree: 31%

---

# Introducción a la configuración de Mobile {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configuración del proveedor de SMS con Journey Optimizer"
>abstract="Adobe Journey Optimizer envía mensajes móviles a través de proveedores de servicios de SMS. Seleccione su proveedor y cumplimente sus credenciales de API."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Configurar el proveedor de MMS con Journey Optimizer"
>abstract="Adobe Journey Optimizer envía contenido de medios a través de proveedores de servicios de MMS. Seleccione su proveedor y cumplimente sus credenciales de API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configuración de su proveedor de SMS/RCS/MMS con Journey Optimizer"
>abstract="Antes de enviar mensajes móviles (SMS/RCS/MMS), debe integrar la configuración del proveedor con Journey Optimizer. Una vez finalizado, debe crear una configuración de SMS/RCS/MMS. Estos pasos debe realizarlos un administrador del sistema de Adobe Journey Optimizer."
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
   * [Infobip](mobile-configuration-infobip.md)
   * [Sinch](mobile-configuration-sinch.md)
   * [Twilio](mobile-configuration-twilio.md)
   * [Proveedor personalizado](mobile-configuration-custom.md)
1. [Crear webhook](mobile-webhook.md)
1. [Crear una configuración móvil](mobile-configuration-surface.md)

Estos pasos debe realizarlos un administrador del sistema [de Adobe Journey Optimizer](../start/path/administrator.md).

## Requisitos previos{#sms-prerequisites}

Adobe Journey Optimizer se integra actualmente con proveedores externos que ofrecen servicios de mensajería móvil independientes de Adobe Journey Optimizer. Los proveedores admitidos para la mensajería móvil y MMS son: **Sinch**, **Twilio** y **Infobip**. Tenga en cuenta que puede configurar proveedores de mensajería adicionales mediante la [configuración de proveedor personalizado](mobile-configuration-custom.md).

Antes de configurar el canal móvil, debe crear una cuenta con uno de estos proveedores para obtener el **token de API** y el **ID de servicio**, que necesita para configurar la conexión entre Adobe Journey Optimizer y el proveedor correspondiente.

El uso de los servicios de mensajería móvil y MMS está sujeto a términos y condiciones adicionales del proveedor correspondiente. Como soluciones de terceros, Sinch, Twilio e Infobip están disponibles para los usuarios de Adobe Journey Optimizer a través de una integración. Adobe no controla y no es responsable de los productos de terceros. Para cualquier problema o solicitud de asistencia relacionada con los servicios de mensajería móvil, póngase en contacto con su proveedor.

>[!CAUTION]
>
>Para acceder y editar subdominios SMS, debe tener el permiso **[!UICONTROL Administrar subdominios SMS]** en la zona protegida de producción. Más información sobre los permisos de [esta página](../administration/high-low-permissions.md#administration-permissions).
>

