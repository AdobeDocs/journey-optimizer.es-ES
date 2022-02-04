---
title: Supervisión de la ejecución de los mensajes
description: Conozca las directrices de monitorización y envío
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 06a7abc2ada930356cbaf45ce01eed5e3156f2e3
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 25%

---

# Administrar la capacidad de entrega {#manage-deliverability}

La capacidad de entrega es una medida del éxito de los envíos que llegan a las bandejas de entrada de los destinatarios.

**La capacidad de envío de correo electrónico hace referencia al conjunto de características que determinan la capacidad de un mensaje para llegar a su destino a través de una dirección de correo electrónico personal, en poco tiempo y con la calidad esperada en términos de contenido y formato.** Estas características se dividen en cuatro categorías principales: calidad de datos, mensaje y contenido, infraestructura de envío y reputación. Juntas forman la base del éxito de un programa de envío de correo electrónico.

La variable **tasa de entrega** es el número de mensajes que llegan a las bandejas de entrada de los destinatarios en comparación con el número de mensajes enviados. Depende de numerosos factores, en particular:

* Reclamaciones por correo no deseado limitadas
* Tasas de devolución duras bajas
* Calidad de las direcciones objetivo
* Contenido del mensaje
* Conocimiento del remitente

Para optimizar la capacidad de entrega de su [!DNL Journey Optimizer] experiencias, recomendamos utilizar las prácticas recomendadas que se enumeran en esta sección. Los problemas de entrega generalmente están relacionados con la protección contra el spam implementada por los proveedores de servicios de Internet (ISP) y los administradores de servidores de correo.

Para profundizar en lo que es la capacidad de envío y para obtener más información sobre los términos, conceptos y enfoques clave de la capacidad de envío, consulte [Guía de prácticas recomendadas de entrega de Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=es){target=&quot;_blank&quot;}.

## Reducir la tasa de quejas {#reduce-complaint-rate}

Los proveedores de servicios de Internet generalmente tienen un medio prominente para informar un mensaje recibido como correo no deseado. Esto permite identificar fuentes no fiables. Al cumplir rápidamente las solicitudes de exclusión y mostrar que es un remitente fiable, puede reducir las tasas de quejas. [Obtenga más información sobre la administración de la exclusión](consent.md#opt-out-management).

Como regla general, no intente interferir con los destinatarios que deseen optar por la exclusión obligándolos a rellenar campos como, por ejemplo, su dirección de correo electrónico o su nombre. La página de aterrizaje de baja de suscripción solo debe tener un botón de validación.

Tenga especial cuidado al solicitar confirmación adicional: un usuario puede tener dos direcciones de correo electrónico redirigidas al mismo cuadro (por ejemplo: firstname.lastname@club.com y firstname.lastname@internet-club.com). Si el perfil solo puede recordar la primera dirección y desea cancelar la suscripción a través de un mensaje enviado al otro, el formulario lo rechazará porque el identificador cifrado y la dirección de correo electrónico introducidos no coincidirán.

## Aprovechar listas de supresión {#suppression-lists}

[!DNL Journey Optimizer] administra una lista de supresión que recopila quejas por correo no deseado, rechazos graves y rechazos leves que se producen de forma coherente.

Para proteger la capacidad de envío, los destinatarios cuyas direcciones están en la lista de supresión se excluyen de forma predeterminada de todos los envíos futuros, ya que el envío a estos contactos podría dañar su reputación de envío.

[Obtenga más información sobre la lista de supresión](suppression-list.md).

## Uso de las herramientas de monitorización {#monitoring-tools}

Utilice las funciones que ofrece [!DNL Journey Optimizer] para monitorizar la capacidad de envío.

La variable **[!UICONTROL Executions]** de la lista de mensajes le permite comprobar el rendimiento de sus envíos a través de un conjunto de indicadores en tiempo real. Entre otras cosas, esta pestaña muestra:
* Número de mensajes que se ejecutan, envían y envían correctamente.
* El número de mensajes que se han abierto y el número de mensajes/vínculos en los que se ha hecho clic.

[Obtenga más información sobre la monitorización de la ejecución de mensajes](message-monitoring.md).

## Adaptación del contenido del mensaje {#adapt-message-content}

En menor medida, el contenido de ciertos mensajes puede detectarse como correo no deseado.

Para mejorar la tasa de entrega y asegurarse de que los correos electrónicos llegan a los destinatarios, siga los principios a continuación al diseñar el contenido del mensaje:

* **Nombre y dirección del remitente**: La dirección debe identificar explícitamente al remitente. El dominio debe ser propiedad del remitente y estar registrado por él. El registro de dominios no debe privatizarse.

* **Cancelar suscripción a un vínculo y a una página de aterrizaje**: El enlace de cancelación de suscripción es esencial. Debe ser visible y válido, y el formulario debe ser funcional.

[Obtenga más información sobre el diseño de contenido de correo electrónico](design-emails.md).

## Establezca su reputación como remitente

Si se ha trasladado recientemente a otro proveedor de servicios de correo electrónico, dirección IP, dominio o subdominio de correo electrónico, debe establecer su reputación de remitente. De lo contrario, los envíos podrían bloquearse o moverse a la carpeta de correo no deseado del buzón de los destinatarios.

Para calentar su IP, puede aumentar gradualmente el número de envíos. Consulte esta [caso de uso](../building-journeys/ramp-up-deliveries-uc.md).
