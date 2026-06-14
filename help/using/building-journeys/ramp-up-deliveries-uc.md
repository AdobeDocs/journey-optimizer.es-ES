---
solution: Journey Optimizer
product: journey optimizer
title: Aumento de las entregas
description: Obtenga información sobre cómo aumentar los envíos
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
hide: true
keywords: entrega, recorrido, caso de uso, correo electrónico, reputación
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/en0jMw69ddHSQrIH05-9FfGuDwNKb36f5Lp3fLp2oAk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 7%

---

# Caso de uso: aumento de envíos{#use-case-ramp-up-your-deliveries}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a crear un recorrido que aumente gradualmente sus envíos de correo electrónico mediante la actividad Optimizar y un límite de perfil, lo que le ayudará a calentar una nueva dirección IP y a establecer su reputación de remitente.

>[!ENDSHADEBOX]

Si se ha trasladado recientemente a otro proveedor de servicios de correo electrónico, dirección IP o dominio o subdominio de correo electrónico, debe establecer su reputación como remitente. De lo contrario, los envíos podrían bloquearse o moverse a la carpeta de correo no deseado del buzón de los destinatarios. Aprenda a aumentar su reputación de correo electrónico con el calentamiento de IP en la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=es){target="_blank"}.

Para calentar la IP, puede aumentar gradualmente la cantidad de envíos. Más información sobre [optimización de la capacidad de entrega en Journey Optimizer](../reports/deliverability.md).

El propósito de este caso de uso es crear un recorrido para aumentar las entregas de correo electrónico. Para configurar este recorrido, siga estos pasos:

1. Cree un recorrido. [Más información](journey-gs.md).

1. Agregue una actividad **[!UICONTROL Optimizar]** al recorrido. [Más información](optimize.md).

1. En la configuración de la actividad **[!UICONTROL Condición]**, establezca el número máximo de destinatarios para la entrega:

   1. En la configuración de la actividad **[!UICONTROL Optimizar]**, seleccione el método **[!UICONTROL Condiciones]** y establezca el campo **[!UICONTROL Tipo]** en **[!UICONTROL Límite de perfil]**. [Más información](conditions.md#profile_cap).

   1. Establezca el campo **[!UICONTROL Limit]** en el número máximo de destinatarios para esta entrega.

   ![Configuración de condición de límite de perfil para controlar el volumen de entrega](assets/profile-cap-condition.png)

   Puede aumentar gradualmente este límite hasta el número total de suscriptores.

1. Agregue una actividad de acción **[!UICONTROL Correo electrónico]** a la ruta nominal después de la actividad **[!UICONTROL Condición]**.

   ![Configuración de mensaje de correo electrónico en el recorrido de envío en rampa](assets/ramp-up-deliveries-message.png)

   Cuando se ejecuta el recorrido, el mensaje se envía junto con la introducción de perfiles, hasta el número máximo de perfiles que haya especificado. Cuando se alcanza este límite, los perfiles que se introducen toman la ruta alternativa.

1. Complete el recorrido con las actividades que elija.

Una vez que su IP se haya calentado, puede eliminar esta condición.
