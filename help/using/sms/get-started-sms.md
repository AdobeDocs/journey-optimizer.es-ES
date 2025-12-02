---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los mensajes de texto (SMS/MMS/RCS)
description: Obtenga información sobre cómo crear y enviar mensajes de texto en Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
source-git-commit: de418dc4feefd99231155c550ad3a51e4850ee66
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 99%

---

# Introducción a la mensajería de texto {#get-started-sms}

Utilice [!DNL Journey Optimizer] para enviar mensajes de texto (SMS/MMS/RCS) a sus clientes en sus dispositivos móviles. Puede crear, personalizar y obtener una vista previa de los mensajes en formato de texto desde el editor de SMS/MMS/RCS.

Los mensajes de texto se pueden crear y enviar en un recorrido o en una campaña. Para SMS, MMS y RCS, utilice la acción SMS.

* En un **recorrido**. Cree un recorrido, añada una actividad SMS y defina la configuración básica. A continuación, vaya al panel derecho Acciones de SMS para crear el contenido del mensaje SMS, MMS o RCS. [Obtenga información sobre cómo crear un recorrido](../building-journeys/journey-gs.md)

* En una **campaña**. Cree una campaña, seleccione SMS como su acción y defina la configuración básica. A continuación, edite el contenido del mensaje para definir el mensaje SMS, MMS o RCS que desea enviar. Aprenda a crear [una campaña de acción](../campaigns/campaign-action.md#action-campaign-action) | [una campaña desencadenada por API](../campaigns/api-triggered-campaigns.md) | [una campaña orquestada](../orchestrated/create-orchestrated-campaign.md#create)

>[!IMPORTANT]
>
>Si es la primera vez que crea mensajes de texto, asegúrese de que el canal SMS esté configurado. [Más información](sms-configuration.md)

## Funciones de mensajería de texto {#sms-capabilities}

Adobe Journey Optimizer ofrece funciones completas de mensajería de texto para atraer a sus clientes a través de múltiples canales:

**SMS (servicio de mensajes cortos)**

Envíe mensajes de solo texto de hasta 160 caracteres. SMS es el formato de mensajería de texto más admitido en todos los dispositivos móviles.

**MMS (servicio de mensajes multimedia)**

Mejore su comunicación con contenido multimedia, incluidos vídeos, imágenes, clips de audio y GIF. Los mensajes MMS admiten hasta 1600 caracteres de texto además de archivos multimedia. [Más información sobre las limitaciones de MMS](../start/guardrails.md#sms-guardrails)

**RCS (servicios de comunicación enriquecidos)**

Envíe mensajes de marca interactivos con funciones avanzadas como carruseles, tarjetas enriquecidas, acciones sugeridas y compatibilidad multimedia mejorada. RCS ofrece una experiencia de mensajería más enriquecida en los dispositivos compatibles.

## Funciones principales {#key-features}

**Personalización y contenido dinámico**

Cree mensajes de texto personalizados mediante el editor de personalización. Añada atributos de perfil, contenido condicional y datos dinámicos para adaptar los mensajes a destinatarios individuales. [Más información sobre la personalización](../personalization/personalize.md)

**Compatibilidad con múltiples proveedores**

Adobe Journey Optimizer se integra con los principales proveedores de servicios de SMS:

* **Sinch** - [Guía de configuración](sms-configuration-sinch.md)
* **Twilio** - [Guía de configuración](sms-configuration-twilio.md)
* **Infobip** - [Guía de configuración](sms-configuration-infobip.md)
* **Proveedores personalizados**: configure cualquier otro proveedor de SMS mediante la integración de API personalizada. [Más información](sms-configuration-custom.md)

**Acortamiento y seguimiento de URL**

Añada URL abreviadas y rastreables a sus mensajes para monitorizar la participación. Se requiere la configuración del subdominio para la funcionalidad de acortamiento de URL. [Más información sobre cómo configurar subdominios de SMS](sms-subdomains.md)

**Administración de exclusión**

Garantice el cumplimiento de las normas y regulaciones del sector mediante la administración de exclusión integrada. Journey Optimizer gestiona automáticamente las palabras clave de exclusión estándar (STOP, QUIT, CANCEL, etc.) para los proveedores de Sinch e Infobip. [Más información sobre la administración de exclusión](sms-opt-out.md)

**Vista previa y pruebas**

Pruebe los mensajes de texto antes de enviarlos mediante perfiles de prueba y datos de muestra. Obtenga una vista previa de la personalización, el contenido y el formato para garantizar que los mensajes se muestren correctamente. [Más información sobre cómo enviar mensajes](send-sms.md)

**Sistema de informes y análisis**

Realice un seguimiento del rendimiento de sus campañas y recorridos de SMS con funciones del sistema de informes completas:

* [Informes de campaña de SMS](../reports/campaign-global-report-cja-sms.md)
* [Informes de recorrido de SMS](../reports/journey-global-report-cja-sms.md)

## Requisitos para la configuración {#configuration-requirements}

Antes de enviar mensajes de texto, debe:

1. **Elegir un proveedor de SMS**: seleccione entre Sinch, Twilio, Infobip o configure un proveedor personalizado
2. **Configurar credenciales de API**: integre los tokens de API y los ID de servicio del proveedor con Journey Optimizer
3. **Crear configuraciones de canal**: realice configuraciones de SMS para mensajes de marketing y transaccionales
4. **Configurar subdominios (opcional)**: necesario únicamente si piensa utilizar el acortamiento de URL en los mensajes

Estos pasos de configuración los suele realizar un administrador del sistema. [Introducción a la configuración de SMS](sms-configuration.md)

## Guía de inicio rápido {#quick-start}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="sms-configuration.md">
<img alt="Validación" src="../assets/do-not-localize/sms-config.jpg">
</a>
<div>
<a href="sms-configuration.md"><strong>Configuración del canal de SMS</strong></a>
</div>
<p>Configure su proveedor de SMS y las configuraciones de canal</p>
</td>
<td>
<a href="create-sms.md">
<img alt="Posible cliente" src="../assets/do-not-localize/sms-create.jpeg">
</a>
<div><a href="create-sms.md"><strong>Creación de un mensaje de texto</strong></a>
</div>
<p>Diseñe y personalice el contenido de SMS, MMS o RCS</p>
</td>
<td>
<a href="send-sms.md">
<img alt="Poco frecuente" src="../assets/do-not-localize/sms-sending.jpg">
</a>
<div>
<a href="send-sms.md"><strong>Vista previa y envío</strong></a>
</div>
<p>Pruebe y envíe mensajes de texto a su público</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="Validación" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong>Administrar exclusiones</strong></a>
</div>
<p>Gestione solicitudes de cancelación de suscripción y garantice el cumplimiento</p>
</td>
</tr></table>

## Recursos adicionales {#additional-resources}

Examine los temas siguientes para obtener más información sobre la mensajería de texto en Journey Optimizer.

+++Guías de configuración

Obtenga información sobre cómo establecer y configurar su entorno de SMS:

* [Información general sobre la configuración del canal SMS](sms-configuration.md)
* [Creación de configuraciones de canal SMS](sms-configuration-surface.md)
* [Configuración de subdominios SMS para acortar la dirección URL](sms-subdomains.md)

+++

+++Guías de configuración del proveedor

Configuración paso a paso para cada proveedor de servicios SMS:

* [Configuración del proveedor de Sinch](sms-configuration-sinch.md)
* [Configuración del proveedor de Twilio](sms-configuration-twilio.md)
* [Configuración del proveedor de Infobip](sms-configuration-infobip.md)
* [Configuración de un proveedor de SMS personalizado](sms-configuration-custom.md)

+++

+++Creación y administración de contenido

Cree, personalice y administre su contenido de mensaje de texto:

* [Creación de mensajes SMS/MMS](create-sms.md)
* [Vista previa, prueba y envío de mensajes](send-sms.md)
* [Personalización en los mensajes de texto](../personalization/personalize.md)
* [Contenido dinámico](../personalization/get-started-dynamic-content.md)
* [Generación de contenido SMS con el asistente de IA](../content-management/generative-text.md)

+++

+++Cumplimiento y privacidad

Asegúrese de que la mensajería de texto cumpla con las regulaciones y las normas de privacidad:

* [Administración de exclusiones](sms-opt-out.md)
* [Privacidad y consentimiento](../privacy/opt-out.md#opt-out-decision-management)

+++

+++Seguimiento del rendimiento

Monitorice y analice sus campañas de SMS y el rendimiento del recorrido:

* [Informes de campaña de SMS](../reports/campaign-global-report-cja-sms.md)
* [Informes de recorrido de SMS](../reports/journey-global-report-cja-sms.md)

+++

+++Integración de recorridos y campañas

Aprenda a incorporar SMS a sus recorridos y campañas de clientes:

* [Añadir mensajes SMS a los recorridos](../building-journeys/journeys-message.md)
* [Crear campañas de SMS](../campaigns/create-campaign.md)

+++

## Vídeotutoriales {#videos}

**Configurar y enviar mensajes SMS**

Obtenga información sobre cómo configurar, crear e incluir mensajes SMS en sus recorridos de cliente.

+++Vea el vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3420509?learn=on)

+++

**Explorar las funcionalidades de mensajería móvil**

Descubra las funcionalidades completas de mensajería móvil que Adobe Journey Optimizer ofrece a los expertos en marketing.

+++Vea el vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3426021?quality=12&learn=on)

+++

**Enviar mensajes RCS de marca**

Aprenda a configurar y enviar mensajes RCS interactivos de marca en Adobe Journey Optimizer mediante un proveedor de SMS personalizado.

+++Vea el vídeo

>[!VIDEO](https://video.tv.adobe.com/v/3464755)

+++

**Temas relacionados**

* [Adición de mensajes a los recorridos](../building-journeys/journeys-message.md)
* [Creación de campañas de marketing](../campaigns/create-campaign.md)
* [Mecanismos de protección y limitaciones](../start/guardrails.md#sms-guardrails)
* [Tutoriales de SMS y mensajería móvil](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/tutorials/channels/sms-channel/sms-mms-messages-overview){target="_blank"}
