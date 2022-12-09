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
ht-degree: 0%

---

# Administración de exclusión de SMS {#sms-opt-out}

De acuerdo con las normas y regulaciones del sector, todos los mensajes de marketing SMS deben contener una forma para que los destinatarios puedan cancelar su suscripción fácilmente. [Obtenga más información sobre la administración de privacidad y exclusión](../privacy/opt-out.md)

De forma predeterminada, Adobe Journey Optimizer gestiona mensajes de respuesta en inglés estándar como STOP, UNSTOP y START para mensajes de código largo y gratuito, de acuerdo con los estándares del sector para la integración nativa como Sinch y Twilio. Estas palabras clave suelen activar una respuesta estándar automática de su proveedor de terceros (por ejemplo, Twilio, Sinch, etc.). Puede confirmarlo directamente con su proveedor o a través de su sitio de documentación.

No se requieren pasos para garantizar que las capacidades de exclusión de SMS funcionen en Adobe Journey Optimizer, ya que las respuestas de palabras clave STOP, UNSTOP y START se reconocerán automáticamente.

Además de detener el envío en Adobe Journey Optimizer en función del estado de exclusión (para integraciones directas con Twilio o Sinch), la mayoría de los proveedores de pasarelas SMS también mantienen una lista de bloqueados que garantiza que no se envíe un mensaje SMS a una persona que haya elegido la exclusión. Si utiliza un proveedor que no sea Sinch o Twilio y envía un SMS a través de [canal personalizado](../building-journeys/using-custom-actions.md), debe confirmarlo con su proveedor.

>[!IMPORTANT]
>
>Las campañas de mensajes de texto pueden estar sujetas a diversos requisitos legales de cumplimiento según la naturaleza de la campaña de mensajería de texto, la ubicación desde la que envía los mensajes de texto y la ubicación de los destinatarios. <br>Aunque Adobe Journey Optimizer gestionará los mensajes con códigos largos y números de teléfono gratuitos como se detalla más arriba, debe consultar a su asesor jurídico para asegurarse de que su campaña de mensajería de texto cumpla todos los requisitos legales aplicables.

## Códigos cortos {#short-codes}

De forma predeterminada, Adobe Journey Optimizer no gestiona las palabras clave de exclusión, inclusión o ayuda para los números de código cortos.

Debe asegurarse de que su código corto cumpla todas las reglas y regulaciones del sector para la gestión de la exclusión.

## ID de remitente alfanumérico {#alphanumeric}

Los ID de remitente alfanuméricos solo son para mensajería unidireccional y no pueden recibir mensajes entrantes. Como resultado, las palabras clave STOP, START y HELP de Adobe Journey Optimizer no son aplicables a los ID de remitente alfa. Debe proporcionar otras instrucciones, como escribir al equipo de asistencia técnica, llamar a una línea telefónica de asistencia o enviar un mensaje de otro número de teléfono o código para permitir a los usuarios desactivar los mensajes enviados a través de un ID de remitente alfanumérico.

## Vídeo {#video-sms}

Para obtener más información sobre cómo funciona la compatibilidad con palabras clave entrantes nativas (START, STOP y UNSTOP) para SMS, consulte el siguiente vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
