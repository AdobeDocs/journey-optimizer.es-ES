---
solution: Journey Optimizer
product: journey optimizer
title: Administración de la exclusión para mensajes de dispositivos móviles
description: Descubra cómo administrar la exclusión con mensajes SMS/MMS
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
TQID: https://experienceleague.adobe.com/mQVaZ8jb-hBBPxDnztkayDEI4vj0KvMTREI0KxOgAf0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7b5244e8bdbbe7458f283ac883cfaf1d695b332e
workflow-type: tm+mt
source-wordcount: 673
ht-degree: 14%

---

# Administración de la exclusión para mensajes de dispositivos móviles {#sms-opt-out}

De acuerdo con las normas y los reglamentos del sector, todos los mensajes SMS sobre marketing deben contener una forma para que los destinatarios puedan cancelar la suscripción fácilmente. [Más información acerca de la administración de la privacidad y la exclusión](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Las comunicaciones por mensajes móviles pueden estar sujetas a diversos requisitos legales de cumplimiento según su naturaleza, la ubicación desde la que se envían los mensajes móviles y la ubicación de los destinatarios. Mientras Adobe Journey Optimizer gestiona los mensajes con códigos cortos, códigos largos y números gratuitos, como se detalla a continuación, consulte a su asesor legal para asegurarse de que sus comunicaciones de mensajería móvil cumplan todos los requisitos legales aplicables.
>

## Palabras clave de entrada nativas {#sms-native-keywords}

>[!NOTE]
>
> Solo Sinch e Infobip admiten palabras clave nativas cuando se utilizan con Journey Optimizer.

De forma predeterminada, Adobe Journey Optimizer gestiona los siguientes mensajes de respuesta estándar en inglés para mensajes de códigos cortos, gratuitos y de código largo:

* **Exclusión**: DETENER, SALIR, CANCELAR, FINALIZAR, CANCELAR SUSCRIPCIÓN, NO.
* **Inclusión**: SUSCRIBIRSE, SÍ, NO DETENER, INICIAR, CONTINUAR, REANUDAR, INICIAR.
* **Ayuda**: HELP.

Estas palabras clave suelen almacenar en déclencheur una respuesta estándar automática de su proveedor de terceros. Puede confirmar esto directamente con su proveedor o a través de su sitio de documentación.

Cuando utilice Infobip, asegúrese de que la acción Reenvío está establecida en Configuración de extracción.

No se requiere ningún paso para garantizar que las funcionalidades de exclusión de SMS funcionen en Adobe Journey Optimizer, ya que STOP, UNSTOP, START, QUIT, CANCEL, END y UNSUBSCRIBE de las respuestas de palabras clave se reconocen automáticamente. Los estados de exclusión de perfiles se actualizan en tiempo real en Adobe Journey Optimizer.

Si define palabras clave de exclusión personalizadas en sus credenciales de API de SMS, anulan las palabras clave de entrada predeterminadas que se enumeran anteriormente. Para mantener funcionales las palabras clave predeterminadas, como STOP, QUIT, CANCEL, END y UNSUBSCRIBE, inclúyalas explícitamente junto con las palabras clave personalizadas en el campo Palabras clave de exclusión de la configuración de SMS. De lo contrario, solo se reconocerán las palabras clave personalizadas y las palabras clave predeterminadas dejarán de estar en déclencheur con las acciones de exclusión.

Tenga en cuenta que si un cliente responde STOP a un mensaje de Mobile, el proveedor bloquea todos los SMS posteriores a partir de ese ID de remitente específico (código corto o número largo), incluidos los mensajes transaccionales. Para garantizar el envío ininterrumpido de SMS transaccionales, utilice un ID de remitente independiente que no se haya excluido anteriormente.


>[!NOTE]
>
>Si planea utilizar SMS bidireccionales (responder con STOP, QUIT, etc.), asegúrese de que ha enviado primero al menos un SMS unidireccional para establecer el número de teléfono de asignación de perfiles. Las credenciales de proveedor caducadas o mal configuradas evitarán que las palabras clave entrantes actualicen el perfil del usuario, lo que dará como resultado registros de exclusión ausentes o retrasados. Las respuestas entrantes se almacenan en el conjunto de datos del sistema _AJO Inbound Activity Event Dataset_. [Más información](../data/get-started-datasets.md#system-datasets)


## Listas de bloqueados {#sms-blocklists}

Además de detener el envío con Adobe Journey Optimizer en función del estado de exclusión (para integraciones directas con Twilio, Infobip o Sinch), la mayoría de los proveedores de puertas de enlace por SMS también mantienen una lista de bloqueados que garantiza que un mensaje SMS no se envíe a una persona que haya elegido excluirse. Si utiliza un proveedor que no sea Sinch o Twilio y envía un SMS a través del [canal personalizado](../building-journeys/using-custom-actions.md), debe confirmarlo con su proveedor.


## Códigos cortos {#short-codes}

De forma predeterminada, Adobe Journey Optimizer no gestiona las palabras clave de inclusión o ayuda para los números de código corto. Para garantizar el cumplimiento de las normas del sector y las reglas para la gestión de la exclusión, es esencial verificar que el código corto cumpla todas las directrices.

Sin embargo, Journey Optimizer admite exclusiones globales basadas en palabras clave entrantes con distintos ID de remitente.

## ID de remitente alfanumérico {#alphanumeric}

Los ID de remitente alfanuméricos solo se utilizan en la mensajería unidireccional y no pueden recibir mensajes. Como resultado, STOP, START y HELP, las palabras clave de SMS de Adobe Journey Optimizer, no son aplicables a los ID de remitente de Alpha. Debe proporcionar otras instrucciones, como escribir al Equipo de Soporte, llamar a una línea telefónica de asistencia o enviar un mensaje de texto a otro número de teléfono o código para permitir a los usuarios excluirse de los mensajes enviados a través de un ID de remitente alfanumérico.

## Vídeo {#video-sms}

* El siguiente vídeo le ayuda a configurar la doble inclusión para SMS.

  +++ Vea el vídeo

  >[!VIDEO](https://video.tv.adobe.com/v/3440278/?captions=spa&learn=on)

  +++
