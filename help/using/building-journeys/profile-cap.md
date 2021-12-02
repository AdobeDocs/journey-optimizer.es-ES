---
title: Límite de perfiles
description: Límite de perfiles
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
hide: true
hidefromtoc: true
source-git-commit: b5ce2ea81d4091b4fa9c09e83573f9043c5e55a8
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---


# Establezca su reputación como remitente

Si se ha trasladado recientemente a otro proveedor de servicios de correo electrónico, dirección IP, dominio o subdominio de correo electrónico, debe establecer su reputación de remitente. De lo contrario, los envíos podrían bloquearse o moverse a la carpeta de correo no deseado del buzón de los destinatarios.

Para calentar su IP, puede aumentar gradualmente el número de envíos. Consulte esta [caso de uso](../building-journeys/ramp-up-deliveries-uc.md).

## Tipo de condición de límite de perfil {#profile_cap}

Otros tipos de condición se detallan en esta [sección](../building-journeys/condition-activity.md).

Utilice este tipo de condición para establecer un número máximo de perfiles para una ruta de recorrido. Cuando se alcanza este límite, los perfiles que se introducen toman una ruta alternativa.

Puede utilizar este tipo de condición para aumentar el volumen de los envíos. Consulte esta [caso de uso](../building-journeys/ramp-up-deliveries-uc.md).

El límite predeterminado es 1000. Puede establecer un valor entero de 1 a 20.000.

El contador solo se aplica a la versión de recorrido seleccionada. El contador se restablece a cero después de un mes. Después de un restablecimiento, los perfiles introducidos siguen la ruta nominal de nuevo hasta que se alcanza el límite del contador.

La ruta nominal siempre tiene prioridad sobre la ruta alternativa, incluso si se mueve la ruta alternativa por encima de la ruta nominal en el lienzo de recorrido.

![](../assets/profile-cap-condition.png)

## Caso de uso: ampliar las entregas

Si se ha trasladado recientemente a otro proveedor de servicios de correo electrónico, dirección IP, dominio o subdominio de correo electrónico, debe establecer su reputación de remitente. De lo contrario, los envíos podrían bloquearse o moverse a la carpeta de correo no deseado del buzón de los destinatarios. Aprenda a aumentar su reputación de correo electrónico con el calentamiento de IP en la [Guía de prácticas recomendadas sobre la capacidad de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}.

Para calentar su IP, puede aumentar gradualmente el número de envíos. Más información sobre [optimización de la capacidad de entrega en Journey Optimizer](../deliverability.md).

El propósito de este caso de uso es crear un recorrido para aumentar los envíos de correo electrónico. Para configurar este recorrido, siga estos pasos:

1. Creación de un recorrido. [Más información](../building-journeys/journey-gs.md).

1. Agregue un **[!UICONTROL Condition]** actividad al recorrido. [Más información](../building-journeys/condition-activity.md).

1. En el **[!UICONTROL Condition]** configuración de actividad, establezca el número máximo de destinatarios para la entrega:

   1. En el **[!UICONTROL Condition]** configuración de actividad, establezca la variable **[!UICONTROL Type]** campo a **[!UICONTROL Profile cap]**. [Más información](profile-cap.md#profile_cap).

   1. Configure las variables **[!UICONTROL Limit]** al número máximo de destinatarios para esta entrega.

   ![](../assets/profile-cap-condition.png)

   Puede aumentar gradualmente este límite hasta el número total de suscriptores.

1. Agregue un **[!UICONTROL Message]** actividad a la ruta nominal después de la **[!UICONTROL Condition]** actividad.

   ![](../assets/ramp-up-deliveries-message.png)

   Cuando se ejecuta el recorrido, el mensaje se envía a los perfiles que se van a introducir, hasta el número máximo de perfiles especificados. Cuando se alcanza este límite, los perfiles que ingresan toman la ruta alternativa.

1. Complete el recorrido con las actividades de su elección.

Una vez que su IP se haya calentado, puede eliminar esta condición.

