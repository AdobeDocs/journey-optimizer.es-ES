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
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 18%

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

Los proveedores de servicios de Internet generalmente tienen un medio prominente para informar un mensaje recibido como correo no deseado. Esto permite identificar fuentes no fiables. Al cumplir rápidamente con las solicitudes de exclusión y, por lo tanto, mostrar que es un remitente confiable, puede reducir las tasas de quejas. [Más información acerca de la administración de la exclusión](../privacy/opt-out.md#opt-out-management).

Como regla general, no intente interferir con los destinatarios que deseen optar por la exclusión obligándolos a rellenar campos como, por ejemplo, su dirección de correo electrónico o su nombre. La página de aterrizaje de baja solo debe tener un botón de validación.

Tenga especial cuidado al solicitar una confirmación adicional: un usuario puede tener dos direcciones de correo electrónico redirigidas a la misma bandeja (por ejemplo: firstname.lastname@club.com y firstname.lastname@internet-club.com). Si el perfil solo puede recordar la primera dirección y desea cancelar la suscripción a través de un mensaje enviado a la otra, el formulario lo rechazará porque el identificador cifrado y la dirección de correo electrónico introducidos no coincidirán.

## Aprovechamiento de listas de supresión {#suppression-lists}

[!DNL Journey Optimizer] administra una lista de supresión que recopila quejas por correo no deseado, rechazos graves y rechazos leves que se producen de forma consistente.

Para proteger la capacidad de entrega, los destinatarios cuyas direcciones están en la lista de supresión se excluyen de forma predeterminada de todas las entregas futuras, ya que la entrega a estos contactos podría dañar su reputación de entrega.

[Más información sobre la lista de supresión](suppression-list.md).

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

[Más información sobre el diseño de contenido de correo electrónico](../email/get-started-email-design.md).

## Establezca su reputación como remitente

Si se ha trasladado recientemente a otro proveedor de servicios de correo electrónico, dirección IP o dominio o subdominio de correo electrónico, debe establecer su reputación como remitente. De lo contrario, los envíos podrían bloquearse o moverse a la carpeta de correo no deseado del buzón de los destinatarios.

Para calentar la IP, puede aumentar gradualmente la cantidad de envíos. Ver esto [caso de uso](../building-journeys/ramp-up-deliveries-uc.md).
