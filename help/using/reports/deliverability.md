---
solution: Journey Optimizer
product: journey optimizer
title: Introducción a la Entregabilidad
description: Conozca las directrices de entrega
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 13%

---

# Introducción a la Entregabilidad {#manage-deliverability}

La capacidad de entrega es una medida del éxito de los envíos que llegan a las bandejas de entrada de los destinatarios.

>[!NOTE]
>
>Para los clientes que obtienen una licencia de Healthcare Shield, Adobe utiliza Transport Layer Security (TLS) 1.2 para proteger el intercambio de datos entre los sistemas de los usuarios (destinatarios) y Journey Optimizer (remitente). Si el servidor de correo receptor no es compatible con TLS 1.2, los clientes experimentarán problemas de envío, incluido el rebote de correo electrónico al remitente original.

**Entrega de correo electrónico** hace referencia al conjunto de características que determinan la capacidad de un mensaje para llegar a su destino a través de una dirección de correo electrónico personal, en poco tiempo y con la calidad esperada en términos de contenido y formato. Estas características se dividen en cuatro categorías principales: calidad de datos, mensaje y contenido, infraestructura de envío y reputación. Juntas forman la base del éxito de un programa de envío de correo electrónico.

El **tasa de entrega** es el número de mensajes que llegan a las bandejas de entrada de los destinatarios en comparación con el número de mensajes enviados. Depende de numerosos factores, en particular:

* Quejas de spam limitadas
* Tasas de devolución duras bajas
* Calidad de las direcciones objetivo
* Contenido del mensaje
* Conocimiento del remitente

Para optimizar la entrega de su [!DNL Journey Optimizer] experiencias, recomendamos utilizar las prácticas recomendadas enumeradas en esta sección. Los problemas de entrega generalmente están vinculados a la protección contra el correo no deseado implementada por los proveedores de servicios de Internet (ISP) y los administradores de servidores de correo.

Para profundizar en lo que es la capacidad de entrega y obtener más información sobre los términos, conceptos y enfoques clave de la capacidad de entrega, consulte la [Guía de prácticas recomendadas de entrega de Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=es){target="_blank"}.

## Reducir la tasa de quejas {#reduce-complaint-rate}

Los proveedores de servicios de Internet generalmente tienen un medio prominente para informar un mensaje recibido como correo no deseado. Esto permite identificar fuentes no fiables. Al cumplir rápidamente con las solicitudes de exclusión y, por lo tanto, mostrar que es un remitente confiable, puede reducir las tasas de quejas. [Más información acerca de la administración de la exclusión](../privacy/opt-out.md#opt-out-management)

Como regla general, no intente interferir con los destinatarios que deseen optar por la exclusión obligándolos a rellenar campos como, por ejemplo, su dirección de correo electrónico o su nombre. La página de aterrizaje de baja solo debe tener un botón de validación.

Tenga especial cuidado al solicitar una confirmación adicional: un usuario puede tener dos direcciones de correo electrónico redirigidas a la misma bandeja (por ejemplo: firstname.lastname@club.com y firstname.lastname@internet-club.com). Si el perfil solo puede recordar la primera dirección y desea cancelar la suscripción a través de un mensaje enviado a la otra, el formulario lo rechazará porque el identificador cifrado y la dirección de correo electrónico introducidos no coincidirán.

## Aprovechamiento de listas de supresión {#suppression-lists}

[!DNL Journey Optimizer] administra una lista de supresión que recopila quejas por correo no deseado, rechazos graves y rechazos leves que se producen de forma consistente.

Para proteger la capacidad de entrega, los destinatarios cuyas direcciones están en la lista de supresión se excluyen de forma predeterminada de todas las entregas futuras, ya que la entrega a estos contactos podría dañar su reputación de entrega.

[Más información sobre la lista de supresión](suppression-list.md)

## Uso de herramientas de monitorización {#monitoring-tools}

Utilice las funciones que ofrece [!DNL Journey Optimizer] para monitorizar la capacidad de envío.

El **[!UICONTROL Ejecuciones]** de la lista de mensajes le permite comprobar el rendimiento de sus envíos a través de un conjunto de indicadores en tiempo real. Entre otras cosas, se muestra esta pestaña:
* Número de mensajes que se ejecutan, envían y entregan correctamente.
* El número de mensajes que se han abierto y el número de mensajes/vínculos en los que se ha hecho clic.

## Adaptación del contenido del mensaje {#adapt-message-content}

En menor medida, el contenido de ciertos mensajes puede detectarse como correo no deseado.

Para mejorar la tasa de entrega y asegurarse de que los correos electrónicos llegan a los destinatarios, siga los principios a continuación al diseñar el contenido del mensaje:

* **Nombre y dirección del remitente**: la dirección debe identificar explícitamente al remitente. El dominio debe ser propiedad del remitente y estar registrado por él. El registro de dominios no debe privatizarse.

* **Vínculo de cancelación de suscripción y página de aterrizaje**: el vínculo &quot;Cancelar la suscripción&quot; es esencial. Debe ser visible y válido, y el formulario debe ser funcional.

[Más información sobre el diseño de contenido de correo electrónico](../email/get-started-email-design.md)

## Establezca su reputación como remitente {#reputation}

Si se ha trasladado recientemente a otro proveedor de servicios de correo electrónico, dirección IP o dominio o subdominio de correo electrónico, debe establecer su reputación como remitente. De lo contrario, los envíos podrían bloquearse o moverse a la carpeta de correo no deseado del buzón de los destinatarios.

Para calentar la IP, puede aumentar gradualmente la cantidad de envíos. Obtenga más información en esta [caso de uso](../building-journeys/ramp-up-deliveries-uc.md).

## Implementación de DMARC {#dmarc}

Para ayudarle a mitigar el riesgo de que los correos electrónicos legítimos se marquen como correo no deseado o se rechacen, y evitar problemas de envío, [!DNL Journey Optimizer] permite configurar el registro DMARC para todos los subdominios delegados en Adobe.

Autenticación de mensajes, creación de informes y conformidad basados en dominio (DMARC) es un método de autenticación por correo electrónico que permite a los propietarios de dominios proteger su dominio del uso no autorizado por agentes malintencionados.

[Más información sobre el registro DMARC](../configuration/dmarc-record.md)

## Obtenga información sobre los bucles de comentarios {#feedback-loops}

Un bucle de comentarios (FBL) es un servicio ofrecido por algunos ISP que permite notificar automáticamente al remitente del correo electrónico cuando el usuario que lo recibe decide marcarlo como correo no deseado (también conocido como &quot;queja&quot;).

Una vez que un usuario final genera una queja que el ISP devuelve al Adobe, la dirección de correo electrónico se agrega automáticamente al [lista de supresión](../reports/suppression-list.md) y se excluyen de futuros entregas. De hecho, enviar correos electrónicos a usuarios que los marcaron como correo no deseado afecta negativamente a la reputación del remitente y puede causar problemas de envío. [Más información sobre las quejas por spam](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>No todos los ISP proporcionan un FBL tradicional, como Gmail. Gmail no ofrece comentarios a nivel individual y no se puede usar para rastrear quejas de spam a destinatarios individuales, centrándose en lugar de eso en los informes a nivel agregado dentro de sus Herramientas de Postmaster de Google. [Más información](https://support.google.com/a/answer/6254652?hl=en){target="_blank"}

Todos los clientes de Adobe se inscriben automáticamente en los FBL tradicionales de los siguientes ISP:

* 1&amp;1

* AOL

* BlueTie

* Comcast

* Fastmail

* Gandi

* Italia Online

* La Poste

* Liberty Global (Chello, UPC, Unity Media)

* Locaweb

* Mail.RU

* Microsoft

* OpenSRS

* Rackspace

* SÉZNM

* SFR

* SilverSky

* Swisscom

* Synacor

* Telecom Italia

* Telenet

* Telenor

* Telstra

* Terra

* UOL

* Virgin Media

* Yahoo

* Ziggo

El Adobe audita estos FBL regularmente para asegurarse de que se añaden los últimos FBL disponibles.
