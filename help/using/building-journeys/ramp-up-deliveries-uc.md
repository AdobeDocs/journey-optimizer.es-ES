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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 807
ht-degree: 2%

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

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

- **TL;DR:** En este caso de uso se describe cómo crear un recorrido de trabajo de Adobe Journey Optimizer que aumente gradualmente el volumen de envíos de correo electrónico mediante una condición de límite de perfil para proteger la reputación del remitente durante el calentamiento de la IP.

**Intenciones:**
- Cree un recorrido para aumentar gradualmente el volumen de entrega de correo electrónico para el calentamiento de la IP
- Configure una condición Límite de perfil para limitar el número de destinatarios por ejecución de envíos
- Proteja la reputación del remitente al cambiar a un nuevo proveedor de servicios de correo electrónico, dirección IP o dominio
- Retire el estado del tapón de volumen una vez que la IP esté completamente caliente

**Glosario:**
- **Calentamiento de IP**: Proceso de aumento gradual del volumen de envíos de correo electrónico desde una nueva dirección IP o dominio para crear la reputación del remitente con los proveedores de buzones de correo *(específicos del producto)*
- **Límite de perfil**: tipo de condición en la actividad de optimización que limita el número máximo de perfiles que reciben un mensaje en una ejecución de recorrido determinada *(específica del producto)*
- **Optimizar actividad**: una actividad de lienzo de recorrido se usa para aplicar condiciones, reglas de segmentación o experimentación para controlar cómo fluyen los perfiles a través de un recorrido *(específico del producto)*

**Protecciones:**
- Se debe establecer una condición Límite de perfil en el método Conditions de la actividad de optimización para controlar el volumen de entrega.
- Los perfiles que exceden el límite toman la ruta alternativa definida en el recorrido.
- El límite máximo de perfil debe aumentarse gradualmente a lo largo del tiempo hasta el número total de suscriptores.

**Terminología:**
- Nombre canónico: Ramp-up deliveries — Acrónimo: none — variantes: Calentamiento de IP, Calentamiento de IP, Aumento de entrega
- Sinónimos: &quot;calentamiento de IP&quot; = &quot;calentamiento de IP&quot; = &quot;creación de reputación del remitente&quot;
- No confunda: &quot;Límite de perfil&quot; ≠ &quot;Límite de tamaño de audiencia&quot; (El límite de perfil es un límite de envío por ejecución; el tamaño de audiencia es el número total de perfiles cualificados)

**PREGUNTAS MÁS FRECUENTES:**
- **Q: ¿Por qué necesito aumentar los envíos al cambiar a una nueva IP o dominio?** — Una nueva IP o dominio no tiene historial de envío, por lo que los proveedores de buzones de correo pueden bloquear los mensajes de carpetas de correo no deseado hasta que se establezca una reputación positiva a través de un volumen gradual y creciente.
- **Q: ¿Cómo controla la condición Límite de perfiles el volumen de entrega?** — Establece un número máximo de perfiles que pueden recibir el mensaje en una sola ejecución de recorrido; los perfiles que superan ese límite toman una ruta alternativa en su lugar.
- **Q: ¿Cuándo puedo quitar la condición Límite de perfiles?** — Una vez que la IP se haya calentado completamente y se haya establecido la reputación del remitente, puede eliminar la condición de la recorrido.
- **Q: ¿Puedo aumentar el límite gradualmente con el tiempo?** — Sí; puede actualizar el campo Limit en la condición Profile cap para aumentar progresivamente el número de destinatarios por ejecución hasta el recuento completo de suscriptores.

+++
