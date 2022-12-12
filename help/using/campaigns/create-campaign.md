---
solution: Journey Optimizer
product: journey optimizer
title: Creación de una campaña
description: Obtenga información sobre cómo crear campañas en [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: ab770b7b48fc906634f12458e0b31c7db0f641e8
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Creación de una campaña {#create-campaign}

>[!NOTE]
>
>Antes de crear una nueva campaña, asegúrese de que tiene un canal superficial (es decir, un mensaje preestablecido) y un segmento de Adobe Experience Platform listos para usar. Obtenga más información en estas secciones:
>
>* [Creación de superficies de canal](../configuration/channel-surfaces.md)
>* [Introducción a los segmentos](../segment/about-segments.md)


Para crear una nueva campaña, acceda al **[!UICONTROL Campaigns]** a continuación, haga clic en **[!UICONTROL Create campaign]**. También puede duplicar una campaña en vivo existente para crear una nueva. [Más información](modify-stop-campaign.md#duplicate)

![](assets/create-campaign.png)

## Elija el tipo de campaña y el canal {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo de campaña"
>abstract="Para un mensaje de marketing especificando una fecha de envío, la variable **Programado** es el más adecuado. Sin embargo, si desea enviar mensajes transaccionales como restablecimiento de contraseña o abandono de tarjeta, la variable **Activado por API** es la mejor opción."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Categoría de la campaña"
>abstract="El valor de categoría está asociado directamente al valor de tipo de campaña. Programar tipo de campaña para **Marketing** categoría y tipo activado por API para la categoría **Transaccional**"

1. En el **[!UICONTROL Properties]** especifique cómo desea ejecutar la campaña. Hay dos tipos de campaña disponibles:

   * **[!UICONTROL Scheduled]**: ejecutar la campaña inmediatamente o en una fecha especificada. Las campañas programadas tienen como objetivo enviar **marketing** escriba mensajes.

   * **[!UICONTROL API-triggered]**: ejecute la campaña utilizando una llamada de API. Las campañas activadas por API están destinadas a enviar **transaccional** mensajes, es decir, mensajes enviados siguiendo una acción realizada por un individuo: restablecimiento de contraseña, abandono de tarjeta, etc. [Obtenga información sobre cómo activar una campaña mediante API](api-triggered-campaigns.md)

1. En el **[!UICONTROL Actions]** , seleccione el canal y la superficie del canal que desea utilizar para enviar el mensaje.

   Una superficie es una configuración que se ha definido mediante una [Administrador del sistema](../start/path/administrator.md). Contiene todos los parámetros técnicos para enviar el mensaje, como parámetros de encabezado, subdominio, aplicaciones móviles, etc. [Más información](../configuration/channel-surfaces.md).

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >En la lista desplegable solo se muestran las superficies de canal compatibles con el tipo de campaña de marketing.

1. Haga clic en **[!UICONTROL Create]** para crear la campaña.

## Definir las propiedades de la campaña {#create}

1. Especifique un título y una descripción para la campaña.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. Para asignar etiquetas de uso de datos principales o personalizadas a la campaña, haga clic en el botón **[!UICONTROL Manage access]** botón. [Obtenga más información sobre Control de acceso a nivel de objeto (OLA)](../administration/object-based-access.md)

   ![](assets/create-campaign-properties.png)

## Creación del mensaje {#content}

En el **[!UICONTROL Actions]** , cree el mensaje que desea enviar con la campaña.

1. Haga clic en el **[!UICONTROL Edit content]** y, a continuación, cree y diseñe el contenido del mensaje.

   Conozca los pasos detallados para crear el contenido del mensaje en las páginas siguientes:

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="Posible cliente" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>Creación de correos electrónicos</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="Poco frecuente" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong>Creación de notificaciones push</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="Validación" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>Creación de mensajes SMS</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

1. Una vez definido el contenido, utilice la variable **[!UICONTROL Simulate content]** para previsualizar y probar el contenido con perfiles de prueba. [Más información](../email/preview.md).

1. Haga clic en la flecha para volver a la pantalla de creación de la campaña.

   ![](assets/create-campaign-design.png)

1. En el **[!UICONTROL Actions tracking]** , especifique si desea rastrear cómo reaccionan los destinatarios a su envío: puede rastrear clics o aperturas.

   Una vez ejecutada la campaña, se podrá acceder a los resultados de seguimiento desde el informe de campaña. [Más información sobre los informes de campaña](../reports/campaign-global-report.md)

## Definición de la audiencia {#audience}

1. Defina la audiencia objetivo. Para ello, haga clic en el botón **[!UICONTROL Select audience]** para mostrar la lista de segmentos disponibles de Adobe Experience Platform. [Más información sobre los segmentos](../segment/about-segments.md)

   >[!NOTE]
   >
   >Para las campañas activadas por API, la audiencia debe configurarse mediante una llamada a la API. [Más información](api-triggered-campaigns.md)

   En el **[!UICONTROL Identity namespace]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado. [Más información sobre áreas de nombres](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Las personas que pertenezcan a un segmento que no tenga la identidad seleccionada (área de nombres) entre sus diferentes identidades no serán el objetivo de la campaña.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Programar la campaña {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Inicio de la campaña"
>abstract="Especifique la fecha y la hora a las que se debe enviar el mensaje."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fin de la campaña"
>abstract="Especifique cuándo se debe detener la ejecución de una campaña recurrente."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Activadores de acciones de Campaign"
>abstract="Defina una frecuencia a la que se debe enviar el mensaje de la campaña."

De forma predeterminada, las campañas se inician una vez activadas manualmente y finalizan en cuanto se envía una vez el mensaje.

Puede definir una frecuencia a la que se debe enviar el mensaje de la campaña. Para ello, utilice el **[!UICONTROL Action triggers]** en la pantalla de creación de la campaña para especificar si la campaña debe ejecutarse diariamente, semanalmente o mensualmente.

Si no desea ejecutar la campaña justo después de su activación, puede especificar una fecha y hora a la que se debe enviar el mensaje mediante la variable **[!UICONTROL Campaign start]** . La variable **[!UICONTROL Campaign end]** permite especificar cuándo se debe detener la ejecución de una campaña recurrente.

![](assets/create-campaign-schedule.png)

Una vez preparada la campaña, puede revisarla y publicarla. [Más información](#review-activate)
