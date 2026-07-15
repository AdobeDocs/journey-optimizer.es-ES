---
title: Introducción a los canales personalizados
description: Aprenda a usar  [!DNL Journey Optimizer]'s Channel Builder to bring any outbound messaging channel into [!DNL Journey Optimizer] y utilícelo en campañas, recorridos y campañas orquestadas.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---


# Introducción a los canales personalizados {#get-started-custom-channel}

>[!AVAILABILITY]
>
>Esta funcionalidad tiene disponibilidad limitada. Póngase en contacto con su representante de Adobe para obtener acceso.

<!--Multilingual support, business rules enforcement, and [!DNL Adobe Experience Decisioning] integration are planned for a future release.-->

La funcionalidad **Canales personalizados** de [!DNL Journey Optimizer] le permite llevar cualquier canal de salida a [!DNL Journey Optimizer] para que pueda usarlo en campañas, recorridos y campañas orquestadas, igual que cualquier canal nativo. Con **Channel Builder**, los administradores pueden crear y configurar nuevos canales sin necesidad de recurrir a técnicos, y los especialistas en mercadotecnia pueden empezar a utilizarlos inmediatamente para comunicarse con los clientes.

## ¿Qué problema resuelve? {#why-custom-channels}

[!DNL Journey Optimizer] admite de forma nativa el correo electrónico, los SMS, las notificaciones push, WhatsApp, LINE y otros canales. Sin embargo, muchas organizaciones utilizan plataformas de mensajería que no están integradas de forma nativa (como WeChat, Kakao Talk, Messenger o un proveedor externo) y desean usarlas en [!DNL Journey Optimizer] para la orquestación y la creación de campañas mientras siguen entregando con su propio proveedor.

<!--TBC: Another use case is when organizations have a legacy messaging gateway that exposes an HTTP endpoint, and they want to use it in [!DNL Journey Optimizer] without having to build a custom integration.-->

Los canales personalizados llenan este vacío: permiten usar cualquier extremo HTTP saliente como un canal [!DNL Journey Optimizer] completo, desbloqueando:

* **Funcionalidades de canal completo**: optimización (experimentación y direccionamiento de contenido), informes y monitorización de OOTB, aplicación de consentimiento y gobernanza, y fragmentos de expresión. <!--Multilingual and business rules are planned for a future release.-->
* **Organización unificada**: administre todos sus canales de mensajería en un solo lugar, independientemente del proveedor de envío subyacente.
* **Configuración sin código**: los administradores configuran el canal a través de la interfaz de usuario de Channel Builder; no se requiere código personalizado ni esfuerzo de ingeniería.

## Canal personalizado frente a acciones personalizadas {#custom-channel-vs-custom-action}

Si ya ha usado [acciones personalizadas](../action/action.md) en [!DNL Journey Optimizer] recorridos, los canales personalizados tratan un conjunto diferente de casos de uso.

**Usa canales personalizados cuando** necesites enviar mensajes a los usuarios finales a través de una plataforma no admitida de forma nativa en [!DNL Journey Optimizer], como WeChat, Kakao Talk o una puerta de enlace de mensajería personalizada. Los canales personalizados están disponibles en campañas, recorridos y campañas orquestadas, y son compatibles con:

* Personalización completa a través del editor de personalización, similar a los canales salientes nativos
* Editor de carga útil visual/de formulario, previsualización y prueba
* Experimentación y direccionamiento de contenido
* Informes y monitorización de OOTB
* Varias credenciales de API y configuraciones de canal
* RBAC/ABAC

Los canales personalizados admiten POST como el único método HTTP.

**Use acciones personalizadas cuando** necesite recuperar datos o insertar información en un sistema externo (como un centro de llamadas, una plataforma de registro o una base de datos sin conexión) como paso dentro de un recorrido. Las acciones personalizadas solo están disponibles en recorrido y admiten los métodos GET, PUT y POST.

<!--
| | Custom Action | Custom Channel |
| --- | --- | --- |
| **Primary use case** | Retrieve data from or send information to external systems (call centers, offline systems, logging) | Send messages to end users through channels not natively supported in [!DNL Journey Optimizer] |
| **Available in** | Journeys only | Campaigns, journeys, and orchestrated campaigns |
| **Supported HTTP methods** | GET, PUT, POST | POST only |
| **Full personalization (PE)** | No | Yes, through the personalization editor, similar to native outbound channels |
| **Visual/form editor** | No | Yes |
| **Preview and proof** | No | Yes |
| **Content experimentation** | No | Yes |
| **Targeting** | No | Yes |
| **OOTB Reporting** | Yes | Yes |
| **Multiple API credentials and channel configurations** | No | Yes |
| **RBAC/ABAC** | No | Yes |
-->

>[!TIP]
>
>Como recomendación general, utilice canales personalizados para casos de uso de canales en los que esté enviando mensajes a usuarios finales. Para otros casos de uso similares a conectores que son necesarios en los recorridos, como la recuperación de datos o la activación de sistemas externos, puede seguir utilizando acciones personalizadas.

## Casos de uso {#use-cases}

Los canales personalizados son ideales para:

* **Plataformas de mensajería no compatibles** - Canales como WeChat, Kakao Talk, Messenger, Telegram o servicios de mensajería regionales que no tienen un canal [!DNL Journey Optimizer] nativo.
* **Proveedores de envío personalizados**: organizaciones que han invertido en un proveedor externo que desean seguir usando para el envío de mensajes, pero que prefieren aprovechar [!DNL Journey Optimizer] para la orquestación, personalización y administración de campañas.
* **Canales heredados**: puertas de enlace de mensajería propietarias o heredadas que exponen un extremo HTTP.
* **Canales específicos del sector**: mensajes seguros para la atención médica, los sistemas de alerta bancaria o los servicios de notificación del gobierno.

## Funcionamiento {#how-it-works}

La configuración y el uso de un canal personalizado siguen las etapas principales a continuación:

1. **Configurar** (administrador): un administrador crea un canal personalizado en el **Generador de canales**, y define el punto de conexión, la autenticación, la directiva de restricción y la estructura de carga del mensaje. A continuación, se crea una configuración de canal y se vincula al canal personalizado. [Más información](configure-custom-channel.md)
1. **Crear** (especialista en marketing): un especialista en marketing agrega el canal personalizado a un recorrido, a una campaña o a una campaña orquestada, selecciona una configuración de canal y crea la carga útil del mensaje con el editor de personalización de [!DNL Journey Optimizer]. [Más información](create-custom-experience.md)
1. **Enviar**: cuando un perfil se califica, [!DNL Journey Optimizer] envía la carga útil personalizada al extremo configurado. El sistema externo procesa la llamada y envía el mensaje.
1. **Supervisar** (Administrador/Especialista en mercadotecnia): los administradores y los especialistas en mercadotecnia pueden supervisar el rendimiento y la confiabilidad del canal personalizado mediante los paneles de informes y supervisión de [!DNL Journey Optimizer]. [Más información](monitor-custom-channel.md)

<!--
## Next steps {#next-steps}

* Review the prerequisites and permissions before setting up your first custom channel. [Learn more](custom-channel-prerequisites.md)
* Configure your first custom channel using the Channel Builder. [Learn more](custom-channel-configuration.md)
* Create a custom channel experience in a journey or campaign. [Learn more](create-custom-experience.md)
-->
