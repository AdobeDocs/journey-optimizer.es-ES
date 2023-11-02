---
solution: Journey Optimizer
product: journey optimizer
title: Lista de permitidos
description: Aprenda a utilizar la lista de permitidos
feature: Deliverability
topic: Content Management
role: Admin
level: Experienced
keywords: lista de permitidos, lista, seguro, configuración
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: b4fda6a0bd3e633811c16ef6dc3a3171b3b350c8
workflow-type: tm+mt
source-wordcount: '1165'
ht-degree: 15%

---

# Lista de permitidos {#allow-list}

Es posible definir una lista específica de seguridad de envío en [espacio aislado](../administration/sandboxes.md) nivel.

Esta lista de permitidos le permite especificar direcciones de correo electrónico o dominios individuales que serán los únicos destinatarios o dominios autorizados para recibir los correos electrónicos que envía desde una zona protegida específica.

>[!CAUTION]
>
>Actualmente, esta función solo se aplica al canal de correo electrónico. Está disponible en entornos limitados de producción y sin producción.

Por ejemplo, en una instancia que no es de producción, donde pueden producirse errores, la lista de permitidos garantiza que no tendrá riesgo de enviar mensajes no deseados a direcciones de clientes reales y, por lo tanto, proporciona un entorno seguro para realizar pruebas.

Además, cuando la lista de permitidos está activa pero vacía, no se envía ningún correo. Por lo tanto, si encuentra algún problema importante, puede utilizar esta función para detener todas las comunicaciones salientes de [!DNL Journey Optimizer] hasta que arregles el problema. Obtenga más información sobre [lógica de lista de permitidos](#logic).

Además, puede aprovechar Journey Optimizer **API de REST de supresión** para controlar los mensajes salientes mediante supresión y listas de permitidos. [Aprenda a trabajar con la API de REST de supresión](https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/manage-suppression-list.html?lang=es)

## Acceso a la lista de permitidos {#access-allowed-list}

Para acceder a la lista detallada de direcciones de correo electrónico y dominios permitidos, vaya a **[!UICONTROL Administration]** > **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** y seleccione **[!UICONTROL Lista de permitidos]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>Los permisos para ver, exportar y administrar la lista de permitidos están restringidos a [Administradores de recorrido](../administration/ootb-product-profiles.md#journey-administrator). Más información sobre la administración de [!DNL Journey Optimizer] derechos de acceso de los usuarios en [esta sección](../administration/permissions-overview.md).

Para exportar la lista de permitidos como archivo CSV, seleccione la **[!UICONTROL Descargar CSV]** botón.

Utilice el **[!UICONTROL Eliminar]** para eliminar una entrada de forma permanente.

Puede buscar en las direcciones de correo electrónico o dominios y filtrar por el **[!UICONTROL Tipo de dirección]**. Una vez seleccionado, puede borrar el filtro mostrado en la parte superior de la lista.

![](assets/allowed-list-filtering-example.png)

## Activar la lista de permitidos {#enable-allow-list}

Para activar la lista de permitidos, siga los pasos a continuación.

1. Acceda a la  **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Lista de permitidos]** menú.

1. Seleccione el botón de alternancia.

   ![](assets/allow-list-edit.png)

1. Seleccionar **[!UICONTROL Activar lista de permitidos]**. La lista de permitidos está activa.

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >Después de activar la lista de permitidos, existe una latencia de 5 minutos para que surta efecto en los recorridos y campañas.

La lógica de lista de permitidos se aplica cuando la función está activa. Obtenga más información en [esta sección](#logic).

>[!NOTE]
>
>Cuando se activa, la función de lista de permitidos se cumple al ejecutar recorridos, pero también al probar mensajes con [pruebas](../content-management/proofs.md) y recorridos de prueba con la variable [modo de prueba](../building-journeys/testing-the-journey.md).

## Desactivar la lista de permitidos {#deactivate-allow-list}

Para desactivar la lista de permitidos, siga los pasos a continuación.

1. Acceda a la  **[!UICONTROL Canales]** > **[!UICONTROL Configuración de correo electrónico]** > **[!UICONTROL Lista de permitidos]** menú.

1. Seleccione el botón de alternancia.

   ![](assets/allow-list-edit-active.png)

1. Seleccionar **[!UICONTROL Desactivar lista de permitidos]**. La lista de permitidos ya no está activa.

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >Después de desactivar la lista de permitidos, existe una latencia de 5 minutos para que surta efecto en los recorridos y campañas.

La lógica de lista de permitidos no se aplica cuando la función está desactivada. Obtenga más información en [esta sección](#logic).

## Añadir entidades a la lista de permitidos {#add-entities}

Para agregar nuevas direcciones de correo electrónico o dominios a la lista de permitidos de una zona protegida específica, puede [rellenar manualmente la lista](#manually-populate-list), o use un [Llamada de API](#api-call-allowed-list).

>[!NOTE]
>
>La lista de permitidos puede contener hasta 1000 entradas.

### Rellenar manualmente la lista de permitidos {#manually-populate-list}

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
>Solo se puede agregar una dirección de correo electrónico o un dominio a la vez.

Para realizar esto, siga los pasos a continuación.

1. Seleccione el **[!UICONTROL Añadir correo electrónico o dominio]** botón.

   ![](assets/allowed-list-add-email.png)

1. Elija el tipo de dirección: **[!UICONTROL Dirección de correo electrónico]** o **[!UICONTROL Dirección del dominio]**.

1. Introduzca la dirección de correo electrónico o el dominio al que desea enviar los correos electrónicos.

   >[!NOTE]
   >
   >Asegúrese de introducir una dirección de correo electrónico válida (como abc@compañía.com) o un dominio (como abc.compañía.com).

1. Especifique una razón, si es necesario.

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >Todos los caracteres ASCII comprendidos entre 32 y 126 están permitidos en **[!UICONTROL Motivo]** field. La lista completa se encuentra en [esta página](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target="_blank"}, por ejemplo.

1. Haga clic en **[!UICONTROL Enviar]**.

### Añadir entidades mediante una llamada de API {#api-call-allowed-list}

Para rellenar la lista de permitidos, también puede llamar a la API de supresión con `ALLOWED` valor para `listType` atributo. Por ejemplo:

![](assets/allow-list-api.png)

Puede realizar las siguientes acciones **Añadir**, **Eliminar** y **Obtener** operaciones.

Obtenga más información sobre cómo realizar llamadas de API en la [API de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target="_blank"} documentación de referencia.

## Descargar la lista de permitidos {#download-allowed-list}

Para exportar la lista de permitidos como archivo CSV, siga los pasos a continuación:

1. Seleccione el **[!UICONTROL Descargar CSV]** botón.

   ![](assets/allowed-list-download-csv.png)

1. Espere hasta que se genere el archivo.

   ![](assets/allowed-list-download-generate.png)

   >[!NOTE]
   >
   >El tiempo de descarga depende del tamaño del archivo, es decir, del número de direcciones que hay en la lista de permitidos.
   >
   >Se puede procesar una solicitud de descarga a la vez para una zona protegida determinada.

1. Una vez generado el archivo, recibirá una notificación. Haga clic en el icono de campana en la parte superior derecha de la pantalla para mostrarlo.

1. Haga clic en la propia notificación para descargar el archivo.

   ![](assets/allowed-list-download-notification.png)

   >[!NOTE]
   >
   >El vínculo es válido durante 24 horas.

## lógica de lista de permitidos {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="Administrar la lista de permitidos"
>abstract="Cuando la lista de permitidos está activada, solo los destinatarios incluidos en la lista de permitidos reciben mensajes de correo electrónico de esta zona protegida. Cuando está desactivado, todos los destinatarios reciben correos electrónicos."

Cuando la lista de permitidos es [activo](#enable-allow-list), se aplica la siguiente lógica:

* Si la lista de permitidos es **vaciar**, no se enviará ningún correo electrónico.

* Si una entidad es **en la lista de permitidos**, y no en la lista de supresión, el correo electrónico se envía a los destinatarios correspondientes. Sin embargo, si la entidad también está en [lista de supresión](../reports/suppression-list.md), los destinatarios correspondientes no recibirán el correo electrónico, el motivo es **[!UICONTROL Suprimido]**.

* Si una entidad es **no en la lista de permitidos** (y no en la lista de supresión), los destinatarios correspondientes no recibirán el correo electrónico, el motivo es **[!UICONTROL No permitido]**.

>[!NOTE]
>
>Los perfiles con **[!UICONTROL No permitido]** Los estados de se excluyen durante el proceso de envío de mensajes. Por lo tanto, mientras que la variable **informes de recorrido** mostrará estos perfiles como si se hubieran movido a través del recorrido ([Leer audiencia](../building-journeys/read-audience.md) y [actividades de mensajería](../building-journeys/journeys-message.md)), el **Informes de correo electrónico** no los incluirá en la **[!UICONTROL Enviado]** las métricas tal como se filtran antes del envío de correo electrónico.
>
>Obtenga más información sobre [Informe en vivo](../reports/live-report.md) y [Informe global](../reports/global-report.md).

Cuando la lista de permitidos es [desactivado](#deactivate-allow-list)Sin embargo, todos los correos electrónicos que envía desde la zona protegida actual se envían a todos los destinatarios (siempre que no estén en la lista de supresión), incluidas las direcciones de clientes reales.

## Informes de exclusión {#reporting}

Cuando la lista de permitidos esté activa, puede recuperar direcciones de correo electrónico o dominios que se excluyeron de un envío porque no estaban en la lista de permitidos. Para ello, puede utilizar el complemento [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"} para realizar las llamadas de API siguientes.

Para obtener la **número de correos electrónicos** que no se enviaron porque los destinatarios no estaban en la lista de permitidos, utilice la siguiente consulta:

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Para obtener la **lista de direcciones de correo electrónico** que no se enviaron porque los destinatarios no estaban en la lista de permitidos, utilice la siguiente consulta:

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
