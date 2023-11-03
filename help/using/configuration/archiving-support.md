---
solution: Journey Optimizer
product: journey optimizer
title: Compatibilidad de archivado en Journey Optimizer
description: Obtenga información sobre cómo archivar mensajes
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: archivo, mensajes, HIPAA, CCO, correos electrónicos
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 8%

---

# Asistencia para el archivado {#archiving-support}

## Cómo archivar mensajes {#about-archiving}

Las regulaciones como la HIPAA requieren que [!DNL Journey Optimizer] debe proporcionar una forma de archivar los mensajes enviados a las personas. De hecho, si sus clientes presentan una reclamación, deben tener la capacidad de obtener una copia del mensaje enviado para fines de verificación.

* Para el canal de correo electrónico, [!DNL Journey Optimizer] proporciona una capacidad de correo electrónico CCO integrada. [Más información](#bcc-email)

* Además, para todos los canales, puede utilizar el campo &quot;Plantilla&quot; en **Conjunto de datos de entidad**, que contiene los detalles de las plantillas de mensajes no personalizadas. Exporte el conjunto de datos con este campo para guardar metadatos como: quién envió el mensaje, a quién y cuándo. Tenga en cuenta que los datos personalizados no se exportan, solo se tiene en cuenta la plantilla (formato y estructura del mensaje). [Más información](../data/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer] no es compatible con los requisitos de archivo de SMS. Para obtener soporte de archivo dedicado, trabaje con su proveedor de SMS (Synch o Twilio).

## Cómo utilizar CCO para correos electrónicos {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Definir una dirección de correo electrónico CCO"
>abstract="Puede conservar una copia de los correos electrónicos enviados enviándolos a una bandeja de entrada CCO. Escriba la dirección de correo electrónico que desee para que cada correo electrónico enviado se copie de forma oculta a esta dirección de CCO. Tenga en cuenta que el dominio de la dirección CCO debe ser diferente de cualquier subdominio delegado a Adobe. Esta funcionalidad es opcional."

Puede enviar una copia oculta (CCO) de un correo electrónico enviado por [!DNL Journey Optimizer] a una dirección de CCO dedicada. Esta función opcional le permite conservar copias de las comunicaciones por correo electrónico que envía a sus usuarios para fines de conformidad o archivo. La dirección CCO no es visible para otros destinatarios del mensaje.

### Habilitar correo electrónico CCO {#enable-bcc}

Para habilitar la variable **[!UICONTROL Correo electrónico CCO]** , introduzca la dirección de correo electrónico de su elección en el campo dedicado del [superficie de canal](channel-surfaces.md) (es decir, ajuste preestablecido de mensaje). Puede especificar cualquier dirección externa en el formato correcto, excepto una dirección de correo electrónico definida en un subdominio delegado al Adobe. Por ejemplo, si delegó la variable *marketing.luma.com* subdominio a Adobe, cualquier dirección como *abc@marketing.luma.com* está prohibido.

>[!CAUTION]
>
>Solo puede definir una dirección de correo electrónico CCO. Asegúrese de que la dirección de CCO tenga suficiente capacidad de recepción para almacenar todos los correos electrónicos enviados mediante la superficie de canal actual.
>
>Encontrará más recomendaciones en [esta sección](#bcc-recommendations-limitations).

>[!NOTE]
>
>Si ha adquirido el complemento Healthcare Shield, debe asegurarse de que el ISP de sus direcciones de CCO sea compatible con el protocolo TLS 1.2.

![](assets/preset-bcc.png)

Una vez completada la configuración, todos los mensajes de correo electrónico basados en esta superficie se copian de forma oculta en la dirección de correo electrónico CCO que haya introducido. A partir de ahí, los mensajes se pueden procesar y archivar mediante un sistema externo.

>[!CAUTION]
>
>El uso de las funciones de CCO se deduce del número de mensajes para los que tiene licencia. Por lo tanto, actívelo solo en las superficies utilizadas para las comunicaciones esenciales que desee archivar. Compruebe si hay volúmenes con licencia en el contrato.

La configuración de la dirección de correo electrónico CCO se guarda y procesa inmediatamente en el nivel de superficie. Al crear un nuevo mensaje con esta superficie, se muestra automáticamente la dirección de correo electrónico CCO.

![](assets/preset-bcc-in-msg.png)

Sin embargo, la dirección de CCO se recoge para enviar comunicaciones siguiendo la lógica descrita [aquí](../email/email-settings.md).

### Recommendations y limitaciones {#bcc-recommendations-limitations}

* Para garantizar el cumplimiento de la privacidad, los correos electrónicos CCO deben procesarse mediante un sistema de archivado capaz de almacenar información de identificación personal (PII) de forma segura.

* Dado que los mensajes pueden contener datos confidenciales o privados, como información de identificación personal (PII), asegúrese de que la dirección de CCO sea correcta y garantice el acceso a los mensajes.

* La bandeja de entrada utilizada para CCO debe administrarse correctamente para el espacio y la entrega. Si la bandeja de entrada devuelve devoluciones, es posible que algunos correos electrónicos no se reciban y, por lo tanto, no se archiven.

* Los mensajes se pueden enviar a la dirección de correo electrónico CCO antes que los destinatarios objetivo. Los mensajes BCC también se pueden enviar aunque los mensajes originales tengan [rechazado](../reports/suppression-list.md#delivery-failures).

  <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* No abra ni haga clic en los correos electrónicos enviados a la dirección de CCO, ya que se tienen en cuenta en el total de aperturas y clics del análisis de envío, lo que podría provocar algunos cálculos erróneos en [informes](../reports/global-report.md).

* No marque los mensajes como correo no deseado en la bandeja de entrada CCO, ya que afectará a todos los demás correos electrónicos enviados a esta dirección.

>[!CAUTION]
>
>No haga clic en el vínculo unsubscribe en los correos electrónicos enviados a la dirección de CCO, ya que cancelará inmediatamente la suscripción de los destinatarios correspondientes.

### Cumplimiento del RGPD {#gdpr-compliance}

Las regulaciones como el RGPD establecen que los sujetos de datos deben poder modificar su consentimiento en cualquier momento. Dado que los correos electrónicos CCO que envía con Journey Optimizer incluyen información de identificación personal (PII) segura, debe editar la **[!UICONTROL Esquema de evento de comentarios CCO de correo electrónico CJM]** para poder administrar estas PII de conformidad con el RGPD y regulaciones similares.

Para realizar esto, siga los pasos a continuación.

1. Ir a **[!UICONTROL Administración de datos]** > **[!UICONTROL Esquemas]** > **[!UICONTROL Examinar]** y seleccione **[!UICONTROL Esquema de evento de comentarios CCO de correo electrónico CJM]**.

   ![](assets/preset-bcc-schema.png)

1. Haga clic para expandir **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagement]** entonces **[!UICONTROL secondaryRecipientDetail]**.

1. Seleccionar **[!UICONTROL originalRecipientAddress]**.

1. En el **[!UICONTROL Propiedades del campo]** a la derecha, desplácese hacia abajo hasta el **[!UICONTROL Identidad]** casilla de verificación

1. Selecciónelo y también seleccione **[!UICONTROL Identidad principal]**.

1. Seleccione un área de nombres de la lista desplegable.

   ![](assets/preset-bcc-schema-identity.png)

1. Haga clic en **[!UICONTROL Aplicar]**.

>[!NOTE]
>
>Obtenga más información sobre la administración de la privacidad y las regulaciones aplicables en la [Documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=es){target="_blank"}.

### Datos de informes de CCO {#bcc-reporting}

La creación de informes como tal en CCO no está disponible en los informes de recorrido y mensaje. Sin embargo, la información se almacena en un conjunto de datos del sistema llamado **[!UICONTROL Conjunto de datos de evento de comentarios AJO BCC]**. Puede ejecutar consultas en este conjunto de datos para encontrar información útil para la depuración, por ejemplo.

Puede acceder a este conjunto de datos a través de la interfaz de usuario. Seleccionar **[!UICONTROL Administración de datos]** > **[!UICONTROL Conjuntos de datos]** > **[!UICONTROL Examinar]** y habilite la **[!UICONTROL Mostrar conjuntos de datos del sistema]** cambie del filtro para mostrar los conjuntos de datos generados por el sistema. Obtenga más información sobre cómo acceder a conjuntos de datos en [esta sección](../data/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

Para ejecutar consultas en este conjunto de datos, puede utilizar el Editor de consultas proporcionado por el [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"}. Para acceder a él, seleccione **[!UICONTROL Administración de datos]** > **[!UICONTROL Consultas]** y haga clic en **[!UICONTROL Crear consulta]**. [Más información](../data/get-started-queries.md)

![](assets/preset-bcc-queries.png)

Según la información que esté buscando, puede ejecutar las siguientes consultas.

1. Para las demás consultas siguientes, necesitará el ID de acción de recorrido. Ejecute esta consulta para recuperar todos los ID de acción asociados a un ID de versión de recorrido concreto en los últimos 2 días:

   ```
   SELECT
   DISTINCT
   CAST(TIMESTAMP AS DATE) AS EventTime,
   _experience.journeyOrchestration.stepEvents.journeyVersionID,
   _experience.journeyOrchestration.stepEvents.actionName, 
   _experience.journeyOrchestration.stepEvents.actionID 
   FROM journey_step_events 
   WHERE 
   _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journey version id>' AND 
   _experience.journeyOrchestration.stepEvents.actionID is not NULL AND 
   TIMESTAMP > NOW() - INTERVAL '2' DAY 
   ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >Para obtener la `<journey version id>`, seleccione el parámetro correspondiente [versión de recorrido](../building-journeys/journey.md#journey-versions) desde el **[!UICONTROL administración de recorrido]** > **[!UICONTROL Recorridos]** menú. El ID de versión del recorrido se muestra al final de la dirección URL mostrada en el explorador web.
   >
   >![](assets/preset-bcc-action-id.png)

1. Ejecute esta consulta para recuperar todos los eventos de comentarios de mensajes (especialmente el estado de los comentarios) generados para un mensaje en particular dirigido a un usuario específico en los últimos 2 días:

   ```
   SELECT  
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       WHEN 'sent' THEN 'Sent'
       WHEN 'delay' THEN 'Retry'
       WHEN 'out_of_band' THEN 'Bounce' 
       WHEN 'bounce' THEN 'Bounce'
   END AS FeedbackStatusCategory
   FROM cjm_message_feedback_event_dataset 
   WHERE  
       timestamp > now() - INTERVAL '2' day  AND
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
       _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND  
       _experience.customerJourneyManagement.emailChannelContext.address = '<recipient email address>'
       ORDER BY EventTime DESC;
   ```

   >[!NOTE]
   >
   >Para obtener la `<journey action id>` , ejecute la primera consulta descrita anteriormente utilizando el id de versión de recorrido. El `<recipient email address>` parámetro es la dirección de correo electrónico del destinatario objetivo o real.

1. Ejecute esta consulta para recuperar todos los eventos de comentarios de mensajes CCO generados para un mensaje en particular dirigidos a un usuario específico en los últimos 2 días:

   ```
   SELECT   
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   _experience.customerJourneyManagement.emailChannelContext.address AS BccEmailAddress,
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
               WHEN 'sent' THEN 'Sent'
               WHEN 'delay' THEN 'Retry'
               WHEN 'out_of_band' THEN 'Bounce' 
               WHEN 'bounce' THEN 'Bounce'
           END AS FeedbackStatusCategory 
   FROM ajo_bcc_feedback_event_dataset  
   WHERE  
   timestamp > now() - INTERVAL '2' day  AND
   _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journeyaction id>' AND 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = '<recipient email address>'
   ORDER BY EventTime DESC;
   ```

1. Ejecute esta consulta para recuperar todas las direcciones de destinatarios que no hayan recibido el mensaje, mientras que su entrada CCO existe en los últimos 30 días:

   ```
    SELECT
        DISTINCT 
    bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddressesNotRecievedMessage
    FROM ajo_bcc_feedback_event_dataset bcc
    LEFT JOIN cjm_message_feedback_event_dataset mfe
    ON 
   bcc._experience.customerJourneyManagement.messageExecution.journeyVersionID =
            mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AND    bcc._experience.customerJourneyManagement.messageExecution.journeyActionID = mfe._experience.customerJourneyManagement.messageExecution.journeyActionID AND 
   bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = mfe._experience.customerJourneyManagement.emailChannelContext.address AND
   mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   mfe._experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND
   mfe.timestamp > now() - INTERVAL '30' DAY AND
   mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus IN ('bounce', 'out_of_band') 
    WHERE bcc.timestamp > now() - INTERVAL '30' DAY;
   ```
