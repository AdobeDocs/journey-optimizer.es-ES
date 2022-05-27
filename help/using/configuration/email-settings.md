---
title: Configuración de correo electrónico
description: Obtenga información sobre cómo configurar la configuración de correo electrónico en el nivel de ajuste preestablecido de mensaje
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: c48d083445d4e4c7cdbed1a61cee13ed3fcfcc8b
workflow-type: tm+mt
source-wordcount: '2166'
ht-degree: 2%

---

# Configuración de correo electrónico {#email-settings}

Defina la configuración del correo electrónico en la sección dedicada de la configuración del ajuste preestablecido de mensaje. Obtenga información sobre cómo crear ajustes preestablecidos de mensaje en [esta sección](message-presets.md).

![](assets/preset-email.png)

## Tipo de correo electrónico {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Definir la categoría de correo electrónico"
>abstract="Seleccione el tipo de mensajes que se enviarán al utilizar este ajuste preestablecido: Marketing para mensajes promocionales, que requieren el consentimiento del usuario, o Transactional para mensajes no comerciales, que también se puede enviar a perfiles cancelados de suscripción en contextos específicos."

En el **TIPO DE CORREO ELECTRÓNICO** , seleccione el tipo de mensaje que se enviará con el ajuste preestablecido: **Marketing** o **Transaccional**.

* Choose **Marketing** para mensajes promocionales: estos mensajes requieren el consentimiento del usuario.

* Choose **Transaccional** para mensajes no comerciales, como confirmación de pedido, notificaciones de restablecimiento de contraseña o información de entrega, por ejemplo.

>[!CAUTION]
>
>**Transaccional** se pueden enviar mensajes a perfiles que cancelen la suscripción a comunicaciones de marketing. Estos mensajes solo se pueden enviar en contextos específicos.

When [creación de un mensaje](../messages/get-started-content.md#create-new-message), debe elegir un ajuste preestablecido de mensaje válido que coincida con la categoría seleccionada para el mensaje.

## Subdominio y grupo de IP {#subdomains-and-ip-pools}

En el **DETALLES DEL GRUPO DE IP Y SUBDOMINIOS** , debe:

1. Seleccione el subdominio que desea utilizar para enviar los correos electrónicos. [Más información](about-subdomain-delegation.md)

1. Seleccione el grupo de IP que desea asociar al ajuste preestablecido. [Más información](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

No puede continuar con la creación preestablecida mientras el grupo IP seleccionado está en [edición](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** ) y nunca se ha asociado con el subdominio seleccionado. De lo contrario, se seguirá utilizando la versión más antigua de la asociación de agrupación/subdominio de IP. Si este es el caso, guarde el ajuste preestablecido como borrador y vuelva a intentarlo una vez que el grupo de IP tenga la variable **[!UICONTROL Success]** estado.

>[!NOTE]
>
>Para los entornos que no son de producción, Adobe no crea subdominios de prueba predeterminados ni concede acceso a un grupo de IP de envío compartido. Debe [delegar sus propios subdominios](delegate-subdomain.md) y usar las IP del grupo asignado a su organización.

## Cancelación de suscripción a una lista {#list-unsubscribe}

upon [selección de un subdominio](#subdomains-and-ip-pools) de la lista, la variable **[!UICONTROL Enable List-Unsubscribe]** se muestra.

![](assets/preset-list-unsubscribe.png)

Esta opción está habilitada de manera predeterminada.

Si lo deja habilitado, se incluirá automáticamente un vínculo de cancelación de suscripción en el encabezado del correo electrónico, como:

![](assets/preset-list-unsubscribe-header.png)

Si desactiva esta opción, no aparecerá ningún vínculo de cancelación de suscripción en el encabezado del correo electrónico.

El vínculo de cancelación de suscripción consta de dos elementos:

* Un **cancelar la suscripción de la dirección de correo electrónico**, a la que se envían todas las solicitudes de cancelación de suscripción.

   En [!DNL Journey Optimizer], la dirección de correo electrónico de cancelación de suscripción es la predeterminada **[!UICONTROL Mailto (unsubscribe)]** dirección mostrada en el ajuste preestablecido de mensaje, en función de la variable [subdominio seleccionado](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* La variable **cancelar la suscripción de la dirección URL**, que es la dirección URL de la página de aterrizaje a la que se redirige al usuario una vez que se da de baja de la suscripción.

   Si agrega un [vínculo de exclusión con un solo clic](../messages/consent.md#one-click-opt-out) a un mensaje creado con este ajuste preestablecido, la URL de cancelación de suscripción será la URL definida para el vínculo de exclusión de un clic.

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >Si no agrega un vínculo de exclusión de un clic al contenido del mensaje, no se mostrará ninguna página de aterrizaje al usuario.

Obtenga más información sobre cómo añadir un vínculo de cancelación de suscripción a un encabezado a sus mensajes en [esta sección](../messages/consent.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## Parámetros de encabezado{#email-header}

En el **[!UICONTROL HEADER PARAMETERS]** , introduzca los nombres del remitente y las direcciones de correo electrónico asociadas al tipo de mensajes enviados mediante ese ajuste preestablecido.

>[!CAUTION]
>
>Las direcciones de correo electrónico deben utilizar el seleccionado actual [subdominio delegado](about-subdomain-delegation.md).

* **[!UICONTROL Sender name]**: El nombre del remitente, como el nombre de su marca.

* **[!UICONTROL Sender email]**: La dirección de correo electrónico que desea utilizar para sus comunicaciones. Por ejemplo, si el subdominio delegado es *marketing.luma.com*, puede usar *contact@marketing.luma.com*.

* **[!UICONTROL Reply to (name)]**: El nombre que se utilizará cuando el destinatario haga clic en la variable **Responder** en el software cliente de correo electrónico.

* **[!UICONTROL Reply to (email)]**: La dirección de correo electrónico que se utilizará cuando el destinatario haga clic en el **Responder** en el software cliente de correo electrónico. Debe utilizar una dirección definida en el subdominio delegado (por ejemplo, *reply@marketing.luma.com*), de lo contrario, se enviarán los correos electrónicos.

* **[!UICONTROL Error email]**: Todos los errores generados por los ISP después de unos días de envío del correo (devoluciones asincrónicas) se reciben en esta dirección.

![](assets/preset-header.png)

>[!NOTE]
>
>Las direcciones deben comenzar por una letra (A-Z) y solo pueden contener caracteres alfanuméricos. También puede utilizar guiones bajos `_`, punto`.` Guión `-` caracteres.

### Reenviar correo electrónico {#forward-email}

Si desea reenviar a una dirección de correo electrónico específica, todos los correos electrónicos recibidos por [!DNL Journey Optimizer] para el subdominio delegado, póngase en contacto con el servicio de atención al cliente de Adobe. Deberá proporcionar:

* La dirección de correo electrónico de reenvío que elija. Tenga en cuenta que el dominio de dirección de correo electrónico de reenvío no puede coincidir con ningún subdominio delegado a Adobe.
* El nombre del simulador de pruebas.
* El nombre del ajuste preestablecido para el que se utilizará la dirección de correo electrónico de reenvío (o &quot;respuesta a&quot;).
* El **[!UICONTROL Reply to (email)]** direcciones definidas en el nivel preestablecido.

>[!NOTE]
>
>Solo puede haber una dirección de correo electrónico de reenvío por subdominio. Por lo tanto, si varios ajustes preestablecidos utilizan el mismo subdominio, se debe utilizar la misma dirección de correo electrónico de reenvío para todos ellos.

La dirección de correo electrónico de reenvío se configura por Adobe. Esto puede tardar entre 3 y 4 días.

## Correo electrónico CCO {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Definir una dirección de correo electrónico CCO"
>abstract="Puede conservar una copia de los correos electrónicos enviados enviándolos a una bandeja de entrada BCC. Escriba la dirección de correo electrónico que desee para que cada correo electrónico enviado se copie de forma ciega a esta dirección de CCO. Esta función es opcional."

Puede enviar una copia idéntica (o una copia ciega de un correo electrónico enviado por [!DNL Journey Optimizer] a una bandeja de entrada BCC. Esta función opcional le permite conservar copias de las comunicaciones por correo electrónico que envía a sus usuarios para que cumplan con las normas o las archiven. Esto es invisible para los destinatarios de la entrega.

>[!CAUTION]
>
>Esta capacidad estará disponible a partir de **31 de mayo**.

### Habilitar correo electrónico CCO {#enable-bcc}

Para habilitar la variable **[!UICONTROL BCC email]** , introduzca la dirección de correo electrónico que desee en el campo dedicado. Puede especificar cualquier dirección externa en el formato correcto, excepto una dirección de correo electrónico definida en el subdominio delegado. Por ejemplo, si el subdominio delegado es *marketing.luma.com*, cualquier dirección como *abc@marketing.luma.com* está prohibido.

>[!NOTE]
>
>Solo puede definir una dirección de correo electrónico CCO. Asegúrese de que la dirección de CCO tenga suficiente capacidad de recepción para almacenar todos los correos electrónicos enviados con el ajuste preestablecido actual.
>
>Más recomendaciones se enumeran en [esta sección](#bcc-recommendations-limitations).

![](assets/preset-bcc.png)

Todos los mensajes de correo electrónico que utilicen este ajuste preestablecido se copiarán de forma ciega en la dirección de correo electrónico de CCO que haya introducido. Desde allí, se pueden procesar y archivar utilizando un sistema externo.

>[!CAUTION]
>
>El uso de la función de CCO se contará con la cantidad de mensajes para los que tenga licencia. Por lo tanto, solo debe habilitarlo en los ajustes preestablecidos utilizados para las comunicaciones críticas que desee archivar. Compruebe si hay volúmenes con licencia en su contrato.

La configuración de la dirección de correo electrónico CCO se guarda inmediatamente y se procesa en el nivel preestablecido. Cuando [crear un nuevo mensaje](../messages/get-started-content.md#create-new-message) con este ajuste preestablecido, la dirección de correo electrónico de CCO se muestra automáticamente.

![](assets/preset-bcc-in-msg.png)

Sin embargo, la dirección de CCO se selecciona para enviar comunicaciones siguiendo la lógica siguiente:

* Para los recorridos por lotes y de ráfagas, no se aplica a la ejecución por lotes o de ráfagas que ya se había iniciado antes de que se realice la configuración de CCO. El cambio se recogerá en la siguiente repetición o en la nueva ejecución.

* En los mensajes transaccionales, el cambio se recoge inmediatamente para la siguiente comunicación (con un retraso de hasta un minuto).

>[!NOTE]
>
>No es necesario volver a publicar un mensaje o recorrido para que se recoja la configuración de CCO.

### Recommendations y limitaciones {#bcc-recommendations-limitations}

* Para garantizar el cumplimiento de la privacidad, los correos electrónicos CCO deben ser procesados por un sistema de archiving capaz de almacenar información personal (PII) de forma segura.

* Como los mensajes pueden contener datos confidenciales o privados, como información de identificación personal (PII), asegúrese de que la dirección de CCO sea correcta y asegure el acceso a los mensajes.

* La bandeja de entrada utilizada para CCO debe administrarse correctamente para el espacio y la entrega. Si la bandeja de entrada devuelve devoluciones, es posible que algunos correos electrónicos no se reciban y, por lo tanto, no se archiven.

* Los mensajes se pueden enviar a la dirección de correo electrónico de CCO antes de los destinatarios objetivo. Los mensajes CCO también se pueden enviar aunque los mensajes originales hayan [rechazado](../reports/suppression-list.md#delivery-failures).

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* No abra ni haga clic en los correos electrónicos enviados a la dirección de CCO, ya que se tienen en cuenta en el total de aperturas y clics del análisis de envío, lo que podría provocar algunos cálculos erróneos en [informes](../reports/message-monitoring.md).

* No marque los mensajes como correo no deseado en la bandeja de entrada BCC, ya que esto afectará a todos los demás correos electrónicos enviados a esta dirección.


>[!CAUTION]
>
>No haga clic en el vínculo unsubscribe de los correos electrónicos enviados a la dirección de CCO, ya que inmediatamente cancelará la suscripción de los destinatarios correspondientes.

### Cumplimiento del RGPD {#gdpr-compliance}

Las regulaciones como el RGPD establecen que los sujetos de datos deben poder modificar su consentimiento en cualquier momento. Dado que los correos electrónicos CCO que envía con Journey Optimizer incluyen información de identificación personal (PII) segura, debe editar la variable **[!UICONTROL CJM Email BCC Feedback Event Schema]** poder gestionar estos PII de conformidad con el RGPD y regulaciones similares.

Para realizar esto, siga los pasos a continuación.

1. Vaya a **[!UICONTROL Data management]** > **[!UICONTROL Schemas]** > **[!UICONTROL Browse]** y seleccione **[!UICONTROL CJM Email BCC Feedback Event Schema]**.

   ![](assets/preset-bcc-schema.png)

1. Haga clic para expandir **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagment]** then **[!UICONTROL secondaryRecipientDetail]**.

1. Seleccione **[!UICONTROL originalRecipientAddress]**.

1. En el **[!UICONTROL Field properties]** a la derecha, desplácese hacia abajo hasta el **[!UICONTROL Identity]** casilla de verificación.

1. Selecciónelo y también seleccione **[!UICONTROL Primary identity]**.

1. Seleccione un área de nombres en la lista desplegable.

   ![](assets/preset-bcc-schema-identity.png)

1. Haga clic en **[!UICONTROL Apply]**.

>[!NOTE]
>
>Obtenga más información sobre la administración de la privacidad y las regulaciones aplicables en la [Documentación de Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=es){target=&quot;_blank&quot;}.

### Datos de informes de CCO {#bcc-reporting}

Los informes como tales sobre CCO no están disponibles en los informes de recorrido y mensajes. Sin embargo, la información se almacena en un conjunto de datos del sistema llamado **[!UICONTROL AJO BCC Feedback Event Dataset]**. Puede ejecutar consultas con este conjunto de datos para encontrar información útil para la depuración, por ejemplo.

Puede acceder a este conjunto de datos a través de la interfaz de usuario. Select **[!UICONTROL Data management]** > **[!UICONTROL Datasets]** > **[!UICONTROL Browse]** y habilite **[!UICONTROL Show system datasets]** cambie desde el filtro para mostrar los conjuntos de datos generados por el sistema. Obtenga más información sobre cómo acceder a los conjuntos de datos en [esta sección](../start/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

Para ejecutar consultas con este conjunto de datos, puede utilizar el Editor de consultas proporcionado por el [Servicio de consultas de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}. Para acceder a él, seleccione **[!UICONTROL Data management]** > **[!UICONTROL Queries]** y haga clic en **[!UICONTROL Create query]**. [Más información](../start/get-started-queries.md)

![](assets/preset-bcc-queries.png)

Según la información que busque, puede ejecutar las siguientes consultas.

1. Para todas las demás consultas a continuación, necesitará el ID de acción de recorrido. Ejecute esta consulta para recuperar todos los ID de acción asociados con un ID de versión de recorrido concreto en los últimos 2 días:

       &quot;
       SELECT
       DISTINCT
       CAST(TIMESTAMP AS DATE) COMO EventTime,
       _experience.journeyOrchestration.stepEvents.journeyVersionID,
       _experience.journeyOrchestration.stepEvents.actionName,
       _experience.journeyOrchestration.stepEvents.actionID
       FROM recorrido_step_events
       WHERE
       _experience.journeyOrchestration.stepEvents.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39; AND
       _experience.journeyOrchestration.stepEvents.actionID no es NULO Y
       MARCA DE HORA > AHORA(): INTERVALO DE &quot;2&quot; DÍA
       ORDER BY EventTime DESC;
       &quot;
   
   >[!NOTE]
   >
   >Para obtener la variable `<journey version id>`seleccione el parámetro [Versión de recorrido](../building-journeys/journey-versions.md) de la variable **[!UICONTROL Journey management]** > **[!UICONTROL Journeys]** para abrir el Navegador. El ID de versión de recorrido se muestra al final de la URL que se muestra en el explorador web.
   >
   >![](assets/preset-bcc-action-id.png)

1. Ejecute esta consulta para recuperar todos los eventos de comentarios de mensajes (especialmente el estado de los comentarios) generados para un mensaje determinado dirigido a un usuario específico en los últimos 2 días:

       &quot;
       SELECT
       _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID,
       _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID,
       timestamp AS EventTime,
       _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
       _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
       CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       CUANDO &#39;enviado&#39; ENTONCES &#39;Enviado&#39;
       CUANDO &#39;delay&#39; ENTONCES &#39;Retry&#39;
       CUANDO &#39;out_of_band&#39; ENTONCES &#39;Bounce&#39;
       CUANDO &quot;devolución&quot; ENTONCES &quot;devolución&quot;
       END AS FeedbackStatusCategory
       FROM cjm_message_feedback_event_dataset
       WHERE
       timestamp > now() - INTERVALO &quot;2&quot; día Y
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39; AND
       _experience.customerJourneyManagement.messageExecution.journeyActionID = &#39;&lt;journey action=&quot;&quot; id=&quot;&quot;>&#39; AND
       _experience.customerJourneyManagement.emailChannelContext.address = &#39;&lt;recipient email=&quot;&quot; address=&quot;&quot;>&#39;
       ORDER BY EventTime DESC;
       &quot;
   
   >[!NOTE]
   >
   >Para obtener la variable `<journey action id>` ejecute la primera consulta descrita anteriormente utilizando el id de versión de recorrido. La variable `<recipient email address>` es la dirección de correo electrónico del destinatario objetivo o real.

1. Ejecute esta consulta para recuperar todos los eventos de comentarios de mensajes BCC generados para un mensaje en particular dirigido a un usuario específico en los últimos 2 días:

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

1. Ejecute esta consulta para recuperar todas las direcciones de destinatario que no hayan recibido el mensaje, mientras que su entrada de CCO existe en los últimos 30 días:

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

## Parámetros de reintentos de correo electrónico {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="Ajustar el período de tiempo de reintento"
>abstract="Los reintentos se realizan durante 3,5 días (84 horas) cuando un mensaje de correo electrónico falla debido a un error temporal de devolución del mensaje. Puede ajustar este período de tiempo de reintento predeterminado para adaptarlo mejor a sus necesidades."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html" text="Acerca de los reintentos"

Puede configurar la variable **Parámetros de reintentos de correo electrónico**.

![](assets/preset-retry-parameters.png)

De forma predeterminada, la variable [periodo de tiempo de reintento](retries.md#retry-duration) está configurada a 84 horas, pero puede ajustar esta configuración para adaptarla mejor a sus necesidades.

Debe introducir un valor entero (en horas o minutos) dentro del siguiente intervalo:

* En los correos electrónicos de marketing, el periodo de reintento mínimo es de 6 horas.
* Para los correos electrónicos transaccionales, el periodo mínimo de reintentos es de 10 minutos.
* Para ambos tipos de correo electrónico, el periodo de reintento máximo es de 84 horas (o 5040 minutos).

Obtenga más información sobre los reintentos en [esta sección](retries.md).

## Seguimiento de URL {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Parámetros de seguimiento de URL"
>abstract="Utilice esta sección para adjuntar automáticamente parámetros de seguimiento a las URL de campaña presentes en el contenido del correo electrónico."

Puede usar **[!UICONTROL URL Tracking Parameters]** para medir la eficacia de sus esfuerzos de marketing en todos los canales. Esta función es opcional.

Los parámetros definidos en esta sección se anexarán al final de las direcciones URL incluidas en el contenido del mensaje de correo electrónico. A continuación, puede capturar estos parámetros en herramientas de análisis web, como Adobe Analytics o Google Analytics, y crear varios informes de rendimiento.

![](assets/preset-url-tracking.png)

Se rellenan automáticamente tres parámetros de seguimiento de URL como ejemplo al crear un ajuste preestablecido de mensaje. Puede editarlas y agregar hasta 10 parámetros de seguimiento mediante la variable **[!UICONTROL Add new parameter]** botón.

Para configurar un parámetro de seguimiento de URL, puede introducir directamente los valores deseados en la variable **[!UICONTROL Name]** y **[!UICONTROL Value]** o elija entre una lista de valores predefinidos navegando a los siguientes objetos:

* Atributos de recorrido: **ID de origen**, **Nombre de origen**, **ID de versión de origen**
* Atributos de acción: **ID de acción**, **Nombre de la acción**
* Atributos de offer decisioning: **ID de oferta**, **Nombre de la oferta**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>No seleccione una carpeta: asegúrese de buscar la carpeta necesaria y seleccionar un atributo de perfil para utilizarlo como valor de parámetro de seguimiento.

A continuación se muestran ejemplos de URL compatibles con Adobe Analytics y Google Analytics.

* URL compatible con Adobe Analytics: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* URL compatible con Google Analytics: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

>[!NOTE]
>
>Puede combinar la escritura de valores de texto y la selección de valores predefinidos. Cada **[!UICONTROL Value]** puede contener hasta 255 caracteres en total.
