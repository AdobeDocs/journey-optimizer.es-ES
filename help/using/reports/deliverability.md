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
TQID: https://experienceleague.adobe.com/7EdZZJgxpZA2AtSo-lMpMEDV6C9zk78mmvNVhe5KXcw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: a122a8a609748b46480a9664f1efc5524582deca
workflow-type: tm+mt
source-wordcount: 1348
ht-degree: 19%

---

# Introducción a la Entregabilidad {#manage-deliverability}

La capacidad de entrega es una medida del éxito de los envíos que llegan a las bandejas de entrada de los destinatarios.

>[!NOTE]
>
>Para los clientes que obtienen una licencia de Healthcare Shield, Adobe utiliza Transport Layer Security (TLS) 1.2 para proteger el intercambio de datos entre los sistemas de los usuarios (destinatarios) y Journey Optimizer (remitente). Si el servidor de correo receptor no es compatible con TLS 1.2, los clientes experimentarán problemas de envío, incluido el rebote de correo electrónico al remitente original.

**La capacidad de envío de correo electrónico** hace referencia al conjunto de características que determinan la capacidad de un mensaje para llegar a su destino a través de una dirección de correo electrónico personal, en poco tiempo y con la calidad esperada en términos de contenido y formato. Estas características se dividen en cuatro categorías principales: calidad de datos, mensaje y contenido, infraestructura de envío y reputación. Juntas forman la base del éxito de un programa de envío de correo electrónico.

La **tasa de entrega** es el número de mensajes que llegan a las bandejas de entrada de los destinatarios en comparación con el número de mensajes que se entregaron. Depende de numerosos factores, en particular:

* Quejas de spam limitadas
* Tasas de devolución duras bajas
* Calidad de las direcciones objetivo
* Contenido del mensaje
* Conocimiento del remitente

Para optimizar la entrega de sus experiencias de [!DNL Journey Optimizer], recomendamos que utilice las prácticas recomendadas que se enumeran en esta sección. Los problemas de entrega generalmente están vinculados a la protección contra el correo no deseado implementada por los proveedores de servicios de Internet (ISP) y los administradores de servidores de correo.

Para profundizar en lo que es la capacidad de entrega y obtener más información sobre los términos, conceptos y enfoques clave de la capacidad de entrega, consulte la [Guía de prácticas recomendadas de entrega de Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=es){target="_blank"}.

## Reducir la tasa de quejas {#reduce-complaint-rate}

Los proveedores de servicios de Internet generalmente tienen un medio prominente para informar un mensaje recibido como correo no deseado. Esto permite identificar fuentes no fiables. Al cumplir rápidamente con las solicitudes de exclusión y, por lo tanto, mostrar que es un remitente confiable, puede reducir las tasas de quejas. [Más información acerca de la administración de la exclusión](../privacy/opt-out.md#opt-out-decision-management)

Como regla general, no intente interferir con los destinatarios que deseen optar por la exclusión obligándolos a rellenar campos como, por ejemplo, su dirección de correo electrónico o su nombre. La página de aterrizaje de baja solo debe tener un botón de validación.

Tenga especial cuidado al solicitar una confirmación adicional: un usuario puede tener dos direcciones de correo electrónico redirigidas a la misma bandeja (por ejemplo: firstname.lastname@club.com y firstname.lastname@internet-club.com). Si el perfil solo puede recordar la primera dirección y desea cancelar la suscripción a través de un mensaje enviado a la otra, el formulario lo rechazará porque el identificador cifrado y la dirección de correo electrónico introducidos no coincidirán.

## Aprovechamiento de listas de supresión {#suppression-lists}

[!DNL Journey Optimizer] administra una lista de supresión que recopila quejas por correo no deseado, rechazos graves y rechazos leves que se producen de forma consistente.

Para proteger la capacidad de entrega, los destinatarios cuyas direcciones están en la lista de supresión se excluyen de forma predeterminada de todas las entregas futuras, ya que la entrega a estos contactos podría dañar su reputación de entrega.

[Más información sobre la lista de supresión](suppression-list.md)

## Uso de herramientas de monitorización {#monitoring-tools}

Use las características de generación de informes que ofrece [!DNL Journey Optimizer] para supervisar su capacidad de entrega.

Los informes de campaña e recorrido permiten comprobar el rendimiento de las entregas a través de un conjunto de indicadores en tiempo real. Entre otras cosas, muestran:

* Número de mensajes que se ejecutan, envían y entregan correctamente.
* El número de mensajes que se han abierto y el número de mensajes/vínculos en los que se ha hecho clic.

Obtenga más información sobre [informe en vivo](../reports/live-report.md) y [informe en todo momento](../reports/report-gs-cja.md)

## Adaptación del contenido del mensaje {#adapt-message-content}

En menor medida, el contenido de ciertos mensajes puede detectarse como correo no deseado.

Para mejorar la tasa de entrega y asegurarse de que los correos electrónicos llegan a los destinatarios, siga los principios a continuación al diseñar el contenido del mensaje:

* **Nombre y dirección del remitente**: la dirección debe identificar explícitamente al remitente. El dominio debe ser propiedad del remitente y estar registrado por él. El registro de dominios no debe privatizarse.

* **Vínculo de cancelación de suscripción y página de aterrizaje**: El vínculo de cancelación de suscripción es esencial. Debe ser visible y válido, y el formulario debe ser funcional.

[Más información sobre el diseño de contenido de correo electrónico](../email/get-started-email-design.md)

## Establezca su reputación como remitente {#reputation}

Si se ha trasladado recientemente a otro proveedor de servicios de correo electrónico, dirección IP o dominio o subdominio de correo electrónico, debe establecer su reputación como remitente. De lo contrario, los envíos podrían bloquearse o moverse a la carpeta de correo no deseado del buzón de los destinatarios.

Al enviar correos electrónicos en una dirección IP completamente nueva, ahora puede realizar fácilmente flujos de trabajo de calentamiento de IP directamente desde la interfaz de usuario.

Adobe Journey Optimizer ofrece una forma estandarizada y eficaz de añadir las direcciones IP que siguen las prácticas recomendadas para lograr una entrega óptima.

[Más información sobre los planes de calentamiento de IP](../configuration/ip-warmup-gs.md)

<!--To warm up your IP, you can gradually ramp up the number of your deliveries. Learn more in this [use case](../building-journeys/ramp-up-deliveries-uc.md).-->

## Implementación de DMARC {#dmarc}

Para ayudarle a mitigar el riesgo de que los correos electrónicos legítimos se marquen como correo no deseado o se rechacen, y para evitar problemas de envío, [!DNL Journey Optimizer] le permite configurar el registro de DMARC para todos los subdominios que delega a Adobe.

Autenticación de mensajes, creación de informes y conformidad basados en dominio (DMARC) es un método de autenticación por correo electrónico que permite a los propietarios de dominios proteger su dominio contra el uso no autorizado por parte de agentes malintencionados.

[Más información sobre el registro de DMARC](../configuration/dmarc-record.md)

## Información sobre los bucles de comentarios {#feedback-loops}

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Algunos subdominios podrían no estar disponibles"
>abstract="Algunos subdominios no están disponibles actualmente para su selección debido a que está pendiente el registro del bucle de comentarios. Este proceso puede tardar hasta 10 días hábiles. Una vez finalizado, puede elegir entre todos los subdominios disponibles."
>additional-url="https://experienceleague.adobe.com/es/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation" text="Introducción a la delegación de subdominios"

Un bucle de comentarios (FBL) es un servicio ofrecido por algunos ISP que permite notificar automáticamente al remitente del correo electrónico cuando el usuario que lo recibe decide marcarlo como correo no deseado (también conocido como &quot;queja&quot;).

Una vez que un usuario final genera una queja que el ISP devuelve a Adobe, la dirección de correo electrónico se agrega automáticamente a la [lista de supresión](../reports/suppression-list.md) y se excluye de futuros envíos. De hecho, enviar correos electrónicos a usuarios que los marcaron como correo no deseado afecta negativamente a la reputación del remitente y puede causar problemas de envío. [Más información sobre quejas por correo no deseado](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>No todos los ISP proporcionan un FBL tradicional, como Gmail. Gmail no ofrece comentarios a nivel individual y no se puede usar para rastrear quejas de spam a destinatarios individuales, centrándose en lugar de eso en los informes a nivel agregado dentro de sus Herramientas de Postmaster de Google. [Más información](#providers-no-fbl)


Todos los clientes de Adobe se inscriben automáticamente en los FBL tradicionales de los ISP que se enumeran a continuación.

+++ ISP que proporcionan un FBL tradicional:

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

+++

Adobe realiza auditorías regulares para asegurarse de que se añaden los FBL más recientes.

### Proveedores sin FBL por destinatario {#providers-no-fbl}

No todos los ISP proporcionan un FBL tradicional. Varios proveedores de buzones de correo principales no devuelven quejas de correo no deseado por destinatario, lo que significa que se espera la ausencia de una entrada en la lista de supresión para los destinatarios que utilizan esos proveedores.

| Proveedor de buzones | ¿Queja FBL por destinatario? |
|---|---|
| **Gmail / Google Workspace** | No: los informes agregados solo se realizan mediante las herramientas de administrador de correo de Google (ID de comentario; no por destinatario). [Más información](https://support.google.com/a/answer/6254652?hl=en){target="_blank"} |
| **Apple iCloud** (icloud.com, me.com, mac.com) | No — [Más información](https://support.apple.com/en-us/102322){target="_blank"} |
| **Microsoft corporativo 365 / Exchange Online** | No: el programa de informes de correo no deseado (JMRP) cubre únicamente la red de Outlook.com del consumidor; los informes de correo no deseado del inquilino procedentes de entornos corporativos M365 no se devuelven al remitente. [Más información](https://learn.microsoft.com/en-us/answers/questions/5787589/does-the-junk-mail-reporting-program-(jmrp)-send-c){target="_blank"} |

Juntos, estos proveedores representan la mayoría de las bandejas de entrada de consumidores y empresas. Como ninguno de ellos devuelve quejas por destinatario, un destinatario que utilice cualquiera de estos servicios y que marque un mensaje como correo no deseado **no** aparecerá automáticamente en la lista de supresión.

## Usar retransmisión SMTP {#smtp-relay}

[!DNL Journey Optimizer] utiliza agentes de transferencia de correo (MTA) e IP propiedad de Adobe para entregar sus correos electrónicos a los proveedores de servicios de Internet (ISP). Sin embargo, en algunos casos puede que desee enrutar los envíos de correo electrónico finales a través de sus propios MTA e IP, o para realizar validaciones finales en los correos electrónicos antes de enviarlos a sus destinatarios.

En este caso, puede elegir que los correos electrónicos se retransmitan a servidores SMTP alojados por su organización en lugar de enviarse directamente desde Journey Optimizer a los ISP.

>[!AVAILABILITY]
>
>La capacidad de retransmisión SMTP está disponible bajo demanda: póngase en contacto con su representante de Adobe.
