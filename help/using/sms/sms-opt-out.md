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
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 96%

---

# Administración de exclusión de SMS {#sms-opt-out}

De acuerdo con las normas y los reglamentos del sector, todos los mensajes SMS sobre marketing deben contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. [Obtenga más información sobre la administración de privacidad y exclusión](../privacy/opt-out.md)

De forma predeterminada, Adobe Journey Optimizer gestiona mensajes de respuesta estándar en inglés como STOP, UNSTOP y START para mensajes de código largo y gratuito, de acuerdo con los estándares del sector para la integración nativa como Sinch y Twilio. Estas palabras clave suelen activar una respuesta estándar automática de su proveedor de terceros (p. ej., Twilio, Sinch, etc.). Puede confirmar esto directamente con su proveedor o a través de su sitio de documentación.

No se necesita hacer nada más para garantizar que las funcionalidades de exclusión de SMS funcionen en Adobe Journey Optimizer, ya que STOP, UNSTOP y START, las respuestas de palabras clave, se reconocerán automáticamente.

Además de detener el envío con Adobe Journey Optimizer en función del estado de exclusión (para integraciones directas con Twilio o Sinch), la mayoría de los proveedores de puertas de enlace por SMS también mantienen una lista de bloqueados que garantiza que un mensaje SMS no se va a enviar a una persona que haya elegido excluirse. Si utiliza un proveedor que no sea Sinch o Twilio y envía un SMS a través de un [canal personalizado](../building-journeys/using-custom-actions.md), debe confirmarlo con su proveedor.

>[!IMPORTANT]
>
>Las campañas de mensajería de texto pueden estar sujetas a diversos requisitos legales de cumplimiento según su naturaleza, la ubicación desde la que se envían los mensajes de texto y la ubicación de los destinatarios. <br>Aunque Adobe Journey Optimizer gestionará los mensajes en códigos largos y números gratuitos, tal y como se detalla más arriba, consulte a su asesor jurídico para asegurarse de que su campaña de mensajería de texto cumpla todos los requisitos legales aplicables.

## Códigos cortos {#short-codes}

De forma predeterminada, Adobe Journey Optimizer no gestiona las palabras clave de exclusión, inclusión o ayuda para los números de código corto.

Debe asegurarse de que el código corto cumpla todas las normas y regulaciones del sector para gestionar la exclusión.

## ID de remitente alfanumérico {#alphanumeric}

Los ID de remitente alfanuméricos solo se utilizan en la mensajería unidireccional y no pueden recibir mensajes. Como resultado, STOP, START y HELP, las palabras clave de SMS de Adobe Journey Optimizer, no son aplicables a los ID de remitente alfa. Debe‧proporcionar‧otras‧instrucciones,‧como‧escribir‧al‧Equipo‧de‧Soporte,‧llamar‧a‧una‧línea‧telefónica‧de‧asistencia‧o‧enviar‧un‧mensaje‧de‧texto‧a‧otro‧número‧de‧teléfono‧o‧código‧para‧permitir‧a‧los‧usuarios‧excluirse‧de‧los‧mensajes‧enviados‧a‧través‧de‧un‧ID‧de‧remitente‧alfanumérico.

## Vídeo {#video-sms}

Para obtener más información sobre cómo funciona la compatibilidad con palabras clave entrantes nativas (START, STOP y UNSTOP) para SMS, mire el siguiente vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
