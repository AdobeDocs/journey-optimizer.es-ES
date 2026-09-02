---
solution: Journey Optimizer
product: journey optimizer
title: Envío de datos a AEP
description: Obtenga información sobre cómo enviar datos a AEP
feature: Journeys, Use Cases
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: recorrido, caso de uso
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 711
ht-degree: 3%

---

# Caso de uso: crear una acción personalizada para enviar datos a [!DNL Adobe Experience Platform]{#send-data-to-aep}

>[!BEGINSHADEBOX]

**En esta página:** Aprenda a crear un recorrido que aumente gradualmente el volumen de correo electrónico mediante una actividad de optimización con una condición de límite de perfil para calentar la IP y proteger la reputación de su remitente.

>[!ENDSHADEBOX]

Si se ha trasladado recientemente a otro proveedor de servicios de correo electrónico, dirección IP o dominio o subdominio de correo electrónico, establezca su reputación como remitente. De lo contrario, los envíos podrían bloquearse o moverse a las carpetas de correo no deseado de los destinatarios. Para obtener instrucciones, consulte la [Guía de prácticas recomendadas de entrega](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=es){target="_blank"}.

Para calentar la IP, puede aumentar gradualmente la cantidad de envíos. Más información sobre [optimización de la capacidad de entrega en Journey Optimizer](../reports/deliverability.md).

El propósito de este caso de uso es crear un recorrido para aumentar las entregas de correo electrónico. Para configurar este recorrido, siga estos pasos:

1. Cree un recorrido. [Más información](journey-gs.md).

1. Agregue una actividad **[!UICONTROL Optimizar]** al recorrido. [Más información](optimize.md).

1. En la configuración de la actividad **[!UICONTROL Condición]**, establezca el número máximo de destinatarios para la entrega:

   1. En la configuración de la actividad **[!UICONTROL Optimizar]**, seleccione el método **[!UICONTROL Condiciones]** y establezca el campo **[!UICONTROL Tipo]** en **[!UICONTROL Límite de perfil]**. [Más información](conditions.md#profile_cap).

   1. Establezca el campo **[!UICONTROL Limit]** en el número máximo de destinatarios para esta entrega.

   ![Condición de límite de perfil para controlar el volumen de ejecución de acciones personalizadas](assets/profile-cap-condition.png)

   Puede aumentar gradualmente este límite hasta el número total de suscriptores.

1. Agregue una actividad de acción **[!UICONTROL Correo electrónico]** a la ruta nominal después de la actividad **[!UICONTROL Condición]**.

   ![Recorrido con acción personalizada para enviar datos al sistema externo](assets/ramp-up-deliveries-message.png)

   Cuando se ejecuta el recorrido, el mensaje se envía junto con la introducción de perfiles, hasta el número máximo de perfiles que haya especificado. Cuando se alcanza este límite, los perfiles que se introducen toman la ruta alternativa.

1. Complete el recorrido con las actividades que elija.

Una vez que su IP se haya calentado, puede eliminar esta condición.

+++ Referencia de conocimientos de AI

Esta sección contiene conocimientos estructurados destinados a apoyar la interpretación, la recuperación y la respuesta a preguntas relacionadas con este tema.

Para una comprensión completa, esta información debe combinarse con la documentación de esta página. Ninguna de las fuentes pretende ser independiente; la página describe la función, mientras que esta sección proporciona contexto adicional que ayuda a desambiguar la terminología, la intención, la aplicabilidad y las restricciones.

* **TL;DR:** Esta página muestra un caso de uso de calentamiento de IP basado en recorrido que aumenta gradualmente el volumen de entrega de correo electrónico mediante una condición Límite de perfil para proteger la reputación del remitente.

**Intenciones:**

* Cree un recorrido de calentamiento de IP para aumentar gradualmente el volumen de envío de correo electrónico
* Configure una condición Límite de perfil para limitar el número de destinatarios por envío
* Añadir una actividad de acción Correo electrónico a la ruta de recorridos nominal
* Quitar la condición de límite de perfil una vez completado el calentamiento de la IP

**Glosario:**

* **Calentamiento de IP**: Proceso para aumentar gradualmente el volumen de envío de correo electrónico desde una nueva dirección IP para establecer la reputación del remitente *(específico del producto)*
* **Límite de perfil**: Tipo de condición en Journey Optimizer que limita el número máximo de perfiles que pueden tomar una ruta de recorrido específica *(específica del producto)*
* **Ruta nominal**: La rama principal de un recorrido que siguen los perfiles cuando se cumplen las condiciones *(específico del producto)*

**Protecciones:**

* Se debe establecer una condición de Límite de perfil en la actividad Condición para controlar el volumen de entrega durante el calentamiento de la IP.
* Los perfiles que superan el límite se enrutan a la ruta alternativa.
* El recorrido debe volver a crearse o modificarse una vez completado el calentamiento de la IP para eliminar la condición de límite.

**Terminología:**

* Nombre canónico: calentamiento de IP — Acrónimo: n/a — variantes: calentamiento de IP, calentamiento de reputación del remitente
* Sinónimos: &quot;Límite de perfil&quot; = &quot;Condición de límite de destinatario&quot;
* No confunda: &quot;calentamiento de IP&quot; ≠ &quot;autenticación por correo electrónico&quot; (la configuración de SPF/DKIM/DMARC es independiente)

**PREGUNTAS MÁS FRECUENTES:**

* **Q: ¿Por qué necesito calentar mi IP?** — Las nuevas direcciones IP no tienen historial de envío, por lo que los proveedores de buzones de correo pueden bloquear los mensajes de carpetas de correo no deseado hasta que se establezca la reputación.
* **Q: ¿Qué les sucede a los perfiles que exceden el límite del perfil?** — siguen la ruta alternativa definida en la actividad Condición.
* **Q: ¿Cómo puedo aumentar el límite con el tiempo?** — Edite el campo Limit en la configuración de actividad Condition y elévelo gradualmente hasta el recuento total de suscriptores.
* **Q: ¿Cuándo puedo quitar la condición de límite de perfil?** — Una vez que la IP tenga suficiente historial de envíos y las métricas de capacidad de envío sean estables, puede eliminar la condición de la recorrido.

+++
