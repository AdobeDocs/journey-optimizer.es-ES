---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a los mensajes móviles
description: Obtenga información sobre cómo crear y enviar mensajes móviles en Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
TQID: https://experienceleague.adobe.com/Ev0xJ86fpweQxgf-VjGUEl4ebk6BdzhVof2BgiMR9EM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c13ff12d-60f1-49cd-833a-d43359628223
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 1314
ht-degree: 19%

---

# Introducción a los mensajes móviles {#get-started-sms}

>[!BEGINSHADEBOX]

**En esta página:** Empiece a utilizar la mensajería móvil en Adobe Journey Optimizer para crear, personalizar y enviar mensajes SMS, MMS y RCS en recorridos y campañas, incluida la compatibilidad con proveedores, los requisitos de configuración y los requisitos previos de RCS.

>[!ENDSHADEBOX]

Use [!DNL Journey Optimizer] para enviar mensajes móviles a sus clientes a través de tres canales, **SMS**, **MMS** y **RCS**, desde un solo editor de SMS/MMS/RCS donde podrá crear, personalizar y previsualizar su contenido.

* **SMS (servicio de mensajes cortos)**: envía mensajes de texto de hasta 160 caracteres, compatibles con todos los dispositivos móviles.
* **MMS (Servicio de mensajes multimedia)**: enriquece tus mensajes con imágenes, vídeos, clips de audio y GIF, además de hasta 1.600 caracteres de texto. [Más información sobre las limitaciones de MMS](../start/guardrails.md#sms-guardrails)
* Contenido interactivo de **RCS (servicios de comunicación enriquecidos)**:Deliver de marca directamente en la aplicación de mensajería nativa de sus clientes, sin que se requiera una descarga de aplicación adicional.

>[!IMPORTANT]
>
>Si es la primera vez que crea mensajes para móviles, asegúrese de que el canal de mensajes para móviles esté configurado. [Más información](mobile-configuration.md)

Los mensajes móviles se pueden crear y enviar en un recorrido o en una campaña mediante la acción Mensaje móvil:

* En un **Recorrido**: agrega una acción de mensaje móvil al recorrido, define la configuración básica y redacta el contenido en el panel Acciones de mensajes móviles de la derecha. [Obtenga información sobre cómo crear un recorrido](../building-journeys/journey-gs.md)

* En una **campaña**:Create de una campaña, selecciona Mensaje móvil como acción, define la configuración básica y edita el contenido del mensaje. Aprenda a crear [una campaña de acción](../campaigns/campaign-action.md#action-campaign-action) | [una campaña desencadenada por API](../campaigns/api-triggered-campaigns.md) | [una campaña orquestada](../orchestrated/create-orchestrated-campaign.md#create)

## Casos de uso {#use-cases}

Los SMS, MMS y RCS funcionan mejor cuando necesita llegar a los usuarios de forma fiable, independientemente de si tienen la aplicación instalada o hay una conexión a Internet disponible.

| Ventaja | Por qué | Casos de uso de ejemplo |
| --- | --- | --- |
| Alcance máximo e inmediatez | No se requiere ninguna aplicación o conexión a Internet para recibir el mensaje | Llegar a usuarios sin una aplicación de smartphone instalada |
| Visibilidad garantizada | Los SMS tienen tasas abiertas superiores al 90 % | Códigos OTP, recordatorios de citas y notificaciones de entregas |
| Contenido enriquecido mediante MMS/RCS | Agrega imágenes, vídeo y elementos interactivos más allá del texto sin formato | Promociones de marca, catálogos de productos |
| Llegar a usuarios sin acceso a la aplicación | Funciona para destinatarios que no han instalado o abierto la aplicación | Volver a atraer a los usuarios de aplicaciones caducadas e incorporar clientes que no sean de aplicaciones |
| CTA de alta urgencia | Entregado directamente a un dispositivo que los usuarios comprueban con frecuencia | Ventas Flash, alertas de fraude, avisos de interrupción del servicio |
| Capas con otros canales | Complementa la mensajería push, por correo electrónico y en la aplicación para una cobertura más amplia | Recorridos multicanal con SMS como canal de reserva |

## Cuándo no utilizar {#when-not-to-use}

SMS, MMS y RCS no siempre son la opción más eficiente o adecuada. Considere otro canal en las siguientes situaciones:

* El coste es motivo de preocupación debido a los altos volúmenes de envío, ya que los SMS y MMS se facturan por mensaje y los costes por mensaje se acumulan rápidamente a escala
* El contenido es largo o complejo y se adapta mejor al correo electrónico, que admite un formato más enriquecido y texto más largo
* Los destinatarios no se han suscrito explícitamente, lo que conlleva riesgos legales y de cumplimiento en la mayoría de las regiones y regulaciones de mensajería

## Funciones principales {#key-features}

| Función | Descripción |
|---|---|
| **Personalización** | Personalice mensajes con atributos de perfil, contenido condicional y datos dinámicos mediante el editor de personalización. [Más información](../personalization/personalize.md) |
| **Soporte técnico para proveedores** | Conéctese con [Sinch](mobile-configuration-sinch.md), [Twilio](mobile-configuration-twilio.md), [Infobip](mobile-configuration-infobip.md) o cualquier [proveedor personalizado](mobile-configuration-custom.md) a través de la integración de API. |
| **Acortamiento de URL** | Añada direcciones URL abreviadas y rastreables para supervisar la participación. Requiere la configuración de subdominios. [Más información](mobile-subdomains.md) |
| **Administración de exclusión** | Gestión integrada de palabras clave de exclusión estándar (STOP, QUIT, CANCEL, etc.) para Sinch e Infobip. [Más información](mobile-opt-out.md) |
| **Vista previa y pruebas** | Valide el contenido con perfiles de prueba y datos de muestra antes de enviarlo. [Más información](send-mobile-message.md) |
| **Creación de informes** | Rastree el rendimiento de la campaña y del recorrido con [informes de campaña](../reports/campaign-global-report-cja-sms.md) y [informes de recorrido](../reports/journey-global-report-cja-sms.md) dedicados. |

## Requisitos para la configuración {#configuration-requirements}

Antes de enviar mensajes de Mobile, debe:

1. **Elige un proveedor de SMS**: selecciona entre Sinch, Twilio, Infobip o configura un proveedor personalizado
2. **Configurar credenciales de API**: integre los tokens de API y los identificadores de servicio de su proveedor con Journey Optimizer
3. **Crear configuraciones de canal**: configure las configuraciones de SMS para los mensajes transaccionales y de marketing
4. **Configurar subdominios (opcional)**: Necesario solo si planea utilizar el acortamiento de URL en los mensajes

Estos pasos de configuración los suele realizar un administrador del sistema. [Introducción a la configuración de SMS](mobile-configuration.md)

### Requisitos para RCS {#requirement-rcs}

Se requieren los siguientes requisitos previos para utilizar RCS en Journey Optimizer:

* **Credenciales de API de RCS de Sinch**: un administrador debe configurar las credenciales de API para el proveedor de RCS de Sinch (ID de proyecto, ID de aplicación y token de API). [Más información](mobile-configuration-sinch.md)
* **Configuración del canal de mensajes móviles**: un administrador debe crear una configuración de canal con una credencial RCS activada, de modo que los mensajes se envíen como RCS en lugar de como SMS. [Más información](mobile-configuration.md)
* **SMS de reserva**: Recomendado. Los destinatarios cuyos dispositivos no admiten RCS no recibirán el mensaje a menos que la reserva de SMS esté disponible. Los clientes sin volumen de SMS existente deben comprar SMS y un código corto. [Más información](design-mobile.md#rcs-content)
* **Proveedor compatible**: la creación nativa de RCS requiere RCS de Sinch (reventa o directa de Adobe). Twilio, Infobip y otros proveedores deben utilizar una integración de proveedor personalizada.
* **Compatibilidad con dispositivos**: la entrega RCS es compatible con dispositivos Android y iOS. La disponibilidad regional y de los operadores varía, y el RCS no está disponible de forma universal en todo el mundo.

## Recursos adicionales {#additional-resources}

Examine los temas siguientes para obtener más información sobre la mensajería móvil en Journey Optimizer. Consulte también la [descripción general de SMS/MMS/RCS](https://experienceleague.adobe.com/es/docs/journey-optimizer-learn/mobile-learning-hub/mobile-channels-overview/sms-mms-rcs-overview){target="_blank"} en el centro de aprendizaje móvil para ver más casos de uso y prácticas recomendadas.

+++Guías de configuración

Obtenga información sobre cómo establecer y configurar su entorno de SMS:

* [Información general sobre la configuración del canal SMS](mobile-configuration.md)
* [Creación de configuraciones de canal SMS](mobile-configuration-surface.md)
* [Configuración de subdominios SMS para acortar la dirección URL](mobile-subdomains.md)

+++

+++Guías de configuración del proveedor

Configuración paso a paso para cada proveedor de servicios SMS:

* [Configuración del proveedor de Sinch](mobile-configuration-sinch.md)
* [Configuración del proveedor de Twilio](mobile-configuration-twilio.md)
* [Configuración del proveedor de Infobip](mobile-configuration-infobip.md)
* [Configuración de un proveedor de SMS personalizado](mobile-configuration-custom.md)

+++

+++Creación y administración de contenido

Cree, personalice y administre su contenido de mensajes de Mobile:

* [Creación de mensajes SMS/RCS/MMS](create-mobile-message.md)
* [Vista previa, prueba y envío de mensajes](send-mobile-message.md)
* [Personalization en mensajes móviles](../personalization/personalize.md)
* [Contenido dinámico](../personalization/get-started-dynamic-content.md)
* [Generación de contenido de SMS con el Asistente de IA](../content-management/generative-text.md)

+++

+++Cumplimiento y privacidad

Asegúrese de que la mensajería móvil cumpla con las regulaciones y los estándares de privacidad:

* [Administración de exclusiones](mobile-opt-out.md)
* [Privacidad y consentimiento](../privacy/opt-out.md#opt-out-decision-management)

+++

+++Seguimiento del rendimiento

Monitorice y analice sus campañas de SMS y el rendimiento del recorrido:

* [Informes de campaña de SMS](../reports/campaign-global-report-cja-sms.md)
* [Informes de recorrido de SMS](../reports/journey-global-report-cja-sms.md)

+++

+++Integración de recorridos y campañas

Aprenda a incorporar SMS a sus recorridos y campañas de clientes:

* [Añadir mensajes SMS a los recorridos](../building-journeys/journey-action.md)
* [Crear campañas de SMS](../campaigns/create-campaign.md)

+++

+++Preguntas frecuentes sobre RCS

**¿Está disponible la mensajería RCS nativa con Twilio o Infobip?**

No. El diseñador RCS nativo de Journey Optimizer no está disponible cuando se utilizan proveedores de SMS de terceros como Twilio o Infobip. Sin embargo, los mensajes RCS se pueden enviar mediante una [integración de proveedor personalizado](mobile-configuration-custom.md).

**¿Por qué comprar SMS junto con RCS?**

Se debe comprar un volumen de SMS y un código corto para habilitar la reserva de SMS, que es la ruta recomendada. Si no se configura SMS, los perfiles cuyo dispositivo o operador no admita RCS no recibirán el mensaje.

**¿Está disponible la mensajería RCS nativa para los clientes directos de Sinch?**

Sí. Los clientes que utilizan la API de conversación de Sinch tienen acceso a la creación de RCS nativa, incluidos los clientes de reventa de Adobe y los clientes directos de Sinch.

**¿Hay RCS disponible en todas partes?**

No. La adopción de operadores sigue creciendo a nivel mundial, pero RCS no tiene un soporte universal en todos los operadores y regiones. Se debe investigar la disponibilidad regional y la compatibilidad con operadores cuando se planifiquen campañas de RCS.

**¿Dónde aparecen los mensajes RCS en el dispositivo?**

Los mensajes RCS aparecen en el mismo lugar que los mensajes SMS estándar, en la aplicación de mensajería nativa del dispositivo. Llegan de un remitente verificado y de marca, lo que proporciona a los destinatarios las señales de confianza para saber que el mensaje es legítimo.

**¿Cuáles son los límites de caracteres de un mensaje RCS?**

Los tipos de mensajes multimedia enriquecidos (únicos) admiten hasta 3072 caracteres, mucho más que el límite de 160 caracteres para los SMS estándar. Los tipos de mensajes RCS básicos están limitados a 160 caracteres, que coinciden con el límite estándar de SMS.

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
