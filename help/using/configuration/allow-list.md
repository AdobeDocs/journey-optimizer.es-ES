---
title: Lista de permitidos
description: Aprenda a utilizar la lista de permitidos .
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: e81e21f714a3c5450defa1129e1e2b9969dc1de7
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 2%

---

# Lista de permitidos {#allow-list}

Es posible definir una lista específica de envío seguro en la variable [entorno limitado](../administration/sandboxes.md) nivel.

Esta lista de permitidos le permite especificar direcciones de correo electrónico o dominios individuales que serán los únicos destinatarios o dominios autorizados para recibir los correos electrónicos que envía desde un entorno limitado específico.

>[!NOTE]
>
>Esta función está disponible en entornos limitados de producción y no de producción.

Por ejemplo, en una instancia que no es de producción, donde pueden producirse errores, la lista de permitidos garantiza que no corra ningún riesgo de enviar mensajes no deseados a direcciones de clientes reales y, por lo tanto, proporciona un entorno seguro para realizar pruebas.

Además, cuando la lista de permitidos está activa pero vacía, no se envía ningún correo. Por lo tanto, si tiene algún problema importante, puede utilizar esta función para detener todas las comunicaciones salientes de [!DNL Journey Optimizer] hasta que solucione el problema. Obtenga más información sobre [lógica de lista de permitidos](#logic).

>[!CAUTION]
>
>Esta función solo se aplica al canal de correo electrónico.

## Acceso a la lista de permitidos {#access-allowed-list}

Para acceder a la lista detallada de direcciones de correo electrónico y dominios permitidos, vaya a **[!UICONTROL Administración]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** y seleccione **[!UICONTROL Lista de permitidos]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>Los permisos para ver, exportar y administrar la lista de permitidos están restringidos a [Administradores de recorrido](../administration/ootb-product-profiles.md#journey-administrator). Más información sobre la administración [!DNL Journey Optimizer] derechos de acceso de los usuarios en [esta sección](../administration/permissions-overview.md).

Para exportar la lista de permitidos como archivo CSV, seleccione la opción **[!UICONTROL Descargar CSV]** botón.

Utilice la variable **[!UICONTROL Eliminar]** para eliminar permanentemente una entrada.

Puede buscar en las direcciones de correo electrónico o en los dominios y filtrar por el **[!UICONTROL Tipo de dirección]**. Una vez seleccionado, puede borrar el filtro mostrado en la parte superior de la lista.

![](assets/allowed-list-filtering-example.png)

## Activar la lista de permitidos {#enable-allow-list}

Para activar la lista de permitidos, siga los pasos a continuación.

1. Acceda a la  **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Lista de permitidos]** para abrir el Navegador.

1. Haga clic en **[!UICONTROL Desactivado]**.

   ![](assets/allow-list-edit.png)

1. Select **[!UICONTROL Activar lista de permitidos]**. La lista de permitidos está activa.

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >Después de activar la lista de permitidos, hay una latencia de 5 minutos para que tenga efecto en sus recorridos y campañas.

La lógica de lista de permitidos se aplica cuando la función está activa. Obtenga más información en [esta sección](#logic).

>[!NOTE]
>
>Cuando se activa, se respeta la función de lista de permitidos al ejecutar recorridos, pero también al probar mensajes con [pruebas](../design/preview.md#send-proofs) y recorridos de prueba utilizando [modo de prueba](../building-journeys/testing-the-journey.md).

## Desactivar la lista de permitidos {#deactivate-allow-list}

Para desactivar la lista de permitidos, siga los pasos a continuación.

1. Acceda a la  **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Lista de permitidos]** para abrir el Navegador.

1. Haga clic en **[!UICONTROL Activo]**.

   ![](assets/allow-list-edit-active.png)

1. Select **[!UICONTROL Desactivar lista de permitidos]**. La lista de permitidos ya no está activa.

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >Después de desactivar la lista de permitidos, hay una latencia de 5 minutos para que tenga efecto en los recorridos y campañas.

La lógica de lista de permitidos no se aplica cuando la función está desactivada. Obtenga más información en [esta sección](#logic).

## Añadir entidades a la lista de permitidos {#add-entities}

Para agregar nuevas direcciones de correo electrónico o dominios a la lista de permitidos de un entorno limitado específico, puede: [rellenar manualmente la lista](#manually-populate-list)o use una [Llamada de API](#api-call-allowed-list).

>[!NOTE]
>
>La lista de permitidos puede contener hasta 1000 entradas.

### Rellenado manual de la lista de permitidos {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="Añadir direcciones o dominios a la lista de permitidos"
>abstract="Puede añadir manualmente nuevas direcciones de correo electrónico o dominios a la lista de permitidos seleccionándolos uno a uno."

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="Añadir direcciones o dominios a la lista de permitidos"
>abstract="Puede añadir manualmente nuevas direcciones de correo electrónico o dominios a la lista de permitidos seleccionándolos uno a uno."

Puede rellenar manualmente la variable [!DNL Journey Optimizer] lista de permitidos añadiendo una dirección de correo electrónico o un dominio a través de la interfaz de usuario.

>[!NOTE]
>
>Solo puede añadir una dirección de correo electrónico o un dominio a la vez.

Para realizar esto, siga los pasos a continuación.

1. Seleccione el **[!UICONTROL Añadir correo electrónico o dominio]** botón.

   ![](assets/allowed-list-add-email.png)

1. Elija el tipo de dirección: **[!UICONTROL Dirección de correo electrónico]** o **[!UICONTROL Dirección del dominio]**.

1. Introduzca la dirección de correo electrónico o el dominio al que desee enviar los correos electrónicos.

   >[!NOTE]
   >
   >Asegúrese de introducir una dirección de correo electrónico válida (como abc@company.com) o un dominio (como abc.company.com).

1. Especifique un motivo si es necesario.

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >Se permiten todos los caracteres ASCII comprendidos entre 32 y 126 en la variable **[!UICONTROL Razón]** campo . La lista completa se encuentra en [esta página](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target=&quot;_blank&quot;} por ejemplo.

1. Haga clic en **[!UICONTROL Enviar]**.

### Añadir entidades mediante una llamada de API {#api-call-allowed-list}

Para rellenar la lista de permitidos, también puede llamar a la API de supresión con la función `ALLOWED` para la variable `listType` atributo. Por ejemplo:

![](assets/allow-list-api.png)

Puede realizar el **Agregar**, **Eliminar** y **Get** operaciones.

Obtenga más información sobre cómo realizar llamadas de API en la sección [API de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html)Documentación de referencia de {target=&quot;_blank&quot;}.

## lógica de lista de permitidos {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="Administrar la lista de permitidos"
>abstract="Cuando se activa la lista de permitidos, solo los destinatarios incluidos en la lista de permitidos reciben mensajes de correo electrónico de este simulador para pruebas."

Cuando la lista de permitidos es [active](#enable-allow-list), se aplica la siguiente lógica:

* Si la lista de permitidos es **empty**, no se enviará ningún correo electrónico.

* Si una entidad es **en la lista de permitidos** y no en la lista de supresión, el correo electrónico se envía a los destinatarios correspondientes. Sin embargo, si la entidad también está en la variable [lista de supresión](../reports/suppression-list.md), los destinatarios correspondientes no recibirán el correo electrónico, por lo que **[!UICONTROL Suprimido]**.

* Si una entidad es **no en la lista de permitidos** (y no en la lista de supresión), los destinatarios correspondientes no recibirán el correo electrónico, por lo que **[!UICONTROL No permitido]**.

>[!NOTE]
>
>Los perfiles con **[!UICONTROL No permitido]** se excluyen durante el proceso de envío de mensajes. Por lo tanto, mientras que la variable **Informes de recorrido** mostrará estos perfiles como si se hubieran movido a través del recorrido ([Leer segmento](../building-journeys/read-segment.md) y [actividades de mensaje](../building-journeys/journeys-message.md)), el **Informes de correo electrónico** no los incluirá en la variable **[!UICONTROL Enviado]** las métricas tal y como están filtradas antes del envío por correo electrónico.
>
>Obtenga más información sobre [Informe Activo](../reports/live-report.md) y [Informe global](../reports/global-report.md).

Cuando la lista de permitidos es [desactivado](#deactivate-allow-list), todos los correos electrónicos que envía desde el entorno limitado actual se envían a todos los destinatarios (siempre que no estén en la lista de supresión), incluidas las direcciones de cliente reales.

## Informes de exclusión {#reporting}

Cuando la lista de permitidos está activa, puede recuperar direcciones de correo electrónico o dominios que se excluyeron de un envío porque no estaban en la lista de permitidos. Para ello, puede usar la variable [Servicio de consultas de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;} para realizar las llamadas de API que se indican a continuación.

Para obtener la variable **número de correos electrónicos** que no se enviaron porque los destinatarios no estaban en la lista de permitidos, utilice la siguiente consulta:

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Para obtener la variable **lista de direcciones de correo electrónico** que no se enviaron porque los destinatarios no estaban en la lista de permitidos, utilice la siguiente consulta:

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
