---
solution: Journey Optimizer
product: journey optimizer
title: Creación de una campaña
description: Obtenga información sobre cómo crear campañas en Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: crear, optimizador, campaña, superficie, mensajes
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 32%

---

# Creación de una campaña {#create-campaign}

>[!NOTE]
>
>Antes de crear una nueva campaña, asegúrese de tener un canal de superficie (es decir, un ajuste preestablecido de mensaje) y una audiencia de Adobe Experience Platform lista para usar. Obtenga más información en estas secciones:
>
>* [Crear superficies de canal](../configuration/channel-surfaces.md)
>* [Introducción a las audiencias](../audience/about-audiences.md)

Para crear una nueva campaña, accede al menú **[!UICONTROL Campañas]** y luego haz clic en **[!UICONTROL Crear campaña]**. También puede duplicar una campaña en directo existente para crear una nueva. [Más información](modify-stop-campaign.md#duplicate)

## Elección del tipo de campaña {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo de campaña"
>abstract="**Campañas programadas** se ejecutan inmediatamente o en una fecha especificada y están pensadas para enviar mensajes de tipo marketing. Las campañas **activadas por API** se ejecutan mediante el uso de una llamada de API. Están destinados a enviar mensajes de marketing (mensajes promocionales que requieren el consentimiento del usuario) o mensajes transaccionales (mensajes no comerciales, que también se pueden enviar a perfiles no suscritos en contextos específicos)."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Categoría de la campaña"
>abstract="Si está creando una campaña programada, la variable **marketing** se selecciona automáticamente. Para las campañas activadas por API, elija si desea enviar un mensaje de **marketing** (mensaje promocional que requiere el consentimiento del usuario) o un mensaje **transaccional** (mensaje no comercial, que también se puede enviar a perfiles no suscritos en contextos específicos)."

1. Seleccione el tipo de campaña que desea ejecutar

   * **[!UICONTROL Programado - Marketing]**: ejecute la campaña inmediatamente o en una fecha especificada. Las campañas programadas están destinadas a enviar **marketing** mensajes. Se configuran y ejecutan desde la interfaz de usuario de.

   * **[!UICONTROL Activado por API - Marketing/Transaccional]**: ejecute la campaña mediante una llamada de API. Las campañas activadas por API están destinadas a enviar **marketing** o **mensajes transaccionales**, es decir, mensajes enviados después de una acción realizada por un individuo: restablecimiento de contraseña, compra en el carro de compras, etc. [Aprenda a almacenar en déclencheur una campaña mediante API](api-triggered-campaigns.md)

   ![](assets/create-campaign-modal.png)

1. Haga clic en **[!UICONTROL Crear]** para crear la campaña.

## Definición de las propiedades de la campaña {#create}

1. En la sección **[!UICONTROL Propiedades]**, especifique un nombre y una descripción para la campaña.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../content-management/content-experiment.md).-->

1. El campo **Etiquetas** le permite asignar etiquetas unificadas de Adobe Experience Platform a su campaña. Esto le permite clasificarlos fácilmente y mejorar la búsqueda desde la lista de campañas. [Descubra cómo trabajar con campañas](../start/search-filter-categorize.md#tags)

1. Para asignar etiquetas de uso de datos principales o personalizadas a la campaña, haz clic en el botón **[!UICONTROL Administrar acceso]**. [Más información sobre el Control de acceso de nivel de objeto (OLA)](../administration/object-based-access.md)

## Definición de la audiencia de campaña {#audience}

Defina la población objetivo de la campaña, siga estos pasos:

>[!IMPORTANT]
>
>El uso de audiencias y atributos de las audiencias [composición de audiencias](../audience/get-started-audience-orchestration.md) y [carga personalizada (archivo CSV)](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience) no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield.
>
>Para campañas activadas por API, la audiencia debe configurarse mediante una llamada de API.

1. En la sección **Audiencia**, haga clic en el botón **[!UICONTROL Seleccionar audiencia]** para mostrar la lista de audiencias de Adobe Experience Platform disponibles. [Más información sobre los públicos](../audience/about-audiences.md)

1. En el campo **[!UICONTROL Área de nombres de identidad]**, elija el área de nombres que desea utilizar para identificar a los individuos del segmento seleccionado.

   Las personas que pertenezcan a un segmento que no tenga la identidad seleccionada (área de nombres) entre sus diferentes identidades no serán el objetivo de la campaña. [Más información sobre áreas de nombres](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Creación del mensaje y configuración del seguimiento {#content}

1. En la sección **[!UICONTROL Acciones]**, elija el canal y la superficie que desea utilizar para enviar el mensaje.

   Una superficie es una configuración que ha definido un [Administrador del sistema](../start/path/administrator.md). Contiene todos los parámetros técnicos para enviar el mensaje, como parámetros de encabezado, subdominio, aplicaciones móviles, etc. [Más información](../configuration/channel-surfaces.md).

   En la lista desplegable solo se muestran las superficies de canal compatibles con el tipo de campaña de marketing.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Si está creando una campaña de notificaciones push, puede habilitar el **[!UICONTROL modo de envío rápido]**, que es un complemento de Journey Optimizer que permite enviar mensajes push muy rápidamente en grandes volúmenes. [Más información](../push/create-push.md#rapid-delivery)

1. Haz clic en el botón **[!UICONTROL Editar contenido]** para crear y diseñar tu mensaje. Conozca los pasos detallados para crear el contenido del mensaje en las siguientes páginas:

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

1. Una vez definido el contenido, use el botón **[!UICONTROL Simular contenido]** para previsualizar y probar el contenido con perfiles de prueba. [Más información](../content-management/preview-test.md).

1. Haga clic en la flecha para volver a la pantalla de creación de campañas.

   ![](assets/create-campaign-design.png)

1. En la sección **[!UICONTROL Seguimiento de acciones]**, especifique si desea rastrear cómo reaccionan los destinatarios a su envío: puede rastrear clics o aperturas.

   Se podrá acceder a los resultados de seguimiento desde el informe de campaña una vez que se haya ejecutado la campaña. [Más información sobre los informes de campaña](../reports/campaign-global-report.md)

## Programación de la campaña {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Programación de campañas"
>abstract="De forma predeterminada, las campañas se inician tras la activación manual y finalizan inmediatamente después de enviar el mensaje una vez. Sin embargo, tiene la flexibilidad de establecer una fecha y hora específicas para que se envíe el mensaje. Además, puede especificar una fecha de finalización para campañas recurrentes o activadas por API. En los Activadores de acción, también puede configurar la frecuencia de envío de mensajes para adaptarla a sus preferencias."

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

De forma predeterminada, las campañas comienzan una vez que se han activado manualmente y finalizan en cuanto se envía un mensaje.

Puede definir una frecuencia con la que se debe enviar el mensaje de la campaña. Para ello, usa las opciones **[!UICONTROL déclencheur de acción]** en la pantalla de creación de campañas para especificar si la campaña se debe ejecutar diaria, semanal o mensualmente.

Si no desea ejecutar la campaña justo después de su activación, puede especificar una fecha y una hora a las que se debe enviar el mensaje mediante la opción **[!UICONTROL Inicio de campaña]**. La opción **[!UICONTROL Fin de campaña]** le permite especificar cuándo debe dejar de ejecutarse una campaña recurrente.

![](assets/create-campaign-schedule.png)

Una vez que la campaña esté lista, puede revisarla y publicarla. [Más información](review-activate-campaign.md)
