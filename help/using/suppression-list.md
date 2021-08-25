---
title: Lista de supresión
description: Aprenda qué es la lista de supresión, su propósito y qué se incluye en ella.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: ea2bb0c2956781138a0c7f2d0babfd91070dd351
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 2%

---

# Lista de supresión {#suppression-list}

Una lista de supresión consiste en direcciones de correo electrónico que desea excluir de los envíos, ya que el envío a estos contactos podría dañar la reputación del envío y las tasas de envío.

La lista de supresión [!DNL Journey Optimizer] se administra en su propio nivel de entorno.

Recopila direcciones de correo electrónico y dominios que se suprimen en todos los correos en un único entorno de cliente, lo que significa que son específicos de un ID de organización de IMS asociado a un ID de simulador de pruebas.

<!--It gathers spam complaints, hard bounces, and soft bounces that occur consistently.-->

## ¿Por qué una lista de supresión? {#why-suppression-list}

Para controlar los mensajes de correo electrónico que reciben los propietarios de las bandejas de entrada y asegurarse de que solo reciben los que desean, los proveedores de servicios de Internet (ISP) y los filtros de correo no deseado comerciales tienen sus algoritmos propietarios para realizar un seguimiento de la reputación general de los remitentes de correo electrónico en función de las direcciones IP y los dominios de envío que utilizan.

Si no recibe sus comentarios (como quejas por correo no deseado, devoluciones, etc.) teniendo en cuenta, valorarán su reputación por debajo. La lista de supresión le ayuda a cumplir con los comentarios de los ISP.

Los destinatarios cuyas direcciones de correo electrónico se supriman se excluyen automáticamente de la entrega de mensajes. Esto acelera las entregas, ya que la tasa de error afecta significativamente a la velocidad de entrega.

## ¿Qué hay en la lista de supresión? {#what-s-on-suppression-list}

Las direcciones de correo electrónico se añaden a la lista de supresión de la siguiente manera:

* Todas las **rechazos graves** y **quejas por correo no deseado** envían automáticamente las direcciones de correo electrónico correspondientes a la lista de supresión tras una sola incidencia.

* **Los** <!--and temporary **ignored** errors--> rechazos leves no envían inmediatamente una dirección de correo electrónico a la lista de supresión, sino que se suman a un contador de errores. A continuación, se realizan varios [reintentos](configuration/retries.md) y, cuando el contador de errores alcanza el umbral, la dirección se agrega a la lista de supresión.

* También puede [**manualmente** agregar una dirección o un dominio](configuration/manage-suppression-list.md#add-addresses-and-domains) a la lista de supresión.

Obtenga más información sobre los rechazos graves y los rechazos leves en [esta sección](#delivery-failures).

>[!NOTE]
>
>Las direcciones de los usuarios cancelados de suscripción no se pueden enviar a la lista de supresión ya que no reciben correos electrónicos de [!DNL Journey Optimizer]. Su elección se gestiona a nivel de Experience Platform. Obtenga más información sobre [exclusión](../using/consent.md).
<!--Email addresses of recipients who **unsubscribe** from your sendings are NOT sent to the suppression list. Confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

Para cada dirección, el motivo básico de la supresión y la categoría de supresión (suave, dura, etc.) se muestran en la lista de supresión. Obtenga más información sobre el acceso y la administración de la lista de supresión en [esta sección](configuration/manage-suppression-list.md).

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

>[!NOTE]
>
>Los perfiles con estado **[!UICONTROL Suppressed]** se excluyen durante el proceso de envío de mensajes. Por lo tanto, mientras que los **informes de Recorrido** mostrarán estos perfiles como si se hubieran movido a través del recorrido ([Leer segmento](building-journeys/read-segment.md) y [Mensaje](building-journeys/journeys-message.md)), los **Informes de correo electrónico** no los incluirán en las métricas **[!UICONTROL Sent]** ya que se filtrarán antes de enviarlos por correo electrónico.
>
>Obtenga más información sobre [Live Report](reports/live-report.md) y [Global Report](reports/global-report.md). Para averiguar el motivo de todos los casos de exclusión, puede utilizar el [Servicio de consulta de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html).

### Errores de entrega {#delivery-failures}

Existen dos tipos de errores cuando falla una entrega:

* **Rechazo** duro. Un rechazo grave indica una dirección de correo electrónico no válida (es decir, una dirección de correo electrónico que no existe). Esto implica un mensaje de rechazo del servidor de correo electrónico receptor que indica explícitamente que la dirección no es válida.
* **Rechazo suave**. Se trata de una devolución temporal de correo electrónico que se produjo para una dirección de correo electrónico válida.
<!--* **Ignored**. This is an email bounce that occurred for a valid email address but is known to be temporary, such as a failed connection attempt, a temporary Spam-related issue (email reputation), or a temporary technical issue.-->

Un **rechazo grave** agrega automáticamente la dirección de correo electrónico a la lista de supresión.

Un **rechazo suave** <!--or an **ignored** error--> que ocurre demasiadas veces también envía la dirección de correo electrónico a la lista de supresión después de varios reintentos. [Más información sobre los reintentos](configuration/retries.md)

Si continúa enviando direcciones a estas, puede afectar a las tasas de envío, ya que indica a los ISP que puede que no siga las prácticas recomendadas de mantenimiento de la lista de direcciones de correo electrónico y, por lo tanto, puede que no sea un remitente fiable.

### Reclamaciones por correo no deseado {#spam-complaints}

La lista de supresión recopila direcciones de correo electrónico que marcan el mensaje como correo no deseado. Por ejemplo, si alguien escribe a un servicio de atención al cliente pidiéndole que nunca vuelva a recibir correo, la dirección de correo electrónico de esa persona se suprime en toda la instancia y ya no podrá enviarlo a esa dirección.

El envío a los destinatarios después de que envíen una queja por correo no deseado puede tener un gran impacto en su reputación de envío, ya que informa a los ISP de que puede enviar correos electrónicos no deseados y no escuchar a sus destinatarios.

Esto podría hacer que su dirección IP o dominio de envío se bloquearan, lo que se puede evitar con estas direcciones en la lista de supresión.

<!--### Unsubscriptions {#unsubscriptions}

Every email sent to recipients must include an unsubscribe link. Upon clicking this link, if a recipient confirms [opting out](consent.md), the corresponding email address is immediately sent to the suppression list. This user must not receive communication from your brand until subscribed again.
NOT TRUE > "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

<!--MOVED to Configuration/Retries section

The threshold is set at three errors:
* For the same delivery, at the third attempt, the address is suppressed.
* If there are different deliveries and two errors occur at least 24 hours apart, the error counter is incremented upon each error and the address is also suppressed at the third attempt.
When a delivery is successful after a retry, the error counter of the address is reinitialized.

### Retries {#retries}

If a message fails due to a temporary bounce of the **Ignored** type, retries will be performed for **3.5 days** from the time the message was added to the email queue.

The minimum delay between retries and the maximum number of retries to be performed are ///managed by the Enhanced MTA/// based on how well an IP is performing, both historically and currently at a given domain.

After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->
