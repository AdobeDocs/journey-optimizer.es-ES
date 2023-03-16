---
solution: Journey Optimizer
product: journey optimizer
title: Administración de exclusión de SMS
description: Obtenga información sobre cómo administrar la exclusión con mensajes SMS
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 63237c02f632d289dba845acdcd0859f2d6de9c9
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 31%

---

# Administración de exclusión de SMS {#sms-opt-out}

De acuerdo con las normas y los reglamentos del sector, todos los mensajes SMS sobre marketing deben contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. [Obtenga más información sobre la administración de privacidad y exclusión](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Las comunicaciones de mensajes de texto pueden estar sujetas a diversos requisitos legales de conformidad según su naturaleza, la ubicación desde la que envía los mensajes de texto y la ubicación de los destinatarios. Aunque Adobe Journey Optimizer gestiona los mensajes con códigos largos y números gratuitos como se detalla a continuación, consulte a su asesor jurídico para asegurarse de que las comunicaciones de mensajes de texto cumplen todos los requisitos legales aplicables.

## Palabras clave de entrada nativas{#sms-native-keywords}

De forma predeterminada, Adobe Journey Optimizer gestiona los siguientes mensajes de respuesta en inglés estándar para los mensajes de código libre y de código largo: STOP, UNSTOP, START, QUIT, CANCEL, END y UNSUBSCRIBE. Tenga en cuenta que solo Sinch admite palabras clave nativas cuando se utiliza con Journey Optimizer.

Estas palabras clave normalmente dan déclencheur a una respuesta estándar automática de su proveedor de terceros. Puede confirmar esto directamente con su proveedor o a través de su sitio de documentación.

No se requieren pasos para garantizar que las funcionalidades de exclusión de SMS funcionen en Adobe Journey Optimizer, ya que las respuestas de palabra clave STOP, UNSTOP, START, QUIT, CANCEL, END y UNSUBSCRIBE se reconocen automáticamente. Los estados de exclusión de perfiles se actualizan en tiempo real en Adobe Journey Optimizer.


## Listas de bloqueados{#sms-blocklists}

Además de detener el envío mediante Adobe Journey Optimizer en función del estado de exclusión (para integraciones directas con Twilio o Sinch), la mayoría de los proveedores de pasarelas SMS también mantienen una lista de bloqueados que garantiza que no se envíe un mensaje SMS a una persona que haya elegido excluirse. Si utiliza un proveedor que no sea Sinch o Twilio y envía un SMS a través de [canal personalizado](../building-journeys/using-custom-actions.md), debe confirmarlo con su proveedor.


## Códigos cortos {#short-codes}

De forma predeterminada, Adobe Journey Optimizer no gestiona las palabras clave de inclusión o de ayuda para números de código cortos. Para garantizar el cumplimiento de las regulaciones y reglas del sector para la gestión de la exclusión, es esencial verificar que su código corto se adhiera a todas las directrices.

Sin embargo, Journey Optimizer sí admite exclusiones globales basadas en palabras clave entrantes con diferentes ID de remitente.

## ID de remitente alfanumérico {#alphanumeric}

Los ID de remitente alfanuméricos solo se utilizan en la mensajería unidireccional y no pueden recibir mensajes. Como resultado, STOP, START y HELP, las palabras clave de SMS de Adobe Journey Optimizer, no son aplicables a los ID de remitente alfa. Debe proporcionar otras instrucciones, como escribir al Equipo de Soporte, llamar a una línea telefónica de asistencia o enviar un mensaje de texto a otro número de teléfono o código para permitir a los usuarios excluirse de los mensajes enviados a través de un ID de remitente alfanumérico.

## Vídeo {#video-sms}

Para obtener más información sobre cómo funciona la compatibilidad con palabras clave entrantes nativas (START, STOP y UNSTOP) para SMS, mire el siguiente vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
