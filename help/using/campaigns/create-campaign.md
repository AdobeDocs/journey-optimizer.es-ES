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
source-git-commit: f9f2cd339680d0dbff1812e64c5082ca97a34771
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 19%

---

# Creación de una campaña {#create-campaign}

Para crear una nueva campaña, accede al menú **[!UICONTROL Campañas]** y luego haz clic en **[!UICONTROL Crear campaña]**. También puede duplicar una campaña en directo existente para crear una nueva. [Más información](modify-stop-campaign.md#duplicate)

>[!NOTE]
>
>Antes de crear una nueva campaña, asegúrese de tener una configuración de canal (es decir, una superficie de mensaje) y una audiencia de Adobe Experience Platform lista para usar. Obtenga más información en estas secciones:
>
>* [Crear configuraciones de canal](../configuration/channel-surfaces.md)
>* [Introducción a las audiencias](../audience/about-audiences.md)

## Selección del tipo de campaña {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo de campaña"
>abstract="**Campañas programadas** se ejecutan inmediatamente o en una fecha especificada y están pensadas para enviar mensajes de tipo marketing. Las campañas **activadas por API** se ejecutan mediante el uso de una llamada de API. Están destinados a enviar mensajes de marketing (mensajes promocionales que requieren el consentimiento del usuario) o mensajes transaccionales (mensajes no comerciales, que también se pueden enviar a perfiles no suscritos en contextos específicos)."

1. Seleccione el tipo de campaña que desea ejecutar

   * **[!UICONTROL Programado - Marketing]**: ejecute la campaña inmediatamente o en una fecha especificada. Las campañas programadas están destinadas a enviar **marketing** mensajes. Se configuran y ejecutan desde la interfaz de usuario de.

   * **[!UICONTROL Activado por API - Marketing/Transaccional]**: ejecute la campaña mediante una llamada de API. Las campañas activadas por API están destinadas a enviar **marketing** o **mensajes transaccionales**, es decir, mensajes enviados después de una acción realizada por un individuo: restablecimiento de contraseña, compra en el carro de compras, etc. [Aprenda a almacenar en déclencheur una campaña mediante API](api-triggered-campaigns.md)

   ![](assets/create-campaign-modal.png)

1. Haga clic en **[!UICONTROL Crear]** para crear la campaña.

## Definición de las propiedades de la campaña {#create}

1. En la sección **[!UICONTROL Propiedades]**, escriba el nombre y una descripción para la campaña.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../content-management/content-experiment.md).-->

1. Utilice el campo **Etiquetas** para asignar etiquetas unificadas de Adobe Experience Platform a su campaña. Esto le permite clasificarlos fácilmente y mejorar la búsqueda desde la lista de campañas. [Aprenda a trabajar con etiquetas](../start/search-filter-categorize.md#tags).

1. Puede limitar el acceso a esta campaña en función de las etiquetas de acceso. Para agregar una limitación de acceso, vaya al botón **[!UICONTROL Administrar acceso]** en la parte superior de esta página. Asegúrese de seleccionar solo las etiquetas para las que tenga permiso. [Más información sobre el Control de acceso a nivel de objeto](../administration/object-based-access.md).

## Definición de la audiencia de campaña {#audience}

Una audiencia es un conjunto de personas que comparten comportamientos o características similares. Para definir la población objetivo de la campaña, siga estos pasos:

1. En la sección **Audiencia**, haga clic en el botón **[!UICONTROL Seleccionar audiencia]** para mostrar la lista de audiencias de Adobe Experience Platform disponibles. Obtenga más información acerca de las audiencias en [esta sección](../audience/about-audiences.md).

1. En el campo **[!UICONTROL Tipo de identidad]**, elija el tipo de clave que desea usar para identificar a los individuos de la audiencia seleccionada. Puede crear un tipo de identidad existente o crear uno nuevo mediante el servicio de identidad de Adobe Experience Platform. Las áreas de nombres de identidad estándar se enumeran en [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

   Solo se permite un tipo de identidad por campaña. La campaña no puede dirigirse a las personas que pertenezcan a un segmento que no tenga el tipo de identidad seleccionado entre sus diferentes identidades.

   ![](assets/create-campaign-namespace.png)

   Obtenga más información acerca de tipos de identidad y áreas de nombres en la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=es){target="_blank"}.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

>[!IMPORTANT]
>
>* El uso de audiencias y atributos de [composición de audiencias](../audience/get-started-audience-orchestration.md) no está disponible actualmente para su uso con Healthcare Shield o Privacy and Security Shield.
>
>* Para campañas activadas por API, la audiencia debe configurarse mediante una llamada de API.


## Creación del mensaje y configuración del seguimiento {#content}

1. En la sección **[!UICONTROL Acciones]**, seleccione el canal.

   La lista de canales disponibles depende del modelo de licencia. Para las campañas transaccionales activadas por API, solo están disponibles los canales de correo electrónico, SMS y notificaciones push.

1. Seleccione la configuración de canal.

   Un [administrador del sistema](../start/path/administrator.md) define una configuración. Contiene todos los parámetros técnicos para enviar el mensaje, como parámetros de encabezado, subdominio, aplicaciones móviles, etc. [Más información](../configuration/channel-surfaces.md).

   En la lista desplegable solo se muestran las configuraciones de canal compatibles con el tipo de campaña de marketing.

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

   Una vez definido el contenido, use el botón **[!UICONTROL Simular contenido]** para previsualizar y probar el contenido con perfiles de prueba. [Más información](../content-management/preview-test.md). Para volver a la pantalla de creación de campañas, haga clic en la flecha izquierda.

   ![](assets/create-campaign-design.png)

1. En la sección **[!UICONTROL Experimento de contenido]**, puede usar el botón **[!UICONTROL Crear experimento]** para probar qué contenido funciona mejor. Las capacidades de experimentación de contenido se detallan en [esta sección](../content-management/content-experiment.md).

1. En la sección **[!UICONTROL Seguimiento de acciones]**, especifique si desea rastrear cómo reaccionan los destinatarios a su envío: puede rastrear clics o aperturas.

   Se podrá acceder a los resultados de seguimiento desde el informe de campaña una vez que se haya ejecutado la campaña. [Más información sobre los informes de campaña](../reports/campaign-global-report-cja.md)

## Programación de la campaña {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Programación de campañas"
>abstract="De forma predeterminada, las campañas se inician tras la activación manual y finalizan inmediatamente después de que se envíe el mensaje una vez. Tiene la flexibilidad de establecer una fecha y hora específicas para el envío del mensaje. Además, puede especificar una fecha de finalización para campañas recurrentes o activadas por API. En los Activadores de acción, también puede configurar la frecuencia de envío de mensajes para adaptarla a sus preferencias."

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

Una vez que la campaña esté lista, puede revisarla y activarla. [Más información](review-activate-campaign.md)
