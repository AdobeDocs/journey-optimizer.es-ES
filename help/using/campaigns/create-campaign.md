---
solution: Journey Optimizer
product: journey optimizer
title: Creación de una campaña
description: Aprenda a crear campañas en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: crear, optimizador, campaña, superficie, mensajes
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 21%

---

# Creación de una campaña {#create-campaign}

>[!NOTE]
>
>Antes de crear una nueva campaña, asegúrese de que tiene un canal superficial (es decir, un mensaje preestablecido) y un segmento de Adobe Experience Platform listo para usar. Obtenga más información en estas secciones:
>
>* [Creación de superficies de canal](../configuration/channel-surfaces.md)
>* [Introducción a los segmentos](../segment/about-segments.md)


Para crear una nueva campaña, acceda al **[!UICONTROL Campañas]** a continuación, haga clic en **[!UICONTROL Crear campaña]**. También puede duplicar una campaña en vivo existente para crear una nueva. [Más información](modify-stop-campaign.md#duplicate)

## Elija el tipo de campaña y el canal {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo de campaña"
>abstract="Para un mensaje de marketing especificando una fecha de envío, el tipo **Programado** es el más adecuado. Sin embargo, si desea enviar mensajes transaccionales como restablecimiento de contraseña o abandono del carro de compras, el tipo **Activado por API** es la mejor opción."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Categoría de la campaña"
>abstract="El valor de categoría está asociado directamente al valor de tipo de campaña. Programar tipo de campaña para la categoría **Marketing** y tipo activado por API para la categoría **Transaccional**"

1. En el **[!UICONTROL Propiedades]** especifique cómo desea ejecutar la campaña. Hay dos tipos de campaña disponibles:

   * **[!UICONTROL Programado]**: ejecutar la campaña inmediatamente o en una fecha especificada. Las campañas programadas tienen como objetivo enviar **marketing** escriba mensajes.

   * **[!UICONTROL Activado por API]**: ejecute la campaña utilizando una llamada de API. Las campañas activadas por API están destinadas a enviar **transaccional** mensajes, es decir, mensajes enviados siguiendo una acción realizada por un individuo: restablecimiento de contraseña, abandono del carro de compras, etc. [Obtenga información sobre cómo almacenar en déclencheur una campaña mediante API](api-triggered-campaigns.md)

1. En el **[!UICONTROL Acciones]** , seleccione el canal y la superficie del canal que desea utilizar para enviar el mensaje.

   Una superficie es una configuración que ha definido un [Administrador del sistema](../start/path/administrator.md). Contiene todos los parámetros técnicos para enviar el mensaje, como parámetros de encabezado, subdominio, aplicaciones móviles, etc. [Más información](../configuration/channel-surfaces.md).

   En la lista desplegable solo se muestran las superficies de canal compatibles con el tipo de campaña de marketing.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Si está creando una campaña de notificaciones push, puede habilitar la variable **[!UICONTROL Modo de entrega rápido]**, que es un complemento de Journey Optimizer que permite enviar mensajes push muy rápidamente en grandes volúmenes. [Más información](../push/create-push.md#rapid-delivery)

1. Haga clic en **[!UICONTROL Crear]** para crear la campaña.

## Definir las propiedades de la campaña {#create}

1. En el **[!UICONTROL Propiedades]** , especifique un nombre y una descripción para la campaña.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. La variable **Etiquetas** permite asignar etiquetas unificadas de Adobe Experience Platform a la campaña. Esto le permite clasificarlos fácilmente y mejorar la búsqueda desde la lista de campañas. [Aprenda a trabajar con etiquetas](../start/search-filter-categorize.md#tags)

1. Para asignar etiquetas de uso de datos principales o personalizadas a la campaña, haga clic en el botón **[!UICONTROL Administrar acceso]** botón. [Obtenga más información sobre Control de acceso a nivel de objeto (OLA)](../administration/object-based-access.md)

## Creación del mensaje y configuración del seguimiento {#content}

En el **[!UICONTROL Acciones]** , cree el mensaje que desea enviar con la campaña.

1. Haga clic en el **[!UICONTROL Editar contenido]** y, a continuación, cree y diseñe el contenido del mensaje.

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

1. Una vez definido el contenido, utilice la variable **[!UICONTROL Simular contenido]** para previsualizar y probar el contenido con perfiles de prueba. [Más información](../email/preview.md).

1. Haga clic en la flecha para volver a la pantalla de creación de la campaña.

   ![](assets/create-campaign-design.png)

1. En el **[!UICONTROL Seguimiento de acciones]** , especifique si desea rastrear cómo reaccionan los destinatarios a su envío: puede rastrear clics o aperturas.

   Una vez ejecutada la campaña, se podrá acceder a los resultados de seguimiento desde el informe de campaña. [Más información sobre los informes de campaña](../reports/campaign-global-report.md)

## Definición de la audiencia {#audience}

Haga clic en el **[!UICONTROL Seleccionar la audiencia]** para mostrar la lista de segmentos de Adobe Experience Platform disponibles. [Más información sobre los segmentos](../segment/about-segments.md)

>[!NOTE]
>
>Para las campañas activadas por API, la audiencia debe configurarse mediante una llamada a la API. [Más información](api-triggered-campaigns.md)

En el **[!UICONTROL Área de nombres de identidad]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado. [Más información sobre áreas de nombres](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

    >[!NOTE]
    >
    >Las personas que pertenezcan a un segmento que no tenga la identidad seleccionada (área de nombres) entre sus distintas identidades no serán el objetivo de la campaña.

<!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Programar la campaña {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Inicio de campaña"
>abstract="Especifique la fecha y la hora a las que se debe enviar el mensaje."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fin de campaña"
>abstract="Especifique cuándo se debe detener la ejecución de una campaña recurrente."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Activadores de acciones de campaña"
>abstract="Defina una frecuencia a la que se debe enviar el mensaje de la campaña."

De forma predeterminada, las campañas se inician una vez activadas manualmente y finalizan en cuanto se envía una vez el mensaje.

Puede definir una frecuencia a la que se debe enviar el mensaje de la campaña. Para ello, utilice el **[!UICONTROL Déclencheur de acción]** en la pantalla de creación de la campaña para especificar si la campaña debe ejecutarse diariamente, semanalmente o mensualmente.

Si no desea ejecutar la campaña justo después de su activación, puede especificar una fecha y hora a la que se debe enviar el mensaje mediante la variable **[!UICONTROL Inicio de la campaña]** . La variable **[!UICONTROL Fin de la campaña]** permite especificar cuándo se debe detener la ejecución de una campaña recurrente.

![](assets/create-campaign-schedule.png)

Una vez preparada la campaña, puede revisarla y publicarla. [Más información](review-activate-campaign.md)
