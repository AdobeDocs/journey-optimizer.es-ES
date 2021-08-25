---
title: Lista de permitidos
description: Aprenda a utilizar la lista de permitidos .
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: 2edb3535c50f83d18ce4d6429a6d76f44b694ac6
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 1%

---

# Lista de permitidos {#allow-list}

Ahora es posible definir una lista específica de envío seguro en el nivel [sandbox](administration/sandboxes.md), para tener un entorno seguro con fines de prueba. En una instancia que no es de producción, donde pueden producirse errores, la lista de permitidos garantiza que no tendrá riesgo de enviar mensajes no deseados a sus clientes.

La lista de permitidos permite especificar direcciones de correo electrónico o dominios individuales que serán los únicos destinatarios o dominios autorizados para recibir los correos electrónicos que envía desde un entorno limitado específico. Esto puede impedir que envíe correos electrónicos accidentalmente a direcciones de clientes reales cuando se encuentre en un entorno de prueba.

>[!CAUTION]
>
>Esta función **no** está disponible en entornos limitados de producción. Solo se aplica al canal de correo electrónico.

## Habilitar la lista de permitidos {#enable-allow-list}

Para habilitar la lista de permitidos en un simulador para pruebas que no sean de producción, debe actualizar la configuración general utilizando el punto final de API correspondiente en el servicio de ajustes preestablecidos de mensajes.

* Con esta API, también puede deshabilitar la función en cualquier momento.

* Puede actualizar la lista de permitidos antes o después de habilitar la función.

* La lógica de lista de permitidos se aplica cuando la función está habilitada **y** si la lista de permitidos está **no** vacía. Obtenga más información en [esta sección](#logic).

<!--To enable this feature on a non-production sandbox, update the allowed list so that it is no longer empty. To disable it, clear up the allowed list so that it is again empty.

Learn more on the allowed list logic in this section.
-->

>[!NOTE]
>
>Cuando está habilitada, la función de lista de permitidos se cumple al ejecutar recorridos, pero también al probar mensajes con [pruebas](preview.md#send-proofs) y probar recorridos usando el [modo de prueba](building-journeys/testing-the-journey.md).

## Añadir entidades a la lista de permitidos {#add-entities}

Para agregar nuevas direcciones de correo electrónico o dominios a la lista de permitidos para un entorno limitado específico, debe llamar a la API de supresión con el valor `ALLOWED` del atributo `listType`. Por ejemplo:

![](assets/allow-list-api.png)

Puede realizar las operaciones **Add**, **Delete** y **Get**.

>[!NOTE]
>
>La lista de permitidos puede contener hasta 1000 entradas.

<!--
Learn more on making these API calls in the API reference documentation.
Found this link in Experience Platform documentation, but may not be the final one: (https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## lógica de lista de permitidos {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Cuando la lista de permitidos está **vacía**, no se aplica la lógica de lista de permitidos. Esto significa que puede enviar correos electrónicos a cualquier perfil, siempre que no estén en la [lista de supresión](suppression-list.md).

Cuando la lista de permitidos es **no está vacía**, se aplica la lógica de lista de permitidos:

* Si una entidad **no está en la lista de permitidos** y no está en la lista de supresión, el destinatario correspondiente no recibirá el correo electrónico, por lo que es **[!UICONTROL Not allowed]**.

* Si una entidad está **en la lista de permitidos** y no en la lista de supresión, el correo electrónico se puede enviar al destinatario correspondiente. Sin embargo, si la entidad también está en la [lista de supresión](suppression-list.md), el destinatario correspondiente no recibirá el correo electrónico, por lo que es **[!UICONTROL Suppressed]**.

>[!NOTE]
>
>Los perfiles con estado **[!UICONTROL Not allowed]** se excluyen durante el proceso de envío de mensajes. Por lo tanto, mientras que los **informes de Recorrido** mostrarán estos perfiles como si se hubieran movido a través del recorrido ([Leer segmento](building-journeys/read-segment.md) y [Mensaje](building-journeys/journeys-message.md)), los **Informes de correo electrónico** no los incluirán en las métricas **[!UICONTROL Sent]** ya que se filtrarán antes de enviarlos por correo electrónico.
>
>Obtenga más información sobre [Live Report](reports/live-report.md) y [Global Report](reports/global-report.md).

## Informes de exclusión {#reporting}

Cuando esta función está habilitada en un simulador para pruebas que no sean de producción, puede recuperar direcciones de correo electrónico o dominios que se excluyeron de un envío porque no estaban en la lista de permitidos. Para ello, puede utilizar el [servicio de consulta de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html) para realizar las llamadas de API que se indican a continuación.

Para obtener el **número de correos electrónicos** que no se enviaron porque los destinatarios no estaban en la lista de permitidos, utilice la siguiente consulta:

```
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Para obtener la **lista de direcciones de correo electrónico** que no se enviaron porque los destinatarios no estaban en la lista de permitidos, utilice la siguiente consulta:

```
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

