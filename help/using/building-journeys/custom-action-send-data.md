---
solution: Journey Optimizer
product: journey optimizer
title: Envío de datos a AEP
description: Obtenga información sobre cómo enviar datos a AEP
feature: Journeys, Use Cases
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: recorrido, caso de uso
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 2%

---

# Caso de uso: Creación de una acción personalizada para enviar datos a Adobe Experience Platform{#send-data-to-aep}

Si se ha trasladado recientemente a otro proveedor de servicios de correo electrónico, dirección IP o dominio o subdominio de correo electrónico, debe establecer su reputación como remitente. De lo contrario, los envíos podrían bloquearse o moverse a la carpeta de correo no deseado del buzón de los destinatarios. Aprenda a aumentar su reputación de correo electrónico con el calentamiento de IP en la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=es){target="_blank"}.

Para calentar la IP, puede aumentar gradualmente la cantidad de envíos. Más información sobre [optimización de la capacidad de entrega en Journey Optimizer](../reports/deliverability.md).

El propósito de este caso de uso es crear un recorrido para aumentar las entregas de correo electrónico. Para configurar este recorrido, siga estos pasos:

1. Cree un recorrido. [Más información](journey-gs.md).

1. Agregue una actividad **[!UICONTROL Condition]** al recorrido. [Más información](condition-activity.md).

1. En la configuración de la actividad **[!UICONTROL Condición]**, establezca el número máximo de destinatarios para la entrega:

   1. En la configuración de la actividad **[!UICONTROL Condición]**, establezca el campo **[!UICONTROL Tipo]** en **[!UICONTROL Límite de perfil]**. [Más información](condition-activity.md#profile_cap).

   1. Establezca el campo **[!UICONTROL Limit]** en el número máximo de destinatarios para esta entrega.

   ![](assets/profile-cap-condition.png)

   Puede aumentar gradualmente este límite hasta el número total de suscriptores.

1. Agregue una actividad de acción **[!UICONTROL Correo electrónico]** a la ruta nominal después de la actividad **[!UICONTROL Condición]**.

   ![](assets/ramp-up-deliveries-message.png)

   Cuando se ejecuta el recorrido, el mensaje se envía junto con la introducción de perfiles, hasta el número máximo de perfiles que haya especificado. Cuando se alcanza este límite, los perfiles que se introducen toman la ruta alternativa.

1. Complete el recorrido con las actividades que elija.

Una vez que su IP se haya calentado, puede eliminar esta condición.
