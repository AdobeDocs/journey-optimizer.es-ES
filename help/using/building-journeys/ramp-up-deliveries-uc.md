---
solution: Journey Optimizer
product: journey optimizer
title: Aumento de los envíos
description: Obtenga información sobre cómo ampliar los envíos
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# Caso de uso: ampliar las entregas{#use-case-ramp-up-your-deliveries}

Si se ha trasladado recientemente a otro proveedor de servicios de correo electrónico, dirección IP, dominio o subdominio de correo electrónico, debe establecer su reputación de remitente. De lo contrario, los envíos podrían bloquearse o moverse a la carpeta de correo no deseado del buzón de los destinatarios. Aprenda a aumentar su reputación de correo electrónico con el calentamiento de IP en la [Guía de prácticas recomendadas sobre la capacidad de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}.

Para calentar su IP, puede aumentar gradualmente el número de envíos. Más información sobre [optimización de la capacidad de entrega en Journey Optimizer](../reports/deliverability.md).

El propósito de este caso de uso es crear un recorrido para aumentar los envíos de correo electrónico. Para configurar este recorrido, siga estos pasos:

1. Cree un recorrido. [Más información](journey-gs.md).

1. Agregue un **[!UICONTROL Condition]** actividad al recorrido. [Más información](condition-activity.md).

1. En el **[!UICONTROL Condition]** configuración de actividad, establezca el número máximo de destinatarios para la entrega:

   1. En el **[!UICONTROL Condition]** configuración de actividad, establezca la variable **[!UICONTROL Type]** campo a **[!UICONTROL Profile cap]**. [Más información](condition-activity.md#profile_cap).

   1. Configure las variables **[!UICONTROL Limit]** al número máximo de destinatarios para esta entrega.

   ![](assets/profile-cap-condition.png)

   Puede aumentar gradualmente este límite hasta el número total de suscriptores.

1. Agregue un **[!UICONTROL Email]** actividad de acción a la ruta nominal después del **[!UICONTROL Condition]** actividad.

   ![](assets/ramp-up-deliveries-message.png)

   Cuando se ejecuta el recorrido, el mensaje se envía a los perfiles que entran, hasta el número máximo de perfiles especificados. Cuando se alcanza este límite, los perfiles que ingresan toman la ruta alternativa.

1. Complete el recorrido con las actividades que elija.

Una vez que su IP se haya calentado, puede eliminar esta condición.
