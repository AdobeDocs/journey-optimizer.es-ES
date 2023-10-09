---
solution: Journey Optimizer
product: journey optimizer
title: Aumento de las entregas
description: Obtenga información sobre cómo aumentar los envíos
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: entrega, recorrido, caso de uso, correo electrónico, reputación
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 6%

---

# Caso de uso: aumento de envíos{#use-case-ramp-up-your-deliveries}

Si se ha trasladado recientemente a otro proveedor de servicios de correo electrónico, dirección IP o dominio o subdominio de correo electrónico, debe establecer su reputación como remitente. De lo contrario, los envíos podrían bloquearse o moverse a la carpeta de correo no deseado del buzón de los destinatarios. Aprenda a aumentar su reputación de correo electrónico con el calentamiento de IP en [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=es){target="_blank"}.

Para calentar la IP, puede aumentar gradualmente la cantidad de envíos. Más información sobre [optimización de la capacidad de entrega en Journey Optimizer](../reports/deliverability.md).

El propósito de este caso de uso es crear un recorrido para aumentar las entregas de correo electrónico. Para configurar este recorrido, siga estos pasos:

1. Creación de un recorrido. [Más información](journey-gs.md).

1. Añadir un **[!UICONTROL Condición]** actividad al recorrido. [Más información](condition-activity.md).

1. En el **[!UICONTROL Condición]** configuración de actividad, establezca el número máximo de destinatarios para la entrega:

   1. En el **[!UICONTROL Condición]** configuración de actividad, establezca el **[!UICONTROL Tipo]** field a **[!UICONTROL Límite de perfil]**. [Más información](condition-activity.md#profile_cap).

   1. Configure las variables **[!UICONTROL Límite]** al número máximo de destinatarios para esta entrega.

   ![](assets/profile-cap-condition.png)

   Puede aumentar gradualmente este límite hasta el número total de suscriptores.

1. Añadir un **[!UICONTROL Correo electrónico]** actividad de acción a la ruta nominal después de **[!UICONTROL Condición]** actividad.

   ![](assets/ramp-up-deliveries-message.png)

   Cuando se ejecuta el recorrido, el mensaje se envía junto con la introducción de perfiles, hasta el número máximo de perfiles que haya especificado. Cuando se alcanza este límite, los perfiles que se introducen toman la ruta alternativa.

1. Complete el recorrido con las actividades que elija.

Una vez que su IP se haya calentado, puede eliminar esta condición.
