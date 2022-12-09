---
solution: Journey Optimizer
product: journey optimizer
title: Creación de un mensaje SMS
description: Aprenda a crear un mensaje SMS en Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 34ab78408981d2b53736b31c94412da06cb860c4
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Creación de un mensaje SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Creación de SMS"
>abstract="Añada el mensaje de texto y comience a personalizarlo con el editor de expresiones."

>[!NOTE]
>
>De acuerdo con las normas y regulaciones del sector, todos los mensajes de marketing SMS deben contener una forma para que los destinatarios puedan cancelar su suscripción fácilmente. Para ello, los destinatarios de SMS pueden responder con las palabras clave de inclusión y exclusión. [Obtenga información sobre cómo administrar la exclusión](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

## Creación de un mensaje SMS en un recorrido o una campaña {#create-sms-journey-campaign}

Para empezar a personalizar el mensaje SMS, siga estos pasos:

>[!BEGINTABS]

>[!TAB Añadir un mensaje SMS a un recorrido]

1. Abra el recorrido y arrastre y suelte una actividad SMS desde la sección Acciones de la paleta.

   ![](assets/sms_create_1.png)

1. Proporcione información básica sobre el mensaje (etiqueta, descripción, categoría) y, a continuación, elija la superficie del mensaje que desea utilizar.

   ![](assets/sms_create_2.png)

   Para obtener más información sobre cómo configurar un recorrido, consulte [esta página](../building-journeys/journey-gs.md)

Ahora puede empezar a diseñar el contenido de su mensaje SMS desde el **[!UICONTROL Edit content]** botón. [Diseño del contenido de SMS](#sms-content)

>[!TAB Añadir un mensaje SMS a una campaña]

1. Cree una nueva campaña programada o activada por la API, seleccione **[!UICONTROL SMS]** como su acción y elija el **[!UICONTROL App surface]** para usar. [Más información sobre la configuración de SMS](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Haga clic en **[!UICONTROL Create]**.

1. En el **[!UICONTROL Properties]** , edite la **[!UICONTROL Title]** y **[!UICONTROL Description]**.

   ![](assets/sms_create_4.png)

1. En el **[!UICONTROL Actions tracking]** , especifique si desea rastrear los clics en los vínculos de su mensaje SMS.

1. Haga clic en el **[!UICONTROL Select audience]** para definir la audiencia a la que se dirigirá desde la lista de segmentos disponibles de Adobe Experience Platform. [Más información](../segment/about-segments.md).

1. En el **[!UICONTROL Identity namespace]** , elija el área de nombres que desea utilizar para identificar a las personas del segmento seleccionado. [Más información](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Las campañas están diseñadas para ejecutarse en una fecha específica o con una frecuencia recurrente. Obtenga información sobre cómo configurar la variable **[!UICONTROL Schedule]** de su campaña en [esta sección](../campaigns/create-campaign.md#schedule).

1. En el **[!UICONTROL Action triggers]** , seleccione **[!UICONTROL Frequency]** de su mensaje SMS:

   * Una vez
   * Diario
   * Semanal
   * Mes

Ahora puede empezar a diseñar el contenido de su mensaje SMS desde el **[!UICONTROL Edit content]** botón. [Diseño del contenido de SMS](#sms-content)

>[!ENDTABS]

## Definir el contenido del SMS{#sms-content}

1. En la pantalla de configuración del recorrido o de la campaña, haga clic en el botón **[!UICONTROL Edit content]** para configurar el contenido del SMS.

1. Haga clic en el **[!UICONTROL Message]** para abrir el editor de expresiones.

   ![](assets/sms-content.png)

1. Utilice el editor de expresiones para definir contenido y añadir contenido dinámico. Puede utilizar cualquier atributo, como el nombre del perfil o la ciudad. Más información sobre [personalización](../personalization/personalize.md) y [contenido dinámico](../personalization/get-started-dynamic-content.md) en el editor de expresiones.

1. Haga clic en **[!UICONTROL Save]** y compruebe el mensaje en la vista previa. [Más información](send-sms.md)

   ![](assets/sms-content-preview.png)

**Temas relacionados**

* [Configurar canal de SMS](sms-configuration.md)
* [Informe SMS](../reports/journey-global-report.md#sms-global)
* [Añadir un mensaje en un recorrido](../building-journeys/journeys-message.md)
