---
solution: Journey Optimizer
product: journey optimizer
title: Configuración del canal SMS
description: Aprenda a configurar su entorno para enviar mensajes de texto con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 37%

---

# Introducción a la configuración de SMS {#sms-configuration}

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
>abstract="Antes de enviar mensajes de texto (SMS/MMS), debe integrar la configuración del proveedor con Journey Optimizer. Una vez finalizado, deberá crear una superficie SMS/MMS. Estos pasos debe realizarlos un administrador del sistema de Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=es#message-preset-sms" text="Crear una superficie de canal SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Seleccione la configuración del proveedor de SMS"
>abstract="Seleccione las credenciales de API configuradas para su proveedor de SMS."

Antes de enviar SMS o MMS, debe configurar el entorno de Adobe Journey Optimizer. Para realizar esto:

1. Integre la configuración del proveedor con Journey Optimizer:
   * [Con Sinch](sms-configuration-sinch.md)
   * [Con Infobip](sms-configuration-infobip.md)
   * [Con Twilio](sms-configuration-twilio.md)
1. [Creación de una superficie SMS](#message-preset-sms)

Estos pasos debe realizarlos un Adobe Journey Optimizer [Administrador del sistema](../start/path/administrator.md).

## Requisitos previos{#sms-prerequisites}

Adobe Journey Optimizer se integra actualmente con proveedores externos que ofrecen servicios de mensajería de texto independientes de Adobe Journey Optimizer. Los proveedores admitidos para los mensajes de texto y MMS son: **Sinch**, **Twilio** y **Infobip**.

Antes de configurar el canal SMS, debe crear una cuenta con uno de estos proveedores para obtener su **Token de API** y **ID de servicio**, que es necesario configurar la conexión entre Adobe Journey Optimizer y el proveedor aplicable.

El uso de los servicios de mensajería de texto y MMS está sujeto a términos y condiciones adicionales del proveedor correspondiente. Como soluciones de terceros, Sinch, Twilio e Infobip están disponibles para los usuarios de Adobe Journey Optimizer a través de una integración. El Adobe no controla y no es responsable de los productos de terceros. Para cualquier problema o solicitud de asistencia relacionada con los servicios de mensajería de texto (SMS/MMS), póngase en contacto con su proveedor.

>[!CAUTION]
>
>Para acceder y editar subdominios SMS, debe tener los siguientes **[!UICONTROL Administrar subdominios de SMS]** en la zona protegida de producción. Obtenga más información acerca de los permisos en [esta página](../administration/high-low-permissions.md#administration-permissions).
>

