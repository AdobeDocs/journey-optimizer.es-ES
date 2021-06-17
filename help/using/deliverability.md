---
title: Supervisión de la ejecución de los mensajes
description: Conozca las directrices de monitorización y envío
feature: Capacidad de entrega
topic: Administración de contenido
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 29%

---

# Administrar la capacidad de envío {#manage-deliverability}

La capacidad de entrega es una medida del éxito de los envíos que llegan a las bandejas de entrada de los destinatarios.

**La capacidad de envío de correo electrónico hace referencia al conjunto de características que determinan la capacidad de un mensaje para llegar a su destino a través de una dirección de correo electrónico personal, en poco tiempo y con la calidad esperada en términos de contenido y formato.** Estas características se dividen en cuatro categorías principales: calidad de datos, mensaje y contenido, infraestructura de envío y reputación. Juntas forman la base del éxito de un programa de envío de correo electrónico.

La **tasa de entrega** es el número de mensajes que llegan a las bandejas de entrada de los destinatarios en comparación con el número de mensajes que se entregaron. Depende de numerosos factores, en particular:

* Reclamaciones por correo no deseado limitadas
* Tasas de devolución duras bajas
* Calidad de las direcciones objetivo
* Contenido del mensaje
* Conocimiento del remitente

Para optimizar la capacidad de envío de sus experiencias [!DNL Journey Optimizer] , recomendamos utilizar las prácticas recomendadas que se enumeran en esta sección. Los problemas de entrega generalmente están relacionados con la protección contra el spam implementada por los proveedores de servicios de Internet (ISP) y los administradores de servidores de correo.

## Reducir la tasa de quejas {#reduce-complaint-rate}

Los proveedores de servicios de Internet generalmente tienen un medio prominente para informar un mensaje recibido como correo no deseado. Esto permite identificar fuentes no fiables. Al cumplir rápidamente las solicitudes de exclusión y mostrar que es un remitente fiable, puede reducir las tasas de quejas. [Obtenga más información sobre la administración de la exclusión](consent.md#opt-out-management).

Como regla general, no intente interferir con los destinatarios que deseen optar por la exclusión obligándolos a rellenar campos como, por ejemplo, su dirección de correo electrónico o su nombre. La página de aterrizaje de baja de suscripción solo debe tener un botón de validación.

Tenga especial cuidado al solicitar confirmación adicional: un usuario puede tener dos direcciones de correo electrónico redirigidas al mismo cuadro (por ejemplo: firstname.lastname@club.com y firstname.lastname@internet-club.com). Si el perfil solo puede recordar la primera dirección y desea cancelar la suscripción a través de un mensaje enviado al otro, el formulario lo rechazará porque el identificador cifrado y la dirección de correo electrónico introducidos no coincidirán.

## Aprovechar las listas de supresión {#suppression-lists}

[!DNL Journey Optimizer] administra una lista de supresión que recopila quejas por correo no deseado, rechazos graves y rechazos leves que se producen de forma coherente.

Para proteger la capacidad de envío, los destinatarios cuyas direcciones están en la lista de supresión se excluyen de forma predeterminada de todos los envíos futuros, ya que el envío a estos contactos podría dañar su reputación de envío.

[Obtenga más información sobre la lista](suppression-list.md) de supresión.

## Usar herramientas de monitorización {#monitoring-tools}

Utilice las funciones que ofrece [!DNL Journey Optimizer] para monitorizar la capacidad de envío.

La pestaña **[!UICONTROL Executions]** de la lista de mensajes le permite comprobar el rendimiento de los envíos a través de un conjunto de indicadores en tiempo real. Entre otras cosas, esta pestaña muestra:
* Número de mensajes que se ejecutan, envían y envían correctamente.
* El número de mensajes que se han abierto y el número de mensajes/vínculos en los que se ha hecho clic.

[Obtenga más información sobre la supervisión de la ejecución](message-monitoring.md) de mensajes.

## Adaptar el contenido del mensaje {#adapt-message-content}

En menor medida, el contenido de ciertos mensajes puede detectarse como correo no deseado.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

Para mejorar la tasa de entrega y asegurarse de que los correos electrónicos llegan a los destinatarios, siga los principios a continuación al diseñar el contenido del mensaje:

* **Nombre y dirección** del remitente: La dirección debe identificar explícitamente al remitente. El dominio debe ser propiedad del remitente y estar registrado por él. El registro de dominios no debe privatizarse.

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **Cancelar suscripción al vínculo y a la página** de aterrizaje: El enlace de cancelación de suscripción es esencial. Debe ser visible y válido, y el formulario debe ser funcional.

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[Obtenga más información sobre el diseño del contenido](design-emails.md) del correo electrónico.
